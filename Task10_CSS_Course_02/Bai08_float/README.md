##Bài 8: Thuộc tính float (left-right-none) trong CSS

>Tài liệu: Thuộc tính float (left-right-none) trong CSS
>
>Người thực hiện: Lê Tú Trinh
>
>Cập nhập lần cuối: 16/11/2016

###Mục lục:

[Sử dụng float: left và float: right để chia bố cục](#1)

###Nội dung:

<a name="1"></a>
####Sử dụng float để chia bố cục:

Ví dụ ta có 1 đoạn HTML như sau:

```
<div id="container">
<div id="header">HEADER</div>
<div id="main_content"> MAIN CONTENT</div>
<div id="sidebar">SIDEBAR</div>
<div id="footer">FOOTER</div>
</div>
```

Bây giờ ta muốn nó hiển thị như ý muốn, tức là phần `header` sẽ là tiêu đề nằm trên cùng chính giữa, phần `main_content` và `sidebar` sẽ là nội dung, và `main_content` sẽ hiển thị phía bên trái bố cục, và `sidebar` sẽ hiển thị phía bên phải, phần `footer` sẽ là phần chân thì ta thêm CSS như sau:

```
#container {
  text-align: center;
  margin: 0px auto;
  width: 800px;
  font-size: 30px;
}
#header {
  border: 1px solid blue;
  background: aqua;
  height: 50px;
}
#main_content {
  border: 1px solid #ff0066;
  background: #ff99cc;
  width: 500px;
  float: left;
  height: 100px;
}
#sidebar {
  border: 1px solid #006600;
  background: #66ff33;
  width: 295px;
  float: right;
  height: 100px;
}
#footer {
  border: 1px solid #ffcc00;
  background: #ffff66;
}
``` 

Kết quả ta có: 

![a](https://github.com/TrinhTu/web_developer/blob/master/Task10_CSS_Course_02/Bai08_float/image/a.png)

