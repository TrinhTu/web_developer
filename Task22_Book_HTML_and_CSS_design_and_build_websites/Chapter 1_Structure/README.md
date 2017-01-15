## HTML & CSS
### Structure

> Chương 1: Cấu trúc
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 09/01/2017

## Mục lục:

[1. Hiểu về cấu trúc](#1)

[2. Học về đánh dấu](#2)

[3. Thẻ và các yếu tố](#3)

***

<a name="1"></a>
### 1. Hiểu về cấu trúc:

- Cấu trúc của 1 trang web:

	+ Nhiều trang web hoạt động như là các tài liệu điện tử. Trong hầu hết các tài liệu thì cấu trúc là phần quan trọng nhất giúp cho người đọc hiểu được nội dung và thông điệp bạn muốn truyền tải. Vì vậy, để viết được 1 trang Web thì ta cần tìm hiểu cấu trúc của nó:

		+ Tìm hiểu về HTML để mô tả cấu trúc của 1 trang web

		+ Tìm hiểu về các thẻ tags và các yếu tố được thêm vào trong tài liệu.

		+ Viết trang web đầu tiên

	- Một tờ báo hay 1 câu chuyện thì đều gồm có tiêu đề, nội dung cụ thể, và ngoài ra còn có thêm hình ảnh. Nếu bài viết phân ra thành nhiều nội dung cụ thể thì có thể sử dụng chú thích, trích dẫn có liên quan. Cấu trúc góp phần giúp cho người đọc hiểu được nội dung của tài liệu.

	- Cấu trúc của tài liệu thường gồm các tiêu đề, trong mỗi tiêu đề sẽ chứa khu vực nội dung, câu hỏi,...

- Cấu trúc của chữ trong tài liệu:

	+ Cách sử dụng tiêu đề và phân nhóm tiêu đề con theo 1 thứ tự phân cấp giảm dần. Ví dụ: Tiêu đề của bài viết sẽ có kích thước lớn nhất, và các mục quan trọng sẽ có kích thước tiêu đề giảm dần. Mỗi tiêu đề như vậy sẽ gồm các đoạn văn mô tả biểu thị nội dung muốn thể hiện.

	+ Chúng ta sẽ sử dụng cấu trúc tương tự như trong Word để thêm tiêu đề cho tài liệu.

<a name="2"></a>
### 2. Học về đánh dấu:

- HTML dùng để mô tả cấu trúc của 1 trang web. Trong đoạn code dưới đây thì mã HTML được đặt trong dấu `<>` và nó sẽ không được hiển thị ra ngoài trình duyệt, còn đoạn văn bản hiển thị thì sẽ được đặt trong các cặp thẻ HTML.

```javascript
<html>
<body>
<h1>Đây là tiêu đề chính</h1>
<p>Đoạn văn bản sau đây giới thiệu sơ qua nội dung chính của trang còn nội dung chi tiết sẽ thể hiện trong các tiêu đề con<p>
<h2>Đây là tiêu đề con</h2>
<p>Đây là nội dung chứa bên trong tiêu đề con</p>
</html>
```

- Mỗi phần tử HTML được tạo thành đều gồm có 1 thẻ mở và 1 thẻ đóng, mỗi phần tử HTML đều nhằm mục đích cung cấp cho trình duyệt những thông tin nằm trong cặp thẻ đó.

- Thuộc tính về các thành phần: 

	+ Thuộc tính cung cấp thêm nội dung cho 1 phần tử, được sử dụng trong các thẻ mở đầu bao gồm 2 yếu tố là tên thuộc tính (name) và giá trị của thuộc tính (value) cách nhau bởi dấu bằng.

	**Ví dụ**:

	`<p lang="vi">Văn bản</p>`

	+ Trong đó thì tên của thuộc tính dùng để chỉ ra thông tin cần thêm vào và được viết bằng chữ thường (trong HTML5 cho phép sử dụng tên thuộc tính viết bằng chữ in hoa)

	+ Giá trị là thông tin được gán cho thuộc tính đó, được đặt trong dấu ngoặc kép 

<a name="3"></a>
### 3. Thẻ và các yếu tố:

- Body, Head & Title:

	+ Tất cả nội dung được đặt trong thẻ `<body>` sẽ được hiển thị trên trình duyệt.

	+ Thẻ `<head>` được đặt trước thẻ `<body>`, chứa thông tin về trang web, bao gồm thuộc tính `<title>`

	+ Thẻ `<title>`: Nội dung bên trong thẻ `<title>` sẽ hiển thị trên cùng trình duyệt, nơi chứa URL của trang web bạn muốn truy cập

- HTML là ngôn ngữ dùng để đánh dấu văn bản, có nghĩa là cho phép người sử dụng tạo ra các liên kết truy cập đến 1 trang web khác 1 cách dễ dàng. Ngôn ngữ đánh dấu cho phép chú thích văn bản, thêm code vào xung quanh nội dung của văn bản gốc mà trình duyệt có thể hiểu được và hiển thị trang đó 1 cách chính xác.

- Tạo ra 1 trang web trên PC:

	+ Chúng ta có thể tạo ra 1 trang web trên PC bằng nhiều công cụ: Sublime Text, Notepad ++, ...

	+ Viết 1 đoạn code đơn giản. Lưu lại với đuôi `.html`

```javascript
<!DOCTYPE html>
<html lang=vi>
	<head>
		<title>PC</title>
		<meta charset="utf-8"
	</head>
	<body>
		<h1>Tiêu đề</h1>
		<p>Nội dung</p>
	</body>
</html>
```

- Sau đó dùng 1 trình duyệt bất kì để chạy được nó.

- Tạo ra 1 trang web trên MAC:

	+ Sử dụng TextEdit nằm trong phần ứng dụng. Hoặc có thể tải miễn phí text editor để tạo trang web gọi là TextWrangler tại `barebones.com`.

	+ Cũng tương tự như trên PC, cần lưu file lại với đuôi `.html`

	+ Vào trình duyệt và mở.

- Mã nội dung quản lí hệ thống:

	+ Nếu muốn làm việc với nội dung quản lí hệ thống, viết blog bạn phải đăng nhập vào quản trị đặc biệt của trang web đó để kiểm soát nó. Các công cụ cho phép chỉnh sửa các bộ phận của trang

	+ Việc thay đổi nội dung từng phần sẽ dễ dàng việc thay đổi toàn bộ trang. Trong 1 hệ thống, khi có 1 văn bản có nội dung lớn cần chỉnh sửa, bạn sẽ mở trình soạn thảo văn bản lên, có rất nhiều lựa chọn khác nhau: như thêm nội dung, hình ảnh, liên kết...

	+ Có 1 số trang mà các quản trị viên sẽ cho phép mình sử dụng 1 số tùy chọn: xem, chỉnh sửa các mã code của họ...

- Cách nhìn khác về xây dựng 1 trang web:

	+ Khi nói về 1 trang web cách phổ biến để tìm hiểu về HTML và khám phá các kĩ thuật mới là nhìn vào mã nguồn tạo nên trang web. Ngày nay thì có nhiều sách và các hướng dẫn trực tuyến dạy về HTML, nhưng chúng ta vẫn có thể nhìn vào mã nguồn mà 1 trang web máy chủ sẽ gởi cho bạn. Để biết mã nguồn của trang web đó ta có thể kiểm tra bằng cách **View Source**.

