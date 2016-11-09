###Bài 21: Thiết kế giao diện đơn giản

> Tài liệu: Thiết kế giao diện đơn giản
>
> 
Thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 1/11/2016

###Mục lục

- [1. Bắt đầu](#1)

- [2. Thêm các thẻ khai báo thông tin](#2)

- [3. Tạo khu vực trong website](#3)

- [4. Viết nội dung cho từng phần](#4)

<ul>

  <li> [4.1 Phần `menu`](#4.1)</li>

  <li> [4.2 Phần `content`](#4.2)</li>

    <ul>

        <li> [4.2.1 Phần `header`](#4.3.3)</li>

        <li> [4.2.2 Phần `row`](#4.2.2)</li>

        <li> [4.2.3 Phần `call-to-action`](#4.2.3)</li>

    </ul>

  <li> [4.3 Phần `footer`](#4.3)</li>
  
  </ul>
  

- [5. Viết CSS cho giao diện](#5)


- [6. Chia khung cho Website](#6)


- [7. Viết CSS cho `#menu`](#7)


- [8. Viết CSS chung cho `content`](#8)


<a name="1"></a>
####1. Bắt đầu:

Copy tài nguyên về sau đó tạo 1 thư mục chứa các file `img` `normalize.css` và tạo thêm các file `index.html` và `style.css` để chứa tài liệu CSS của website.

Đầu tiên là viết các cặp thẻ mở đầu khai báo cho website như sau:

```
<!DOCTYPE html>
<html lang="vi">
  <head>
  </head>
   <body>
   </body>
</html>
```

<a name="2"></a>
####2. Thêm các thẻ khai báo thông tin:

Thêm các thẻ khai báo thông tin trong cặp thẻ `<head>` như sau:


```
  <head>
  <meta charset="utf-8"/>
  <title> TÚ TRINH</title>
  <meta name="description" content="Thực hành tạo layout"/>
  <meta name="keyword" content="hoc css, css co ban. html"/>
  <link type="TEXT/css" rel="stylesheet" href="style.css"/>
  <link type="TEXT/css" rel="stylesheet" href="normalize.css"/>
  </head>
```

<a name="3"></a>
####3. Tạo khu vực trong website

Tạo bố cục cho website như sau:

<ul>

 <li>#container: Khung này sẽ bao phủ toàn trang để khi bạn muốn chỉnh chiều rộng của website thì sẽ chỉnh ở khu vực này là nó áp dụng lên toàn trang.</li>

 <ul>

  <li>#menu: Khu vực hiển thị menu màu đen bên tay trái.</li>

  <li>#content: Khu vực hiển thị nội dung bên phải.</li>

  <ul>

     <li>#header: Hiển thị logo và cái slogan của website bên tay phải.</li>

     <ul>

          <li>#logo: Hiển thị logo.</li>

          <li>#slogan: Hiển thị slogan.</li>

      </ul>

      <li>.call-to-action: Hiển thị cái khung màu xám</li>

      <li>.row: Cái khung bao bọc 3 cột ở dưới.</li>

      <ul>

          <li>#box 1: Cột thứ nhất</li>

          <li>#box 2: Cột thứ hai.</li>

          <li>#box 3: Cột thứ ba.</li>

      </ul>

      <li> #footer: Phần chân website</li>
  </ul>

 </ul>

</ul>


Ta có được bố cục như sau:

![1](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_21/image/1.png)

<a name="4"></a>
####4. Viết nội dung cho từng phần:

<a name="4.1"></a>
- 4.1 Phần `menu`

```
 <div id="menu">
          <ul>
            <li> <a href="#">Trang chủ</a></li>
             <li> <a href="#">Dịch vụ</a></li>
             <li> <a href="#">Sản phẩm</a></li>
             <li> <a href="#">Tin tức</a></li>
             <li> <a href="#">Diễn đàn</a></li>
             <li> <a href="#">Liên hệ</a></li>
          </ul>
         </div><!--#menu-->
```

<a name="4.2"></a>
- 4.2 Phần `content`

Phần này chứa 3 phần nhỏ đó là: #header, .row, .call-to-action

<a name="4.2.1"></a>
- 4.2.1 Phần `header`


```
<div id="header">
    <div id="logo"><img src="img/tplogo2014.png"/></div>
    <div id="slogan">
    <p>Serie học CSS cơ bản cho người mới bắt đầu</p>
    </div>
</div><!--#header-->
  ```

<a name="4.2.2"></a>
- 4.2.2 Phần `row`


```
 <div class="row">
    <div id="box1" class="col">
       <h2>CSS</h2>
       <img src="img/css-icon.png"/>
       <p>Nooijdung box1</p>
    </div>
       <div id="box2" class="col">
       <h2>URL</h2>
       <img src="img/url-icon.png"/>
       <p>Nội dung box2</p>
    </div>
       <div id="box3" class="col">
       <h2>HTML</h2>
       <img src="img/html-icon.png"/>
       <p>Nội dung box3</p>
  </div>
</div><!--.row--> 
```


<a name="4.2.3"></a>
- 4.2.3 Phần `.call-to-ation`:

```
<div class="call-to-action">
    <h3>Bạn sẽ học được những gì</h3>
    <p>Serienày sẽ cung cấp cho bạn các kiến thức cơ bản về HTML, CSS để bạn có thể tự thiết kế giao diện website riêng cho mình</p> 
</div><!--.call-to-action-->
```

<a name="4.3"></a>
- 4.3 Phần `footer`:

```
<div id="footer">
    <p>Copyright copy: 2015 www.thachpham.com</p>
</div><!--#footer-->
```

Kết quả ban đầu như sau:

![2](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_21/image/2.png)

<a name="5"></a>
####5. Viết CSS cho giao diện:

Đầu tiên ta thiết lập các thuộc tính cơ bản cho web như màu chữ, màu nền, font chữ...

```
* {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
body{
  font-family: Helvetica, sans-serif;
  font-weight: 300;
  line-height: 1.5;
  margin: 0;
  padding:0;
  color:#000099;
  background-color: #ffff99;
}
a {
  text-decoration: none;
  color: #cc0000;
  transition: all 0.5s;
  -moz-transition: all 0.5s;
  -webkit-transition: all 0.5s;
}
a:hover, a:visited {
  color: #ff00ff;
}
```

<a name="6"></a>
####6. Chia khung cho Website

Tiếp theo mình sẽ viết CSS cho phần `#container` và chia cột cho phần `#menu`:

```
#container{
  padding-left: 150px;
  position: relative;
  left: 0;
  width: 100%;
}
#menu{
  background-color: black;
  color: #66ff33;
  position: fixed;
  height: 100%;
  width: 150px;
  left0;
```
Ta sẽ có kết quả ban đầu như sau:

![3](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_21/image/3.png)

Trang trí cho #menu: Xóa padding, margin, xóa danh sách mặc định, thêm chiều cao cho từng mục trong menu:

```
#menu ul{
  list-style-type: none;
  padding:0;
  margin: 0;
}
#menu ul li{
  line-height: 3em;
  height:3em;
  transition: all 1s;
  -moz-transition: all 1s;
  -webkit-transition: all 1s;
}
```
Sau đó chuyển các thẻ liên kết về dạng Block và thêm khung, màu...

```
#menu ul li a{
  display: block;
  padding: 0 1em;
  border-bottom: 1px solid blue;
  color: #fff;
}
```
Sau đó là thêm Style khi rê chuột vào menu:

```
#menu ul li:hover {
  background-color: pink;
}
```

![4](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_21/image/4.png)

<a name="7"></a>
####7. Viết CSS cho `#menu`

```
#content {
  padding: 1em 8em;
}
#header, .call-to-action{
  text-align: center;
}
/*==trang trí header==*/
#header #slogan{
  color:#0000cc;
  font-size: 1em;
}
/*==thêm màu nền, khung==*/
.call-to-action{
  padding: 1.5em 30%;
  background-color:#66ffcc;
  border: 2px solid ;
}
```
Sau đó là phần chia cột cho #menu:

```
.row {
  overflow: hidden;
  margin: 2em auto;
}
```
Thêm CSS cho các phần nằm bên trong `.row`:

```
.row .col{
  float: left;
  width: 30%;
  margin-right: 1em;
}
/*==xóa margin-right để hiển thị cân đối hơn==*/
.row .col:last-child{
  float:right;
  margin-right: 0;
}
/*==co ảnh float qua bên trái==*/
.row .col img{
  float:left;
}
```

<a name="8"></a>
####8. Viết CSS cho `#footer`:

```
#footer{
  font-size:95%;
  border-top: 1px solid #00ff00;
  color: #0066ff;
}
```
Giờ thì xem kết quả:

![5](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_21/image/5.png)

###Tài liệu tham khảo:

https://thachpham.com/web-development/html-css/thuc-hanh-tao-layout-css-don-gian.html

https://www.youtube.com/watch?v=Og1acXRcse0&index=21&list=PLl4nkmb3a8w1cnIhegAj5_mE8w_mbYvY4
