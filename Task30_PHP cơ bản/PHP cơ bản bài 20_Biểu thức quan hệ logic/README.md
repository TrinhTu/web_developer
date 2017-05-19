## PHP CƠ BẢN BÀI 20: BIỂU THỨC QUAN HỆ (LOGIC)

> Tài liệu: Biểu thức quan hệ (logic)
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 19/05/2017

### Mục lục:

[Biểu thức quan hệ (logic)](#1)

[Tài liệu tham khảo](#2)

***

<a name="1"></a>
### Biểu thức quan hệ (logic):

- Biểu thức logic dùng để kết hợp các điều kiện lại với nhau trong khi chúng ta xét đến 1 điều kiện

- Ví dụ:

```javascript
<?php
	
	$a = 10;
	$b = 20;

	$x = true;
	$y = false;

	if ($a == $b || $x)  // || <=> or
		echo 'a = b or x is true<br />';  // biểu thức 1 sai, biểu thức 2 đúng  -> biểu thức đúng

	if ($a >= 5 && !$y){
		echo 'a > =5 and y is false<br />';  // biểu thức 1 và 2 đều đúng -> biểu thức đúng
	}

	if (!$a xor $x){
		echo 'true';
	}

?>
```
<a name="2"></a>
### Tài liệu tham khảo:

> [1] Biểu thức quan hệ (logic). https://www.youtube.com/watch?v=VnoFVCmD3bY&index=24&list=PLuOlFjICKPR6RRl82a8DYGuP1YoJZ9w8L