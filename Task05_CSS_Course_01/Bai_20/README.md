###Bài 20: Kĩ thuật tạo menu dọc cơ bản

> Tài liệu: Kĩ thuật tạo menu dọc cơ bản
>
> Thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 31/10/2016

###Mục lục

[1. Tạo menu dọc cơ bản](#1)

[2. Tạo menu dọc đổ xuống(dropdown)](#2)

###Nội dung:

<a name="1"></a>
####1. Tạo menu dọc cơ bản:

Tạo tương tự như tạo menu ngang:

```
<div id="menu">
  <ul>
    <li><a href="#">Mục 1</a></li>
    <li><a href="#">Mục 2</a>
    <li><a href="#">Mục 3</a></li>
    <li><a href="#">Mục 4</a></li>
    <li><a href="#">Mục 5</a></li>
  </ul>
</div>
```

- Sau đó cũng reset lại CSS để bỏ mấy dấu chấm tròn sau đó thêm màu nền màu chữ các thuộc tính khác cho thẻ `#menu ul`

```
#menu ul {
  list-style-type: none;
  background: #CD5C5C;
  text-align: center;
  width: 200px;
  padding: 0;
}
```

- Sau đó tiếp tục viết CSS cho thẻ `<li>` :

```
#menu ul li{
  color: #EE82EE;
  width: 200px;
  height: 50px;
  line-height: 50px;
  border-bottom: 2px solid blue;
 }
 ```

- Sau đó viết CSS cho các thẻ `a` bên trong:

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

<a name="2"></a>
####2. Tạo menu dọc đổ xuống (dropdown)

Cũng tương tự như cách tạo menu ngang, đầu tiên ta tạo thêm các mục con bên trong các mục vừa tạo:

```
<div id="menu">
  <ul>
    <li><a href="#">Mục 1</a></li>
    <li><a href="#">Mục 2</a>
    <li><a href="#">Mục 3</a>
      <ul class="sub-menu">
        <li><a href="#"></a>mục con 1</li>
        <li><a href="#"></a>mục con 2</li>
        <li><a href="#"></a>mục con 3</li>
      </ul>
    </li>
    <li><a href="#">Mục 4</a></li>
    <li><a href="#">Mục 5</a></li>
  </ul>
</div>
```

- Tiếp đến là thêm thuộc tính `position` vào `#menu ul li` 

- Chuyển `#menu .sub-menu` về dạng `absolute` và tiến hành chỉnh vị trí của nó:

```
#menu .sub-menu {
 position: absolute;
 left: 250px;
 top: 0;
}
```
- Viết CSS cho các phần tử con đó ẩn đi và khi rê chuột vào chúng sẽ hiện ra:

```
#menu .sub-menu {
 position: absolute;
 left: 250px;
 top: 0;
  display: none;
}
#menu ul li:hover .sub-menu{
  display: block;
}
```

Kết quả ta có:

![anh](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_20/image/1.png)

