## PHP CƠ BẢN BÀI 13: BIỂU THỨC ĐIỀU KIỆN IF ELSE

> Tài liệu: Biểu thức điều kiện if else
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 19/05/2017

### Mục lục:

[Biểu thức điều kiện if else](#1)

[Tài liệu tham khảo](#2)

***

<a name="1"></a>
### Biểu thức điều kiện if else:

- Ví dụ 1:

```javascript
<?php
$a = 2;
if ($a == 2)
	echo 'Right';
?>
```

- Khi có nhiều hơn 1 dòng lệnh trong biểu thức `if` phải khai báo trong 1 cặp dấu `{}`.

- Ví dụ 2:

```javascript
<?php
$a = 5;
if ($a == 2){
	echo 'Right';
}
else {
	echo 'Wrong !!!';
}
?>
```
- `else` là ngược lại của biểu thức `if`, nếu biểu thức if sai thì nó sẽ thực thi dòng lệnh biểu thức else.

- Ví dụ 3:

```javascript
<?php
$a = 5;
$b = 10;

if ($a == 2){
	echo 'Right';
}
else {
	echo 'Wrong !!!';

	if ($b == 10){
		echo 'true';
	} else {
		echo 'false';
	}
}
?>
```
<a name="2"></a>
### Tài liệu tham khảo:

> [1] Biểu thức điều kiện if else. https://www.youtube.com/watch?v=LYpfUzTrIH0&list=PLuOlFjICKPR6RRl82a8DYGuP1YoJZ9w8L&index=17