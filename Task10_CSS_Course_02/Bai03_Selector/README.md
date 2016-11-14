##Bài 3: Tìm hiểu CSS Selector căn bản

>Tài liệu: Tìm hiểu CSS Selector căn bản
>
>Người thực hiện: Lê Tú Trinh
>
>Cập nhập lần cuối: 14/11/2016

###Mục lục:

[1. Selector là gì?](#1)

[2. Các CSS selector thông dụng](#2)

- [2.1 Selector phân cấp](#2.1)

- [2.2 Selector ID](#2.2)

- [2.3 Selector class](#2.3)

[3. Một vài lưu ý về CSS Selector](#3)

###Nội dung:

<a name="1"></a>
####1. Selector là gì?

CSS trong selector dùng để truy vấn đến các thẻ HTML. Trong HTML có nhiều thẻ giống nhau và ta phải đặt cho nó các ID, class để dễ phân biệt, CSS sẽ dựa vào đó để truy xuất tới phần nội dung đó, cách truy xuất đó là selector. Ví dụ: 

```
<!-- Truy xuất tới thẻ div và gán màu cho nó:-->
div{
	background: red;
}
```

<a name="2"></a>
####2. Các CSS selector thông dụng:

<a name="2.1"></a>
#####2.1 Selector phân cấp:

Phân cấp là dựa vào cấp mẹ để tìm cấp con, tức là dựa vào thẻ bao bọc bên ngoài mà tìm ra thẻ cần tìm nằm bên trong thẻ đó.

Ví dụ ta có tài lệu HTML như sau:

```
<div>
	<p>Đây là nội dung nằm bên trong thẻ p</p>
</div>
	<p>Nội dung này cũng nằm trong thẻ p nhưng không nằm trong thẻ `div`</p> 
```
Thêm CSS:

```
div p {
	color: blue;
}
``` 
Ta có kết quả như sau:

![1](https://github.com/TrinhTu/web_developer/blob/master/Task10_CSS_Course_02/Bai03_Selector/image/1.png)

<a name="2.2"></a>
#####2.2 Selector ID:

Trong 1 trang web thì ID là duy nhất, không được định nghĩa 2 ID giống nhau trong 1 layout. Dấu # chính là đại diện cho ID. Ví dụ:

HTML:

```
<div id="hihi"> <!--thẻ div sử dụng ID-->
	XIN CHÀO
</div>
<div> <!--thẻ div không sử dụng ID-->
	TẠM BIỆT
</div>
```
CSS:

```
div#hihi {
	color:red;
}
```

Ta xem kết quả:

![2](https://github.com/TrinhTu/web_developer/blob/master/Task10_CSS_Course_02/Bai03_Selector/image/2.png)

<a name="2.3"></a>
#####2.3 Selector class:


`class` là viết CSS cho nhiều thẻ cùng lúc mà không cần phải viết đi viết lại nhiều lần. Selection cho `class` là dấu `(.)`

Ví dụ:

HTML:

```
<div class="color">
	Green
</div>
<div class="color">
	Green
</div>
<div class="color">
	Green
</div>
<div>
	Không có màu gì hết
</div>
```

CSS:

```
.color{ color: green;}
```
![3](https://github.com/TrinhTu/web_developer/blob/master/Task10_CSS_Course_02/Bai03_Selector/image/3.png)

<a name="3"></a>
####3. Một vài lưu ý về CSS selector:

Cần phân biệt giữa ID selector với CSS selector:

- `ID`: là duy nhất, sử dụng cho những vị trí không có tính lặp lại nhiều lần

- `class` có thể dùng đặt nhiều vị trí để tiện cho việc thêm thuộc tính nhanh hơn, tiện hơn mà không cần phải viết lại nhiều lần

- Dù là `ID` lhay `class` thì đều có quy luật phân cấp

Phân biệt giữa viết liền và có dấu cách:

- `div#trinh`: chọn thẻ div có id là trinh

- `div #trinh`: chọn thẻ có id là trinh nằm trong thẻ div
