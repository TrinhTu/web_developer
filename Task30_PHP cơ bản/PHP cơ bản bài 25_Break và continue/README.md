## PHP CƠ BẢN BÀI 25: BREAK VÀ CONTINUE

> Tài liệu: Break và continue
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 19/05/2017

### Mục lục:

[Break và continue](#1)

[Tài liệu tham khảo](#2)

***

<a name="1"></a>
### Break và continue:

- Continue bỏ qua trường hợp mà ta xét tới nó

- Break hoạt động tương tự như `continue` nhưng khác ở chỗ nó sẽ ngắt luôn vòng lặp

- Ví dụ:

```javascript
<?php
	
	$a = 10;
	$b =4;

	do {
		$a--;
		if ($a == $b) break;
		echo $a.'<br />';
	} while ($a > 0);
	
/*
	do {
		$a--;
		if ($a == $b) continue;
		echo $a.'<br />';
	} while ($a > 0);
*/
?>
```

<a name="2"></a>
### Tài liệu tham khảo:

> [1] Break và continue. https://www.youtube.com/watch?v=CBvEHLeg0MM&list=PLuOlFjICKPR6RRl82a8DYGuP1YoJZ9w8L&index=29