## BÀI 04: TOÁN TỬ VÀ BIỂU THỨC TRONG PHP

> Tài liệu: Khai báo biến và hằng số trong php
> 
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 24/05/2017

### Mục lục:

[1. Biểu thức là gì?](#1)

[2. Toán tử quan hệ](#2)

[3. Toán tử luận lý](#3)

[4. Độ ưu tiên các toán tử](#4)

[Tài liệu tham khảo](#5)

***

<a name="1"></a>
### 1. Biểu thức là gì?

- Biểu thức là tổ hợp các toán tử và toán hạng, toán tử thực hiện các thao tác cộng, trừ, nhân, chia, so sánh... toán hạng là những biến hay những giá trị mà các phép toán được thực hiện trên nó. Ví dụ `$a + $b` thì $a và $b là toán hạng, dấu + là toán tử, kết hợp cả 2 gọi là biểu thức.

```javascript
$ketqua = $a - $b;
$ketqua = 7 + 6;
$ketqua = 3*$x + 4*$y;
```

#### Toán tử gán (Assignment Operator):

- Dùng dấu `=` để gán giá trị cho 1 biến bất kì. `$a = 12;`

- Nhiều biến có thể được gán cùng 1 giá trị qua 1 câu lệnh đơn gọi là gán gián tiếp.

`$a = $b = $c = $d = 12;`

#### Biểu thức số học:

- Biểu thức số học là biểu thức được thực hiện bằng cách sử dụng các toán tử số học cùng với các toán tử hạng số hoặc kí tự (biến)

```javascript
$ketqua = $a + $b/2;
$ketqua = $a / 7;
$ketqua = $a + ($b = 5 + 6);
```

<a name="2"></a>
### 2. Toán tử quan hệ:

- Toán tử quan hệ được dùng để kiểm tra mối quan hệ giữa 2 biến hay giữa 1 biến với 1 hằng số. Ví dụ để kiểm tra 2 biến $a và $b xem biến nào lớn hơn ta làm như sau: `($a > $b)` và kết quả sẽ trả về kiểu boolean là true or false

```javascript
$a = 12; // Biến $a kiểu INT có giá trị = 12
$t = ($a == 12); // Biến $t có giá trị là TRUE vì biểu thức (12 == 12) đúng
$t = ($a > 12);  // Biến $t có giá trị là FALSE vì biểu thức (12 > 12) sai
$t = ($a >= 12); // Biến $t có giá trị TRUE vief biểu thức (12 >= 12) đúng
$t = ($a != 12); // Biến $t có giá trị FALSE vì biểu thức (12 != 12) sai
```

- Toán tử quan hệ === dùng để so sánh giá trị giữa các biến và hằng theo giá trị và theo kiểu dữ liệu

<a name="3"></a>
### 3. Toán tử luận lý:

- Toán tử luận lý là kí hiệu dùng để kết hợp  hay phủ định biểu thức có chứa các toán tử quan hệ, những biểu thức dùng toán tử luận lí trả về giá trị TRUE or FALSE.

```javascript
$a = 100;
$b = 200;
$tong = $a + $b;
$check = ($a < $b) && ($tong > 200); //true
```

- AND: &&, OR: || , NOT: !

- Độ ưu tiên theo thứ tự: NOT -> AND -> OR

<a name="4"></a>
### 4. Độ ưu tiên các toán tử:

- Độ ưu tiên của các toán tử thiết lập thứ tự ưu tiên tính toán của 1 biểu thức. Các toán tử và biểu thức trong php có sự liên hệ lẫn nhau, toán tử kết hợp toán hạng tạo thành biểu thức

<a name="5"></a>
### Tài liệu tham khảo:

> [1] Toán tử và biểu thức trong php. https://freetuts.net/toan-tu-va-bieu-thuc-trong-php-4.html