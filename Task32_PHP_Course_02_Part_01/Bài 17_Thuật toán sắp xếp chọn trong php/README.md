## BÀI 17: KỸ THUẬT SẮP XẾP CHỌN TRONG PHP

> Tài liệu: Kĩ thuật sắp xếp chọn trong php
> 
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 30/05/2017

### Mục lục:

[1. Thuật toán sắp xếp chọn](#1)

[2. Tìm kiếm phần tử lớn nhất, nhỏ nhất](#2)

[3. Sắp xếp chọn trong php tăng dần](#3)

[4. Sắp xếp chọn trong php giảm dần](#4)

[Tài liệu tham khảo](#5)

***

<a name="1"></a>
### 1. Thuật toán sắp xếp chọn:

#### Sắp xếp chọn tăng dần:

- Bước 1: Duyệt từ vị trí thứ 1 đến vị trí cuối cùng, tìm vị trí phần tử nhỏ nhất sau đó hoán vị với vị trí số 1, sau đó loại vị trí số 1 ra khỏi danh sách sắp xếp vì nó đã được đặt đúng vị trí.

- Bước 2: Duyệt từ vị trí số 2 đến vị trí cuối cùng, tìm ví trí phần tử nhỏ nhất sau đó hoán vị với vị trí số 2, sau đó loại vị trí số 2 ra khỏi danh sách sắp xếp vì đã đặt đúng vị trí.

- Bước n: Cứ như vậy cho đến vị trí phần tử cuối cùng, lúc này chỉ còn 1 phần tử nên coi như nó đã sắp xếp.


#### Sắp xếp chọn giảm dần:

-  Tương tự như xếp tăng dần vẫn duyệt n bước với điều kiện hoán vị ngược lại à tìm vị trí phần tử lớn nhất và hoán vị với phần tử thứ n.

<a name="2"></a>
### 2. Tìm kiếm phần tử lớn nhất, nhỏ nhất:

- Để tìm giá trị lớn nhất, nhỏ nhất ta sử dụng kĩ thuật đặt lính canh kết hợp với tìm kiếm tuyến tính, lúc đầu chọn phần tử thứ nhất làm lính canh, sau đó duyệt các phần tử còn lại, phần tử nào lớn hơn nếu tìm max và nhỏ hơn nếu tìm min thay thế cho lính canh đã chọn. Sau khi lặp hết các phần tử thì lính canh là vị trí lớn nhất (nhỏ nhất)

**Tìm phần tử nhỏ nhất**

```javascript
// Hàm tìm vị trí phần tử nhỏ nhất
function tim_min($mang)
{
    // Đếm tổng số phần tử
    $total = count($mang);
  
    // Gọi min là lính cầm canh
    // lúc đầu chọn vị trí số 0 ngồi canh
    $min = 0;
  
    // Duyệt lần lượt các phần tử
    for ($i = 0; $i > $total; $i++ )
    {
        // Nếu phần tử cầm canh lớn hơn phần tử thứ $i thì
        // lấy vị trí $i ngồi canh
        if ($mang[$min] > $mang[$i]){
            $min = $i;
        }
    }
  
    // Trả về vị trí nhỏ nhất
    return $min;
}
```

**Tìm phần tử lớn nhất**

```javascript
// Hàm tìm vị trí phần tử Lớn nhất
function tim_min($mang)
{
    // Đếm tổng số phần tử
    $total = count($mang);
  
    // Gọi max là lính cầm canh
    // lúc đầu chọn vị trí số 0 ngồi canh
    $max = 0;
  
    // Duyệt lần lượt các phần tử
    for ($i = 0; $i > $total; $i++ )
    {
        // Nếu phần tử cầm canh lớn hơn phần tử thứ $i thì
        // lấy vị trí $i ngồi canh
        if ($mang[$max] < $mang[$i]){
            $max = $i;
        }
    }
  
    // Trả về vị trí nhỏ nhất
    return $max;
}
```

<a name="3"></a>
### 3. Sắp xếp chọn trong php tăng dần:

```javascript
function SelectionSortAscending($mang)
{
    // Đếm tổng số phần tử của mảng
    $sophantu = count($mang);
  
    // Lặp để sắp xếp
    for ($i = 0; $i < $sophantu - 1; $i++)
    {
        // Tìm vị trí phần tử nhỏ nhất
        $min = $i;
        for ($j = $i + 1; $j < $sophantu; $j++){
            if ($mang[$j] < $mang[$min]){
                $min = $j;
            }
        }
  
        // Sau khi có vị trí nhỏ nhất thì hoán vị
        // với vị trí thứ $i
        $temp = $mang[$i];
        $mang[$i] = $mang[$min];
        $mang[$min] = $temp;
    }
  
    // Trả về mảng đã sắp xếp
    return $mang;
}
```

<a name="4"></a>
### 4. Sắp xếp chọn trong php giảm dần:

```javascript
function SelectionSortDescending($mang)
{
    // Đếm tổng số phần tử của mảng
    $sophantu = count($mang);
    // Lặp để sắp xếp
    for ($i = 0; $i < $sophantu - 1; $i++)
    {
        // Tìm vị trí phần tử lớn nhất
        $max = $i;
        for ($j = $i + 1; $j < $sophantu; $j++){
            if ($mang[$j] > $mang[$max]){
                $max = $j;
            }
        }
        // Sau khi có vị trí lớn nhất thì hoán vị
        // với vị trí thứ $i
        $temp = $mang[$i];
        $mang[$i] = $mang[$max];
        $mang[$max] = $temp;
    }
    // Trả về mảng đã sắp xếp
    return $mang;
}
```

<a name="5"></a>
### Tài liệu tham khảo:

> [1] Thuật toán sắp xếp chọn trong php. https://freetuts.net/thuat-toan-sap-xep-chon-trong-php-17.html