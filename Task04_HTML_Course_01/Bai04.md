###Bài 3: Các thẻ khai báo thông tin Web cơ bản

> Tài liệu: Các thẻ khai báo thông tin Web cơ bản
> 
> Thực hiện: **Lê Tú Trinh**
> 
> Cập nhật lần cuối: **14/10/2016**

####Mục lục

[1. Khai báo tên tài liệu với cặp thẻ `<title>`](#khaibao1)

[2. Khai báo dữ liệu vĩ mô với thẻ `<meta>`](#khaibao2)

###Nội dung

<a name="khaibao1"></a>
####1. Khai báo tên tài liệu với cặp thẻ `<title>`:
Thẻ `<title>` `</title>` có tác dụng giúp khai báo tên tài liệu web bạn đang soạn,  có nghĩa là giúp trình duyệt hiển thị tên tài liệu khi mở lên. Thực hiện bằng cú pháp như sau:

```
<title>Lê Tú Trinh</title>
```
Trong cặp thẻ đó là tên sẽ hiển thị lên khi mở bằng trình duyệt. Đây là hình ảnh khi demo:

![anh](http://imageshack.com/a/img921/2851/G0VaS2.png)

<a name="khaibao2"></a>
####2. Khai báo dữ liệu vĩ mô với thẻ `<meta>`

- Đối với thẻ `<meta>` thì không có thẻ đóng như các thẻ vừa tìm hiểu nó chỉ có dấu gạch chéo `/` phía trước kí tự `>` cuối cùng. Nó có tác dụng khai báo dữ liệu vĩ mô trong tài liệu web HTML củ bạn mô tả như là từ khóa, tên tác giả, kí tự sử dụng...

- Thẻ meta luôn được khai báo kèm theo ít nhất một thuộc tính, mỗi thuộc tính luôn luôn có giá trị trong đó.

- Thẻ meta có rất nhiều thuộc tính, chẳng hạn như : [charset](#01), [name](#02)

<a name="01"></a>
Thuộc tính **charset**:

Thuộc tính `charset` trong thẻ `<meta>` có tác dụng khai báo bảng mã cho website, và hiện nay thì hầu hết sử dụng bảng mã UTF-8 cho tất cả các ngôn ngữ.
```
<meta charset="utf-8" />
```

<a name="02"></a>
Thuộc tính **name**: có 1 số giá trị như sau

- author: Khai báo tên tác giả của tài liệu, trong này còn có thêm thuộc tính nữa là `content` để khai báo mô tả cho nó, thẻ này thì không có thẻ đóng.

```
<meta name="author" content="Tú Trinh" />
```

- description: khai báo mô tả tài liệu, và cũng có thêm thẻ `content` như `author`

```
<meta name="description" content=" học HTML rất thú vị" />
```

- keyword: khai báo những từ khóa đại diện cho tai liệu này, sau này nó sẽ là công cụ giúp hỗ trợ các trình tìm kiếm văn bản hoặc máy tìm kiếm website dò tìm.

```
<meta name="keyword" content=" hoc html, tu trinh" />
```
Ngoài ra chúng ta còn có thể tìm hiểu thêm các thuộc tính khác của ther`<meta>` tại [meta mozilla developer network](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meta)


Đây là hình ảnh ví dụ cho những thuộc tính đã nói ở trên:

![anh](http://imageshack.com/a/img922/7456/vYbBZ9.png)



