## HTML & CSS

### IMAGES

> Chương 16: IMAGES
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 19/02/2017

## Mục lục:

[1. Controlling size of images in CSS](#1)

[2. Aligning images in CSS](#2)

[3. Adding background images](#3)

[Tài liệu tham khảo](#4)

***

<a name="1"></a>
### 1. CONTROLLING SIZES OF IMAGES IN CSS (Kiểm soát kích thước của hình ảnh trong CSS):

- Có thể kiểm soát kích thước của hình ảnh bằng cách sử dụng thuộc tính chiều rộng và chiều cao trong CSS. Xác định kích thước của hình ảnh giúp cho trang web của bạn tải nhanh hơn bởi vì các đoạn mã trong HTML và CSS thường được tải trước hình ảnh, và nói với trình duyệt không gian để lại cho 1 hình ảnh để trang có thể tiếp tục tải mà không cần đợi hình ảnh tải xong.

```javascript
img.large {
width: 500px;
height: 500px;}
img.medium {
width: 250px;
height: 250px;}
img.small {
width: 100px;
height: 100px;}
```

- Trên trang web có thể sử dụng nhiều hình ảnh có kích thước khác nhau nhưng thông thường thì sử dụng hình ảnh có cùng kích thước tương đương với nhau trên nhiều trang. Có thể lựa chọn hình ảnh có kích thước phổ biến trên tất cả các trang như:

	+ Small portrait: 220 x 360

	+ Small landscape: 330 x 210

	+ Feature photo: 620 x 400

Khi sử dụng kích thước thống nhất cho hình ảnh trong website có thể sử dụng CSS để kiểm soát kích thước của hình ảnh thay vì đặt trong HTML.

```javascript
img.large {
width: 500px;
height: 500px;}
img.medium {
width: 250px;
height: 250px;}
img.small {
width: 100px;
height: 100px;}
```

- Đầu tiên là cần xác định kích thước của hình ảnh thường được sử dụng trong website và cho mỗi kích thước 1 tên tương ứng như: small, medium, large. Tring HTML tại nơi phần tử `<img>` thay vì sử dụng thuộc tính width, height thì có thể sử dụng tên như các giá trị cho thuộc tính class. Trong CSS có thể thêm lựa chọn cho mỗi tên class và sử dụng thuộc tính width, height trong CSS để kiểm soát kích thước của hình ảnh.

<a name="2"></a>
### 2. ALIGNING IMAGES USING CSS (Căn chỉnh hình ảnh sử dụng CSS):

- Thay vì sử dụng thuộc tính align của phần tử `<img>` thì sử dụng thuộc tính float đẻ căn chỉnh hình ảnh, gồm có 2 giá trị sau:

	1. Thuộc tính float được thêm vào trong class để đại diện cho kích thước của hình ảnh

	2. Class mới được tạo ra với tên như: align-left hoặc align-right để căng chỉnh hình ảnh xuất hiện về bên trái hay bên phải của trang, ngoài ra còn sử dụng để chỉ định kích thước của hình ảnh. Nó cũng thường được thêm vào margin để đảm bảo rằng các đoạn văn không chạm vào các cạnh của hình ảnh
#### 2.1 CENTERING IMAGES USING CSS (Căng hình ảnh ở giữa):

- Theo mặc định thì hình ảnh là phần tử inline vậy nên các văn bản sẽ hiển thị xung quanh nó, để hình ảnh được căng chỉnh ở giữa thì nó phải trở thành 1 phần tử blocklevel sử dụng thuộc tính display với giá trị là block.

```
img.align-center {
display: block;
margin: 0px auto;}
img.medium {
width: 250px;
height: 250px;}
```

- Khi trở thành phần tử block-level thì có 2 cách để hình ảnh ở trung tâm theo chiều ngang:

	1. Trong phần tử đang chứa sử dụng thuộc tính text-align với giá trị là center.

	2. Trong hình ảnh đó sử dụng thuộc tính margin và thiết lập giá trị ở bên phải bên trái là auto. 

<a name="3"></a>
### 3.BACKGROUND IMAGES (Ảnh nền):

- Thuộc tính background-image cho phép đặt hình ảnh bất kì phía sau phần tử HTML, theo mặc định thì hình ảnh nền sẽ được lặp lại sau sao điền đầy hộp. Đường dẫn hình ảnh được đặt trong `url` và bên trong dấu ngoặc kép. Như các hình ảnh được sử dụng trực tiếp, nếu kích thước của tập tin đó lớn thì sẽ mất nhiều thời gian để tải hơn.

#### 3.1 REPEATING IMAGES (Lặp lại hình ảnh):

**Repeating images & background-attachment**

- Thuộc tính background-repeat gồm có 4 giá trị:

	+ **repeat**: Hình nền được lặp lại về chiều ngang và chiều dọc 

	+ **repeat-x**: hình ảnh sẽ được lặp lại theo chiều ngang

	+ **repeat-y**: hình ảnh sẽ được lặp lại theo chiều dọc

	+ **no-repeat**: chỉ hiển thị duy nhất 1 hình. Thuộc tính Background-attachment xác định vị trí hiển thị hình ảnh hoặc di chuyển bởi người dùng, nó có 2 giá trị:

		- **fixed**: hình ảnh ở 1 vị trí cố định trong trang web

		- **scroll**: hình ảnh sẽ được di chuyển bằng cách kéo trang lên xuống.

#### 3.2 BACKGROUND POSITION (Vị trí hình nền):

**background-position**: Khi 1 hình ảnh không được lặp lại có thể sử dụng thuộc tính background-position để xác định vị trí đặt hình ảnh. Thuộc tính sử dụng bởi 1 cặp giá trị, giá trị đầu tiên là chiều ngang, giá trị thứ 2 là chiều dọc: `left top`,  `left center`, `left bottom`, `center top`, `center center`, `center bottom`, `right top`, `right center`, `right bottom`.

- Nếu như chỉ xác định 1 giá trị thì mặc định giá trị thứ 2 sẽ là center. Cũng có thể sử dụng 1 cặp pixels và tỉ lệ phần trăm. 

#### 3.3 SHORTHAND (Viết gọn):

**background**: Các thuộc tính phải được xác định theo thứ tự sau, có thể bỏ qua bất cứ giá trị nào nếu như không muốn xác định nó.

+ 1: background-color

+ 2: background-image

+ 3: background-repeat

+ 4: background-attachment

+ 5: background-position

CSS3 cung cấp cho bạn nhiều ảnh nền bằng cách lặp lại cách background shorthand, vì không phải tất cả các trình duyệt đều cung cấp thuộc tính này, nó không được sử dụng phổ biến.

```
div {
background:
url(example-1.jpg)
top left no-repeat,
url(example-2.jpg)
bottom left no-repeat,
url(example-3.jpg)
centre top repeat-x;}
```

#### 3.4 IMAGE ROLLOVERS & SPRITES: 

- Bằng cách sử dụng CSS có thể tạo ra 1 liên kết hay 1 button thay đổi bằng 2 cách là khi người dùng di chuyển chuột trên nó (được gọi là rollover) và phong cách tiếp theo đó là khi người dùng click vào nó. Khi người dùng di chuyển chuột trên các phần tử hoặc click vào nó thì vị trí của hình nền sẽ được di chuyển đến các hình ảnh liên quan.

- Khi sử dụng 1 hình ảnh duy nhất cho 1 số các phần khác nhau của 1 giao diện đó được gọi là sprite, có thể thêm logo và các giao diện khác cũng như các button trên hình ảnh. Ưu điểm của việc sử dụng sprites là trình duyệt web chỉ cần yêu cầu 1 hình ảnh hơn là nhiều hình ảnh và làm cho các trang web tải nhanh hơn.

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task22_Book_HTML_and_CSS_design_and_build_websites/Chapter16_IMAGES/11.png"/></p>

- Trong ví dụ trên có thể thấy 2 liên kết nằm trong button, và mỗi button nằm trong 3 bảng khác nhau và tất cả đại diện cho 1 hình ảnh duy nhất

- Bởi vì phần tử `<a>` là phần tử inline vậy nên thiết lập thuộc tính display của link để chỉ định nó thành phần tử inline-block. Ở đây cho phép bạn xác định chiều dài và chiều rộng cho mỗi phần tử vì vậy kích thước của nó sẽ tương ứng với các button.

- Thuộc tính background-position được sử dụng di chuyển hình ảnh để nó hiện thị đúng trong button. Khi người dùng di chuyển chuột qua các liên kết, hover pseudo-class là quy tắc dùng di chuyển background-position của hình ảnh hiển thị trong các trạng thái khác nhau trong button. Tương tự người dùng có thể click vào các liên kết, active pseudo-class là quy tắc hiển thị the third state cho button.

#### 3.5 CSS3: GRADIENTS:

CSS3 giới thiệu 1 cách xác định 1 gradient cho màu nền của hộp, gradient được tạo ra bằng cách sử dụng thuộc tính background-image, các trình duyệt khác nhau thì yêu cầu các cú pháp khác nhau. Vì nó không được hỗ trợ trên tất cả trình duyệt vậy nên có thể xác định hình nền cho hộp trước và cung cấp các lựa chọn thay thế cho các trình duyệt có hỗ trợ gradient CSS.

#### 3.6 CONTRAST OF BACKGROUND IMAGES:

- Khi muốn phủ văn bản trên hình ảnh nền thì hình ảnh đó phải có độ tương phản thấp để văn bản dễ đọc

	+ **Hight contrast**: đa số thì các hình ảnh có độ tương phản khá cao và không phù hợp để sử dụng là hình nền

	+ **Low contrast**: sử dụng các ứng dụng chỉnh sửa hình ảnh để có được hình ảnh có độ tương phản thấp hơn

	+ **Screen**: để che phủ văn bản trên 1 hình ảnh có độ tương phản cao có thể đặt 1 hình nền semi-transparent (trong suốt) để cho văn bản trở nên dễ đọc hơn.

<a name="4"></a>
### Tài liệu tham khảo

> [1] Duckett, J. (2011). HTML and CSS: design and build websites. John Wiley & Sons. 

