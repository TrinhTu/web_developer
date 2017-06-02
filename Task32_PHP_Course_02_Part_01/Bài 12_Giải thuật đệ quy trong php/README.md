## BÀI 12: GIẢI THUẬT ĐỆ QUY TRONG PHP

> Tài liệu: Giải thuật đệ quy trong php
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 31/05/2017

### Mục lục:

[1. Giải thuật đệ quy là gì](#1)

[2. Đệ quy tuyến tính](#2)

[3. Đệ quy nhị phân](#3)

[4. Đệ quy hổ tương](#4)

[5. Khử đệ quy](#5)

[Tài liệu tham khảo](#6)

***

<a nam="1"></a>
### 1. Giải thuật đệ quy là gì:

- Một tính chất trong toán học được gọi là đệ quy nếu trong đó 1 lớp các đối tượng có các tính chất giống nhau và có mối liên hệ với nhau, kết quả của bước 1 là 1 thành phần của bước 2, bước 2 là thành phần của bước 3

- Một chương trình đệ quy phải có điều kiện dừng, nếu không thì chương trình sẽ bị lặp vô hạn.

<a name="2"></a>
### 2. Đệ quy tuyến tính:

- Đây là loại đệ quy mà trong hàm đệ quy chỉ gọi duy nhất 1 lần đến nó

- Ví dụ: Cho n=100, tính tổng các số từ 1 -> 100

```javascript
function tinhtong($n){
    $tong = 0;
    for ($i = 1; $i <= $n; $i++){
        $tong += $i; // mỗi vòng lặp cộng lại với nhau
    }
    return $tong;
}
```

- Sử dụng đệ quy với bài toán trên là ở mỗi lần đệ quy sẽ lấy số đó cộng với hàm chính nó và biến truyền vào là số đó trừ đi 1. Điều kiện dừng là nếu số đó = 1 thì dừng vòng lặp và trả về kết quả. Mỗi bước đệ quy chính là 1 lần lặp, cộng dồn tổng các lần đệ quy chính là cộng dồn tổng các lần lặp.

```javascript
function tinhtong($n)
{
    if ($n == 1){ return $n; }
    return $n + tinhtong($n-1);
}
echo tinhtong(100);
```

<a name="3"></a>
### 3. Đệ quy nhị phân:

<a name="4"></a>
### 4. Đệ quy hổ tương:

- Là đệ quy 1 hàm A gọi sang 1 hàm B, trong hàm B lại gọi sang hàm A, chúng gọi qua lại lẫn nhau. Nếu hàm A,B đều không có điều kiện dừng thì sẽ bị lặp vô hạn
<a name="5"></a>
### 5. Khử đệ quy:


<a name="6"></a>
### Tài liệu tham khảo:

> [1] Giải thuật đệ quy trong php. https://freetuts.net/giai-thuat-de-quy-trong-php-12.html