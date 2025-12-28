### State management là gì trong Flutter?

State management trong Flutter là cách tổ chức, lưu trữ, cập nhật và chia sẻ state (trạng thái dữ liệu) của ứng dụng sao cho UI luôn phản ánh đúng dữ liệu hiện tại.

**1. State là gì?**

Trong Flutter, state là bất kỳ dữ liệu nào có thể thay đổi theo thời gian và ảnh hưởng đến giao diện người dùng (UI).

Ví dụ:

- Giá trị counter
- Trạng thái loading / error
- Dữ liệu người dùng đã đăng nhập
- Nội dung form input
- Item được chọn trong danh sách

**Khi state thay đổi → UI phải được rebuild để phản ánh sự thay đổi đó**

**2. Bản chất của State management**

Flutter tuân theo tư duy:

**UI = f(state)**
(Giao diện là kết quả của state)

📌 Nghĩa là:

- UI không tự thay đổi
- UI chỉ thay đổi khi state thay đổi
- State là nguồn sự thật duy nhất (single source of truth)

State management chính là việc:

- Xác định state nằm ở đâu
- Ai được phép thay đổi state
- Widget nào lắng nghe state
- Khi state đổi thì widget nào được rebuild

### Mục đích của State management

🎯 1. Đảm bảo UI luôn nhất quán với dữ liệu

- Tránh UI hiển thị sai trạng thái
- Tránh dữ liệu bị lệch giữa các màn hình

🎯 2. Kiểm soát luồng dữ liệu (Data flow)

- Flutter dùng unidirectional data flow
- State đi từ trên xuống
- Sự kiện đi từ dưới lên (callback)

🎯 3. Dễ mở rộng và bảo trì ứng dụng

- Ứng dụng nhỏ: setState
- Ứng dụng lớn: cần cấu trúc rõ ràng cho state
- Tránh “spaghetti state”

🎯 4. Tối ưu hiệu năng

- Chỉ rebuild widget cần thiết
- Tránh rebuild toàn bộ cây widget

🎯 5. Hỗ trợ test & debug

- Tách state logic khỏi UI
- Dễ viết unit test cho state

**_=> State management trong Flutter là cách quản lý dữ liệu thay đổi theo thời gian và điều phối việc cập nhật UI sao cho giao diện luôn nhất quán, dễ mở rộng, dễ bảo trì và hiệu quả về hiệu năng._**
