## PHP CƠ BẢN BÀI 21: HÀM DIE VÀ EXIT

> Tài liệu: Hàm die và exit
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 19/05/2017

### Mục lục:

[Hàm die và exit](#1)

[Tài liệu tham khảo](#2)

***

<a name="1"></a>
### Hàm die và exit:

- Hàm die và exit dùng để ngắt quảng chương trình khi gặp phải sự cố ngoài ý muốn, nó sẽ đưa ra các dòng báo lỗi, đóng tất cả kết nối mà chương trình đang sử dụng, giải phóng tài nguyên.

- Ví dụ 1:

```javascript
<?php
	
	$a = 10;
	echo 'a = '.$a.'<br />';
	die("Khong the ket noi toi database"); // dừng không thực thi các hàm bên dưới
	//tương tự như hàm die ta sử dụng hàm exit();

	$b = $a ;
	echo 'b = a ='.$b.'<br />';
?>
```
- Ví dụ 2:

```javascript
<?php
	mysqli_connect("localhost", "root", "") or die("Can't connect to database");	
?>
```

<a name="2"></a>
### Tài liệu tham khảo:

> [1] Hàm die và exit. https://www.youtube.com/watch?v=6M0gdyGZSnQ&index=25&list=PLuOlFjICKPR6RRl82a8DYGuP1YoJZ9w8L