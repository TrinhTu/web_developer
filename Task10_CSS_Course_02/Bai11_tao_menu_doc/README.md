###Bài 11: Kĩ thuật tạo menu dọc cấp hai cơ bản

> Tài liệu: Kĩ thuật tạo menu dọc cấp hai cơ bản
>
> Thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 19/11/2016

###Mục lục

[1. Tạo menu dọc cơ bản](#1)

[2. Tạo menu dọc đổ xuống(dropdown)](#2)

###Nội dung:

<a name="1"></a>
####1. Tạo menu dọc cơ bản:

Sử dụng thẻ `ul` và `li` để tạo menu cơ bản

```
<div id="menu">
  <ul>
    <li><a href="#">Trang chủ</a></li>
    <li><a href="#">Thư viện</a>
    <li><a href="#">Dành cho sinh viên</a></li>
    <li><a href="#">Tuyển sinh</a></li>
    <li><a href="#">Sau đại học</a></li>
  </ul>
</div>
```

- Sau đó cũng reset lại CSS để bỏ mấy dấu chấm tròn sau đó thêm màu nền màu chữ các thuộc tính khác cho thẻ `#menu ul`

```
#menu ul {
  list-style-type: none;
  background: pink;
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

![1](https://github.com/TrinhTu/web_developer/blob/master/Task10_CSS_Course_02/Bai11_tao_menu_doc/image/(a).png)

<a name="2"></a>
####2. Tạo menu dọc đổ xuống (dropdown)

Tạo thêm các mục con bên trong các mục vừa tạo:

```
<div id="menu">
  <ul>
    <li><a href="#">Trang chủ</a></li>
    <li><a href="#">Thư viện</a>
    <li><a href="#">Dành cho sinh viên</a>
      <ul class="sub-menu">
        <li><a href="#">Thảo luận</a></li>
        <li><a href="#">Tra cứu điểm</a></li>
        <li><a href="#">Thông tin sinh viên</a></li>
      </ul>
      </li>
    <li><a href="#">Tuyển sinh</a>
      <ul>
        <li><a href="#">Điểm chuẩn</a></li>
        <li><a href="#">Tư vấn</a></li>
        <li><a href="#">Ngành học</a></li>
      </ul>
      </li>
    <li><a href="#">Sau đại học</a></li>
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
background: aqua;
}
#menu ul li:hover .sub-menu{
  display: block;
}
```

Kết quả ta có:

![anh](https://github.com/TrinhTu/web_developer/blob/master/Task10_CSS_Course_02/Bai11_tao_menu_doc/image/(b).png)
