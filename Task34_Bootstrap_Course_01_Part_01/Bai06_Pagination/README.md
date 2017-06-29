## BÀI 06: PAGINATION TRONG BOOTSTRAP 3

> Tài liệu: Pagination trong bootstrap 3
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 29/06/2017

### Mục lục:

[1. Tạo pagination đơn giản với bootstrap 3](#1)

[2. Pagination sử dụng class active & disabled](#2)

[3. Tạo nút previous & next với class pager](#3)

[Tài liệu tham khảo](#4)

***

<a name="1"></a>
### 1. Tạo pagination đơn giản với bootstrap 3:

- Pagination có nhiệm vụ giới hạn dữ liệu trên 1 trang, mọi thành phần tạo ra pagination đều nằm trong cặp thẻ `ul & li` thêm vào thẻ `ul` class `pagination`

<a name="2"></a>
### 2. Pagination sử dụng class active & disabled:

- Class active và disabled giúp người dùng nhận biết họ đang ở trang nào:

	+ Class `active` hiển thị background để báo cho biết đang ở trang nào

	+ Class `disabled` cấm chúng ta click vào trang nào đó (thường là trang hiện tại)

<a name="3"></a>
### 3. Tạo nút previous & next với class pager:

- Class này giúp tạo ra 2 nút `previous & next` bằng cách thêm class pager vào thẻ ul

```javascript
<ul class="pager">
    <li><a href="#">Previous</a></li>
    <li><a href="#">Next</a></li>
</ul>
```
<a name="4"></a>
### Tài liệu tham khảo:

> [1] Pagination trong bootstrap 3. https://freetuts.net/pagination-trong-bootstrap-3-179.html