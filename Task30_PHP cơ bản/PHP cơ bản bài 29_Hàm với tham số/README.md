## PHP CƠ BẢN BÀI 29: HÀM VỚI THAM SỐ

> Tài liệu: Hàm với tham số
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 19/05/2017

### Mục lục:

[Hàm với tham số](#1)

[Tài liệu tham khảo](#2)

***

<a name="1"></a>
### Hàm với tham số:

- Tham số của 1 hàm thì giá trị truyền vào cho nó có thể là giá trị của 1 biến, hoặc giá trị cụ thể nào đó. Ở ví dụ dưới đây tham số của hàm là `dow`

```javascript
function detecDayOfWeek($dow){
		switch($dow){
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
				echo 'sorry. not a day of week !<br />';
				break;
		}
	}

	$dayOfWeek = 2;
	detecDayOfWeek($dayOfWeek);
	detecDayOfWeek(7);
	detecDayOfWeek(6);
	detecDayOfWeek(5);
	detecDayOfWeek(4);
	detecDayOfWeek(20);
```

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task30_PHP%20c%C6%A1%20b%E1%BA%A3n/image/10.png"/></p>

<a name="2"></a>
### Tài liệu tham khảo:

> [1] Hàm với tham số. https://www.youtube.com/watch?v=LQ6CuwKTO3E&list=PLuOlFjICKPR6RRl82a8DYGuP1YoJZ9w8L&index=33