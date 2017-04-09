## Bài 12: Màu nền và ảnh nền (background)

> Tài liệu: Màu nền và ảnh nền 
> 
> Thực hiện: Lê Tú Trinh
> 
> Cập nhập lần cuối: 30/10/2016

### Mục lục:

[1. Màu nền với background-color](#1)

[2. Ảnh nền với background-image](#2)

[3. Tùy chỉnh lặp lại ảnh nền với background-repeat](#3)

[4. Đổi vị trí ảnh nền với background-position](#4)

### Nội dung

<a name="1"></a>
#### 1. Màu nền với background-color:

Như trong các bài học trước mặt dù chưa học tới thuộc tính màu nền nhưng ta đã áp dụng rất nhiều trong tất cả các ví dụ, vậy nên thuộc tính màu nền khá là đơn giản với cú pháp như sau: 

```
			background-color: tên màu;
```
Thay vì sử dụng tên màu ta cũng có thể thay bằng sử dụng mã màu. Ví dụ:

![1](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_12/image/1.png)


<a name="2"></a>
#### 2. Ảnh nền với background-image:

Ảnh nền với `background-image` cũng khá là đơn giản. Cú pháp như sau:

```
	background-image: url('anh1'), url('anh2'),...;
```

Trong đó bên trong giá trị 	`url` là đường dẫn tới ảnh đó, chúng ta có thể thêm nhiều ảnh bằng cách thêm nhiều thuộc tính `url` ngăn cách nhau bởi dấu phẩy. Ví dụ:

![2](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_12/image/2.png)

<a name="3"></a>
#### 3. Tùy chỉnh lặp lại ảnh nền với background-repeat:

Nếu như thiết lập chiều cao và chiều rộng của khung lớn hơn so với độ lớn của ảnh thì ảnh đó sẽ bị lặp lại chiều cao và chiều rộng cho đến khi nào lấp vừa khung của nội dung đó, vậy nên để tránh việc lặp lại hình ảnh như vậy ta có thêm 1 thuộc tính nữa đó là `background-repeat` và nó gồm các giá trị như sau:

- `no-repeat` : không lặp

- `repeat-x` : Lặp theo chiều ngang

- `repeat-y` : lặp theo chiều dọc

- `space` : lặp đều chiều ngang và chiều dọc, ảnh nền sẽ cách nhau bằng khoảng trắng.

- `repeat`: mặc định

![3](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_12/image/3.png)

<a name="4"></a>
#### 4. Đổi vị trí ảnh nền với background-position:

Đối với những tấm ảnh nhỏ dùng để chèn vô trong website mà muốn tùy chỉnh hiển thị vị trí đặt của nó thì dùng thuộc tính `background-position` , và thuộc tính này có giá trị như sau:

- `top` hiển thị trên đầu phần tử

- `bottom` hiển thị bên dưới phần tử

- `left` hiển thị bên trái phần tử

- `right` hiển thị bên phải phần tử

- `center` hiển thị ở giữa phần tử

- `y-x` tùy chỉnh vị trí tọa độ, với giá trị này có thể sử dụng tối đa 2 giá trị. Ví dụ như là `top right` là hiển thị phía trên bên phải phần tử. Ngoài ra còn có thể tham khảo thêm 1 vài thuộc tính tùy chỉnh ảnh nền tại https://developer.mozilla.org/en-US/docs/Web/CSS.

![4](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_12/image/4.png)
