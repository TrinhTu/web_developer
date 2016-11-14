##Bài 5: Các thuộc tính CSS định dạng text

>Tài liệu: Các thuộc tính CSS định dạng text
>
>Người thực hiện: Lê Tú Trinh
>
>Cập nhập lần cuối: 14/11/2016

###Mục lục:

[1. Chọn màu cho chữ với color](#1)

[2. Thiết lập chữ in hoa và in thường](#2)

[3. Thiết lập vị trí text](#3)

[4. Thiết lập gạch chân cho chữ](#4)

[5. Xác định vị trí hiển thị chữ với text-indent](#5)

###Nội dung:

<a name="1"></a>
####1. Chọn màu cho chữ với color:

Sử dụng thuộc tính color để gán màu cho chữ. Có 3 cách biểu diễn color như sau:

- `HEX`: có định dạng `#ma_mau`

- `RGB`: có định dạng `rgb(xxx,yyy,zzz)`

- Tên màu: red, pink, blue...

Ví dụ khá đơn giản nè:

```
<div>
	<p id="hi">chữ này màu đỏ nè</p>
	<p id="he">chữ này màu xanh da trời nè</p>
	<p id="ha">chữ này màu hồng nè</p>
	<p id="ho">chữ này màu xanh lá cây nè</p>
</div>
```

CSS:

```
#hi{
	color: red;
}
#he{
	color: blue;
}
#ha{
	color: #ff33cc;
}
#ho{
	color: #00ff00;
}
```

![1](https://github.com/TrinhTu/web_developer/blob/master/Task10_CSS_Course_02/Bai05_Dinh_dang/image/(1).png)


<a name="2"></a>
####2. Thiết lập chữ in hoa và in thường:

Nếu muốn chỉnh cho thẻ nào đó luôn hiển thị chữ in hoa hoặc chữ thường thì ta sử dụng thuộc tính `text-trasform` với cái giá trị:

- `uppercase` : chuyển sang in hoa

- `lowercase`: chuyển sang in thường

- `none`: mặc định( không chuyển đổi)

Ví dụ ta có 1 đoạn văn sau:

```
<p id="hi">HTTP is designed to permit intermediate network elements to improve or enable communications between clients and servers. High-traffic websites often benefit from web cache servers that deliver content on behalf of upstream servers to improve response time. </p>
<p id="he">ĐÂY LÀ ĐOẠN VĂN VIẾT IN HOA, NHƯNG KHI BẠN NHÌN THẤY NÓ THÌ NÓ ĐÃ THÀNH CHỮ THƯỜNG MẤT RỒI. HIHI</p>

```
CSS:

```
#hi{
	text-transform: uppercase;
}
#he{
	text-transform: lowercase;
}
```

![2](https://github.com/TrinhTu/web_developer/blob/master/Task10_CSS_Course_02/Bai05_Dinh_dang/image/(2).png)


<a name="3"></a>
####3. Thiết lập vị trí của text:

Nếu muốn nội dung hiển thị ra giữa màn hình hay về bên trái, bên phải thì sử dụng thuộc tính `text-align` với các giá trị:

- `center`: ở giữa

- `left`: bên trái

- `right`: bên phải

- `justify`: căn đều 2 bên

Thêm các thuộc tính giá trị này vào ví dụ trên ta có kết quả như sau:

![3](https://github.com/TrinhTu/web_developer/blob/master/Task10_CSS_Course_02/Bai05_Dinh_dang/image/(3).png)


<a name="4"></a>
####4. Thiết lập gạch chân cho chữ:

Để thiết lập gạch chân cho chữ ta sử dụng thuộc tính `text-decoration` với giá trị:

- `underline`: gạch chân

- `none`: bỏ gạch chân

<a name="5"></a>
####5. Xác định vị trí hiển thị chữ với text-indent:

Thuộc tính này giúp chữ hiển thị ở vị trí nào đó tính từ góc trái trên cùng `text-indent`. Nó thường dùng gắn trong nội dung thẻ a của logo và ẩn nó đi

Ví dụ như sau: HTML

```
<div class="hi"> Nội dung hiển thị</div>
<div class="he">Nội dung đã bị ẩn đi rồi </div>
```

CSS:

```
.hi{
	color: #ff6600;
	text-align: center;
	text-transform: uppercase;
}
.he{
	text-indent: -1000px;
}
```

![4](https://github.com/TrinhTu/web_developer/blob/master/Task10_CSS_Course_02/Bai05_Dinh_dang/image/(4).png)
