## PHP CƠ BẢN BÀI 23: VÒNG LẶP WHILE

> Tài liệu: Vòng lặp while
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 19/05/2017

### Mục lục:

[Vòng lặp while](#1)

[Tài liệu tham khảo](#2)

***

<a name="1"></a>
### Vòng lặp while:

- Sự khác nhau giữa vòng lặp `while` và `do while`

	+ `do while` thực hiện trước rồi mới kiểm tra điều kiện, do while sẽ thực hiện ít nhất là 1 lần lặp

	+ `while` kiểm tra điều kiện trước sau đó mới thực hiện, nếu điều kiện đầu tiên là sai thì nó sẽ không thực hiện

- Ví dụ:

```javascript
$so_qua_tao = 10;
	while ($so_qua_tao > 20){
		$so_qua_tao--;
		echo 'toi da an mot qua tao va con lai '.$so_qua_tao.'<br />';	
	}
$so_qua_tao = 0;
	while ($so_qua_tao < 10){
		echo 'hien tai toi dang co '.$so_qua_tao.'<br />';
		$so_qua_tao++;
	}
```

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task30_PHP_Course_01/image/7.png"/></p>

- Cần phải có biểu thức điều kiện để dừng vòng lặp nếu không nó sẽ lặp vô hạn.

<a name="2"></a>
### Tài liệu tham khảo:

> [1] Vòng lặp while. https://www.youtube.com/watch?v=ZYDBpu2f2Fw&index=27&list=PLuOlFjICKPR6RRl82a8DYGuP1YoJZ9w8L