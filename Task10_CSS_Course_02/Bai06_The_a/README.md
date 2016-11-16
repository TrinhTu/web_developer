##Bài 6: Các thuộc tính CSS định dạng thẻ a (links)

>Tài liệu: Các thuộc tính CSS định dạng thẻ a (links)
>
>Người thực hiện: Lê Tú Trinh
>
>Cập nhập lần cuối: 16/11/2016

###Mục lục:

[1. Chọn màu sắc cho thẻ a](#1)

[2. Tắt gạch chân thẻ a với text-decoration](#2)

[3. Chọn background cho thẻ a](#3)

[4. Style các sự kiện (hover, vistied, active, link)](#4)

###Nội dung:

Thẻ a đóng vai trò quan trọng trong việc giúp chuyển trang giữa các file trong website, ngoài ra còn tác dụng chuyển hướng trang để các công cụ tìm kiếm có thể lọc toàn bộ website của người sử dụng.

<a name="1"></a>
####1. Chọn màu sắc cho thẻ a

Mặc định màu sắc của thẻ a là màu tím, nếu muốn thay đổi màu sắc cho thẻ a thì ta sử dụng thuộc tính `color` và `selector`: 

Ví dụ ta có 1 đoạn HTML như sau:

```
<a href="#"> Đây là nội dung được viết trong thẻ a</a>
```

Nếu muốn thay đổi màu sắc cho thẻ a phía trên bằng cách viết CSS, ta có:

```
	a{
		color: red;
	}
```
 Bây giờ thì thẻ a của ta đã có màu đỏ:

 ![1](https://github.com/TrinhTu/web_developer/blob/master/Task10_CSS_Course_02/Bai06_The_a/image/1.png)

<a name="2"></a>
####2. Tắt gạch chân thẻ a với text-decoration

Nhưng theo như ví dụ trên thì nội dung nằm bên trong thẻ a bị gạch chân bên dưới, vậy để tắt gạch chân cho thẻ a ta sử dụng thuộc tính `text-decoration` với giá trị là `none`

```
		text-decoration: none;
```

![2](https://github.com/TrinhTu/web_developer/blob/master/Task10_CSS_Course_02/Bai06_The_a/image/2.png)

<a name="3"></a>
####3. Chọn background cho thẻ a

Với thuộc tính background này ta có thể thêm màu nền, hình nền cho thẻ a...

```
		background: #ff9999;
```

![3](https://github.com/TrinhTu/web_developer/blob/master/Task10_CSS_Course_02/Bai06_The_a/image/3.png)

<a name="4"></a>
####4. Style các sự kiện (hover, visited, active, link)

Các sự kiện này sẽ thay đổi style khi ta rê chuột hay click vào thẻ a:

- `hover` : hover chuột qua nó sẽ có tác dụng

- `visited`: khi click vào thẻ a thì trạng thái của nó sẽ thay đổi

- `active`: khi click vào nhưng vẫn giữ chuột

- `link`: thẻ a chưa được click sẽ có tác dụng

Ta có ví dụ như sau:

![4](https://github.com/TrinhTu/web_developer/blob/master/Task10_CSS_Course_02/Bai06_The_a/image/4.png)

