## Bài 13: Chia cột với float và clear float

> Tài liệu: Chia cột với float và clear float 
> 
> Thực hiện: Lê Tú Trinh
> 
> Cập nhập lần cuối: 30/10/2016

### Mục lục

[1. Chia cột trong CSS](#1)

[2. Các bước chia cột](#2)

[3. Cách chia cột](#3)

[4. Cách sử dụng Clear float](#4)

- [4.1.Sử dụng thẻ `div` trống](#4.1)

- [4.1. Sử dụng overflow](#4.2)

### Nội dung:

<a name="1"></a>
#### 1. Chia cột trong CSS:

Khi thực hiện viết tài liệu trong website thì có 1 kĩ thuật rất quan trọng và không thể thiếu đó là cách chia cột, vậy việc chia cột trong CSS là việc thiết lập các phần tử con trong phần tử mẹ nằm trên cùng 1 hàng. Để thực hiện được việc đó trước tiên cần tạo ra 1  thẻ `div` container ( phần tử mẹ ) và các thẻ `div` nằm bên trong các phần tử mẹ đó là các phần tử con để thực hiện việc chia cột (column). Cơ bản như sau:

```
<div id="content" class="container">
  <div id="cot1">Cột thứ nhất</div>
  <div id="cot2">Cột thứ hai</div>
</div>
```
Vậy phần `content` ở đây  là phần tử mẹ trong đó chưa 2 nội dung là `cot1` và `cot2` việc cần làm là thiết lập sao cho 2 nội dung đó thành 2 cột riêng biệt nằm thẳng hàng với nhau.

<a name="2"></a>
#### 2. Các bước chia cột:

- Tạo 1 container bao bọc các phần tử bên trong

- Thiết lập những giá trị cơ bản cho container như width, height, padding, border, margin,...

- Thiết lập width, height, background-color, color,.. cho các nội dung bên trong hay là 2 cột cần chia sao cho tổng width height của 2 cột không vượt quá width height của container.

- Thêm vào 2 cột thuộc tính `float` với các giá trị `left` `right` để phần tử hiển thị bên trái hoặc bên phải.

- Tiến hành clear float.
<a name="3"></a>
#### 3. Cách chia cột:
 - Thiết lập các thuộc tính cơ bản cho container:

```
.container{
  height: 300px;
  width: 600px;
  padding: 20px;
  border: 20px inset green;
  margin: 0 auto;
}
```
- Thiết lập width height cho `cot1`:

```
#cot1{
  width:300px;
  height: 150px;
  background: #ff9900;
}
```
- Thiết lập tương tự với `cot2`:

```
#cot2{
  width:300px;
  height: 150px;
  background: #ff3399;
}
```

Sau khi thiết lập cơ bản ta có result như sau:

![5](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_13/image/5.png)

- Thêm thuộc tính `float` vào 2 cột:

Cột 1 cho hiển thị phía bên trái :  ` float: left;`

Cột 2 cho hiển thị về phía bên phải:  ` float: right;`

Ta sẽ có kết quả như sau:

![6](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_13/image/6.png)

Nhưng ở đây khi ta thêm giá trị height vào `container` thì 2 cột sẽ bị giới hạn về chiều rộng có thể không bao phủ hết chiều rộng hoặc bị nhảy ra ngoài.

![7](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_13/image/7.png)

 Mặc khác nếu thêm height cho `container` thì nếu nội dung bên trong dài quá thì nó không thể hiển thị tiếp được vì đã bị giới hạn bởi độ dài cố định vậy nên ta có cách giải quyết vấn đề này bằng cách sử dụng **Clear float**

<a name="4"></a>
#### 4. Cách sử dụng Clear float:

Clear float là tạo điểm kết thúc cho phần tử cho nó không float ra ngoài khung mẹ.

<a name="4.1"></a>
##### 4.1 Cách sử dụng thẻ `div` trống:

Tạo thêm 1 thẻ `div` trống không có nội dung với thuộc tính khai báo là `class` với giá trị là `clear` nằm ở hàng cuối cùng trong nội dung.

```
<div id="content" class="container">
  <div id="cot1">Cột thứ nhất</div>
  <div id="cot2">Cột thứ hai</div>
  <div class="clear"></div>
</div>
```

 Viết CSS cho class tên là clear với nội dung sau:
```
		.clear { clear:both}
```

Both nghĩa là clear đều 2 bên. Vậy bây giờ khung của mình đã nằm bên trong và không bị float ra ngoài nữa:

![8](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_13/image/8.png)


<a name="4.2"></a>
##### 4.2 Sử dụng overflow:

Tìm đến phần tử mẹ và thêm cho nó thuộc tính ở phần CSS là `overflow: auto;` mà không cần chỉnh sửa nội dung phần HTML

![9](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_13/image/9.png)
