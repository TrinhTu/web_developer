## BÀI 11: XÂY DỰNG HÀM TRONG PHP

> Tài liệu: Xây dựng hàm trong php
> 
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 28/05/2017

### Mục lục:

[1. Cách sử dụng hàm trong php](#1)

[2. Cấu trúc của 1 hàm trong php](#2)

[3. Các cách gọi hàm trong php](#3)

[4. Các quy tắc và phạm vi của hàm](#4)

[Tài liệu tham khảo](#5)

***

<a name="1"></a>
### 1. Cách sử dụng hàm trong php:

- Hàm trong php dùng để thực hiện 1 khối lệnh liên tiếp có điểm đầu và điểm cuối. Một hàm được xác định thực hiện 1 công việc cụ thể nào đó, hàm có thể được gọi ở nhiều nơi, nhiều chương trình khác nhau.

<a name="2"></a>
### 2. Cấu trúc của 1 hàm trong php:

- Cú pháp tổng quát khai bao quát trong php là:

```javascript
function func_name($vars)
{
	// các đoạn code
	return $val;
}
```

- Trong đó: `func_name` là tên của hàm, `$vars` là các biến sẽ truyền vào trong hàm, `return $val` là hàm sẽ trả về giá trị `$val`. Nếu hàm không có giá trị nào thì ta không có dòng return.

- Ví dụ:

```javascript
// Số cần kiểm tra
$number = 12;
  
// gọi đến hàm kiem_tra_so_chan và truyền biến cần kiểm tra vào
// vì hàm kiem_tra_so_chan trả về true/false nên ta có thể đặt nó trong câu điều
// kiện if như thế này
if (kiem_tra_so_chan($number)){
    echo 'Số chẵn';
}
else{
    echo 'Số lẽ';
}
  
// Hàm kiểm tra số chẵn sẽ trả về true nếu $number là số chẵn và ngược lại.
// biến $number gọi là biến truyền vào hàm, đó chính là biến cần kiểm tra
function kiem_tra_so_chan($number)
{
    if ($number % 2 == 0)
        return true;
    else return false;
}
```

- Hàm `kiem_tra_so_chan` có nhiệm bvuj kiểm tra 1 số là số chẵn hay lẻ, nếu số chẵn thì trả về true, ngược lại trả về false

#### Truyền nhiều biến vào hàm trong php:

- Các biến truyền vào hàm trong php có thể là các kiểu bất kì. Và số biến truyền vào không giới hạn, có thể truyền nhiều biến vào bằng cách mỗi biến cách nhau bởi dấu phẩy.

- Ví dụ:

```javascript
function tinhtong($a, $b)
{
    return $a + $b;
}
```

- Hàm này sẽ tính tổng của 2 biến truyền vào, các biến cách nhau bởi dấu phẩy.

```javascript
$so1 = 12;
$so2 = 13;
  
echo tinhtong($so1, $so2);
  
function tinhtong($a, $b)
{
    return $a + $b;
}
```

#### Gán giá trị mặc định cho biến truyền vào:

- Nếu 1 hàm trong php khai báo có 2 biến truyền vào mà chỉ truyền vào 1 biến thì hệ thống sẽ báo lỗi. Trong php cung cấp cho ta chức năng truyền giá trị mặc định cho biến trong các hàm:

```javascript
$so1 = 12;
$so2 = 13;
  
// chỉ truyền 2 đối số vào
echo tinhtong($so1, $so2);
  
// $c có một giá trị mặc định
// hàm này tính tổng của 3 số
function tinhtong($a, $b, $c = false)
{
    $tong = $a + b;
    if ($c != false){ // nếu $c được truyền vào (vì false là giá trị mặc định)
        $tong = $tong + $c; // thì thực hiện cộng thêm $c
    }
    return $tong;
}
```

Hàm `tinhtong` có nhiệm vụ tính tổng cả 3 số, nếu $c không truyền vào thì chỉ tính tổng của 2 số.

#### Tham số thực và tham số hình thức:

- Các biến ta định nghĩa trong hàm gọi là tham số hình thức, còn biến ta truyền vào chương trình gọi là tham số thực

```javascript
// Chuong trinh chinh
$so = 12;
$flag = kiem_tra_so_nguyen_to($so);
  
// ham kiem tra so nguyen to
function kiem_tra_so_nguyen_to($number)
{
  // code
}
```

- Tham số `number` trong hàm `kiem_tra_so_nguyen_to` gọi là tham số hình thức, biến `$so` trong chương trình chính là tham số thực

#### Biến toàn cục, biến cục bộ:

- Biến toàn cục là biến khai báo ở chương trình chính, biến cục bộ là biến khai báo ở các hàm.

```javascript
// Biến toàn cục
$bien_toan_cuc = 12;
  
function kiem_tra()
{
    // Biến cục bộ
    $bien_cuc_bo = 13;
  
    // Lấy biến toàn cục
    global $bien_toan_cuc;
  
    // Lấy số dư biến cục bộ chia cho biến toàn cục và
    // kiểm trả về true nếu số dư = 0, ngược lại trả về false
    if ($bien_cuc_bo % $bien_toan_cuc){
        return true;
    }
    else{
        return false;
    }
}
```

- Trong php để lấy giá trị biến toàn cục, ta dùng lệnh `global $tenbien` 

#### Biến tĩnh:

- Là các biến cố định trong các hàm, được biết đến trong hàm, giá trị sẽ được lưu lại sau mỗi lần gọi hàm. Để khai báo là 1 biến tĩnh dùng từ khóa `static $tenbien`

- Ví dụ:

```javascript
// ham kiem tra
function kiem_tra()
{
    // bien tinh
    static $a = 0;
    $a++;
    echo $a;
}
  
kiem_tra();
kiem_tra();
```

<a name="3"></a>
### 3. Các cách gọi hàm trong php:

#### Truyền bằng giá trị:

- Mặc định tất cả các đối số truyền vào hàm đều là truyền bằng giá trị, có nghĩa là khi các đối số được truyền đến hàm được gọi giá trị được truyền thông qua các biến tạm (tham số hình thức), mọi thao tác thực hiện trên biến tạm này nên không hề tác động đến biến chính. Nếu truyền bằng giá trị thì trong hàm nếu ta tác động đến giá trị biến truyền vào thì sau khi thoát khỏi hàm giá trị đó không thay đổi.

```javascript
// Biến
$a = 1;
  
// Hàm tăng giá trị tham số truyền vào lên 1
function tang_len_1($a)
{
    return $a + 1;
}
  
// Xuất giá trị trả về của hàm
echo tang_len_1($a);
  
// Xuất giá trị của biến
echo $a;
```

#### Truyền bằng tham chiếu:

- Khi các đối số được truyền bằng giá trị thì giá trị của các đối số của hàm đang gọi không bị thay đổi. Nếu muốn những giá trị đó thay đổi phải truyền biến vào hàm dạng tham chiếu.

```javascript
// Biến
 $a = 1;
  
// Hàm tăng giá trị tham số truyền vào lên 1
 function tang_len_1(&$a)
 {
    $a = $a + 1;
     return $a; 
 }
  
// Xuất giá trị trả về của hàm
 echo tang_len_1($a);
  
// Xuất giá trị của biến
 echo $a;
 ```

 - Dấu `&` báo cho trình phiên dịch biết đó là biến ở dạng tham chiếu.

<a name="4"></a>
### 4. Các quy tắc và phạm vi của hàm:

- Một hàm có thể gọi tới 1 hàm, tức là trong phần thân của hàm A có thể gọi đến hàm B, phần thân hàm B có thể gọi đến hàm C.

```javascript
// Danh sách các hàm
function A()
{
    B();
}
  
function B()
{
    C();
}
  
function C()
{
    echo 'C';
}
  
// Chương trình chính gọi đến hàm A
A(); // Kết quả xuất ra màn hình là 'C'
```

<a name="5"></a>
### Tài liệu tham khảo:

> [1] Xây dựng hàm trong php. https://freetuts.net/xay-dung-ham-trong-php-11.html
