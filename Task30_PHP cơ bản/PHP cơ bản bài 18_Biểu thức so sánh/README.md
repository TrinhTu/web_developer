## PHP CƠ BẢN BÀI 18: BIỂU THỨC SO SÁNH

> Tài liệu: Biểu thức so sánh
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 19/05/2017

### Mục lục: 

[Biểu thức so sánh](#1)

[Tài liệu tham khảo](#2)

***

<a name="1"></a>
### Biểu thức so sánh:

- Các biểu thức so sánh: +, -. *, /

- Ví dụ:

```javascript
<?php
	
	$a = 10;
	$b = 20;

	$x = true;
	$y = false;

	if ($a ==$b){
		echo 'a = b<br />';
	} else {
		if ($a > $b) echo 'a > b<br />';
		else echo 'a < b<br />';
	}

	if ($a >= $b) echo 'a >= b<br />';
	else echo 'a < b<br />';

	if ($x) echo 'a is true<br />';
	else echo 'a is false<br />';
	
	if (!$y) echo 'y is false<br />';
	else echo 'y is true<br />';

	if ($a) echo 'a != 0<br />';
	else echo 'a = 0<br />';

	if ($a != $b) echo 'a != b<br />';
	else echo 'a == b<br />';
?>
```

<a name="2"></a>
### Tài liệu tham khảo:

> [1] Biểu thức so sánh. https://www.youtube.com/watch?v=gIL1iGzlS2o&index=22&list=PLuOlFjICKPR6RRl82a8DYGuP1YoJZ9w8L