## PHP CƠ BẢN BÀI 17: TOÁN TỬ TĂNG VÀ GIẢM (INCREMENT AND DECREMENT)

> Tài liệu: Toán tử tăng và giảm (Increment and Decrement)
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 19/05/2017

### Mục lục:

[Toán tử tăng và giảm](#1)

[Tài liệu tham khảo](#2)

***

<a name="1"></a>
### Toán tử tăng và giảm:

- Ví dụ:

```javascript
<?php

	$x = 10;
	echo $x.'<br />';

	$x++;  //$x = $x + 1, $x += 1 => 11
	echo $x.'<br />';

	$y = ++$x; //thực hiện tăng giá trị của biến x trước khi gán giá trị vào biến y => x = 12 -> y = x =12
	$z = $x++;  //z = x = 12, x = 13
	echo $x.', '.$y.', '.$z.'<br />';
	echo $x++.'<br />';  //13 (thực chất x = 14)
	echo $x.'<br />';	//14
	
	$a = 10;
	$b = --$a; //a = 9, b = a =9
	$c = $a--; //c = a = 9, a = 8
	$d = $a-- - --$b + $c--;  //d = 8-8+9 = 9
	echo $a.', '.$b.', '.$c.', '.$d.'<br />'; //7, 8, 8, 9
	echo $a--.'<br />'; //7
	echo $a;  //6
?>
```

<a name="2"></a>
### Tài liệu tham khảo:

> [1] Toán tử tăng và giảm. https://www.youtube.com/watch?v=WqNntgZCEPQ&index=21&list=PLuOlFjICKPR6RRl82a8DYGuP1YoJZ9w8L