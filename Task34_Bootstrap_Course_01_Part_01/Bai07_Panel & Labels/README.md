## BÀI 07: PANEL & LABELs TRONG BOOTSTRAP 3

> Tài liệu: Panel & Labels trong bootstrap 3
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 29/06/2017

### Mục lục:

[1. Labels & Panel là gì?](#1)

[2. Class label trong bootstrap 3](#2)

[3. Class Panel trong bootstrap 3](#3)

[Tài liệu tham khảo](#4)

***

<a name="1"></a>
### 1. Labels & Panel là gì?

- Labels là nhãn dán được dùng để định nghĩa mô tả 1 phần text nổi bật, còn panel là khung điều khiển.

<a name="2"></a>
### 2. Class labels trong bootstrap 3:

- Để hiển thị đoạn text hỗ trợ stylesheet thì thêm class label là class `label-default`

```javascript
	<h1>Freetuts là website học lập trình miễn phí<span class="label label-default">Mới</span></h1>
	<h2>Freetuts là website học lập trình miễn phí<span class="label label-default">Mới</span></h2>
	<h3>Freetuts là website học lập trình miễn phí<span class="label label-default">Mới</span></h3>
	<h4>Freetuts là website học lập trình miễn phí<span class="label label-default">Mới</span></h4>
	<h5>Freetuts là website học lập trình miễn phí<span class="label label-default">Mới</span></h5>
	<h6>Freetuts là website học lập trình miễn phí<span class="label label-default">Mới</span></h6>
```

- Có thể thay đổi màu sắc các label bằng cách sử dụng các class sau:

	+ label-primary (hiển thị màu xanh dương đậm)

	+ label-success (hiển thị màu xanh lá)

	+ label-warning (hiển thị màu cam)

	+ label-info (hiển thị màu xanh dương nhạt)

	+ label-danger (hiển thị màu đỏ)

<a name="3"></a>
### 3. Class Panel trong bootstrap 3:

- Giúp tạo ra các khối block (sidebar) hay các đoạn text được bao bọc trong khung có đường viền, có 3 class sau đây:

	+ panel-default (class này phải khai báo chung với class panel)

	+ panel-heading (hiển thị phần bao bọc đoạn tiêu đề)

	+ panel-body (phần nội dung bên trong khung)

Trong phần `panel-heading` có thể sử dụng tag h1->h6 nhưng cần gán thêm class `panel-title`

<a name="4"></a>
### Tài liệu tham khảo:

> [1] Panel Labels trong bootstrap 3. https://freetuts.net/panel-labels-trong-bootstrap-3-184.html