## PHP CƠ BẢN

### Mục lục:

[1. Giới thiệu về ngôn ngữ PHP](#1)

[2. Nhúng PHP vào trang HTML](#2)

[3. Biến và chú thích](#3)

[4. Cấu hình Web Server phần 1](#4)

[5. Cấu hình Web Server phần 2](#5)

[6. Hàm phpinfo()](#6)

[7. Định dạng code (Indentation)](#7)

[8. Sử dụng echo, print](#8)

[9. echo/print mã html 1](#9)

[10. echo/print mã html 2](#10)

***

<a name="1"></a>
### 1. Giới thiệu về ngôn ngữ PHP:

- PHP (Hypertext Preprocessor) là ngôn ngữ lập trình mã nguồn mở được thực thi trên máy chủ

- Một tập tin PHP có phần mở rộng là `*.php` nó có thể chứa các văn bản, mã nguồn HTML, CSS, Javascript, Jquery,... và mã PHP

- PHP tạo ra trang Web động, thao tác với file trên server, nhận và gởi cookie, cập nhập database, hạn chế người dùng truy cập vào website mã hóa dữ liệu,...

- Ưu điểm: thực thi tốt trên các hệ điều hành, các máy chủ phổ biến hiện nay, kết hợp dễ dàng với các hệ quản trị cơ sở dữ liệu, tài liệu phong phú và đa dạng, cộng đồng sử dụng rộng rãi, được cung cấp hoàn toàn miễn phí

- 4 yếu tố cần thiết tạo nên trang web động với các tính năng cần thiết:

	+ Apache (Web Server): Wampp, Xampp, Lampp,...

	+ Ngôn ngữ kịch bản máy chủ (Server-side scripting Language): PHP, ASP, NET, JSP,...

	+ Hệ quản trị cơ sở dữ liệu (Database): MySQL, SQL Server, Orcle, SQLite,...

	+ Ngôn ngữ phía máy khách (Client-side scripting Language)

<a name="2"></a>
### 2. Nhúng PHP vào trang HTML:

- PHP là ngôn ngữ nhúng trực tiếp vào HTML bằng cách lưu lại file với đuôi `.php`

- `echo` là hàm in các chuỗi dạng text ra ngoài màn hình

```javascript
<?php 
	echo 'Hoc PHP co ban';
	echo '<h1>Tieu de 1</h1>';
	echo '<h2>Tieu de 2</h2>';
?>
```

![1]()

<a name="3"></a>
### 3. Biến và chú thích:

- Cài đặt Web Server Wampp trên Windows

- Muốn comment 1 dòng đơn sử dụng `//`, `#`

- Muốn commnet 1 đoạn sử dụng `/* */`

```javascript
<?php
	// day la bien variable
	$variable = 'My Name';
	
	/* 
	This is multiple line comment
	first line
	second line
	third line
	*/
?>
```

- Cú pháp khai báo biến cơ bản:

```javascript
<?php
	$var = 1;
	$myName = 'Tu Trinh';
	$myArr = array("first", "second", "third");
?>
```
- Khi muốn in ra màn hình giá trị của biến sử dụng câu lệnh `echo`+ tên biến.

<a name="4"></a>
### 4. Cấu hình Web Server phần 1:

- Thư mục **bin** trong Wampp chứa 3 thư mục, mỗi thư mục là thành phần của webserver.

!2

- Sửa lỗi xung đột cổng: vào thư mục `httpd.conf`, tại đây sửa cổng mặc định cổng 80 thành cống khác

!3

<a name="5"></a>
### 5. Cấu hình Web Server phần 2:

<a name="6"></a>
### 6. Hàm phpinfo():

- Hàm có tác dụng đưa tất cả thông tin liên quan đến web server cũng như cấu hình cài đặt của web server đó, để có thể thay đổi phù hợp với nhu cầu sử dụng

- Câu lệnh `echo phpinfo();` đưa ra version của webserver

![4]

- phpinfo() hiển thị các thông tin cần thiết để cấu hình web server, hiểu được cơ chế hoạt động...

<a name="7"></a>
### 7. Định dạng code (Indentation):

<a name="8"></a>
### 8. Sử dụng echo, print:



<a name="9"></a>
### 9. echo/print mã html 1:

- echo dùng để in ra chuỗi, in ra biến, giá trị 1 hằng...

<a name="10"></a>
### 10. echo/print mã html 2:

<a name="15"></a>
### 15. Biểu thức gán:

```javascript
<?php
	$x = 6;
	$y = 3;

	$z = $x + $y; 
	$z += $y; // $z = $z + $y
	$z -= $x;
	$z *= ($x + $y);
	$z /= ($y - $x);

	echo $z. 
?>
```
<a name="16"></a>
### 16. Biểu thức toán học:

- Các biểu thức +, -, *, /, %

 