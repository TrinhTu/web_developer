## BÀI 13: THUẬT TOÁN SẮP XẾP NỔI BỌT TRONG PHP

> Tài liệu: Thuật toán sắp xếp nổi bọt trong php
> 
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 28/05/2017

### Mục lục:

[1. Sắp xếp nổi bọt tăng dần](#1)

[2. Sắp xếp nổi bọt giảm dần](#2)

[3. Đưa thuật toán sắp xếp nổi bọt vào hàm](#3)

[Tài liệu tham khảo](#4)

***

<a name="1"></a>
### 1. Sắp xếp nổi bọt tăng dần:

- Thuật toán sắp xếp nổi bọt tăng dần được xử lí như sau:

	+ Cho vòng lặp `$i` chạy từ 1 tới `($n-1)`:

		+ Lần lặp 1: $i = 1, lần lượt so sánh với các vị trí khác bắt đầu từ ($i + 1) tức là vị trí thứ 2, nếu phần tử thứ 1 lớn hơn các phần từ đứng sau bắt đâu từ vị trí thứ 2 thì hoán vị chúng

		+ Lần lặp 2: $i = 2, lần lược so sánh với các vị trí khác bắt đầu từ ($i + 1) tức là vị trí 3, nếu phần tử thứ 2 lớn hơn các phần tử  đứng sau nó bắt đầu từ 3 thì hoán vụ chúng.

		+ Lặp đến lần thứ ($n - 1), lúc này biến $i = ($n -1) so sánh tới phần tử cuối cùng ($n) và hoán vị nếu không thoả mãn

- Ví dụ: Cho mảng sau `$mang = array(1,5,9,2,4,9)` dùng thuật toán sắp xếp nổi bọt sắp xếp mảng theo thứ tự tăng dần. Mảng này có 6 phần tử bắt đầu từ 0->5.

```javascript
$mang = array(1, 5, 9, 2, 4, 9); // mảng theo đề bài
  
$sophantu = 6; // hoặc dùng hàm $sophantu = count($mang);
  
// Sắp xếp mảng
for ($i = 0; $i < ($sophantu - 1); $i++)
{
    for ($j = $i + 1; $j < $sophantu; $j++) // lặp các phần tử phía sau
    {
        if ($mang[$i] > $mang[$j]) // nếu phần tử $i bé hơn phần tử phía sau
        {
            // hoán vị
            $tmp = $mang[$j];
            $mang[$j] = $mang[$i];
            $mang[$i] = $tmp;
        }
    }
}
  
// Hiển thị các phần tử của mảng đã sắp xếp
for ($i = 0; $i < $sophantu; $i++){
    echo $mang[$i] . ' ';
}
```

`$tmp` là biến lưu trữ trung gian.

<a name="2"></a>
### 2. Sắp xếp nổi bọt giảm dần:

- Thuật toán sắp xếp nổi bọt giảm dần tương tự như so sánh tăng dần bằng cách so sánh 2 phần tử với nhau, nếu phần tử thứ `$i` bé hơn phần tử `($i + 1)` thì hoán i=vị 2 vị trí đó.

```javascript
$mang = array(1, 5, 9, 2, 4, 9); // mảng theo đề bài
  
$sophantu = 6; // hoặc dùng hàm $sophantu = count($mang);
  
// Sắp xếp mảng
for ($i = 0; $i < ($sophantu - 1); $i++)
{
    for ($j = $i + 1; $j < $sophantu; $j++) // lặp các phần tử phía sau
    {
        if ($mang[$i] < $mang[$j]) // nếu phần tử $i bé hơn phần tử phía sau
        {
            // hoán vị
            $tmp = $mang[$j];
            $mang[$j] = $mang[$i];
            $mang[$i] = $tmp;
        }
    }
}
  
// Hiển thị các phần tử của mảng đã sắp xếp
for ($i = 0; $i < $sophantu; $i++){
    echo $mang[$i] . ' ';
}
```

<a name="3"></a>
### 3. Đưa thuật toán sắp xếp nổi bọt vào hàm:

- Để chương trình có tính chuyên nghiệp dễ quản lí sửa đổi nên sắp xếp đoạn code vào trong 1 hàm.

```javascript
// Ham sắp xếp
function sap_xep_tang($mang)
{
    $sophantu = count($mang);
    // Sắp xếp mảng
    for ($i = 0; $i < ($sophantu - 1); $i++)
    {
        for ($j = $i + 1; $j < $sophantu; $j++)
        {
            if ($mang[$i] > $mang[$j])
            {
                // hoán vị
                $tmp = $mang[$j];
                $mang[$j] = $mang[$i];
                $mang[$i] = $tmp;
            }
        }
    }
    return $mang;
}
  
// Hàm xuất ra màn hình
function xuat_mang_ra_man_hinh($mang)
{
    $sophantu = count($mang);
    for ($i = 0; $i < $sophantu; $i++){
        echo $mang[$i] . ' ';
    }
}
  
//--------------------------------------------------
// Chương trình chính
$mang = array(1, 5, 9, 2, 4, 9); // mảng theo đề bài
  
// sắp xếp
$mang = sap_xep_tang($mang);
  
// xuất ra màn hình
xuat_mang_ra_man_hinh($mang);
```

<a name="4"></a>
### Tài liệu tham khảo:

> [1] Thuật toán sắp xếp nổi bọt trong php. https://freetuts.net/thuat-toan-sap-xep-noi-bot-trong-php-13.html