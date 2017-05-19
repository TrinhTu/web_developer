## PHP CƠ BẢN BÀI 31: BIẾN TOÀN CỤC VÀ BIẾN CỤC BỘ

> Tài liệu: Biến toàn cục và biến cục bộ
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 19/05/2017

### Mục lục:

[Biến toàn cục và biến cục bộ](#1)

[Tài liệu tham khảo](#2)

***

<a name="1"></a>
### Biến toàn cục và biến cục bộ:

- 2 biến này khác nhau về phạm vi sử dụng của nó trong chương trình:

	+ Biến toàn cục được sử dụng trong toàn bộ chương trình, có thể gọi ra bất cứ lúc nào

	+ Biến cục bộ chỉ được sử dụng trong hàm khai báo nó

	+ Từ khóa để sử dụng biến cục bộ bên ngoài trong hàm: `global ten_bien`

- Ví dụ 1:

```javascript
$a = 5;
	$b = 10;
	$c = 20;

	function something(){
		global $a, $b;
		echo 'a = '.$a ', b = ' .$b. '<br />';
	}

	something();
```

- Ví dụ 2: sử dụng biến môi trường trong php `$GLOBALS[]` biến này chính là 1 mảng

```javascript
$a = 5;
	$b = 10;
	$c = 20;

	function something(){
		$a_temp = $GLOBALS['a']; //biến môi trường, a là chỉ số index cũng chính là tên biến
		$b_temp = $GLOBALS['b'];
		echo 'a = '.$a_temp. ', b = ' .$b_temp.'<br />';  // a=5,b=10
	}

	something();  //không thể sử dụng biến $a_temp bên ngoài hàm
```

<a name="2"></a>
### Tài liệu tham khảo:

> [1] Biến toàn cục và biến cục bộ. https://www.youtube.com/watch?v=uS-HMqiQ1h4&index=35&list=PLuOlFjICKPR6RRl82a8DYGuP1YoJZ9w8L