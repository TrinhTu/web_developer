## PHP CƠ BẢN BÀI 24: VÒNG LẶP FOR

> Tài liệu: Vòng lặp for
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 19/05/2017

### Mục lục:

[Vòng lặp for](#1)

[Tài liệu tham khảo](#2)

***

<a name="1"></a>
### Vòng lặp for:

- Vòng lặp for ta có thể biết trước được số lần lặp của vòng lặp.

- Ví dụ:

```javascript
<?php
	
	$so_qua_tao = 10;

	for ($i = 0; $i < $so_qua_tao; $i+=2){
		echo 'hien tai toi dang co '.$i.' qua tao<br />';
	}

	for ($i = $so_qua_tao; $i >= 0; $i-=2){
		if ($i == 0) echo 'toi khong con tao !!!<br />';
		else {
		echo 'so qua tao toi dang co '.$i.' qua tao<br />';
		}
	}
?>
```

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task30_PHP_Course_01/image/8.png"/></p>

<a name="2"></a>
### Tài liệu tham khảo:

> [1] Vòng lặp for. https://www.youtube.com/watch?v=4k95P7qikzw&index=28&list=PLuOlFjICKPR6RRl82a8DYGuP1YoJZ9w8L