### State và UI khác nhau như thế nào?

**_🔹State_**

- State là dữ liệu (data) có thể thay đổi theo thời gian
- State không phải giao diện
- State quyết định UI sẽ hiển thị như thế nào

**Ví dụ state:**

`int counter`

`bool isLoading`

`User? currentUser`

Danh sách sản phẩm

Giá trị nhập trong TextField

**_🔹 UI (Widget)_**

- UI là cách biểu diễn state ra màn hình
- UI trong Flutter là immutable (bất biến)
- UI không lưu dữ liệu, chỉ render dữ liệu từ state

**Ví dụ UI:**

Text hiển thị counter

Button enable/disable dựa trên isLoading

ListView hiển thị danh sách sản phẩm

**_👉 Flutter coi widget chỉ là bản mô tả giao diện, không phải giao diện thật._**
