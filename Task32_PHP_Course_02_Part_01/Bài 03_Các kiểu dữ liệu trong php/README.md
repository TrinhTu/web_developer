## BÀI 03: CÁC KIỂU DỮ LIỆU TRONG PHP

> Tài liệu: Các kiểu dữ liệu trong php
> 
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 23/05/2017

### Mục lục:

[1. Kiểu dữ liệu INT](#1)

[2. Kiểu dữ liệu boolean](#2)

[3. Kiểu số thực](#3)

[4. Kiểu chuỗi](#4)

[5. Kiểu mảng(array)](#5)

[6. Kiểu giá trị null](#6)

[7. Kiểu Object (đối tượng)](#7)

[Tài liệu tham khảo](#8)

***

<a name="1"></a>
### 1. Kiểu dữ liệu INT:

- Đây là kiểu dữ liệu dạng số, có thể viết ở nhiều cơ số khác nhau

```javascript
<?php

	$thap_phan = 123; //số thập phân
	$so_am = -123; 	//số âm
	$bat_phan = 0123;	//số bát phân
	$thap_luc_phan = 0x1A;	//số thập lục phân
?>
```

- Kiểu `int` không cần đặt trong dấu nháy, kích thước của nó là 32 bit, trong php không hỗ trợ nhiều kiểu Unsigned Integer (số nguyên dương), nếu sử dụng vượt quá giới hạn của nó trình mặc định trình phiên dịch sẽ hiểu đây là kiểu số thực.

#### Khai báo biến kiểu INT:

- Để khai báo biến kiểu INT, phải gán giá trị cho nó là số nguyên (số âm)

`$tuoi = 12; 	// biến $tuoi là kiểu int có giá trị là 12`

#### Ép dữ liệu sang kiểu INT:

- Cú pháp: `(int)$ten_bien;

```javascript
<?php
$tuoi = '98'; // biến tuổi là một chuỗi có giá trị bằng '98'
$tuoi = (int)$tuoi; // lúc này biến $tuoi là một kiểu int có giá trị 98
?>
```

- Trong PHP sẽ tự động chuyển các biến sang kiểu dữ liệu thích hợp để tính toán, sau khi thực hiện xong nó sẽ trả về kiểu dữ liệu ban đầu

```javascript
<?php
$a = '123';  // Biến $a là kiểu chuỗi có giá trị bằng '123'
$b = 123; // Biến $b là kiểu INT có giá trị bằng 123
$c = $a + $b; // Biến C là kết quả của phép toán $a + $b và sẽ có giá trị là 246 nên nó là kiểu INT
var_dump(is_int($c)); // hàm is_int($tenbien) dùng để kiểm tra một biến có phải là kiểu INT hay không
var_dump(is_int($a)); // kết quả là false vì biến $a là kiểu string
?>
```

- Để kiểm tra 1 biến nào đó có phải kiểu dữ liệu INT hay không dùng hàm `is_int($bien)` hoặc `is_integer($bien)`, kết quả trả về sẽ là true hoặc false.

<a name="2"></a>
### 2. Kiểu dữ liệu boolean:

- Đây là kiểu dữ liệu chỉ chứa 2 giá trị là đúng hoặc sai (TRUE or FALSE). Để tạo biến kiểu boolean thì gán giá trị cho nó là true or false, ở đây không phân biệt chữ hoa chữ thường.

`$result = true;  //biến $result là biến kiểu boolean có giá trị là true`

#### Ép dữ liệu sang kiểu boolean:

```javascript
<?php
$bool = 1; // biến $bool là kiểu int
$bool = (bool)$bool; // lúc này biến $bool sẽ có kiểu boolean
// Hoặc
$bool = (boolean)$bool; // lúc này biến $bool sẽ có kiểu boolean
?>
```

- Các kí tự 0, kí tự trống và null đều được quy về giá trị FALSE còn có kí tự còn lại quy về TRUE 

```javascript
<?php
$a = 123; // TRUE
$b = 0; // FALSE
$c = '0'; // FALSE
$d = 'a123b' // TRUE
$e = null; // FALSE
$f = ''; // FALSE
?>
```

- Để kiểm tra 1 biến có phải kiểu boolean dùng hàm `is_bool($bien);`

<a name="3"></a>
### 3. Kiểu số thực:

- Kiểu số thực là những số có phần dư, ví dụ như `$a = 1.234;`

### Ép dữ liệu sang kiểu số thực:

- Dùng (float), (double) để chuyển kiểu dữ liệu sang số thực cho 1 biến

```javascript
<?php
$a = 123; // biến $a kiểu int
$a = (float)$a; // Biến $a lúc này kiểu số thực (float)
$a = (double)$a; // Biến $a lúc này kiểu số thực (double)
?>
```

### Kiểm tra 1 biến kiểu số thực:

- Sử dụng hàm `is_float($bien)` để kiểm tra cho kiểu float, `is_double($bien)` để kiểm tra cho kiểu double

<a name="4"></a>
### 4. Kiểu chuỗi:

- Kiểu chuỗi bao gồm kiểu string (chuỗi) và char (kí tự), mỗi kí tự là 1 byte và là 1 trong 256 kí tự khác nhau, chuỗi phải được bao quanh bằng dấu nháy đơn hoặc dấu nháy kép. Dùng (string) để chuyển sang kiểu chuỗi. 

```javascript
<?php
$a = 123; // khai báo biến $a kiểu int có giá trị 123
$a = (string)$a; //Chuyển biến $a thành kiểu chuỗi và có giá trị là '123'
?>
```

- Kiểm tra kiểu chuỗi (string) ta dùng hàm `is_string($bien)`.

<a name="5"></a>
### 5. Kiểu mảng (array):

- Mảng là danh sách các phần tử có cùng kiểu dữ liệu, có 2 loại mảng là mảng 1 chiều và mảng nhiều chiều. Đối với PHP thì các phần tử của mảng có thẻ không cùng kiểu dữ liệu, các phần tử của mảng được truy xuất thông qua các chỉ mục (vị trí) của nó nằm trong mảng.

#### Khởi tạo và truy xuất các phần tử nằm trong mảng

- Để khai báo mảng ta dùng cú pháp sau:

```
<?php
	$ten_mang = array();	//khởi tạo 1 mảng gán vào biến $ten_mang
?>
```

- Sử dụng hàm `var_dump($mang);` để in ra các phần tử của mảng, hàm này có thể sử dụng được với tất cả các kiểu dữ liệu trong PHP

#### Mảng có chỉ mục:

- Là mảng có các phần tử được định danh 1 chỉ mục (kiểu số) và bắt đầu bằng số 0 và phần tử cuối cùng có chỉ mục là `(n-1)`, n là tổng số phần tử của mảng

- Để truy xuất các phần tử của mảng chỉ mục ta sử dụng cú pháp `$ten_mang[$index];` trong đó `$index` là chỉ mục muốn lấy

```javascript
<?php
$sinhvien = array(
0 => 'Nguyễn Văn A',
1 => 'Nguyễn Văn B'
);
echo $sinhvien[0]; // Xuất ra màn hình phần tử 0 => Nguyễn Văn A
echo $sinhvien[1]; // Xuất ra màn hình phần tử 1 => Nguyễn Văn B
?>
```

#### Mảng kết hợp:

- Là mảng có các phần tử được định danh bằng 1 cái tên, vị trí của các phần tử sẽ không có thứ tự

```javascript
<?php
$sinhvien = array(
'sinhvien_a' => 'Nguyễn Văn A',
'sinhvien_b' => 'Nguyễn Văn B'
);
print_r($sinhvien);
?>
```

#### Mảng 1 chiều:

- Các ví dụ phía trên là mảng 1 chiều

#### Mảng nhiều chiều:

- Là mảng có nhiều chỉ mục cho từng phần tử, ví dụ mảng 2 chiều thì mỗi phần tử có 2 chỉ mục, 3 chiều thì mỗi phần tử có 3 chỉ mục...

- Mảng nhiều chiều thực chất là mảng 1 chiều được thể hiện dưới dạng nhiều chiều.

- Ví dụ: thêm phần tử trong mảng 2 chiều

```javascript
<?php
$a = array();
$a[0][1] = 123;
$a[0][2] = 321;
?>
```

- Ví dụ: truy xuất phần tử trong mảng 2 chiều:

```javascript
<?php
$a = array();
$a[0][1] = 123;
$a[0][2] = 321;
echo $a[0][1]; // in ra giá trị 123
echo $a[0][2]; // in ra giá trị 321
?>
```

- Để kiểm tra một biến có phải kiểu mảng (array) không ta dùng hàm is_array($bien), hàm này trả về TRUE nếu đúng và FALSE nếu không đúng.

<a name="6"></a>
### 6. Kiểu giá trị null:

- Đây là kiểu đặc biệc trong php cũng như các ngôn ngữ lập trình khác, nó mang giá trị rỗng. Khởi tạo 1 biến gán = NULL thì hệ thống sẽ không tốn bộ nhớ để lưu trữ.

- Kiểu NULL khi ép sang kiểu INT thì bằng 0, ép sang kiểu chuỗi thì bằng rỗng, ép sang kiểu boolean thì mang giá trị FALSE.

```javascript
<?php 
$a = null; // Khởi tạo biến $a và gán giá trị null
$b = (int)$a; // Biến $b có giá trị là ( 0 )
$c = (string)$a; // Biến $c có giá trị rỗng ( '' )
$d = (bool)$a; // Biến $d có giá trị FALSE
?>
```

- Để kiểm tra 1 biến có giá trị null hay không sử dụng hàm `is_null($bien)`. 

<a name="7"></a>
### 7. Kiểu Object (đối tượng):

<a name="8"></a>
### Tài liệu tham khảo:

> [1] Các kiểu dữ liệu trong php. https://freetuts.net/cac-kieu-du-lieu-trong-php-3.html

