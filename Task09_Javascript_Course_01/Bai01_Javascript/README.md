##BÀi 1: Javascript là gì? Viết ứng dụng JS đầu tiên

>Tài liệu: Javascript là gì, viết ứng dụng JS
>
>Người thực hiện: Lê Tú Trinh
>
>Cập nhập lần cuối: 11/11/2016

###Mục lục:

[1. Javascrip là gì?](#1)

[2 Các thư viện Javascrip](#2)

[3. Viết chương trình Javascrip đầu tiên](#3)

###Nội dung:

<a name="1"></a>
####1. Javascrip là gì?

Javascrip là ngôn ngữ lập trình kịch bản dựa vào đối tượng phát triển có sẵn hoặc tự định nghĩa ra, được sử dụng rộng rãi trong ứng dụng của các website. Javascrip hỗ trợ hầu như trên mọi trình duyệt có cả trình duyệt trên thiết bị di động.

<a name="2"></a>
####2. Các thư viện Javascrip:

Các thư viện, Framework:

- AngularJS: thư viện dùng để xây dựng ứng dụng Single Page

- NodeJS: thư viện được phát triển phía Server dùng để xây dựng ứng dụng realtime

- Sencha Touch: Framework  dùng để xây dựng ứng dụng Mobile

- ExtJS: Framework dùng xây dựng ứng dụng quản lý (Web Applications)

- jQuery: thư viện rất mạnh về hiểu ứng

<a name="3"></a>
####3. Viết chương trình Javascrip đầu tiên:

Tất cả những đoạn mã Javascrip đều phải được đặt trong cặp thẻ `<script>` 

```
<script language="javascript">
	alert("Hello World!");
</script>
```
Có 2 cách đặt thẻ javasrcip:

- Internal- viết trong file html hiện tại:

Chúng ta có thể đặt các đoạn mã javascrip ở bất cứ chỗ nào miễn sao nó đc bao bọc bởi cắp thẻ `scrip` là được. Ví dụ ở đây ta có đoạn javascrip được đặt trong thẻ body như sau:

```
<html>
	<head>
		<tille>web</tille>
		<meta charset="utf-8"/>
	</head>
	<body>
		<script language="javascript">
			alert("Click me now!")
		</script>
	</body>
</html>
```

Ta sẽ thấy hiển thị như sau:

![1](https://github.com/TrinhTu/web_developer/blob/master/Task09_Javascript_Course_01/Bai01_Javascript/image/1.png)

- Inline - viết trực tiếp trong thẻ HTML:

Tức là sẽ tạo 1 button chứa nội dung trong đó khi click vào sẽ hiển thị ra.

```
<input type="buton" onclick="alert(1)" value="Click me"/>
```
Ví dụ:

```
<!DOCTYPE html>
<html lang="vi">
	<head>
		<title>Web</title>
		<meta charset="utf-8"/>
	</head>
	<body>
		<input type="button" id="clickme" value="Click me"/>
		 <script language="javascript">
        var button = document.getElementById('clickme');
        button.addEventListener('click', function(){
            alert('Hello World!');
        });
        </script>
	</body>
	
</html>
```

![2](https://github.com/TrinhTu/web_developer/blob/master/Task09_Javascript_Course_01/Bai01_Javascript/image/2.png)
