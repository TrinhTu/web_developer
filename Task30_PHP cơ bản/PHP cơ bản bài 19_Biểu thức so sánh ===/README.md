## PHP CƠ BẢN BÀI 19: BIỂU THỨC SO SÁNH ===

> Tài liệu: Biểu thức so sánh ===
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 19/05/2017

### Mục lục:

[Biểu thức so sánh ===](#1)

[Tài liệu tham khảo](#2)

***

<a name="1"></a>
### Biểu thức so sánh ===:

- Biểu thức === so sánh về giá trị và kiểu dữ liệu của biến đó

- Khi sử dụng biểu thức 2 dấu = thì sẽ tự động chuyển kiểu dữ liệu của biến được so sánh về cùng kiểu dữ liệu của biến so sánh

- Ví dụ:

```javascript
<?php
	
	$a = 10;
	$b = '10';
	$c = 10;

	$x = true;
	$y = 'true';
	$z= true;

	// == and !=
	if ($x == $y) echo 'x == y<br />';  //x == y
	else echo 'x != y<br />';

	// === and !==
	if ($a === $b) echo 'a === b<br />';
	else echo 'a !== b<br />';    //a !== b

	if ($x === $z) echo 'x === z<br />';   //x === z
	if ($a === $c) echo 'a === c<br />';   //a ===c
?>
```

<a name="2"></a>
### Tài liệu tham khảo:

> [1] Biểu thức so sánh ===. https://www.youtube.com/watch?v=IwWrEqeYUi4&list=PLuOlFjICKPR6RRl82a8DYGuP1YoJZ9w8L&index=23