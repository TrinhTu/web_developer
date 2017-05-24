## BÀI 06: CÂU LỆNH SWITCH CASE TRONG PHP

> Tài liệu: Câu lệnh switch case trong php
> 
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 24/05/2017

### Mục lục:

[1. Câu lệnh switch case trong php](#1)

[2. Switch và if](#2)

[3. Switch lồng nhau](#3)

[Tài liệu tham khảo](#4)

***

<a name="1"></a>
### 1. Câu lệnh switch case trong php:

- Câu lệnh switch trong php giúp đưa ra quyết định cách lựa chọn cho giá trị của biểu thức truyền vào, nếu giá trị của biểu thức truyền vào trùng với giá trị biểu thức điều kiện thì các câu lệnh bên trong biểu thức điều kiện sẽ được thực hiện.

- Cú pháp:

```javascript
switch ($variable) {
    case $value_1:
       // chuỗi câu lênh
       break;
    case $value_2:
        // chuỗi câu lệnh
        break;
    default:
        // chuỗi câu lệnh
        break;
}
```

- Trong đó lệnh switch, case, default là các từ khóa trong php. Các chuỗi câu lệnh có thể là lệnh đơn hoặc lệnh ghép và không cần đặt vào trong dấu ngoặc nhọn. Giá trị ở case chỉ chấp nhận các kiểu dữ liệu string, INT, boolean, null, float hoặc là 1 biểu thức có kết quả trả về 1 trong 5 loại dữ liệu đó và toán tử quan hệ so sánh trong switch luôn là `==`

- Ví dụ: Viết chương trình nhập vào 1 số, dùng lệnh rẽ nhánh switch kiểm tra số đó nếu:

	+ Bằng 0 thì xuất hiện dòng lệnh "so khong"

	+ Bằng 1 thì xuất hiện dòng lệnh 'so mot'

	+ Bằng 2 thì xuất hiện dòng lệnh 'so 2'

	+...

	+ Các số còn lại 'khong tim thay'

```javascript
$so = 1;
	switch ($so) {
		case 0:
			echo 'so khong';
			break;
		case 1:
			echo 'so mot';
			break;
		case 2:
			echo 'so hai';
			break;
		case 3:
			echo 'so ba';
			break;
		case 4:
			echo 'so bon';
			break;
		default:
			echo 'khong tim thay';
			break;
	}
```

<a name="2"></a>
### 2. Switch và if:

- Lệnh if và lệnh switch là dạng lệnh rẻ nhánh trong php, lệnh if hoạt động linh hoạt hơn switch và tốc độ cũng nhanh hơn

- Lệnh switch có thể chuyển sang lệnh if nhưng lệnh if chưa chắc có thể chuyển sang switch được.

```javascript
$number = 10;
if ($number == 0){
    echo 'Số không';
}
else if ($number == 1){
    echo 'Số một';
}
else if ($number == 2){
    echo 'Số hai';
}
else if ($number == 3){
    echo 'Số ba';
}
else if ($number == 4){
    echo 'Số bốn';
}
else {
    echo 'Không tìm thấy';   
}
```

<a name="3"></a>
### 3. Switch lồng nhau:

- Tương tự như lệnh if, lệnh switch có thể lồng nhau.

```javascript
$number = 12;
$midle = null;
switch ($number)
{
    case 12 : // nếu $number = 12
        $midle = $number % 2; // lấy số dư
        switch ($midle)
        {
            case 0 : // nếu số dư = 0
                echo 'Số chẵn';
                break;
            default :
                echo 'Số lẽ';
                break;
        }
        break;
    default: // nếu không phải 12 thì không làm gì
        break;
}
```

<a name="4"></a>
### Tài liệu tham khảo:

> [1] Câu lệnh switch case trong php. https://freetuts.net/cau-lenh-switch-case-trong-php-6.html