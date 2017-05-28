## PHP CƠ BẢN BÀI 22: VÒNG LẶP DO WHILE

> Tài liệu: Vòng lặp do while
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 19/05/2017

### Mục lục:

[Vòng lặp do while](#1)

[Tài liệu tham khảo](#2)

***

<a name="1"></a>
### Vòng lặp do while:

- Ví dụ 1:

```javascript
<?php
	
	$so_qua_tao = 10;

	do {
		$so_qua_tao--;
		echo 'Toi da an 1 qua tao va con lai '.$so_qua_tao.'<br />';
	}	while ($so_qua_tao > 0);
?>
```

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task30_PHP%20c%C6%A1%20b%E1%BA%A3n/image/5.png"/></p>

- Vòng lặp do while sẽ thực hiện `do` trước rồi mới xét tới điều kiện `while`

- Ví dụ 2:

```javascript
$so_qua_tao = 0;
	do {
		echo 'hien tai toi dang co '.$so_qua_tao.' qua tao<br />';
		$so_qua_tao++;
	} while ($so_qua_tao < 10);
```
<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task30_PHP%20c%C6%A1%20b%E1%BA%A3n/image/6.png"/></p>

<a name="2"></a>
### Tài liệu tham khảo:

> [1] Vòng lặp do while. https://www.youtube.com/watch?v=izjKFXnq3pI&list=PLuOlFjICKPR6RRl82a8DYGuP1YoJZ9w8L&index=26