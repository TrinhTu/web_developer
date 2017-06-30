## BÀI 10: TẠO BUTTON TRONG BOOTSTRAP 3

> Tài liệu: Tạo button trong bootstrap 3
> 
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 30/06/2017

### Mục lục:

[1. Định nghĩa các class button trong bootstrap 3](#1)

[2. Class resize button bootstrap 3](#2)

[3. Class active & disabled bootstrap 3](#3)

[Tài liệu tham khảo](#4)

***

<a name="1"></a>
### 1. Định nghĩa các class button trong bootstrap 3:

- .btn: Button mặc định (Bắt buộc phải khai báo)

- .btn-primary: Tạo ra button màu xanh dương đậm

- .btn-success: Tạo ra button màu xanh

- .btn-info: Tạo ra button màu xanh dương

- .btn-warning:	Tạo ra button màu cam

- .btn-danger: Tạo ra button màu đỏ

- .btn-link: Tạo ra button có dạng cick liên kết

```javascript
        <h2>Định nghĩa các class buttons</h2>
        <button type="button" class="btn btn-default">Default Button</button>
        <button type="button" class="btn btn-primary">Primary Button</button>
        <button type="button" class="btn btn-success">Success Button</button>
        <button type="button" class="btn btn-info">Info Button</button>
        <button type="button" class="btn btn-warning">Warning Button</button>
        <button type="button" class="btn btn-danger">Danger Button</button>
        <button type="button" class="btn btn-link">Link Button</button>
```

<a name="2"></a>
### 2. Class resize button bootstrap 3:

- .btn-lg: Tạo ra button với size lớn nhất

- .btn-sm: Tạo ra button với size nhỏ vừa

- .btn-xs: Tạo ra button với size nhỏ xíu

- .btn-block: Tạo ra button với dạng block.

```javascript
 	<h2>Định nghĩa các class buttons resize (btn-xx)</h2>
    <button type="button" class="btn btn-default btn-lg">Button lớn nhất</button>
    <button type="button" class="btn btn-primary btn-sm">Button nhỏ vừa</button>
    <button type="button" class="btn btn-success btn-xs">Button nhỏ nhất</button>
    <button type="button" class="btn btn-info btn-block">Button block</button>
```

<a name="3"></a>
### 3. Class active & disabled bootstrap 3:

- Giúp làm nổi bậc button sau khi đã click và không cho click nữa

```javascript
		<h2>Định nghĩa các class active & disabled</h2>
        <button type="button" class="btn btn-info active">Button Active</button>
        <button type="button" class="btn btn-primary disabled">Button Disabled</button>
        <button type="button" class="btn btn-link active">Link Active</button>
        <button type="button" class="btn btn-link disabled">Link Disabled</button>
```
<a name="4"></a>
### Tài liệu tham khảo:

> [1] Tạo button trong bootstrap 3. https://freetuts.net/tao-button-trong-bootstrap-3-186.html 