## PHP CƠ BẢN BÀI 9+10: ECHO/PRINT MÃ HTML

> Tài liệu: echo/print mã html
> 
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 17/05/2017

### Mục lục:

[echo/print mã html](#1)

[Tài liệu tham khảo](#2)

***

<a name="1"></a>
### echo/print mã html:

- **Ví dụ 1**:

```javascript
<!DOCTYPE html>
<html>
<head>
	<title>PHP basic</title>
</head>
<body>
	<?php
		$name = "PHP";
		echo '<p>This is <strong>bold</strong> text, <em>italic</em> text and '.$name.' some span tag in <span id ="spanTag">here</span>.</p>';
	?>
</body>
</html>
```

- Ở ví dụ trên code php được nhúng trực tiếp vào trang html, có thể đặt tại bất kì vị trí nào trong trang.

- **Ví dụ 2**:

```javascript
<?php
	$a = 2;
	if ($a == 2){
		echo '<strong>'.$a.'</strong>';
	}
	else {
		echo 'Nothing in here';
	}
?>
```

- Chúng ta có thể sử dụng dấu nháy đơn hoặc nháy kép để khai báo biến.

<a name="2"></a>
### Tài liệu tham khảo:

> [1] echo/print mã html. https://www.youtube.com/watch?v=cZfgcnPGDnE&list=PLuOlFjICKPR6RRl82a8DYGuP1YoJZ9w8L&index=13