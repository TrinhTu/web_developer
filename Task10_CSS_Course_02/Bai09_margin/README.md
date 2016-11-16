##Bài 9: Thuộc tính margin-padding và Box Model trong CSS

>Tài liệu: Thuộc tính margin-padding và Box Model trong CSS
>
>Người thực hiện: Lê Tú Trinh
>
>Cập nhập lần cuối: 16/11/2016

###Mục lục:

[1. Thuộc tính margin và padding trong CSS](#1)

- [1.1 Margin](#1.1)

- [1.2 Padding](#1.2)

[2.Mô hình Box Model trong CSS](#2)

###Nội dung: 

<a name="1"></a>
####1. Thuộc tính margin và  padding trong CSS:

<a name="1.1"></a>
#####1.1 Margin:

Dùng để tạo khoảng cách giữa 2 thẻ HTML, `margin` thuộc tính con sau: `left`, `right`, `top`, `bottom`

- `left`: căng lề bên trái

- `right`: căng lề bên phải

- `top`: căn lề bên trên

- `bottom`: căn lề bên dưới

Ngoài ra chúng ta còn có thể sử dụng cú pháp như sau:

```
		margin: 20px;
```
 Điều đó có nghĩa là căn lề trên dưới trái phải đều bằng nhau và bằng 20px. Khi sử dụng thuộc tính margin sẽ không ảnh tới chiều rộng. Ví dụ:

 ![a](https://github.com/TrinhTu/web_developer/blob/master/Task10_CSS_Course_02/Bai09_margin/image/(a).png)

 Sau khi ta thiết lập chiều rộng và padding thì chiều rộng khung vẫn không thay đổi.

 ![b](https://github.com/TrinhTu/web_developer/blob/master/Task10_CSS_Course_02/Bai09_margin/image/(b).png)

<a name="1.2"></a>
#####1.2 Padding:

Thuộc tính padding dùng để tạo khoảng cách giữa các thẻ HTML và nội dung bên trong của nó. Nó cũng có cái giá trị tương tự như `margin`. Khi sử dụng padding thì chiều rộng của thẻ cũng tăng lên:

Cũng với các thông số như ví dụ vừa rồi, khi ta thêm thuộc tính `padding` với giá trị là 10px thì khung của tăng lên.

![c](https://github.com/TrinhTu/web_developer/blob/master/Task10_CSS_Course_02/Bai09_margin/image/(c).png)

![d](https://github.com/TrinhTu/web_developer/blob/master/Task10_CSS_Course_02/Bai09_margin/image/(d).png)


<a name="2"></a>
####2. Mô hình Box Model trong CSS:

Sự kết hợp của 3 thuộc tính `margin`, `padding`, `border` ta có được mô hình Box Model

![e](https://github.com/TrinhTu/web_developer/blob/master/Task10_CSS_Course_02/Bai09_margin/image/(e).png)
