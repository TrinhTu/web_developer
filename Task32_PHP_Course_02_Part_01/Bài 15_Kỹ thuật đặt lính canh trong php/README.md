## BÀI 15: KĨ THUẬT ĐẶT LÍNH CANH TRONG PHP

> Tài liệu: Kĩ thuật đặt lính canh trong php
> 
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 28/05/2017

### Mục lục:

[1. Kĩ thuật đặt lính canh là gì?](#1)

[2. Khi nào sử dụng kĩ thuật đặt lính canh](#2)

[Tài liệu tham khảo](#3)

*** 

<a name="1"></a>
### 1. Kĩ thuật đặt lính canh là gì?

- Ví dụ 1: Tìm người cao nhất trong lớp học:

	+ Chọn 1 bạn làm mẫu rồi lần lượt so sánh với các bạn còn lại, nếu bạn nào cao hơn thì đổi chỗ cho bạn làm mẫu đó và những người bạn cao hơn, lúc này người bạn cao hơn sẽ đứng làm mẫu, vậy cho đến hết -> kết quả người làm mẫu cuối cùng là người cao nhất. Đây là kỹ thuật đặt lính canh.

- Ví dụ 2: Dùng kĩ thuật đặt lính canh tìm giá trị lớn nhất của 3 số $a, $b, $c.

	+ Khởi tạo 1 biến $max để chứa giá trị lớn nhất

	+ Giả sử biến lớn nhất là biến $a, gán $max = $a

	+ So sánh biến $max với $b, nếu $b lớn hơn $max thì gán $max = b;

	+ SO sánh biến $max với $c, nếu $c lớn hơn $max thì gán $max = c;

Cuối cùng biến $max chứa giá trị lớn nhất.

```javascript
function tim_max($a, $b, $c)
{
    $max = $a;
    if ($max < $b){
        $max = $b;
    }
    if ($max < $c){
        $max = $c;
    }
    return $max;
}
```

<a name="2"></a>
### 2. Khi nào sử dụng kĩ thuật đặt lính canh:

- Kĩ thuật đặt lính canh dùng khi muốn duyệt qua danh sách và chọn 1 phần tử đặc biệt nào đó.

- Dùng để tìm min max, giá trị lớn nhất, nhỏ nhất, số nguyên tố lớn nhất, nhỏ nhất... của 1 mảng trong danh sách

<a name="3"></a>
### Tài liệu tham khảo:

> [1] Kĩ thuật đặt lính canh trong php. https://freetuts.net/ky-thuat-dat-linh-canh-trong-php-15.html