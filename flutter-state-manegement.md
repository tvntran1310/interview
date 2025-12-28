## FLUTTER - STATE MANEGEMENT

### Kiến thức nền tảng (Fundamental)

1. State management là gì trong Flutter?
   -> Giải thích bản chất và mục đích của state management.
2. State khác gì so với UI trong Flutter?
   -> Khi nào UI cần redraw? (liên quan tới thay đổi state).
3. Sự khác nhau giữa StatelessWidget và StatefulWidget là gì?
   -> Khi nào nên dùng mỗi loại widget? (Medium)
4. SetState() hoạt động như thế nào và nó dùng để làm gì?
   -> Điểm mạnh/yếu trong quản lý state.
5. Bạn nói gì về “ephemeral state” và “app state”?

### Chia sẻ state giữa các widget

1. Làm thế nào để chia sẻ state giữa các widget?
   -> Ví dụ: constructor, callback, InheritedWidget.
2. Khi nào nên dùng widget constructor để truyền state?
   -> Ưu/nhược điểm so với các cách khác.
3. InheritedWidget là gì và vì sao nó quan trọng?
   -> Giải thích cách hoạt động và lợi ích.
4. Callback trong Flutter dùng như thế nào để cập nhật state?
   -> So sánh với các cách khác truyền dữ liệu.
5. Làm thế nào để widget ở sâu trong cây widget nhận notify khi state thay đổi?
   -> Ví dụ sử dụng Listenable, ValueNotifier, ChangeNotifier.

### State management nâng cao / kiến trúc

1. Bạn hiểu gì về Model-View-ViewModel (MVVM) trong Flutter?
   -> Khi nào nên dùng MVVM?
2. So sánh MVVM với cách quản lý state thuần Flutter (không dùng package).
   -> Ưu và nhược điểm từng cách.
3. Khi nào bạn nên dùng state management package thay vì cách thủ công?
   -> Ví dụ: provider, riverpod, bloc… (tham khảo thêm ngoài docs).
4. Các cách tiếp cận để quản lý app state lớn hơn (complex apps).
   -> Có thể hỏi về patterns/arch (e.g., MVVM, Clean Architecture).
5. Bạn sẽ xử lý state khi dữ liệu đến từ backend (API)?
   -> Dùng async/futures, streams, repository pattern.

### Câu hỏi kèm thực hành / code

1. Viết ví dụ đơn giản sử dụng StatefulWidget để quản lý counter.
   -> Yêu cầu candidate giải thích dòng code.
2. Làm cách nào để truyền dữ liệu từ parent widget đến child widget?
   -> Cách dùng constructor vs InheritedWidget.
3. Viết ví dụ sử dụng ChangeNotifier để notify widget khác khi state thay đổi.
   -> Giải thích cách hoạt động.
4. Bạn làm gì khi cần cập nhật nhiều widget cùng lúc khi một state thay đổi?
   -> Hỏi về notify, listeners.
5. Giới thiệu cách kiểm tra state management bằng unit test.
   -> Hỏi về viết test cho state logic riêng.

### Định hướng mở rộng (ứng dụng thực tế)

1. Bạn sẽ dùng approach nào để quản lý state trong một app lớn và vì sao?
   -> So sánh Provider, Riverpod, Bloc… (tham khảo thêm kiến thức phổ biến).
   Medium
2. Làm thế nào tối ưu hiệu suất khi state thay đổi liên tục?
   -> Hỏi rule rebuild widget, keys, selective rebuild.
3. So sánh state management local vs global.
   -> Khi nào cần global app state?
   Medium
4. Bạn đã từng debug state nào khó xử lý chưa? Làm sao bạn fix?
   -> Câu hỏi behavioral thực tế.
5. Bạn sẽ thiết kế state để reset toàn bộ app khi người dùng logout?
   -> Hỏi kiến trúc tổng thể.

### KHÁI NIỆM CỐT LÕI VỀ STATE (RẤT HAY HỎI)

1. State trong Flutter được định nghĩa là gì theo docs chính thức?
2. Vì sao Flutter nói rằng UI = function(state)?
3. Điều gì xảy ra trong framework khi state thay đổi?
4. Tại sao Flutter cần quản lý state thay vì chỉ rebuild UI?
5. State có tồn tại ngoài Widget không? Nếu có thì ở đâu?
6. Điều gì quyết định một widget có cần state hay không?
7. Tại sao state không nên được lưu trực tiếp trong Widget class?
8. Vì sao Flutter khuyến khích immutable widget?
9. Điều gì xảy ra nếu state bị thay đổi nhưng UI không rebuild?
10. Flutter xử lý state khác gì so với React / Android View truyền thống?

### STATEFUL VS STATELESS (HỎI RẤT NHIỀU)

1. StatelessWidget có thực sự “stateless” không? Giải thích rõ.
2. Khi nào StatelessWidget vẫn có thể hiển thị dữ liệu thay đổi?
3. StatefulWidget gồm những phần nào? Trách nhiệm của từng phần?
4. Vì sao State<T> tách khỏi StatefulWidget?
5. Lifecycle cơ bản của StatefulWidget là gì?
6. createState() được gọi khi nào?
7. Khi nào build() được gọi lại?
8. setState() thực sự làm gì bên trong?
9. Có bắt buộc mọi thay đổi state đều phải gọi setState() không?
10. Điều gì xảy ra nếu gọi setState() sau khi widget dispose?

### EPHEMERAL STATE vs APP STATE (CỰC QUAN TRỌNG)

1. Ephemeral state là gì? Nêu ít nhất 5 ví dụ thực tế.
2. Vì sao Flutter docs khuyên giữ ephemeral state càng gần widget càng tốt?
3. App state là gì? Khác gì với ephemeral state?
4. Nêu ví dụ app state trong ứng dụng thực tế.
5. Counter nên là ephemeral state hay app state? Vì sao?
6. Form input nên thuộc loại state nào?
7. User login info thuộc loại state nào?
8. Điều gì xảy ra nếu bạn dùng app state cho ephemeral state?
9. Điều gì xảy ra nếu bạn dùng ephemeral state cho app state?
10. Làm sao nhận biết khi nào cần “nâng cấp” state từ local lên global?

### DATA FLOW & UNIDIRECTIONAL DATA FLOW

1. Flutter có data flow theo hướng nào?
2. Unidirectional data flow là gì?
3. Vì sao Flutter khuyến khích data flow một chiều?
4. Widget con có được phép thay đổi state của widget cha không?
5. Callback giúp giải quyết vấn đề gì trong data flow?
6. Vì sao callback là một phần quan trọng trong state management?
7. So sánh truyền dữ liệu bằng constructor vs callback.
8. Điều gì xảy ra nếu data flow hai chiều?
9. Lỗi thường gặp khi thiết kế data flow sai?
10. Cách Flutter đảm bảo UI nhất quán khi state thay đổi?

### LIFTING STATE UP (RẤT HAY RA PHỎNG VẤN)

1. Lifting state up là gì?
2. Khi nào cần lifting state up?
3. Ví dụ lifting state up với 2 widget sibling.
4. Vì sao lifting state up giúp code dễ bảo trì hơn?
5. Nhược điểm của việc lifting state quá cao?
6. Dấu hiệu cho thấy bạn đang lift state sai chỗ?
7. So sánh lifting state vs global state.
8. Khi lift state, widget cha chịu trách nhiệm gì?
9. Widget con nên làm gì sau khi lift state?
10. Lifting state có ảnh hưởng performance không?

### INHERITEDWIDGET (PHẦN NẶNG – HAY HỎI MIDDLE)

1. InheritedWidget dùng để giải quyết vấn đề gì?
2. Vì sao InheritedWidget tốt hơn truyền constructor nhiều tầng?
3. of(context) trong InheritedWidget hoạt động như thế nào?
4. updateShouldNotify có vai trò gì?
5. Khi nào widget con rebuild khi dùng InheritedWidget?
6. So sánh InheritedWidget và Global variable.
7. InheritedWidget có quản lý logic không?
8. Vì sao InheritedWidget là nền tảng của Provider?
9. Nhược điểm khi dùng InheritedWidget trực tiếp?
10. Khi nào KHÔNG nên dùng InheritedWidget?

### LISTENABLE, CHANGENOTIFIER, VALUENOTIFIER

1. Listenable là gì trong Flutter?
2. ChangeNotifier hoạt động dựa trên cơ chế gì?
3. Khi nào notifyListeners() được gọi?
4. ValueNotifier khác ChangeNotifier ở điểm nào?
5. Khi nào nên dùng ValueNotifier?
6. Ưu điểm của Listenable so với setState?
7. Nhược điểm của ChangeNotifier?
8. Điều gì xảy ra nếu quên dispose ChangeNotifier?
9. Vì sao ChangeNotifier phù hợp cho app state?
10. Mối quan hệ giữa ChangeNotifier và InheritedWidget?

### REBUILD & PERFORMANCE (PHỎNG VẤN RẤT THÍCH)

1. Khi state thay đổi, Flutter rebuild cái gì?
2. Flutter có rebuild toàn bộ app không?
3. Vì sao build() phải là pure function?
4. Làm sao để hạn chế rebuild không cần thiết?
5. Widget const giúp gì cho state management?
6. Keys có liên quan gì tới state?
7. Lỗi phổ biến gây rebuild dư thừa?
8. Tại sao logic không nên để trong build()?
9. setState() có tốn kém không?
10. Cách debug rebuild trong Flutter?

### KIẾN TRÚC & THIẾT KẾ STATE

1. Vì sao Flutter docs khuyên tách UI và state logic?
2. State nên chứa logic hay chỉ chứa dữ liệu?
3. Vì sao state management liên quan chặt tới architecture?
4. Khi app lớn dần, vấn đề gì xảy ra nếu không quản lý state tốt?
5. Vì sao Flutter không ép dùng 1 state management package?
6. Flutter docs định hướng developer học gì trước khi dùng package?
7. Khi nào nên chuyển sang Provider/Riverpod?
8. Điều gì xảy ra nếu lạm dụng global state?
9. Cách tổ chức file khi quản lý app state?
10. State management ảnh hưởng thế nào tới test?

### CÂU HỎI TÌNH HUỐNG (RẤT HAY DÙNG)

1. App có 3 màn hình cùng dùng chung user info → bạn làm thế nào?
2. Một widget cần state của widget không cùng cây → giải pháp?
3. Counter chỉ dùng trong dialog → nên đặt state ở đâu?
4. Nhiều widget cần biết loading state → xử lý thế nào?
5. Logout → reset toàn bộ state → làm sao thiết kế?
6. App bị lag do rebuild → bạn debug từ đâu?
7. Khi nào nên refactor state management?
8. Làm sao test logic state mà không test UI?
9. Nếu không dùng package, Flutter cho bạn những công cụ gì?
10. Theo bạn, state management “tốt” là như thế nào?
