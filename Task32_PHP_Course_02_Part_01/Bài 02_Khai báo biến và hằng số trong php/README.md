## BÀI 02: KHAI BÁO BIẾN VÀ HẰNG SỐ TRONG PHP

> Tài liệu: Khai báo biến và hằng số trong php
> 
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 23/05/2017

### Mục lục:

[1. Chương trình "Hello World"](#1)

[2. Ghi chú](#2)

[3. Khai báo biến số trong php](#3)

[4. Hiển thị giá trị của biến ra màn hình](#4)

[5. Khai báo hằng](#5)

[Tài liệu tham khảo](#6)

***

<a name="1"></a>
### 1. Chương trình "Hello Word":

- Để xuất 1 chuỗi ra màn hình dùng cú pháp: `<?php echo "Hello World"; ?>`

- Ví dụ in ra màn hình chuỗi sau:

`<?php echo 'Xin chào tất cả các bạn'; ?>`

<a name="2"></a>
### 2. Ghi chú:

- Ghi chú cho 1 dòng `//nội dung cần ghi chú`

- Ghi chú cho 1 đoạn `/*nội dung cần ghi chú*/`

- Ví dụ:

```javascript
<?php
	echo 'Chào các bạn' ; //ghi chú
	/*đoạn ghi chú*/
?>
```

<a name="3"></a>
### 3. Khai báo biến số trong php:

- Biến là 1 định danh dùng để lưu trữ các giá trị và nó có thể dùng phép gán để thay đổi giá trị, cú pháp bắt đầu là dấu `$` tiếp theo là các chữ, số, dấu gạch dưới. Kí tự đầu tiên của tên biến phải là chữ hoặc dấu gạch dưới không được là số

- Ví dụ:

```javascript
<?php
$sinhvien = ''; //đúng
$_sinh_vien = ''; //đúng
$sinh_vien90 = ''; //đúng
$90sinhvien = ''; //sai
?>
```

- Để gán giá trị cho biến sử dụng toán tử gán `=`, ví dụ:

`$hello = 'Hello World';`

<a name="4"></a>
### 4. Hiển thị giá trị của biến ra màn hình:

- Thay vì xuất trực tiếp chuỗi thì ta xuất giá trị của biến ra màn hình:

- Ví dụ:

```javascript
<?php
	$ho_ten = 'Le Tu Trinh';
	echo $ho_ten;  //xuất giá trị của biến ra màn hình
?>
```

<a name="5"></a>
### 5. Khai báo hằng:

- Hằng cũng là 1 biến nhưng không thể thay đổi giá trị của nó, cách khai báo hằng:

	+ Cú pháp: `define('ten_hang', 'gia_tri');`

	+ Trong đó:

		+ `define`: hàm tạo biến hằng

		+ `ten_hang`: là tên biến hằng

		+ `gia_tri`: giá trị của hằng

```javascript
<?php
	//tạo hằng số có tên là sdt và gán giá trị cho nó

	define('sdt','123456789');
	echo sdt;	//xuất ra màn hình giá trị của hằng
?>
```

<a name="6"></a>
### Tài liệu tham khảo:

> [1] Khai báo biến và hằng số trong php. https://freetuts.net/khai-bao-bien-va-hang-so-trong-php-2.html