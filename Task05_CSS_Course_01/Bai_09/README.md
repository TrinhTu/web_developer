##Bài 9: Box Model và các thuộc tính

> Tài liệu: Box Model và các thuộc tính
> 
> Thực hiện: Lê Tú Trinh
> 
> Cập nhập lần cuối: 26/10/2016

###Mục lục:

[1. Box Model ](#1)

- [1.1 Padding](#1.1)

- [1.2 Border](#1.2)

- [1.3 Margin](#1.3)

[2. Kiểm tra Box Model với Developer Tools](#2)

###Nội dung

<a name="1"></a>
####1. Box Model:

Là kĩ thuật cơ bản nhất trong CSS layout được sử dụng để mô tả về khoảng cách mà mỗi phần tử trên Website được sở hữu hay nói cách khác là kĩ thuật chỉnh khoảng cách cho mỗi phần tử trong Website.

Kĩ thuật Box Model trong CSS có 4 phần quan trọng đó là:

- Padding: là khoảng cách tính từ bên trong của phần tử.

- Margin: khoảng cách tính từ bên ngoài của phần tử.

- Content: nội dung trong phần tử.

- Border: đường viền của phần tử.

Được mô tả cụ thể như sau:

![anh](https://thachpham.com/wp-content/uploads/2015/04/box-model.gif)

Phần **content** sẽ không có thuộc tính nào đại diện cho nó vì nó là nội dung bên trong của phần tử. Còn 3 thuộc tính còn lại có giá trị như sau:
```
- margin: top right bottom left;
 
- border: top right bottom left;
 
- padding: top right bottom left;
```
<a name="1.1"></a>
####1.1 Padding:

 Là thiết lập khoảng cách từ phần **content** trở ra viền của phần tử, có thuộc tính là `padding` với các giá trị lần lượt là **top right bottom left** (trên > phải > dưới > trái) và có kèm theo đơn vị đo lường. 

 ![1](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_09/image/1.png)
 Nếu muốn thiết lập padding cho top và bottom cùng giá trị, left và right cùng giá trị thì có thể viết giá trị theo cách ngắn gọn 20px 10px, nghĩa là bottom sẽ có 20px left và right sẽ có 10px.

 Còn nếu chỉ nhập 1 giá trị thì nó sẽ tự động căn đểu 4 mặt với cùng 1 giá trị đó. Ngoài ra còn có thêm các thuộc tính khác như là `padding-top,padding-bottom, padding-left và padding-right` dùng để thiết lập cho từng mặt cụ thể.

 
<a name="1.2"></a>
####1.2 Border:

Nghĩa là thuộc tính để tạo viền cho phần tử sẽ được khai báo bằng thuộc tính `border` trong CSS.
 
 Cấu trúc: `border: [size] [type] [color];	

 Ví dụ nếu muốn tạo 1 viền có kích thước 1px kiểu trơn và màu viền là đỏ thì ta có như sau

 `border: 1px solid red;`

 Kiểu `type` có 1 số giá trị như sau: `solid`, `dotted`, `double`, `groove`, `ridge`, `inset`, `outset`

 Giống như các thẻ trên, `border` cũng có các thẻ con là `border-top`, `border-right`, `border-bottom`, `border-left`.

 Xem thêm thông tin về cách sử dụng các thuộc tính trong CSS Border http://www.w3schools.com/css/css_border.asp

 Ví dụ cụ thể:

 ![2](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_09/image/2.png)
 
<a name="1.3"></a>
####1.3 Margin:

Trong Padding cón nhiệm vụ tạo khoảng cách giữa các phần tử Content với Margin sẽ có tác dụng tạo khoảng cách từ Border trở ra ngoài tức là nó sẽ giúp bạn tùy chỉnh khoảng cách giữa các phần tử với nhau. Ví dụ:

![3](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_09/image/3.png)

Giữa 2 giá trị **box** có 1 khoảng trắng, đó là Margin. Cú pháp của Margin tương tự như Padding đó là: top right bottom left. Và nó cũng có thuộc tính con là: `margin-top`, `margin-right`, `margin-bottom`, `margin-left`.

<a name="2"></a>
####2. Kiểm tra Box Model với Developer Tools:

Để kiểm tra Box Model thì trên trình duyệt Google Chrome và Firefor có tích hợp sẵn bộ dụng cụ dành cho nhà phát triển Web là Developer Tools.

Nhấn phím **F12** trên bàn phím để bật nó sau đó nhấn vào Tab computed (Google chrome) hoặc Box Model (Firefox) bên phải.

![4](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_09/image/4.png)

Trong khung đó miêu tả rõ là Vùng màu xanh là **content**, xanh lá cây là **Padding**, Cam là **Border**, da cam là **Margin**. Để xem thông tin phàn tử nhấn vào nút tìm kiếm bên tay trái

![5](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_09/image/5.png)

Rê chuột vào 1 phần tử bất kì trên Website và nhấn vào để xem Box Model bên tay phải, Có thể nhấn vô từng ô giá trị bên khung Box Model và thay đổi giá trị để xem sự thay đổi của nó ( sẽ mất sau khi refresh trình duyệt).

![6](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_09/image/6.png)
