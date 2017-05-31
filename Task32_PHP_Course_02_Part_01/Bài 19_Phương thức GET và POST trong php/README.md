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


<a name="2"></a>
### 2 Phương thức POST trong php:

<a name="2.1"></a>
#### 2.1 Client gởi lên:

<a name="2.2"></a>
#### 2.2 Server nhận dữ liệu:

<a name="2.3"></a>
#### 2.3 Ví dụ:

<a name="3"></a>
### 3. So sánh giữa POST và GET:

<a name="3.1"></a>
#### 3.1 Giống nhau:

<a name="3.2"></a>
#### 3.2 Khác nhau:

<a name="4"></a>
### Tài liệu tham khảo:

> [1] Phương thức get và post trong php. https://freetuts.net/phuong-thuc-get-va-post-trong-php-19.html