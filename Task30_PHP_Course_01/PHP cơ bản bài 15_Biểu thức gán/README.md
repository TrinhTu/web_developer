## PHP CƠ BẢN BÀI 15: BIỂU THỨC GÁN

> Tài liệu: Biểu thức gán
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 19/05/2017

### Mục lục:

[Biểu thức gán](#1)

[Tài liệu tham khảo](#2)

***

<a name="1"></a>
### Biểu thức gán:

- **Ví dụ**:

```javascript
<?php
	$x = 15;
	$y = 7;

	$z = $x + $y; //22
	echo $z. '<br />';
	$z += $y; // $z = $z + $y //29
	echo $z. '<br />';
	$z -= $x; //14
	echo $z. '<br />';
	$z *= ($x + $y); //14*22 = 308
	echo $z. '<br />';
	$z /= ($y - $x); //308 / -8 = -38.5
	echo $z. '<br />';
	$z %= ($x % $y); // -38.5 % 1 = 0

	echo $z; 
?>
```

<a name="2"></a>
### Tài liệu tham khảo:

> [1] Biểu thức gán. https://www.youtube.com/watch?v=uWWA7dpNE2I&index=19&list=PLuOlFjICKPR6RRl82a8DYGuP1YoJZ9w8L