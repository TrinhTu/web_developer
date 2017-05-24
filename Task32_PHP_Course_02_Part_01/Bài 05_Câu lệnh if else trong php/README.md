## BÀI 05: CÂU LỆNH IF ELSE TRONG PHP

> Tài liệu: Câu lệnh if else trong php
> 
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 24/05/2017

### Mục lục:

[1. Câu lệnh điều kiện là gì?](#1)

[2. Câu lệnh điều kiện if](#2)

[3. Câu lệnh if else trong php](#3)

[4. Kết hợp nhiều câu lệnh if else trong php](#4)

[5. Câu lệnh if else lồng nhau](#5)

[Tài liệu tham khảo](#6)

***

<a name="1"></a>
### 1. Câu lệnh điều kiện là gì?

- Câu lệnh điều kiện if else cho phép thay đổi luồng của chương trình dựa vào  điều kiện nào đó. Nếu điều kiện đúng là true thì chương trinhg sẽ được thực hiện, nếu điều kiện sai là false thì công việc đó sẽ không được thực hiện.

<a name="2"></a>
### 2. Câu lệnh điều kiện if:

- Câu lệnh if cho phép đưa ra các quyết định dựa trên việc kiểm tra điều kiện đúng hay sai. Cú pháp sau:

```
if ($bieuthuc){
	// các câu lệnh
}
```

- Ví dụ: Chương trình kiểm tra 1 số chẵn hay lẻ

```javascript
$so_can_kiem_tra = 12;
$so_du = $so_can_kiem_tra % 2;
if ($so_du == 0){
     echo 'Số '.$so_can_kiem_tra.' Là Số Chẵn';
}
```

<a name="3"></a>
### 3. Câu lệnh if else trong php:

- Lệnh if dùng để kiểm tra 1 điều kiện có đúng hay không

```javascript
if ($bieuthuc){
    // Những Câu Lệnh 1;
}
else{
    // Những câu lệnh 2;
}
```

<a name="4"></a>
### 4. Kết hợp nhiều câu lệnh if else trong php:

- **Ví dụ**: Nhập vào 1 màu và kiểm tra

	+ Nếu là màu xanh thì xuất ra màn hình dòng chữ "đây là màu xanh"

	+ Nếu là màu đỏ thì xuất ra màn hình dòng chữ "đây là màu đỏ"

	+ Nếu là màu vàng thì xuất ra màn hình dòng chữ "đây là màu vàng"

	+ Các màu còn lại xuất ra dòng chữ "các màu khác"

```javascript
$mau ='mau do';

	if($mau == 'mau xanh')
		echo 'day la mau xanh';

	else if($mau == 'mau do')
		echo 'day la mau do';

	else if($mau == 'mau vang')
		echo 'day la mau vang';

	else {
		echo 'cac mau khac';
	}
```

<a name="5"></a>
### 5. Câu lệnh if else lồng nhau:

- VÍ dụ: Kiểm tra số nhập vào có phải là số chẵn hay không, nếu là số chẵn thì kiểm tra tiếp số đó có lớn hơn 100 không, xuất ra màn hình  'số chẵn và lớn hơn 100', ngược lại xuất ra màn hình 'số chẵn và nhỏ hơn 100'

```javascript
$so = 120;

	if($so % 2 == 0){
		if($so > 100)
			echo 'so chan va lon hon 100';
		else{
			echo 'so chan va nho hon 100';
		}
	}
```

<a name="6"></a>
### Tài liệu tham khảo:

> [1] Câu lệnh if else trong php. https://freetuts.net/cau-lenh-if-else-trong-php-5.html
