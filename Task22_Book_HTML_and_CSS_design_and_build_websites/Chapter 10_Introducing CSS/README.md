## HTML & CSS

### INTRODUCING CSS

> Chương 10: INTRODUCING CSS
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 04/02/2017

## Mục lục:

[1. Cách thức hoạt động của CSS](#1)

[2. Cách nhúng CSS vào trong website](#2)

[3. Áp dụng CSS trong website](#3)

[Tài liệu tham khảo](#4)

***

Trong phần này chúng ta sẽ tìm hiểu cách làm cho trang web trở nên hấp dẫn hơn, kiểm soát các thiết kế bằng cách sử dụng CSS.

- CSS cho phép tạo các quy định xác định nội dung của phần tử cần xuất hiện như màu nền, phông chữ, màu chữ... Trong bài này chúng ta sẽ tìm hiểu:

	+ Giới thiệu cách thức làm việc của CSS

	+ Học cách viết các quy tắc CSS

	+ Hiển thị các quy tắc CSS áp dụng cho các tài liệu HTML

<a name="1"></a>
### 1. Cách thức hoạt động của CSS:

#### Understanding CSS thinking inside the box:

CSS cho phép tạo các quy định điều khiển cách mà mỗi hộp cá nhân (và nội dung trong hộp) được trình bày. 

[4]

- Trong ví dụ này, phần tử block được hiển thị với đường viền màu đỏ và phần tử inline có đường viền màu xanh. Phần tử `<body>` được tạo ra đầu dòng và các phần tử `<h1>, <h2, <p>, <i> và <a>` tạo ra mỗi hộp riêng bên trong. Sử dụng CSS để thêm đường viền xung quanh hộp nhằm xác định chiều dài và chiều rộng hoặc thêm màu nền. Có thể điều khiển văn bản trong hộp như thêm kích thước, font chữ, màu sắc...

**Example Styles**:

- **Boxes**: chiều dài và chiều rộng, màu nền, hình ảnh, vị trí trong cửa sổ trình duyệt.

- **Text**: kiểu chữ, kích thước chữ, màu sắc, in đậm, in nghiêng, viết hoa viết thường...

- **Specific**: tạo các danh sách, bảng và form riêng.

#### CSS Associates Style Rules With HTML Elements (CSS kết hợp với phần tử HTML):

- CSS hoạt động bằng cách kết hợp với phần tử HTML. Các quy tắc dùng để ràng buộc nội dung được hiển thị, chứa 2 phần: vùng chọn và khai báo.

[5]

- Quy tắc này chỉ ra rằng phần tử `<p>` được áp dụng kiểu chữ Arial.

- Vùng chọn chỉ ra các phần tử được áp dụng quy tắc. Các quy tắc giống nhau có thể được áp dụng cho nhiều phần tử và cách chúng bằng dấu phẩy.

- Các khai báo (declarations) chỉ ra các phần tử được đề cập theo kiểu nào và được chia thành 2 bộ phận thuộc tính và giá trị và được cách nhau bằng dấu 2 chấm.

#### CSS Properties Affect How Elements Are Displayed (thuộc tính của CSS ảnh hưởng như thế nào đến sự hiển thị):

- Khai báo CSS được đặt trong dấu ngoặc nhọn và chia thành 2 phần là: thuộc tính và giá trị. Có thể có nhiều tính chất trong 1 khai báo và chúng cách nhau bởi dấu chấm phẩy.

[6]

- Theo quy tắc chỉ ra tất cả phần tử `<h1>, <h2>, <h3>` hiển thị với kiểu chữ Arial và có màu vàng

- Thuộc tính chỉ ra các phần tử thay đổi, ví dụ như màu sắc, font chữ, chiều rộng, chiều cao, đường viền...

- Giá trị chỉ định thiết lập muốn lựa chọn sử dụng cho thuộc tính.

<a name="2"></a>
### 2. Cách nhúng CSS vào trong website:

#### Using External CSS:

- `<link>`: thẻ `<link>` có thể được sử dụng trong tài liệu HTML để thông báo cho trình duyệt nơi để tập tin CSS được sử dụng trong trang. Nó là 1 phần tử rỗng (không có thẻ đóng) và tồn tại bên trong phần tử `<head>` gồm có 3 thuộc tính sau:

	+ `href`: xác định đường dẫn đến tập tin CSS (thường đặt trong thư mục có tên là css hoặc styles)

	+ `type`: thuộc tính chỉ ra kiểu tài liệu được liên kết đến. Giá trị nên là `text/css`.

	+ `rel`: xác định quan hệ giữa trang HTML và tập tin được liên kết đến. Giá trị nên là stylesheet khi liên kết tới tập tin CSS.

Một trang HTML có thể sử dụng nhiều hơn 1 CSS. Để làm được điều này có thể có 1 thẻ `<link>` cho mọi tập tin CSS được sử dụng. Ví dụ: 1 số tác giả sử dụng file CSS để kiểm soát trình bày (phông chữ, màu sắc) và thứ 2 là để kiểm soát bố trí.

#### Using Internal CSS:

- `<style>`: Có thể sử dụng bao gồm quy tắc CSS trong 1 trang HTML bằng cách đặt chúng bên trong thẻ `<style>` và thẻ đó luôn đặt trong thẻ `<head>` của trang.

- Thẻ `<style>` nên được sử dụng kiểu thuộc tính để xác định kiểu quy định trong CSS, giá trị nên là `text/css`.

- Khi xây dựng 1 trang web lớn nên sử dụng 1 kiểu external CSS style sheet:

	+ Cho phép tất cả các trang sử dụng các quy tắc tương tự nhau

	+ Giữ cho nội dung các trong riêng biệt rõ ràng

	+ Có thể thay đổi kiểu sử dụng trên tất cả các trang bằng cách thay đổi chỉ 1 file

<a name="3"></a>
### 3. Áp dụng CSS trong website:

#### CSS Selectors:

- [7]

#### How CSS Rules Cascade:

- Nếu có 2 hoặc nhiều quy tắc áp dụng cho cùng 1 yếu tố thì cần phải hiểu rõ thứ tự ưu tiên.

- **Last rule** (quy tắc cuối cùng): nếu 2 vùng chọn là giống hệt nhau thì ưu tiên áp dụng thuộc tính của vùng chọn đầu tiên.

- **Specificity** (đặc tính): có nhiều quy tắc cụ thể được áp dụng để xác định thứ tự sẽ được ưu tiên:

	+ h1: cụ thể hơn là *

	+ `p b` cu thể hơn là p 

	+ `p #` cụ thể hơn là p

- **important**: có thể thêm `!important` sau thuộc tính giá trị chỉ ra nó quan trọng hơn các quy định khác áp dụng cho cùng 1 phân tử.

#### Inheritance:

- Nếu chỉ rõ thuộc tính `font-family` hoặc `color` trong thẻ `<body>` họ sẽ áp dụng với hầu hết các phần tử con nằm trong đó, bởi vì giá trị của thuộc tính font-family được kế thừa bởi nó là phần tử con.

#### Why Use External Style Sheeets? (Tại sao sử dụng External Style Sheets)

- Khi xây dựng 1 trang web có nhiều lợi thế để áp dụng quy tắc CSS trong 1 cách riêng biệt. Tất cả trang web có thể chia sẻ cùng style sheet bằng cách sử dụng thẻ `<link>` trên mỗi trang HTML trên trang web để liên kết với cùng tài liệu CSS. Điều này có nghĩa là cùng 1 đoạn code không cần phải lặp đi lại lại ở mỗi trang.

- Do đó khi người dùng tải về các CSS stylesheet thì phần còn lại của trang web sẽ được tải nhanh hơn, nếu muốn thay đổi sự xuất hiện của trang web chỉ cần chỉnh sửa tập tin CSS và tất cả các trang của bạn sẽ được cập nhập.

- Đôi khi có thể xem xét việc đặt quy định CSS trong cùng 1 trang như code HTML:
	+ Nếu bạn tạo ra 1 trang độc lập bạn có thể quyết định đặt các quy tắc trong tập tin cùng 1 nơi (tuy nhiên tốt hơn nơi đặt CSS trong 1 file riêng biệt)

	+ Nếu có 1 trang mà đòi hỏi chỉ sử dụng 1 và quy tắc thì có thể xem xét việc sử dụng CSS trong cùng 1 trang

### Tóm lại:

- Quy tắc được tạo thành từ vùng chọn (chỉ ra phần tử cần áp dụng thuộc tính) và khai báo (điều đó mô tả yếu tố đó như thế nào)

- Các loại khác nhau của vùng chọn cho phép nhắm mục tiêu quy định tại các yếu tố khác nhau.

- Khai báo được tạo thành từ 2 phần: thuộc tính của các phần tử mà bạn muốn thay đổi và giá trị của thuộc tính đó. Ví dụ như thuộc tính font-family thiết lập chọn các font chữ, và có giá trị xác định là Arial như là kiểu chữ ưa thích.

- Quy tắc CSS xuất hiện trong 1 tài liệu riêng mặc dù vẫn hiển thị và áp dụng trong trang HTML.

<a name="4"></a>
### Tài liệu tham khảo

> [1] Duckett, J. (2011). HTML and CSS: design and build websites. John Wiley & Sons. 

