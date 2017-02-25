## HTML & CSS

### LISTS, TABLES AND FORMS

> Chương 14: LIST, TABLES AND FORMS
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 13/02/2017

## Mục lục:

[1. Xác định kiểu cho các điểm](#1)

[2. Thêm đường viền và hình nền cho bảng](#2)

[3. Thay đổi sự xuất hiện của các phần tử](#3)

[Tài liệu tham khảo](#4)

***

<a name="1"></a>
### 1. Xác định kiểu cho điểm:

#### 1.1 BULLET POINT STYLES:

**list-style-type**: thuộc tính này cho phép kiểm soát hình dạng hoặc phong cách của 1 điểm (hay 1 điểm đánh dấu). Nó có thể sử dụng các quy tắc áp dụng trên các phần tử `<ol>`, `<ul>` và `<li>`.

- **unordered lists**: sử dụng cho danh sách không sắp xếp với các giá trị sau: none, disc, circle, square.

- **ordered list**: sử dụng cho danh sách sắp xếp với các giá trị sau: decimal, decimal-leading-zero, lower-alpha, upper-alpha, lower-roman, upper-roman.

#### 1.2 IMAGES FOR BULLETS:

**list-style-image**

- Có thể chỉ định các hình ảnh thêm vào trong các điểm chính bằng cách sử dụng thuộc tính list-style-image. Giá trị của thuộc tính này bắt đầu với chữ `url` và theo sau bởi cặp dấu ngoặc kép, bên trong đó là đường dẫn đến file chứa hình ảnh. Thuộc tính này có thể áp dụng các quy tắc lên các phần tử `<ul>` và `<li>`

#### 1.3 POSITIONING THE MARKER (đánh dấu vùng chọn)

**list-style-position**: Bởi theo mặc định thì danh sách sẽ thụt vào trong so với trang và thuộc tính list-style-position xác định nơi đánh dấu nên xuất hiện ra ngoài và thụt vô trong của các ý chính trong hộp, bao gồm 1 trong 2 giá trị sau:

- **outside**: đánh dấu được đặt về phía bên trái của văn bản

- **inside**: đánh dấu được đặt trong hộp văn bản

#### 1.4 LIST SHORTHAND:

**list-style**: Cũng tương tự như các thuộc tính CSS khác có 1 thuộc tính dùng để trình bày ngắn gọn hơn để thêm phong cách cho danh sách là list-style cho phép hiển thị đánh dấu phong cách, hình ảnh và thuộc tính vùng chọn bất kì khác.

<a name="2"></a>
### 2. Thêm hình nền và đường viền cho bảng:

#### 2.1 TABLE PROPERTIES:

Một số thuộc tính thường đi kèm với bảng:

- **width**: thiết lập chiều rộng cho bảng

- **padding**: thiết lập khoảng cách đường viền của mỗi ô trong bảng và nội dung của nó

- **text-transform**: đặt lại nội dung của tiêu để thành chữ in hoa

- **letter-spacing, font-size**: bổ sung thông tin cho tiêu đề của bảng

- **border-top, border-bottom**: thiết lập đường viền trên và dưới cho các tiêu đề bảng.

- **text-align**: Căng chỉnh vản bản về phía bên trái ô này và bên phải ô khác

- **background-color**: Thay đổi hình nền của các hàng xen kẽ

- **:hover**: là nổi bậc các dòng của văn bản khi người dùng rê chuột qua nó

**Dưới đây là 1 số điểm cần lưu ý khi tạo phong cách cho bảng**:

- **GIVE CELLS PADDING**: thêm padding cho mỗi ô giúp đọc dễ dàng hơn

- **DISTINGUISH HEADINGS** (phân biệt tiêu đề): có thể tạo tiêu đề là chữ in hoa hoặc thêm màu nền cho nó để phân biệt được với các nội dung

- **SHARE ALTERNATE ROWS**: Tạo bóng thay thế cho các hàng giúp cho người đọc dõi theo đường thẳng, sử dụng màu sắc đơn giản giúp bảng gọn gàng hơn.

- **ALIGN NUMBERALS** (căng chỉnh chữ số): có thể sử dụng thuộc tính text-align để căng chỉnh nội dung bên trong của bất kì cột chứa số để bên phải

#### 2.2 BORDER ON EMPTY CELLS:

**empty-cells**: Nếu có các ô trống trong bảng có thể sử dụng thuộc tính empty-cells để xác định có nên hiển thị đường viền hay không, có thể sử dụng 1 trong 3 thuộc tính:

- **show**: Hiển thị đường viền trong bất kì ô trống nào

- **hide**: ẩn đường viền trong bất kì ô trống nào

- **inherit**: nếu có 1 bảng được lồng vào bên trong các bảng khác thì các ô trong bảng sẽ được kế thừa các giá trị đã thiết lập tuân theo các quy tắc. 

#### 2.3 GAPS BETWEEN CELLS (khoảng trống giữa các ô):

**border-spacing, border-collapse**

- Thuộc tính border-spacing cho phép điều chỉnh khoảng cách giữa các ô trong bảng, theo như mặc định thì trình duyệt sẽ để 1 khoảng cách nhỏ giữa mỗi ô trong bảng vậy có thể sử dụng thuộc tính này để kéo giãn hoặc thu hẹp khoảng cách lại. Giá trị của thuộc tính thường sử dụng đơn vị pixels. Giữa 2 ô gặp nhau thì chiều rộng của dòng đó sẽ tăng lên gấp 2 lần có thể sử dụng thuộc tính border-collapse để thiết lập đường viền giữa chúng, thuộc tính bao gồm các giá trị sau:

	+ **collapse**: đường viền bị biến mất chỉ để lại 1 đường duy nhất giữa 2 ô đó.

	+ **separate**: đường viền sẽ được tách ra cho mỗi bên.

<a name="3"></a>
### 3. Thay đổi sự xuất hiện của các phần tử:

#### 3.1 STYLING FORMS: 

CSS thông thường được sử dụng để kiểm soát sự xuất hiện của phần tử form, làm cho chúng trở nên hấp dẫn hơn và phù hợp hơn đối với các trình duyệt khác nhau. Phong cách phổ biến nhất:

- Nhập văn bản vào và khu vực chứa văn bản

- Submit buttons

- Nhãn dán trên form để kiểm soát và sắp xếp

Tạo phong cách cho văn bản được nhập vào và submit button khá đơn giản, việc khó khăn ở đây là chọn boxes, radio button và kiểm tra việc nhất quán trên tất cả các trình duyệt, để làm được có thể tải các tập tin CSS có sẵn tại địa chỉ http://formalize.me

#### 3.2 STYLING TEXT INPUTS:

Các giá trị đi kèm với thuộc tính CSS cho xác định văn bản nhập vào là:

- **font-size**: Thiết lập kích thước của văn bản được nhập vào bởi người sử dụng

- **color**: Thiết lập màu sắc cho văn bản và background-color thiết lập màu nền nơi chứa văn bản

- **border**: thêm đường viền xung quanh các cạnh của hộp và border-radius sử dụng để bo tròn các góc (sử dụng cho các trình duyệt hỗ trợ thuộc tính này)

- **:focus** pseudo-class sử dụng để thay đổi màu nền của văn bản nhập vào và **:hover** pseudo-class áp dụng thêm phong cách khi người dùng rê chuột qua nó

- **background-image**: thêm ảnh nền cho hộp, bởi vì mỗi văn bản được nhập vào cần sử dụng hình ảnh khác nhau nên có thể sử dụng thuộc tính vùng chọn với giá trị là `id` cho mỗi văn bản được nhập vào.

#### 3.3 STYLING SUBMIT BUTTONS:

Một số thuộc tính được sử dụng để thêm phong cách cho submit button:

- **color**: sử dụng để thay đổi màu sắc của văn bản trong button

- **text-shadow**: trình duyệt cung cấp thuộc tính cho văn bản trông 3D hơn

- **border-bottom**: sử dụng để thêm đường viền bên dưới button làm nó trở nên dày hơn, tạo cảm giác 3D.

- **background-color**: làm cho nút submit trở nên nổi bậc hơn so với các mục xung quanh.

- **:hover** pseudo-class thay đổi sự xuật hiện của button khi người dùng hover qua nó.

#### 3.4 STYLING FIELDSETS & LEGENDS:

Thuộc tính Fieldsets rất hữu ích trong việc xác định các cạch cho form. The legend được sử dụng để chỉ ra các thông tin được yêu cầu trong fieldset. Thông thường thuộc tính nào bao gồm 2 giá trị:

- **width**: sử dụng để kiểm soát độ rộng của fieldset. 

- **color**: sử dụng để thay đổi màu sắc đằng sau các mục

- **border**: sử dụng để kiểm soát sự xuất hiện của đường viền xung quanh fieldset và legend

- **border-radius**: sử dụng để làm các cạnh trở nên linh hoạt hơn.

- **padding**: sử dụng để thêm khoảng cách giữa các phần tử

#### 3.5  ALIGNING FORM CONTROLS: PROBLEM:

#### 3.6 ALIGNING FORM CONTROLS: SOLUTION

#### 3.7 CURSOR STYLES (kiểu con trỏ):

**cursor**: thuộc tính cursor cho phép kiểm soát các loại con trỏ sẽ hiển thị cho người dùng. Một số giá trị của thuộc tính: auto, crosshair, default, pointer, move, text, wait, help, url("cursor.gif"). Nên sử dụng thuộc tính này để cung cấp thông tin hữu ích chi người dùng ở những nơi họ mong muốn thấy con trỏ.

#### WEB DEVELOPER TOOLBAR:

> Đây là công cụ mở rộng rất hữu ích cho trình duyệt Firefox và Chrome cung cấp công cụ hiển thị kiểu CSS được áp dụng cho phần tử khi rê chuột qua nó cùng với cấu trúc HTML

- Tải công cụ tại: www.chrispederick.com/work/web-developer

- Để xem kiểu CSS và cấu trúc HTML trong trang web vào menu CSS của Web Developer Toolbar và chọn xem thông tin

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task22_Book_HTML_and_CSS_design_and_build_websites/Chapter14_Lists%20Tables%20%26%20Forms/1.png"/></p>

1. OUTLINES: khi rê chuột qua thuộc tính sẽ hiển thị lên đường viền màu đỏ xung quanh hiển thị không gian mà phần tử đó chiếm.

2. STRUCTURE: khi rê chuột qua phần tử cấu trúc sẽ hiển thị ở phía trên cùng của phần tử. Ở đây ta có thể nhìn thấy phần tử `<li>` sử dụng class và bên trong là `<ul>` với class to-do. Danh sách bên trong phần tử `<div>` với id của trang được đặt trong phần tử `<body>` và `<html>`

3. CSS STYLES: khi rê chuột qua phần tử, click chuột để hiển thị CSS. Nó sẽ hiện ra các quy tắc được áp dụng trong phần tử, trên quy tắc đó có thể thấy được tên đường dẫn của nó.

### Tóm lại:

- Một vài thuộc tính CSS được sử dụng dùng để thiết lập nội dung của tất cả phần tử, số khác dùng để kiểm soát sự xuất hiện của lists, tables và forms.

- Đánh dấu danh sách để xuất hiện khác nhau thì sử dụng thuộc tính list-style-type và list-style image.

- Các ô trong bảng có thể có đường viền và khoảng cách khác nhau trong các trình duyệt khác nhau.

- Form được sử dụng dễ hơn nếu form đó được căn chỉnh theo chiều dọc bằng cách sử dụng CSS

<a name="4"></a>
### Tài liệu tham khảo

> [1] Duckett, J. (2011). HTML and CSS: design and build websites. John Wiley & Sons. 

