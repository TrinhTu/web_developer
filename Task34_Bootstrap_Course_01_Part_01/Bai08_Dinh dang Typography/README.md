## BÀI 8: ĐỊNH DẠNG TYPOGRAPHY BOOTSTRAP 3

> Tài liệu: Định dạng Typography bootstrap 3
> 
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 30/06/2017

### Mục lục:

[1. Định dạng typography với tag h1->h6](#1)

[2. Định dạng paragraphs hay còn gọi là tag](#2)

[3. Định dạng blockquotes](#3)

[Tài liệu tham khảo](#4)

###

<a name="1"></a>
### 1. Định dạng typography với tag h1->h6:

```javascript
<div class="h1">h1. học lập trình</div>
<div class="h2">h2. học lập trình</div>
<div class="h3">h3. học lập trình</div>
<div class="h4">h4. học lập trình</div>
<div class="h5">h5. học lập trình</div>
<div class="h6">h6. học lập trình</div>
```

#### Tạo tiêu đề trang với class page-header:

- Phần này giúp tạo 1 tiêu đề kết hợp với tag h1 và small hoặc các thành phần html khác:

```javascript
<h1> Tạo tiêu đề trang <small> với class page-header</small></h1>
```

<a name="2"></a>
### 2. Định dạng paragraphs hay còn gọi là tag:

- Mặc định `font-size` mà bootstrap hỗ trợ là 14px áp dụng cho toàn bộ nội dung được bao bọc bên trong thẻ `<body>` và chiều cao văn bản được áp dụng cho mọi thẻ `<p>` là 10px, để làm nổi bậc nội dung thì dùng class `lead`

```javascript
<p class="lead"> học lập trình</p>
```

- Bên cạnh đó thuộc tính typography bootstrap giúp căng chỉnh hiển thị nội dung:

	+ text-left (canh trái)

	+ text-center (canh giữa)

	+ text-right (canh phải)

	+ text-justify (canh đều nội dung)

- Chuyển đổi nội dung thành in hoa, in thường và viết hoa chũ cái đầu:

	+ text-lowercase (in thường)

	+ text-uppercase (in hoa)

	+ text-capitalize (in hoa chữ cái đầu)

- Ngoài ra còn có thể dùng màu sắc để làm nổi bậc nội dung:

	+ text-muted

	+ text-primary

	+ text-success

	+ text-info

	+ text-warning

	+ text-danger

<a name="3"></a>
### 3. Định dạng blockquotes:

- Khi nội dung muốn thể hiện thành trích dẫn thì bọc nội dung đó và thẻ `<blockquote>`

```javascript
<blockquote>
	<p>Học học nữa học mãi</p>
	<small>bởi<cite>Mác Lê-nin</cite></small>
</blockquote>
```

<a name="4"></a>
### Tài liệu tham khảo:

> [1] Định dạng typography bootstrap 3. https://freetuts.net/dinh-dang-typography-bootstrap-3-185.html


