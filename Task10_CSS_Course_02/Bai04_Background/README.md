##Bài 4: Thiết lập màu nền với CSS background

>Tài liệu: Thiết lập màu nền với CSS background
>
>Người thực hiện: Lê Tú Trinh
>
>Cập nhập lần cuối: 14/11/2016

###Mục lục:

[1. Thiết lập màu nền](#1)

[2. THiết lập hình nền](#2)

[3. Cho phép lặp hoặc không lặp background](#3)

[4. Thiết lập vị trí hiển thị background](#4)

[5. Thiết lập background đứng im khi scroll( fixed background)](#5)

[6. Sử dụng thuộc tính background nâng cao](#6)

[7. Sử dụng selector và background](#7)

###Nội dung:

<a name="1"></a>
####1. Thiết lập màu nền cho background:

Cái này đơn giản chỉ việc vào trong thẻ muốn áp dụng CSS và sử dụng cú pháp như sau:

```
div{
	background-color: tên hoặc mã màu 
}
```
Hoặc sử dụng `background` thay vì `background-color`

<a name="2"></a>
####2. Thiết lập hình nền cho background:

Sử dụng thuộc tính **CSS background** hoặc `background-image` với tham số là URL của hình ảnh:

```
body{
	background-image: url('http://i.imgur.com/6sjqzTh.jpg');
}
```

Kết quả hiển thị như sau:

![a](https://github.com/TrinhTu/web_developer/blob/master/Task10_CSS_Course_02/Bai04_Background/image/a.png)

<a name="3"></a>
####3. Cho phép lặp hoặc không lặp background:

Nhưng ở trên có thể thấy là cái hình bị lặp lại 2 lần, vậy nếu không muốn nó lặp thì sử dụng thuộc tính `background-repeat` có các giá trị như sau:

- `no-repeat`: không lặp

- `repeat`: cho lặp

- `repeat-X` lặp theo chiều ngang

- `repeat-y` : lặp theo chiều đứng

Áp dụng lại với ví dụ trên

```
body{
	background: url('http://i.imgur.com/6sjqzTh.jpg');
	background-repeat: no-repeat;
}
```

![b](https://github.com/TrinhTu/web_developer/blob/master/Task10_CSS_Course_02/Bai04_Background/image/b.png)

Dễ thương rồi đó! hihi
<a name="4"></a>
####4. Thiết lập vị trí hiển thị background

Nhưng cũng đối với hình ở trên, giờ muốn nó hiển thị giữa chính giữa(center) hay bên phải(right)... thì ta sử dụng thuộc tính `background-position`. Cấu trúc như sau:

```
			background-position: position1 position 2;
```

Nó cũng có các giá trị như sau:

- `bottom`: ở dưới

- `left`: bên trái

- `right`: bên phải

- `center`: ở giữa

- `top`: ở trên

Ví dụ muốn cho hình hiển thị chính giữa phía bên trên:

```
	background-position: center top;
```

![c](https://github.com/TrinhTu/web_developer/blob/master/Task10_CSS_Course_02/Bai04_Background/image/c.png)

<a name="5"></a>
####5. Thiết lập background đứng im khi scroll( fixed background)

Nếu như màn hình dài quá, sẽ bị thay đôi, dịch chuyển khi kéo lên, muốn nó đứng yên thì sử dụng thuộc tính background-attachment, có 2 giá trị như sau:

- `fixed`: sẽ đứng im

- `scroll`: di chuyển khi kéo theo

Ví dụ:

```
body{
	background: url('http://i.imgur.com/6sjqzTh.jpg');
	background-repeat: no-repeat;
	background-position: center top;
	background-attachment: fixed;
	height: 1000px;
	}
```
<a name="6"></a>
####6. Sử dụng thuộc tính background nâng cao

Thay vì sử dụng nhiều câu lệnh cú pháp dài dòng có thể ghi tắt ở dạng như sau:

```
	background: url('http://i.imgur.com/6sjqzTh.jpg') no repeat center top fixed;
```
<a name="7"></a>
####7. Sử dụng selector và background

Điều này có nghĩa là thay vì như các ví dụ trên ta sử dung CSS và các thuộc tính áp dụng cho  thẻ `body` thì ta có thể sử dụng cho bất cứ thẻ nào khác và cũng phải tuân theo quy luật phân cấp và áp dụng CSS đúng chỗ. 
