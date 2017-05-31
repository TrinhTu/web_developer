## BÀI 18: THUẬT TOÁN SẮP XẾP CHÈN TRONG PHP

> Tài liệu: Thuật toán sắp xếp chèn trong php
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 31/05/2017

### Mục lục:

[1. Thuật toán sắp xếp chèn](#1)

[2. Cài đặt thuật toán sắp xếp chèn](#2)

[Tài liệu tham khảo](#3)

***

<a name="1"></a>
### 1. Thuật toán sắp xếp chèn:

- Xem phần tử a[0] là 1 dãy đã có thứ tự

	+ Bước 1: chèn phần tử a[1] vào dãy theo đúng vị trí sao cho dãy a[0] và a[1] đã sắp đúng thứ tự

	+ Bước 2: chèn phần tử a[2] và dãy a[0], a[1] sao cho dãy a[0], a[1], a[2] đã sắp đúng thứ tự.

	+ Bước i: Chèn phần tử a[i] vào dãy a[0], a[1],...,a[i-1] sao cho  dãy a[0], a[1], a[2],...,a[i-1], a[i] đã sắp đúng thứ tự

Sau N-1 bước thì kết thúc (mảng có n-1 phần tử)


- **Ví dụ**: Sắp xếp tăng dần dãy 5 – 1 – 3 – 4 – 6 – 8.

	+ Bước 1: Coi như phần tử thứ nhất là số 5 đã được sắp xếp, dãy lúc này như sau: 5 - 1 – 3 – 4 – 6 – 8.

	+ Bước 2: Lấy phần tử thứ hai là số 1 gán vào đúng vị trí trong dãy 5, lúc này dãy như sau: 1 – 5 - 3 – 4 – 6 – 8.

	+ Bước 3: Lấy phần tử thứ ba là số 3 gán vào đúng vị trí trong dãy 1 – 5, lúc này dãy như sau: 1 – 3 – 5 – 4 – 6 – 8.

	+ Bước 4: Lấy phần tử thứ tư là số 4 gán vào đúng vị trí trong dãy 1 – 3 – 5, lúc này dãy như sau: 1 – 3 – 4 – 5 – 6 – 8.

	+ Bước 5: Lấy phần tử thứ năm là số 6 gán vào đúng vị trí trong dãy 1 – 3 – 4 – 5, lúc này dãy như sau: 1 – 3 – 4 – 5 – 6 – 8.

	+ Bước 6: Lấy phần tử thứ sáu ( phần tử cuối cùng) gán vào đúng vị trí trong dãy 1 – 3 – 4 – 5 – 6, lúc này dãy như sau: 1 – 3 – 4 – 5 – 6 – 8.

- Kết thúc: kết quả đã được sắp xếp như sau: 1 – 3 – 4 – 5 – 6 – 8

<a name="2"></a>
### 2. Cài đặt thuật toán sắp xếp chèn:

**Sắp xếp tăng dần**

```javascript
function InsertionSort($mang)  {
    // Tổng số phần tử
    $sophantu = count($mang);
  
    // Lặp qua từng phần tử của mảng để sắp xếp
    for ($i = 0; $i < $sophantu; $i++)
    {
        // Lặp từ phần tử thứ $i, ví dụ $i = 6
        // thì sẽ lặp từ phần tử số 6 trở về 0 để kiểm tra
        $loop = $i;
  
        // Lưu lại giá trị của $mang[$i] để khỏi bị mất
        $current = $mang[$i];
  
        // điều kiện dừng là $loop <= 0 (tức là hết mảng) hoặc
        // phần tử thứ $loop - 1 bé hơn phần tử thứ $i (vì đã tìm đc đúng vị trí)
        // nếu một trong 2 điều kiện đó đúng thì sẽ dừng vòng lặp
        while($loop > 0 && ($mang[$loop - 1] > $current))
        {
            // Di dời các phần tử lên 1 bậc
            $mang[$loop] = $mang[$loop - 1];
            $loop -= 1;
        }
  
        // Gán giá trị $current vào vị trí tìm được
        $mang[$loop] = $current;
    }
  
    return $m
```

**Sắp xếp giảm dần**

```javascript
function InsertionSort($mang)  {
    // Tổng số phần tử
    $sophantu = count($mang);
  
    // Lặp qua từng phần tử của mảng để sắp xếp
    for ($i = 0; $i < $sophantu; $i++)
    {
        // Lặp từ phần tử thứ $i, ví dụ $i = 6
        // thì sẽ lặp từ phần tử số 6 trở về 0 để kiểm tra
        $loop = $i;
  
        // Lưu lại giá trị của $mang[$i] để khỏi bị mất
        $current = $mang[$i];
  
        // điều kiện dừng là $loop <= 0 (tức là hết mảng) hoặc
        // phần tử thứ $loop - 1 lớn hơn phần tử thứ $i (vì đã tìm đc đúng vị trí)
        // nếu một trong 2 điều kiện đó đúng thì sẽ dừng vòng lặp
        while($loop > 0 && ($mang[$loop - 1] < $current))
        {
            // Di dời các phần tử lên 1 bậc
            $mang[$loop] = $mang[$loop - 1];
            $loop -= 1;
        }
  
        // Gán giá trị $current vào vị trí tìm được
        $mang[$loop] = $current;
    }
    return $mang;
```

<a name="3"></a>
### Tài liệu tham khảo:

> [1] Thuật toán sắp xếp chèn trong php. https://freetuts.net/thuat-toan-sap-xep-chen-trong-php-18.html