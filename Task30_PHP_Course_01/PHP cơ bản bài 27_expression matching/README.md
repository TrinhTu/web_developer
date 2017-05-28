## PHP CƠ BẢN BÀI 27: EXPRESSION MATCHING

> Tài liệu: Expression Matching
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 19/05/2017

### Mục lục:

[expression matching](#1)

[Tài liệu tham khảo](#2)

***

<a name="1"></a>
### expression matching:

- expression matching (tính hợp lệ của dữ liệu)

- Ví dụ tìm kiếm 1 chữ hoặc 1 từ xem có xuất hiện trong chuỗi:

```javascript
$str = 'I want to sing a song';

	if (preg_match('/sing/', $str)) {
		echo 'Found it';
	} else {
		echo 'Not found';
	}
```

- Tìm kiếm trong chuỗi có xuất hiện dãy chữ số [0-9]:

```javascript
$str = 'I want to sing a song';

	if (preg_match('/[0-9]/', $str)) {
		echo 'Found it';
	} else {
		echo 'Not found';
	}
```

- Kiểm tra trong chuỗi kí tự bắt đầu chuỗi có nằm trong dãy [a-zA-Z] hay không:

```javascript
$str = 'I want to sing a song';

	if (preg_match('/^[a-zA-Z]/', $str)) {
		echo 'Found it';
	} else {
		echo 'Not found';
	}
```

<a name="2"></a>
### Tài liệu tham khảo:

> [1] expression matching. https://www.youtube.com/watch?v=SocbGKqQWR0&list=PLuOlFjICKPR6RRl82a8DYGuP1YoJZ9w8L&index=31