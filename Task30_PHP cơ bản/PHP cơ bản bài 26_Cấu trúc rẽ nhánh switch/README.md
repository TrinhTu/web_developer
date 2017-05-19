## PHP CƠ BẢN BÀI 26: CẤU TRÚC RẼ NHÁNH SWITCH

> Tài liệu: Cáu trúc rẽ nhánh Switch
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 19/05/2017

### Mục lục:

[Cấu trúc rẽ nhánh switch](#1)

[Tài liệu tham khảo](#2)

***

<a name="1"></a>
### Cấu trúc rẽ nhánh switch:

- Khai báo switch để bắt các trường hợp của 1 biến.

**Cú pháp cơ bản như sau**:

```javascript
switch (variable) {
		case 'value':
			# code...
			break;
		
		default:
			# code...
			break;
	}
```

- Ví dụ:

```javascript
<?php
	
	$dayOfWeek = 4;

	if ($dayOfWeek == 2) echo 'monday<br />';
	else if ($dayOfWeek == 3) echo 'tuesday<br />';
	else if ($dayOfWeek == 4) echo 'wednesday<br />';
	else if ($dayOfWeek == 5) echo 'thursday<br />';
	else if ($dayOfWeek == 6) echo 'friday<br />';
	else if ($dayOfWeek == 7) echo 'saturday<br />';
	else if ($dayOfWeek == 8) echo 'sunday<br />';
	else echo 'sorry,. not a day of week !<br />';

	switch($dayOfWeek){
		case 2:
			echo 'monday<br />';
			break;
		case 3: 
			echo 'tuesday<br />';
			break;
		case 4:
			echo 'wednesday<br />';
			break;
		case 5: 
			echo 'thursday<br />';
			break;
		case 6:
			echo 'friday<br />';
			break;
		case 7: 
			echo 'saturday<br />';
			break;
		case 8:
			echo 'sunday<br />';
			break;
		
		default:
			echo 'sory. not a day of week !<br />';
			break;
	}
?>
```

<a name="2"></a>
### Tài liệu tham khảo:

> [1] Cấu trúc rẽ nhánh switch. https://www.youtube.com/watch?v=7NCG2IQ7roI&index=30&list=PLuOlFjICKPR6RRl82a8DYGuP1YoJZ9w8L