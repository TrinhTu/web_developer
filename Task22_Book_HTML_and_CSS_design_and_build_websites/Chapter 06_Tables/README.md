## HTML & CSS

### TABLES

> Chương 6: Tables
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 22/01/2017

## Mục lục:

[1. Cách tạo bảng](#1)

[2. Cấu trúc đơn giản của bảng](#2)

[3. Các thuộc tính khác](#3)

[Tài liệu tham khảo](#4)

***

<a name="1"></a>
### 1. Cách tạo bảng (How to create tables):

- Có 1 số loại thông tin có nhu cầu sẽ được hiển thị trong 1 mạng lưới hoặc 1 bảng. Ví dụ như: Kết quả thể thao, báo cáo chứng khoán, thời khóa biểu.

- Khi biểu diễn thông tin trên bảng, cần thiết kế 1 bảng gồm các hàng và các cột. Trong chương này sẽ hướng dẫn cách:

	+ Sử dụng 4 yếu tố quan trọng cho việc tạo bảng

	+ Dữ liệu đại diện cho các bảng

	+ Thêm chú thích vào bảng

### Bảng là gì? (What's A Table)

- Một bảng đại diện cho thông tin cần thể hiện. Ví dụ về bảng bao gồm các báo cáo tài chính, chương trình truyền hình,...

- Mỗi khối trong mạng lưới được gọi là 1 ô trong bảng. Trong HTML 1 bảng được viết thành nhiều hàng.

### 2. Cấu trúc đơn giản của bảng:

#### Basic Table Structure:

- `<table>`: Thẻ `<table>` được sử dụng để tạo bảng. Nội dung trong bảng được viết ra từng hàng. `<tr>`: Trên mỗi hàng bắt đầu với thẻ `<tr>`. Tiếp theo bởi 1 hoặc nhiều thẻ `<td>` áp dụng cho mỗi nội dung trong dòng đó. Vào cuối hàng sử dụng thẻ đóng `</tr>`

- `<td>`: Mỗi yếu tố trong bảng đại diện sử dụng thẻ `<td>`. Kết thúc mỗi nội dung sử dụng thẻ đóng `</td>`. 

#### Tiêu đề cho bảng (Table Headings):

- `<th>`: Thẻ `<th>` sử dụng như thẻ `<td>` nhưng mục đích là đại diện cho cả một cột hoặc 1 hàng

- Ngay khi ô đó không có nội dung vẫn nên sử dụng `<td>` hoặc `<th>` để đại diện cho sự hiện diện của ô trống nếu không bản đó sẽ không hiển thị chính xác

- Sử dụng yếu tố `<th>` cho tiêu đề giúp người sử dụng đọc tốt hơn, cải thiện khả năng tìm kiếm cho các công cụ tìm kiếm, lập chỉ mục các trang của bạn, cho phép kiểm soát sự xuất hiện của bảng tốt hơn khi bắt đầu sử dụng CSS. Các trình duyệt thường hiển thị nội dung của thẻ phần tử `<th>` in đậm và ở giữa ô.

#### Bảng dài (Long Tables):

- Có 3 yếu tố giúp phân biệt giữa nội dung chính của bảng với hàng đầu tiên và hàng cuối cùng có thể chứa nội dung khác nhau:

	+ `<thead>`: Tiêu đề của bản nên đặt giữa thẻ `<thead>`

	+ `<tbody>`: Nội dung nên được đặt trong thẻ `<tbody>`

	+ `<tfoot>`: Phần chân được đặt trong thẻ `<tbody>`

<a name="3"></a>
### 3. Các thuộc tính khác:

#### Chiều rộng và khoảng cách (Old Code: Width & Spacing):

- Có 1 vài thuộc tính đã cũ và không nên sử dụng trong website mới. Tất cả thuộc tính đó có thể được thay thế bằng sử dụng CSS.

- Chiều rộng thuộc tính đã sử dụng thẻ mở `<table>` để chỉ ra cách mở rộng bảng với `<th>` `<td>` để thiết lập chiều rộng cho các ô. Giá trị của thuộc tính là chiều rộng của bảng hoặc ô theo đơn vị pixels.

- Các cột trong bảng cần tạo thành 1 đường thẳng, vì vậy chỉ thường thấy thuộc tính chiều rộng trên hàng đầu tiên, tất cả các hàng tiếp theo sẽ sử dụng thiết lập đó.

- Thẻ mở `<table>` có thể sử dụng thuộc tính cellpadding để thêm khoảng trống bên trong mỗi ô trong bảng, và thuộc tính cellspacing để tạo khoảng trống giữa mỗi ô trong bảng, giá trị của các thuộc tính đó được tính them đơn vị pixels.

#### Viền và nền (Old Code: Border & Background):

- Thuộc tính viền sử dụng cả 2 yếu tố `<table>` và `<td>` để xác định chiều rộng của viền theo đơn vị pixels.

- Thuộc tính background chỉ định màu nền của toàn bộ bảng hoặc của mỗi ô. Giá trị thường sử dụng là mã hex.

- Khi xây dựng 1 trang web nên sử dụng CSS để điều chỉnh sự xuất hiện của bảng hơn là sử dụng các thuộc tính. 

### Tóm lại:

- Thẻ `<table>` dùng để tạo bảng trong trang web

- 1 bảng được tạo ra bởi các hàng. Mỗi hàng được tạo ra bởi thẻ `<tr>`

- Trong mỗi hàng có 1 ô đại diện bởi thẻ `<td>` (hay `<th>` nếu nó là 1 tiêu đề)

- Bạn cũng có thể tạo mỗi ô trong bảng được mở rộng hơn 1 dòng hoặc cột bằng cách sử dụng rowspan và các thuộc tính colspan.

- Đối với các bảng dài có thể phân ra thành `<thead>` `<tbody>` `<tfoot>`.

<a name="4"></a>
### Tài liệu tham khảo

> [1] Duckett, J. (2011). HTML and CSS: design and build websites. John Wiley & Sons.

