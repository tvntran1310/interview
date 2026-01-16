# Sự khác nhau giữa StatelessWidget và StatefulWidget

## 1. Định nghĩa

### StatelessWidget

- Không tự quản lý state
- Dữ liệu không thay đổi trong vòng đời widget
- UI chỉ phụ thuộc vào input (constructor)

```dart
class MyText extends StatelessWidget {
  final String title;
  const MyText({super.key, required this.title});

  @override
  Widget build(BuildContext context) {
    return Text(title);
  }
}
```

---

### StatefulWidget

- Có state nội bộ
- Dữ liệu có thể thay đổi theo thời gian
- Khi state đổi → UI rebuild

```dart
class Counter extends StatefulWidget {
  const Counter({super.key});

  @override
  State<Counter> createState() => _CounterState();
}

class _CounterState extends State<Counter> {
  int count = 0;

  @override
  Widget build(BuildContext context) {
    return Text('$count');
  }
}
```

---

## 2. Bảng so sánh

| Tiêu chí         | StatelessWidget | StatefulWidget      |
| ---------------- | --------------- | ------------------- |
| Có state nội bộ  | ❌ Không        | ✅ Có               |
| Dữ liệu thay đổi | ❌ Không        | ✅ Có               |
| Có lifecycle     | ❌ Không        | ✅ Có               |
| setState()       | ❌ Không        | ✅ Có               |
| Dễ test          | ✅ Rất dễ       | ⚠️ Khó hơn          |
| Performance      | ⚡ Tốt hơn      | Phụ thuộc cách dùng |
| Phù hợp          | UI tĩnh         | UI động             |

---

## 3. Khi nào dùng StatelessWidget?

Sử dụng khi:

- UI không thay đổi sau khi build
- Chỉ hiển thị dữ liệu từ widget cha
- Không cần:
  - loading state
  - animation
  - timer
  - form input

**Ví dụ:**

- Text
- Icon
- Card hiển thị data
- Item trong ListView
- Custom UI component

---

## 4. Khi nào dùng StatefulWidget?

Sử dụng khi:

- Widget tự quản lý dữ liệu
- Dữ liệu thay đổi theo:
  - user interaction
  - API response
  - timer
  - animation
- Cần:
  - loading
  - toggle
  - counter
  - TextEditingController
  - FocusNode

**Ví dụ:**

- Form nhập liệu
- TabController
- Animation
- Counter
- Video player

---

## 5. Câu hỏi phỏng vấn nâng cao (Middle)

### StatelessWidget có thực sự "stateless" không?

- Không hoàn toàn
- Nó không giữ state nội bộ
- Nhưng vẫn phụ thuộc state bên ngoài

### StatefulWidget gồm 2 phần để làm gì?

```dart
StatefulWidget  // cấu hình
State<T>        // logic + state
```

- Widget: immutable
- State: mutable

### Vì sao tách Widget và State?

- Giữ widget immutable
- Flutter có thể reuse widget
- Quản lý lifecycle rõ ràng

## Kết luận

> StatelessWidget dùng cho UI tĩnh, không thay đổi theo thời gian.  
> StatefulWidget dùng khi widget cần quản lý state nội bộ và thay đổi UI dựa trên state.  
> Chọn loại widget dựa trên việc widget có cần lưu trữ và cập nhật dữ liệu hay không.
