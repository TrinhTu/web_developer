##Bài 7: Thuộc tính display trong CSS

>Tài liệu: Thuộc tính display trong CSS
>
>Người thực hiện: Lê Tú Trinh
>
>Cập nhập lần cuối: 16/11/2016

###Mục lục:

[1. Phân biệt display inline-block của thẻ HTML](#1)

[2. Ẩn thẻ HTML với thuộc tính display none](#2)

[3. Thay đổi giá trị display cho các thẻ](#3)

###Nội dung:

<a name="1"></a>
####1. Phân biệt display inline- block của thẻ HTML:

**Inine**: 
Là cách hiển thị trên 1 hàng, chiều rộng sẽ phụ thuộc vào nội dung bên trong của thẻ, dù ta có thêm thuộc tính `margin` cũng không thể hiển thị được. Các thẻ được mặc định là **inline**: `span`, `a`, `strong`, `b`, `i`,...Ví dụ:

![1](https://github.com/TrinhTu/web_developer/blob/master/Task10_CSS_Course_02/Bai07_Display/image/(1).png)

**Block**:

Đây là kiểu hiển thị nội dung theo từng dòng, khác với kiểu Inline là nội dung hiển thị trên cùng 1 dòng, kiểu block mặc định cho nội dung từng thẻ nằm bên trong nó chiếm chiều rộng 100%. Các thẻ HTML hiển thị Block là: `div`, `p`, `h1`, `header`, `footer`, `section`, `nav`,... Ví dụ:

![2](https://github.com/TrinhTu/web_developer/blob/master/Task10_CSS_Course_02/Bai07_Display/image/(2).png)

**Inline-block**: đây là kiểu hiển thị kết hợp 2 cách trên, sử dụng cho việc muốn thẻ hiển thị dạng khối nhưng nằm trên cùng 1 dòng.

<a name="2"></a>
####2. Ẩn thẻ HTML với thuộc tính display none:

Nếu muốn ẩn thẻ HTML thì dùng thuộc tính `display: none`

![3](https://github.com/TrinhTu/web_developer/blob/master/Task10_CSS_Course_02/Bai07_Display/image/(3).png)

Như chúng ta có thể thấy, thẻ `div` có thuộc tính `display: none` đã bị ẩn đi.

<a name="3"></a>
####3. Thay đổi giá trị display cho các thẻ HTML:

Để thay đổi giá trị cho các thẻ, sử dụng thuộc tính : `none`, `inline`, `block`, `inline-block` thì theo cú pháp:

```	
		display: value;
```
