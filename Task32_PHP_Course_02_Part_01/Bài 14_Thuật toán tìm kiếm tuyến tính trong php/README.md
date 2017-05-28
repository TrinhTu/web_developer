## BÀI 14: THUẬT TOÁN TÌM KIẾM TUYẾN TÍNH TRONG PHP

> Tài liệu: Thuật toán tìm kiếm tuyến tính trong php
> 
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 28/05/2017

### Mục lục:

[1. Tìm kiếm tuyến tính là gì](#1)

[2. Ví dụ tìm kiếm tuyến tính](#2)

[Tài liệu tham khảo](#3)

***

<a name="1"></a>
### 1. Tìm kiếm tuyến tính là gì:

- Tìm kiếm tuyến tính hay tìm kiếm tuần tự là 1 thuật toán tìm kiếm 1 phần tử cho trước nằm trong 1 danh sách bằng cách duyệt lần lượt các phần tử và so sánh cho đến khi tìm thấy phần tử đó.

<a name="2"></a>
### 2. Ví dụ tìm kiếm tuyến tính:

- Ví dụ 1: cho mảng `$mang = array(321,312,3,4,5,45,56,5,7,6,787,8,7,2);` Hãy viết hàm kiểm tra số 67 có nằm trong mảng không?

Giải không dùng hàm:

```javascript
$mang = array(321,312,3,4,5,45,56,5,7,6,787,8,7,2);
  
$can_tim = 67;
  
for ($i = 0; $i < count($mang); $i++){ // duyệt qua từng phần tử của mảng
    if ($mang[$i] == $can_tim){ // và so sánh xem có bằng số 67 không, nếu có thì xuất ra màn hình và dừng vòng lặp
        echo 'Số ' . $can_tim . ' có nằm trong mảng tại ví trí thứ ' . $i;
        break;
    }
```

Giải dùng hàm:

```javascript
// hàm kiểm tra
function kiem_tra($mang, $can_tim)
{
    for ($i = 0; $i < count($mang); $i++){ // duyệt qua từng phần tử của mảng
        if ($mang[$i] == $can_tim){ // và so sánh xem có bằng số 67 không, nếu có thì xuất ra màn hình
            return true; // và không cần làm gì trong hàm này nữa, trả về là đúng luôn
        }
    }
    return false; // sau khi lặp hết mà ko có thì return về false
}
  
// ---------------------- chương trình chính
// Cho mảng
$mang = array(321,312,3,4,5,45,56,5,7,6,787,8,7,2);
  
// biến cần tìm
$can_tim = 67;
  
// gọi hàm và xuất kết quả
if (kiem_tra($mang, $can_tim)){
    echo 'Số ' . $can_tim . ' có nằm trong mảng';
}
```

- Ví dụ 2: Cho một mảng gồm các phần tử từ 1 đến 100. Hãy tìm vị trí các số chia hết cho 3 trong dãy

```javascript
// Hàm tìm các số chia hết cho 3
function tim_so_chia_het_cho_3($mang)
{
    foreach ($mang as $key => $val){
        if ($val % 3 == 0){
            echo 'Ví trí thứ ' . $key . '<br/>';
        }
    }
}
  
// Chương trình chính
//-----------------------------------------------
// Lặp từ 1 đến 100 để gán giá trị vào mảng
$mang = array();
for ($i = 1; $i <= 100; $i++){
    $mang[$i] = $i;
}
  
// Gọi hàm để xuất ra vị trí chia hết cho 3
tim_so_chia_het_cho_3($mang);
```

<a name="3"></a>
### Tài liệu tham khảo:

> [1] Thuật toán tìm kiếm tuyến tính trong php. https://freetuts.net/thuat-toan-tim-kiem-tuyen-tinh-trong-php-14.html