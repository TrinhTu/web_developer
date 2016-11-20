##Bài 14: Thuộc tính `z-index` trong CSS

>Tài liệu: Thuộc tính `z-index` trong CSS
>
>Người thực hiện: Lê Tú Trinh
>
>Cập nhập lần cuối: 19/11/2016

###Mục lục:

[1. Thuộc tính `z-index` trong CSS](#1)

[2. Ví dụ `z-index` trong CSS](#2)

- [2.1 `z-index` khi không có position absolute](#2.1)

- [2.2 `z-index` giữa absolute và không có absolute](#2.2)

- [2.3 `z-index` giữa hai thẻ có absolute](#2.3)

###Nội dung:

<a name="1"></a>
####1. Thuộc tính `z-index` trong CSS:

Thuộc tính `z-index` nhằm đánh số thứ tự hiển thị, thẻ nào có `z-index` lớn hơn thì sẽ hiển thị phía trên còn thẻ nào có `z-index` nhỏ hơn thì hiển thị phía dưới.

`z-index` có các tính chất sau:

- Chỉ thiết lập `z-index` được cho các thẻ có khai báo: `position:absolute`

- Giá trị của `z-index` có thể là số âm hoặc dương

- Hai thẻ `z-index` thì cùng tuân theo quy luật thẻ nào nằm dưới sẽ hiển thị phía trên, thẻ con sẽ nằm trên thẻ cha.

- Giá trị `z-index` mặc định của các thẻ HTML là 1

Cú pháp của `z-index` như sau:

```
		selector{
		z-index: value;
		}
```

Trong đó selector là vùng chọn cần áp dụng CSS, còn value là giá trị của thuộc tính, `z-index` có 1 số giá trị sau đây:

- auto: tự động sắp xếp chồng lên nhau theo thứ tự mặc định HTML.

- một con số: sắp xếp chồng lên nhau theo giá trị truyền vào.

- inherit: thừa hưởng thuộc tính `z-index` của thành phần cha.


<a name="2"></a>
####2. Ví dụ `z-index` trong CSS:


Ta có ví dụ sau:

```
<div id="vd1">
</div>
<div id="vd2">
</div>
```
<a name="2.1"></a>
#####2.1 `z-index` khi không có position absolute:

Viết CSS cho thẻ `div#vd2` đè lên thẻ `div#vd1`, và thiết lập `z-index` sao cho #vd1 > #vd2

```
#vd1{
	width: 200px;
	height: 100px;
	background: tomato;
	z-index: 2;
}
#vd2{
	width: 200px;
	height: 100px;
	background: aqua;
	margin-top: -50px;
	z-index: 1;
}
```

![1](https://github.com/TrinhTu/web_developer/blob/master/Task10_CSS_Course_02/Bai13_z-index/image/11.png)

Vì cả 2 thẻ chưa sử dụng thuộc position nên không áp dụng được `z-index`

<a name="2.2"></a>
#####2.2 `z-index` giữa absolute và không có absolute:


Khai báo tương tự ví dụ trên nhưng thay vì `#vd2` nhận giá trị `z-index` là 1 thì ta thay bằng giá trị âm. Trong ví dụ này ta  áp dụng `z-index` cho `#vd2` và khai báo cho nó thuộc tính là `position: absolute` thì cách hiển thị của nó sẽ như thế này:

```
#vd1{
	width: 200px;
	height: 100px;
	background: tomato;
	z-index: 1;
}
#vd2{
	width: 200px;
	height: 100px;
	background: aqua;
	position:absolute;
	z-index: -2;
	top: 50px;
```

![2](https://github.com/TrinhTu/web_developer/blob/master/Task10_CSS_Course_02/Bai13_z-index/image/12.png)

<a name="2.3"></a>
#####2.3 `z-index` giữa hai thẻ có absolute:

Trường hợp này cũng tương tự, thẻ nào có `z-index` cao hơn sẽ nằm ở trên.

```
#vd1{
	width: 200px;
	height: 100px;
	background: tomato;
	z-index: 1;
	top: 30px;
	left: 50px;
}
#vd2{
	width: 200px;
	height: 100px;
	background: aqua;
	position:absolute;
	z-index: 3;
	top: 50px;
	left: 80px;
```

![3](https://github.com/TrinhTu/web_developer/blob/master/Task10_CSS_Course_02/Bai13_z-index/image/13.png)

Rõ ràng ở `#vd2` có `z-index` cao hơn nên đã hiển thị đè lên trên `#vd1`

