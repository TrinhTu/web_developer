## BÀI 02: DOWNLOAD BOOTSTRAP VÀ NHÚNG BOOTSTRAP VÀO WEBSITE

> Tài liệu: Download Bootstrap và nhúng bootstrap vào website
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 08/06/2017

### Mục lục:

[1. Download Bootstrap 3](#1)

[2. Nhúng thư viện Bootstrap vào website](#2)

[Tài liệu tham khảo](#3)

***

<a name="1"></a>
### 1. Download Bootstrap 3:

- Lựa chọn phiên bản cần download và tải về [tại đây](http://getbootstrap.com/)

<a name="2"></a>
### 2. Nhúng thư viện Bootstrap vào website:

- Tương tự như nhúng file css vào website. Download về giải nén ra và nhúng trực tiếp vào website.

```javascript
<!-- Latest compiled and minified CSS -->
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.2.0/css/bootstrap.min.css">
 
<!-- Optional theme -->
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.2.0/css/bootstrap-theme.min.css">
 
<!-- Latest compiled and minified JavaScript -->
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.2.0/js/bootstrap.min.js"></script>
```

- Tạo ra 1 mẫu file bootstrap cơ bản để sử dụng nó:

```javascript
<!DOCTYPE html>
<html>
<head>
<title>Bootstrap 3 example</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
    <h1>Learning Bootstrap 3</h1>
</body>
</html>
```

- Nội dung trong thẻ `meta` dùng để enable Responsive design, dùng để thiết lập màn hình theo tỉ lệ 1x1, loại bỏ các chức năng mặc định từ các trình duyệt smartphone, hiển thị vừa màn hình để xem và có thể phóng to bằng tay, được thêm vào trong thẻ `<head>`

- Tiếp theo nhúng bootstrap file vào file HTML này:

```javascript
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Bootstrap 3 example</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<link rel="stylesheet" type="text/css" href="css/bootstrap.min.css">
</head>
<body>
    <h1>Learning Bootstrap</h1>
    <script src="http://code.jquery.com/jquery.min.js"></script>
    <script src="js/bootstrap.min.js"></script>
</body>
</html>     
```

<a name="3"></a>
### Tài liệu tham khảo:

> [1] Download bootstrap và nhúng bootstrap và website. https://freetuts.net/download-bootstrap-va-nhung-bootstrap-vao-website-172.html