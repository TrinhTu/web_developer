##Bài 24: Thay đổi hình dạng với transform và transform-origin

>Tài liệu: Thay đổi hình dạng với transform và transform-origin
>
>Người thực hiện: Lê Tú Trinh
>
>Cập nhập lần cuối: 26/11/2016

###Mục lục:

[1. Thay đổi hình dạng với transform](#1)

- [1.1 Xoay](#1.1)

- [1.2 Co giãn](#1.2)

- [1.3 Kéo nghiêng](#1.3)

[2. Tùy chỉnh tâm hình dạng với transform-origin](#2)

###Nội dung

<a name="1"></a>
####1. Thay đổi hình dạng với transform:

Với transform có thể xoay, co giãn kích thước hoặc bóp nghiêng hình dạng 1 phần tử. Cú pháp:

```
transform: function(value);
-moz-transform: function(value);
-webkit-transform: function( value);
```

Trong đó `function` là tên hàm làm thay đổi hình dạng và giá trị(value) của hàm, mỗi hàm sẽ có các cách viết giá trị khác nhau. Các hàm thay đổi giá trị thường dùng là: Skew, Scale, Rotate, Translate.

<a name="1.1"></a>
#####1.1 Xoay: (rotate)

Hàm `rotate` này nhằm thiết lập đối tượng bị xoay theo độ góc, giá trị của hàm này là: `[n]deg` ( giá trị góc đơn vị là độ) hoặc có thể `[n]turn`. Ví dụ:

```
<div id="rotate">
	<img src="http://nguonanhdep.com/wp-content/uploads/2016/08/avatar-de-thuong-1.jpg"/>
</div>
<div id="transition">
	<img src="http://nguonanhdep.com/wp-content/uploads/2016/08/avatar-de-thuong-1.jpg"/>
</div>
```

Thêm thuộc tính CSS:

```
 #rotate:hover img{
   	transform: rotate(4turn);
   	-webkit-transform: rotate(4turn);
   	-moz-transform: rotate(4turn);
   	float: left;
}
#transition img {
   	float: right;
}
#transition:hover img{
   	transform: rotate(180deg);
   	-webkit-transform: rotate(180deg);
   	-moz-transform: rotate(180deg);
}
```

Ta có kết quả như sau: http://tutrinh01.chuyengiaseoweb.net/transform.html

<a name="1.2"></a>
#####1.2 Co giãn:
 Hàm `scale` thiết lập kích thước của 1 phần tủ dựa vào trục thẳng đứng và trục ngang, hàm này có giá trị như sau: `scale(X)` hoặc `scale(Y)` 

 Ví dụ tương tự như trên ta thay giá trị của hàm `rotate` thành `scale`:

 ```
 #scale:hover img{
   	transform: scaleY(1.5);
   	-webkit-transform: scaleY(1.5);
   	-moz-transform: scaleY(1.5);
}
#transition img{
   	transition: 1s ease-in-out;
   	float: right;
}
#transition:hover img{
   	transform: scale(2);
   	-webkit-transform: scale(2);
   	-moz-transform: scale(2);
}
```

Kết quả như sau: http://tutrinh01.chuyengiaseoweb.net/scale.html

<a name="1.3"></a>
#####1.3 Kéo nghiêng:

Có thể kéo nghiêng đối tượng dựa trên trục Y và trục X với hàm `skewX()` và hàm `skewY()`, giá trị bên trong là số `[n]deg` tương tự như `rotate()`

```
#skew img{
   	float: left;
}
#skew:hover img {
  	transform: skewY(45deg);
    -moz-transform: skewY(45deg);
    -webkit-transform: skewY(45deg);
}

#transition img {
    transition: 1s ease-in-out;
    float: right;
}
#transition:hover img {
    transform: skew(-45deg);
    -moz-transform: skew(-45deg);
    -webkit-transform: skew(-45deg);
}
```

Kết quả như sau: http://tutrinh01.chuyengiaseoweb.net/skew.html

<a name="2"></a>
####2. Tùy chỉnh tâm hình dạng với transform:

Ngoài ra còn có thêm thuộc tính đó là `transform-origin`, cho phép dịch chuyển phần tử dựa vào thay đổi hình dạng `transform`. Thuộc tính `transform-origin` được dùng kèm với `transform` và có thể áp dụng cho bất kì hàm nào.

Thuộc tính `transform-origin` có 2 giá trị là X (phương thẳng đứng) và Y (phương nằm ngang), giá trị của nó sẽ phụ thuộc vào kích thước của phần tử

```
	transform-origin: 100% 50%;
```

Ví dụ:

```
<img  class="rotate" src="http://images4.fanpop.com/image/photos/23300000/Pikachu-pikachu-23385611-400-500.jpg"/>
<img  class="scale" src="http://images4.fanpop.com/image/photos/23300000/Pikachu-pikachu-23385611-400-500.jpg"/>
<img class="skew" src="http://images4.fanpop.com/image/photos/23300000/Pikachu-pikachu-23385611-400-500.jpg"/>
```
Thêm CSS:

```
  transition: 1s ease-in-out;
}

.rotate:hover {
  transform: rotate(5turn);
  -moz-transform: rotate(5turn);
  -webkit-transform: rotate(5turn);
  
  transform-origin: 200% 200%;
  -moz-transform-origin: 200% 200%;
  -webkit-transform-origin: 200% 200%;
}

.scale:hover {
  transform: scaleX(-1.5);
  -moz-transform: scaleX(-1.5);
  -webkit-transform: scaleX(-1.5);
  
  transform-origin: 150% 150%;
  -moz-transform-origin: 150% 150%;
  -webkit-transform-origin: 150% 150%;
}

.skew:hover {
  transform: skewX(-60deg);
  -moz-transform: skewX(-60deg);
  -webkit-transform: skewX(-60deg);
  
  transform-origin: 100% 100%;
  -moz-transform-origin: 100% 100%;
  -webkit-transform-origin: 100% 100%;
}
```

Kết quả: http://tutrinh01.chuyengiaseoweb.net/origin.html
