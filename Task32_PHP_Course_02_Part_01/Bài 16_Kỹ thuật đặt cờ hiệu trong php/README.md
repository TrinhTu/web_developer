## BÀI 16: KĨ THUẬT ĐẶT CỜ HIỆU TRONG PHP

> Tài liệu: Kĩ thuật đặt cờ hiệu trong php
> 
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 30/05/2017

### Mục lục:

[1. Kỹ thuật đặt cờ hiệu là gì?](#1)

[2. Khi nào sử dụng kĩ thuật đặt cờ hiệu](#2)

[Tài liệu tham khảo](#3)

***

<a name="1"></a>
### 1. Kỹ thuật đặt cờ hiệu là gì?

- Ví dụ 1: Quy trình của đội bóng trước khi ra sân

	+ Giả sử có đội bóng kiểm tra sức khỏe trước khi ra sân thi đấu ,nếu có 1 người sử dụng chất kích thích thì cả đội bóng sẽ không được thi đấu. Cách thực hiện là duyệt qua từng người và kiểm tra, đây là kỹ thuật đặt cờ hiệu.

- Ví dụ 2: Kiểm tra xem các số từ 1 -> 1000 có số nào chia hết cho 40 không
	+ Dùng kỹ thuật đặt cờ hiệu lặp từ 1 -> 1000 rồi chia lấy dư cho 40, chỉ cần 1 số chia hết cho 40 là kết luận tồn tại số chia hết cho 40 khoảng từ 1- > 1000

```javascript
// Khai báo cờ và gán cho cờ có giá trị là không tìm thấy
$flag = false;
  
// duyệt qua từng số
for ($i = 1; $i <= 1000; $i++){
    if ($i % 40 == 0){
        $flag = true;
    }
}
  
if ($flag == true){
    echo 'Có';
}
else {
    echo 'Không';
}
```

<a name="2"></a>
### 2. Khi nào sử dụng kĩ thuật đặt cờ hiệu:

- Kĩ thuật đặt cờ hiệu dùng để duyệt mảng danh sách và kiểm tra từng phần tử để đưa ra kết quả cuối cùng.

<a name="3"></a>
### Tài liệu tham khảo:

> [1] Kỹ thuật đặt cờ hiệu trong php. https://freetuts.net/ky-thuat-dat-co-hieu-trong-php-16.html