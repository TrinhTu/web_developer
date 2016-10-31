##Bài 19: Kĩ thuật tạo menu ngang

> Tài liệu: Kĩ thuật tạo menu ngang
>
> Thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 31/10/2016

###Mục lục

[1. Cách tạo menu ngang cơ bản](#1)

[2. Cách tạo menu dropdown đơn giản](#2)

###Nội dung:

<a name="1"></a>
####1. Cách tạo menu ngang cơ bản

- Sử dụng thẻ `<ul>` để tạo ra menu không sắp xếp trong đó sử dụng các thẻ `<li>` để tạo các mục trong menu đó, đặt menu nằm trong thẻ `<div>` như sau:

```
<div id="menu">
  <ul>
    <li><a href="#">Mục 1</a></li>
    <li><a href="#">Mục 2</a></li>
    <li><a href="#">Mục 3</a></li>
    <li><a href="#">Mục 4</a></li>
    <li><a href="#">Mục 5</a></li>
  </ul>
</div>
```
- Sau đó cần reset lại CSS, trong này áp dụng reset CSS them kiểu đơn giản là đặt margin=0 và paading=0.  và thêm 1 số thuộc tính cơ bản cho trang web:

```
* {
  margin: 0;
  padding: 0;
}
body{
  font-family: arial;
  color: red;
}
```
  
 - Tiếp đến là viết CSS cho phần thẻ `<ul>` thêm các thuộc tính quen thuộc như là background-color, xóa các dấu hiển thị mặc định đầu dòng, đưa nội dung ra giữa:

```
 #menu ul {
	  list-style-type: none;
	  background: #CD5C5C;
	  text-align: center;
	}
```

![1](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_19/image/1.png)

- Lựa chọn 1: kiểu inline-block

Khi viết CSS cho các mục con nằm bên trong thẻ `<ul>` nên viết theo kiển inline-block, đơn giản như sau:

```
#menu ul li{
  color: #EE82EE;
  display: inline-table;
  width: 200px;
  height: 50px;
  line-height: 50px;
}
```

- Lựa chọn 2: kiểu float:

```
#menu ul li{
  color: #EE82EE;
  float: left;
  width: 200px;
  height: 50px;
  line-height: 50px;
}
```
Khi sử dụng kiểu float cần thêm vào cho thẻ `<ul>` thuộc tính nữa là overflow và thêm width.

![2](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_19/image/2.png)

- Tiếp theo là sẽ thêm style cho thẻ `<a>` :

```
#menu ul li a{
  color: #ADFF2F;
   text-decoration: none;
  display: block;
}
#menu ul li a:hover{
  background-color:	#8A2BE2;
  color: 	#DDA0DD;
}
```

Kết quả sau các bước thực hiện.

![3](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_19/image/3.png)

<a name="2"></a>
2. Cách tạo menu dropdown đơn giản

Tạo thêm 1 vài menu con bằng cách tạo thêm các thẻ `<ul>` lồng vào bên trong các thẻ `<li>` như sau:

```
<div id="menu">
  <ul>
    <li><a href="#">Mục 1</a></li>
    <li><a href="#">Mục 2</a>
      <ul class="sub-menu">
        <li><a href="#">danh mục con 1</a></li>
        <li><a href="#">danh mục con 2</a></li>
        <li><a href="#">danh mục con 3</a></li>
      </ul>
    <li><a href="#">Mục 3</a></li>
    <li><a href="#">Mục 4</a></li>
    <li><a href="#">Mục 5</a></li>
  </ul>
</div>
```
Ta có kết quả như sau:

![4](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_19/image/4.png)

Sau đó ta thực hiện ẩn đi 1 phần tử vừa tạo như sau:

```
#menu ul li > .sub-menu{
  display: none;
}
```

Sau đó nếu ta muốn khi rê chuột vào Mục mẹ thì sẽ hiển thị ra danh sách mục con thì như sau:

```
#menu ul li:hover .sub-menu{
  display: block;
}
```
Kết quả:

![5](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_19/image/5.png)

Giờ muốn thiết lập lại cho cái `#menu ul` không bị đẩy lên như hình thì ta sử dụng thuộc tính `position` và thiết lập sao cho `sub-menu` nằm gần menu mẹ, thì phải thiết lập `#menu li` thành kiểu `relative`

Kết quả là các mục con sẽ không bị tràn qua các mục khác và hiển thị sẽ đẹp hơn:

![6](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_19/image/1.png)


