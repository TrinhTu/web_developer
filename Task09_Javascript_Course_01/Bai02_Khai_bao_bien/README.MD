##BÀi 2: Biến và khai báo biến trong Javascrip

>Tài liệu: Biến và khai báo biến trong Javascrip
>
>Người thực hiện: Lê Tú Trinh
>
>Cập nhập lần cuối: 11/11/2016

###Mục lục

[1. Khai báo biến trong javascrip](#1)

[2. Gán giá trị cho biến](#2)

[3. Gán kiểu giá trị cho biến](#3)

[4. In giá trị của biến ra trình duyệt](#4)

###Nội dung:

<a name="1"></a>
####1. Khai báo giá trị cho biến trong javascrip:

Để khai báo 1 biến ta sử dụng từ khóa `var tenbien` :

```
		**var** username;
```

Tên biến được đặt theo quy tắc sau đây:

- Tên biến phải là các chữ viết hoa không dấu hoặc viết thường, các chữ số từ 0-9, dấu gạch dưới (_)

- Tên biến bắt đầu là chữ hoặc dấu gạch dưới, không được bắt đầu là số

- Tên biến có thể dài hay ngắn tùy người đặt


Ví dụ: 

```
var username;
var _username;
var username10;
```

Ngoài ra còn có thể khai báo liên tiếp cách nhau bởi dấu phẩy:

```
	var username, _username, __username, username10;
```

<a name="2"></a>
####2. Gán giá trị cho biến:

Ta sử dụng dấu (=) để gán giá trị cho biến. Có 2 cách gán thông dụng đó là:

- Vừa khai báo vừa gán giá trị: `var username = 'tutrinh';`

- Khai báo xong mới gán giá trị:

```
var username;
username ='tutrinh';
```


<a name="3"></a>
####3. Gán kiểu giá trị cho biến:

Dựa vào giá trị của biến để xác định xem biến có kiểu dữ kiệu gì. Ví dụ:

```
//Biến kiểu giá trị string
var website ="tutrinh";

//Biến kiểu giá trị INT
var website =12;

//Biến kiểu float
var website = 10.5;
```

Trong javascrip có những kiểu dữ liệu thông dụng như sau: kiểu chuỗi(String), số (number), mảng(Array), đối tượng (Object).
<a name="4"></a>
####4. In giá trị của biến ra trình duyệt:

Để in giá trị của biến hoặc chuỗi ra trình duyệt sử dụng hàm `document.write(value)`

Ví dụ:

```
<html>
	<head>
		<title>Trinh</title>
	</head>
	<body>
		<script language="javascript">
			var name = 'TuTrinh';
			document.write(name);	
		</script>
	</body>
</html>
```
Để kiểm tra kiểu giá trị cho biến sử dụng hàm `typeof` tên biến. Ví dụ:

```
<html>
	<head>
		<title>Web</title>
	</head>
	<body>
		<script language="javascript">
			var name=1234.5;
			document.write( typeof name);	
		</script>
	</body>
</html>
```

![anh](http://i.imgur.com/zfjs5AC.png)
