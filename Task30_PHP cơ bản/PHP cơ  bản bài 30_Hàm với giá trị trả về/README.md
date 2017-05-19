## PHP CƠ BẢN BÀI 30: HÀM VỚI GIÁ TRỊ TRẢ VỀ

> Tài liệu: Hàm với giá trị trả về
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 19/05/2017

### Mục lục:

[Hàm với giá trị trả về](#1)

[Tài liệu tham khảo](#2)

***

<a name="1"></a>
### Hàm với giá trị trả về:

- Ví dụ:

```javascript
function add($a, $b){
		$c = $a + $b;
		return $c;
	}
	function concatStr($str1, $str2){
		$str = $str1.$str2;
		return $str;
	}
	
	$d = add (8, 8);
	echo $d.'<br />';

	$s = concatStr("I'm a robot", "I'm a student");
	echo $s;
```

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task30_PHP%20c%C6%A1%20b%E1%BA%A3n/image/11.png"/></p>

<a name="2"></a>
### Tài liệu tham khảo:

> [1] Hàm với giá trị trả về. https://www.youtube.com/watch?v=x3hSEesM3dc&list=PLuOlFjICKPR6RRl82a8DYGuP1YoJZ9w8L&index=34&spfreload=10