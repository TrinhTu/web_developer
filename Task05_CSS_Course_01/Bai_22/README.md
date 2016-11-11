##Bài 22: CSS Framework và cách sử dụng

>Tài liệu: CSS Framework và cách sử dụng
>
>Người thực hiện: Lê Tú Trinh
>
>Cập nhập lần cuối: 9/11/2016

###Mục lục:

[1. CSS Framework là gì](#1)

[2. Các bộ CSS Framework](#2)

- [2.1 Bootstrap](#2.1)

- [2.2 960 Grid system](#2.2)

- [2.3 Purecss](#2.3)

- [2.4 Golden Grid system](#2.4)

- [2.5 Foundation](#2.5)

[3. Cách sử dụng CSS Framework](#3)

###Nội dung:

<a name="1"></a>
####1. CSS Framework là gì?

CSS Framework: là 1 bộ mã nguồn CSS đã được viết sẵn để chúng ta có thể sử dụng

Chức năng của CSS Framework là có sẵn định dạng để chúng ta có thể sử dụng dễ dàng trang trí cho các phần tử website như tạo menu, nút bấm

Mục đích của CSS là hỗ trợ thiết kế website nhanh hơn mà không cần phải viết lại CSS từ đầu

Có 2 loại CSS Framework là:

- Grid Framework: là bộ CSS famework chuyên mục đích chính là sử dụng để chia cột 1 cách dễ dàng hơn.

- UI Framework: Bộ CSS hoàn chỉnh bao gồm đầy đủ các thành phần cho website như nút bấm, menu, form...

<a name="2"></a>
####2.Các bộ CSS Framework phổ biến hiện nay:

<a name="2.1"></a>
- Bootstrap: 

![a](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_22/image/a.png)

Đây là bộ CSS Framework nổi tiếng nhất hiện nay mà hầu như dễ dàng tìm được website có sử dụng bộ này, bởi nó khá chi tiết, ngoài ra thì nó hỗ trợ gần như toàn bộ thành phần trong website, và nó cũng hỗ trợ sẵn nhiều hiệu ứng javascrip với 

Nhưng đối với những người mới học thì không nên sử dụng vì cấu trúc của nó phức tạp khó hiểu

Tham khảo tại đây: http://getbootstrap.com/

<a name="2.2"></a>
- 960 Grid System: chỉ hỗ trợ chủ yếu cho việc chia cột trong wensite

![b](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_22/image/b.png)

Tham khảo và download tài liệu: http://960.gs/

<a name="2.3"></a>
- Purecss: 

![c](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_22/image/c.png)

Tham khảo và download tài liệu: http://purecss.io/

Tương tự như bootstrap nhưng nhẹ hơn, vẫn hỗ trợ các thành phần chủ đạo bên trong website, cách sử dụng đơn giản hơn so với Bootstrap

<a name="2.4"></a>
- Golden grid system: 

![d](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_22/image/d.png)

Cũng giống như 960Grid, Golden Grid System là một hệ thống grid system hỗ trợ bạn chia cột dễ dàng và có hỗ trợ Responsive.( hỗ trợ hiển thị trên các trình duyệt di động)

Tham khảo: http://www.vfinspections.com/ggs/goldengridsystem.com/

<a name="2.5"></a>
- Foundation: 

![e](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_22/image/e.png)

Cũng giống như Bootstrap, Foundation có hỗ trợ các thành phần bên trong website, bên cạnh đó còn hỗ trợ kiểu menu dành cho di động khá đẹp và dễ sử dụng, nó cũng hỗ trợ nhiều hiệu ứng javascrip.

Tham khảo: http://foundation.zurb.com/

<a name="3"></a>
####3. Cách sử dụng:

Cách sử dụng Framework là đọc tài liệu hướng dẫn sử dụng thật kĩ, thêm các Class tương ứng, với các chức năng cần sử dụng vào phần tử style. Các bước thực hiện như sau:

- Tải bộ framework về máy, nó sẽ bao gồm các file CSS và Javascript và một tài liệu HTML mẫu.

- Sau đó bạn tiến hành nhúng các file CSS của framework đó vào tài liệu bạn cần thiết kế với thẻ `<link>`.

- Cuối cùng là thêm class của framework vào các phần tử muốn sử dụng.

Ví dụ: Tạo 1 file html và nhúng trực tiếp các link về hoặc có thể tải về máy.

```
<head>
		<meta charset="utf-8"/>
		<title>Framework</title>
		<link rel="stylesheet" href="http://yui.yahooapis.com/pure/0.6.0/pure-min.css">
		<meta name="viewport" content="width=device-width, initial-scale=1">
	</head>
```

Tham khảo hướng dẫn trong tài liệu và nhúng các đoạn mã vào tài liệu. Sau đó thêm CSS vào tài liệu trực tiếp.

![f](https://github.com/TrinhTu/web_developer/blob/master/Task05_CSS_Course_01/Bai_22/image/f.png)
