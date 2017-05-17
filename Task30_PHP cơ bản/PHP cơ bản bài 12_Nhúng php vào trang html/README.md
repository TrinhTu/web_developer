## PHP CƠ BẢN BÀI 12: NHÚNG PHP VÀO TRANG HTML

> Tài liệu: Nhúng PHP vào trang html
>
> Người thực hiện: Lê Tú Trinh
> 
> Cập nhập lần cuối: 17/05/2017

### Mục lục:

[Nhúng PHP vào trang html](#1)

[Tài liệu tham khảo](#2)

***

<a name="1"></a>
### Nhúng PHP vào trang html:

```javascript
<?php
	// khoi tao gia tri bien, mang, ket qua, ...
	$name = "trinh";
	$age = 20;

	// xu ly ...
	$name .= "is the nothing in here";
?>
<!DOCTYPE html>
<html>
<head>
	<title>PHP basic</title>
</head>
<body>
	<?php
		// dua ket qua ra man hinh + html format
		echo 'my name:'.$name.'<br />';
		echo 'age:'.$age.'<br />';
	?>
</body>
</html>
<?php
	//huy gia tri bien, mang, ket noi
	//closeConnection();
?>
```

<a name="2"></a>
### Tài liệu tham khảo:

> [1] Nhúng PHP vào trang html. https://www.youtube.com/watch?v=UgJ62SmRooI&list=PLuOlFjICKPR6RRl82a8DYGuP1YoJZ9w8L&index=16