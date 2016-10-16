###Bài 3: Cấu trúc một tài liệu Web bằng HTML

> Tài liệu: Cấu trúc một tài liệu Web bằng HTML
> 
> Thực hiện: **Lê Tú Trinh**
> 
> Cập nhật lần cuối: **14/10/2016**

####Mục lục

[1. Thẻ khai báo loại tập tin](#the01)

[2. Thẻ đóng mở tài liệu HTML](#the02)

[3. Thẻ đóng và mở phần thông tin Website](#the03)

[4. Thẻ đóng và mở phần nội dung Website](#the04)

###Nội dung

<a name="the01"></a>
####1. Thẻ khai báo loại tập tin
Thẻ đầu tiên trong tài liệu Website bằng HTML là thẻ `<!DOCTYPE>`  và thẻ này có một thuộc tính là HTML, đây không phải là một thẻ HTML mà chỉ là giúp cho trình duyệt hiểu rằng đây là tài liệu bằng HTML

			 <!DOCTYPE html>
**html** này là phiên bản HTML5
<a name="the02"></a>
####2. Thẻ đóng mở tài liệu HTML

- Kế tiếp ở hàng tiếp theo là cặp thẻ `<html>` `</html>` bao bọc toàn bộ nội dung của Website mà không bao gồm thẻ `<!DOCTYPE html>` . Thẻ này có ý nghĩa là khai báo cho trình duyệt biết rằng toàn bộ nội dụng bên trong cặp thẻ là HTML

- Trong thẻ này có những tham số mà tham số mà hay sử dụng nhất đó là tham số **lang** có nghĩa là *language* mà giá trị của nó là mã ngôn ngữ mà bạn chọn để viết. Nếu như viết tài liệu này băng tiếng việt thì mã ngôn ngữ sẽ là **vi**

![anh](http://imageshack.com/a/img922/3595/8fdkJv.png)

- Ngoài ra còn có thể tham khảo thêm 1 số mã ngôn ngữ khác [tại đây](https://webvn.com/ma-ngon-ngu-theo-chuan-iso/)

<a name="the03"></a>
####3. Thẻ đóng mở phần thông tin Website

Tiếp theo nữa đó là thẻ `<head>` thẻ này cũng có thẻ đóng là `</head>` nằm trong cặp thẻ `<html>`  `</html>` dùng để khai báo 1 số thông tin về tài liệu website của bạn. Thẻ `<head>` này sẽ chứa nhưng thông tin của website mà không hiển thị ra màn hình nhưng có nhiệm vụ chứa các thông tin quan trọng về website. Trong thẻ này chứa những thẻ khác như là:

- Thẻ `<title>` thẻ này cũng có thẻ đóng `</title>`: dùng để khai báo tên Website.

- Thẻ `<meta>` thẻ này không có thẻ đóng có thuộc tính là khai báo bảng mã để sử dụng.
	
*Về nội dung cũng như thuộc tính của 2 thẻ trên sẽ được nói rõ hơn trong bài sau*

![anh](http://imageshack.com/a/img922/3391/BOMZev.png)
<a name="the04"></a>
####4. Thẻ đóng và mở phần nội dung Website

Đây là cặp thẻ bạn có thể tiến hành viết nội dung vào đó `<body>` `</body>` thẻ này sẽ chứa toàn đoạn văn bản nằm trong nội dung website của bạn. Với tài liệu HTML được mở bằng trình duyệt thì chỉ có thể thấy nội dung nằm bên trong thẻ body thôi nếu viết bên ngoài thẻ `<body>` `</body>` thì sẽ không thể hiển thị được.

![anh](http://imageshack.com/a/img924/1276/McMVy0.png)


