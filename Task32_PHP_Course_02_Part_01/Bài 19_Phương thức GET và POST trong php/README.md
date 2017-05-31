## BÀI 19: PHƯƠNG THỨC GET VÀ POST TRONG PHP

> Tài liệu: Phương thức GET và POST trong php
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 31/05/2017

### Mục lục:

- [1. Phương thức GET trong php](#1)

	- [1.1 Client gởi lên](#1.1)

	- [1.2 Server nhận dữ liệu](#1.2)

	- [1.3 Ví dụ](#1.3)

- [2. Phương thức POST trong php](#2)

	- [2.1 Client gởi lên](#2.1)

	- [2.2 Server nhận dữ liệu](#2.2)

	- [2.3 Ví dụ](#2.3)

- [3. So sánh giữa POST và GET](#3)

	- [3.1 Giống nhau](#3.1)

	- [3.2 Khác nhau](#3.2)

- [Tài liệu tham khảo](#4)

***

<a name="1"></a>
### 1. Phương thức GET trong php:

- Phương thức GET sẽ hiển thị lên URL dữ liệu mà ta gởi

<a name="1.1"></a>
#### 1.1 Client gởi lên:

- Phương thức GET là phương thức gởi dữ liệu thông qua đường dẫn URL nằm trên thanh địa chỉ của Browser, server nhận được đường dẫn đó và phân tích trả về kết quả , server sẽ phân tích tất cả thông tin đằng sau dấu hỏi (?) chính là phần dữ liệu mà client gởi lên

- Để truyền nhiều dữ liệu  lên server dùng dấu & để phân cách giữa các cặp giá trị, giả sử muốn truyền id = 12 và title = 'method_get'thì URL có dạng `domain.com?id=12&title=method_get`, vị trí các cặp giá trị không quan trọng.

<a name="1.2"></a>
#### 1.2 Server nhận dữ liệu:

- Tất cả các dữ liệu client gởi lên bằng phương thức GET đều được lưu trong biến toàn cục mà PHP tạo ra là **$_GET**, biến này là kiểu mảng kết hợp lưu trữ danh sách dữ liệu từ client gởi lên theo quy luật **key => value**.  Ví du với URL freetuts.net?id=12&title=method_get thì dữ liệu sẽ được lưu trong biến $_GET dưới dạng:

```javascript
$_GET = array(
    'id' => '12',
    'title' => 'method_get'
);
```

- Để lấy dữ liệu:

```javascript
// Lấy ID
$id = $_GET['id'];
echo $id; // kết quả là 12
  
// Lấy title
$title = $_GET['title'];
echo $title; // kết quả là method_get
```

<a name="1.3"></a>
#### 1.3 Ví dụ:

- Tạo 1 file get.php` có nội dung sau:

```javascript
echo 'Dữ Liệu Chúng Tôi Nhận Được Là <br/>';
foreach ($_GET as $key => $val)
{
    echo '<strong>' . $key . ' => ' . $val . '</strong><br/>';
}
```

Sau đó ra trình duyệt gõ đường dẫn: `http://localhost/get.php?id=12&title=method_get`

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task32_PHP_Course_02_Part_01/B%C3%A0i%2019_Ph%C6%B0%C6%A1ng%20th%E1%BB%A9c%20GET%20v%C3%A0%20POST%20trong%20php/1.png"/></p>

- Trước khi lấy dữ liệu nào đó cần kiểm tra xem dữ liệu có tồn tại không, để kiểm tra dữ liệu sử dụng hàm **isset($tenbien)** trong php

```javascript
if (isset($_GET['id'])){
    $id = $_GET['id'];
}
```

<a name="2"></a>
### 2 Phương thức POST trong php:

- Phương thức POST có tính bảo mật hơn vì dữ liệu phải gởi thông qua 1 form HTML nên bị ẩn đi, không hiển thị giá trị trên URL.

<a name="2.1"></a>
#### 2.1 Client gởi lên:

- Với phương thức GET thì dữ liệu được thấy trên URL thì POST sẽ gởi dữ liệu thông qua form HTML và các giá trị sẽ được định nghĩa trong các input gồm các kiểu (textbox, radio, checkbox, password, textarea, hidden) và được nhận dạng thông qua tên (name) của các input đó.

<a name="2.2"></a>
#### 2.2 Server nhận dữ liệu:

- Tất cả các dữ liệu gởi bằng phương thức POST được lưu trong 1 biến toàn cục **$_POST** do PHP tạo ra, để lấy dữ liệu chỉ cần lấy trong biến này, dùng hàm `isset($bien)` kiểm tra biến có tồn tại không.

```javascript
if (isset($_POST['id'])){
    $id = $_POST['id'];
}
```

<a name="2.3"></a>
#### 2.3 Ví dụ:

- Tạo 1 file `post.php` có nội dung sau

```javascript
<!DOCTYPE html>
<html>
    <head>
        <title></title>
        <meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
    </head>
    <body>
        <form method="POST">
            Username: <input type="text" name="username" value=""/> <br/>
            password: <input type="password" name="password" value=""/><br/>
            <input type="submit" name="form_click" value="Gửi Dữ Liệu"/>
        </form>
    </body>
</html>
```

- Thêm nội dung sau vào đoạn code trên

```javascript
<?php
    // Nếu người dùng click vào button Gửi Dữ Liệu
    // Vì button đó tên là form_click nên đó cũng là
    // tên của key nằm trong biến $_POST
    if (isset($_POST['form_click'])){
        echo 'Tên đăng nhập là: ' . $_POST['username'];
        echo '<br/>';
        echo 'Mật khẩu là: ' . $_POST['password'];
    }
?>
```

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task32_PHP_Course_02_Part_01/B%C3%A0i%2019_Ph%C6%B0%C6%A1ng%20th%E1%BB%A9c%20GET%20v%C3%A0%20POST%20trong%20php/2.png"/></p>

<a name="3"></a>
### 3. So sánh giữa POST và GET:

<a name="3.1"></a>
#### 3.1 Giống nhau:

- Để gởi dữ liệu lên server

<a name="3.2"></a>
#### 3.2 Khác nhau:

- Phương thức POST bảm mật hơn GET vì dữ liệu được gởi ngầm không hiển thị trên URL

- GET được gởi tường minh hơn, không bảo mật

- GET nhanh hơn POST vì dữ liệu gởi đi được Browser giữ lại trong cache. Khi sử dụng POST thì server luôn thực thi lệnh rồi trả về cho client, còn GET thì browser sẽ kiểm tra trong cache có chưa, nếu có sẵn sẽ trả về ngay mà không cần gởi lên server

- Sử dụng SEO dữ liệu dùng GET

- Đăng nhập, comment, đăng tin dùng POST, lấy thông tin dùng GET

- Request sử dụng câu lệnh select dùng GET, khi request có sử dụng câu lệnh insert update, delete nên dùng POST

<a name="4"></a>
### Tài liệu tham khảo:

> [1] Phương thức get và post trong php. https://freetuts.net/phuong-thuc-get-va-post-trong-php-19.html