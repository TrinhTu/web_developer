## BÀI 07: VÒNG LẶP FOR TRONG PHP

> Tài liệu: Vòng lặp for trong php
> 
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 24/05/2017

### Mục lục:

[1. Vòng lặp là gì?](#1)

[2. Vòng lặp for](#2)

[3. Vòng lặp lồng nhau](#3)

[4. Vòng lặp for kết hợp với mảng](#4)

[Tài liệu tham khảo](#5)

***

<a name="1"></a>
### 1. Vòng lặp là gì?

- Vòng lặp là 1 mã lệnh trong đó chương trình được thực hiện lặp đi lặp lại nhiều lần cho đến khi thoải 1 điều kiện nào đó. PHP gồm các loại vòng lặp sau:

	+ Vòng lặp for

	+ Vòng lặp While và do while

	+ Vòng lặp foreach

<a name="2"></a>
### 2. Vòng lặp for:

- Cú pháp:

```
for ($bien_dieu_khien; $bieu_thuc_dieu_kien; $bieu_thuc_thay_doi_bien_dieu_khien)
{
    // lệnh
}
```

- Trong đó:

	+ `$bien_dieu_khien`: là một câu lệnh gán giá trị ban đầu cho biến điều khiển trước khi thực hiên vòng lặp, hoặc là một biến có giá trị sẵn mà ta đã truyền vào cho nó trước khi tạo vòng lặp này, lệnh này được thực hiện duy nhất một lần.

	+ `$bieu_thuc_dieu_kien`: là một biểu thức quan hệ xác định điều kiện thoát khỏi vòng lặp.

	+ `$bieu_thuc_thay_doi_bien_dieu_khien`: Xác định biến điều khiển sẽ bị thay đổi như thế nào sau mỗi lần lặp được lặp lại (thường là tăng hoặc giảm giá trị của biến điều khiển).

- Ví dụ:

```javascript
for ($i = 0; $i < 10; $i++){
    echo $i . ' - ';
}
```

- Trong đó:

	+ $i = 0 là biến điều khiển có giá trị khởi tạo bằng 0

	+ $i < 10 là biểu thức điều kiện dừng vòng lặp, có ý nghĩa nếu $i < 10 thì vòng lặp vẫn tiếp tục, ngược lại nếu $i >= 10 thì biểu thức sai nên vòng lặp sẽ thoát

	+ $i++ là biểu thức thay đổi biến điều khiển, sau mỗi vòng lặp $i sẽ tăng lên 1

<a name="3"></a>
### 3. Vòng lặp lồng nhau:

- Vòng lặp for có thể lồng nhau, ở mỗi vòng lặp cha thì vòng lặp con sẽ được thực hiện, thực hiện hết nội dung bên trong vòng lặp mới thực hiện vòng lặp kế tiếp.

```javascript
for ($i = 1; $i < 10; $i++)
{
    for ($j = 9; $j >= $i; $j--)
    {
        echo $j;
    }
echo '<br/>';;
}
```

- Tổng số lần lặp bằng tích số lần lặp của 2 vòng lặp cộng thêm số lần lặp của vòng lặp cha

<a name="4"></a>
### 4. Vòng lặp for kết hợp với mảng:

- Vòng lặp for lặp 1 cách trình tự tăng hoặc giảm đều giống với các chỉ mục trong mảng, vậy có thể dùng vòng lặp để truy xuất từng phần tử của mảng

- Ví dụ: cho 1 mảng danh sách các sinh viên

```javascript
$sinhvien = array(
'Nguyễn A',
'Nguyễn B',
'Nguyễn C',
'Nguyễn D',
'Nguyễn E',
'Nguyễn F'
);
```

- Xuất các sinh viên ra màn hình dùng vòng lặp for

```javascript
$count = count($sinhvien); //đếm số sinh viên
for ($i = 0; $i < $count; $i++){
    echo $sinhvien[$i];
}
```

<a name="5"></a>
### Tài liệu tham khảo:

> [1] Vòng lặp for trong php. https://freetuts.net/vong-lap-for-trong-php-7.html