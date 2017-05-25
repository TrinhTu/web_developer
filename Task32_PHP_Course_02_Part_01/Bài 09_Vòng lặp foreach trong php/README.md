## BÀI 09: VÒNG LẶP FOREACH TRONG PHP

> Tài liệu: Vòng lặp foreach trong php
> 
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 25/05/2017

### Mục lục:

[1. Cú pháp vòng lặp foreach trong php](#1)

[Tài liệu tham khảo](#2)

***

<a name="1"></a>
### 1. Cú pháp vòng lặp foreach trong php:

- Cú pháp vòng lặp foreach trong php:

```javascript
foreach ($array as $key => $value){
	// các dòng lệnh
}
```

Hoặc:

```javascript
foreach ($array as $value){
	// các dòng lệnh
}
```

- Trong đó $array là mảng cần lặp, $key là số chỉ mục (mảng có chỉ mục) hoặc là key (trong mảng kết hợp), $value là giá trị của phần tử ở vị trí $key.

```javascript
// Danh sách các năm
$nam = array(
    1990,
    1991,
    1992,
    1993,
    1994,
    1995
);
  
//Dùng foreach xuất ra các năm trong $nam
foreach ($nam as $key => $value){
    echo $value;
}
```

- Vòng lặp foreach tự động lặp qua các phần tử trong mảng, lặp cho tới khi nào tới phần tử cuối cùng. $nam là mảng truyền vào, $key và $value là 2 tham số mà ở mỗi vòng lặp tự động truyền giá trị vào. Kết quả xuất ra màn hình là:

```
0 => 1990
1 => 1991
2 => 1992
3 => 1993
4 => 1994
5 => 1995<br />
<br />
<br />
<br />
<br />
```

- Ví dụ 2: 

```javascript
// Danh sách mã số sinh viên và sinh viên tương ứng
$sinhvien = array(
    'SV001' => 'Nguyễn Văn A',
    'SV002' => 'Nguyễn Văn B',
    'SV003' => 'Nguyễn Văn C',
    'SV004' => 'Nguyễn Văn D',
    'SV005' => 'Nguyễn Văn E'
);
  
// Xuất ra danh sách sinh viên
foreach ($sinhvien as $tensv){
    echo $tensv . '<br/>';
}
```

<a name="2"></a>
### 2. Tài liệu tham khảo:

> [1] Vòng lặp foreach trong php. https://freetuts.net/vong-lap-foreach-trong-php-9.html