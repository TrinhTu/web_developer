##Bài 6: Vòng lặp for trong javascript

>Tài liệu: Vòng lặp for trong javascript
>
>Người thực hiện: Lê Tú Trinh
>
>Cập nhập lần cuối: 12/11/2016

###Mục lục:

[1. Một số cách sử dụng vòng lặp for](#1)

[2. Lặp vô hạn với vòng lặp for](#2)

[3. Vòng lặp for lồng nhau](#3)

[4. Bài tập thực hành](#4)

###Nội dung:

Vòng lặp for trong javascript dùng để lặp 1 khoảng hoặc 1 mảng nào đó để giải quyết vấn đề cho bài toán. Cấu trúc của vòng lặp for như sau:

```
var i = 0;
for (i = 0; i < 100; i++){
	
}
```
Trong đó:

- `var i = 0`: là khai báo biến điều khiển vòng lặp i

- `(i = 0)` : là điểm bắt đầu vòng lặp, ở đây là lặp từ 0

- `(i < 100)` là điều kiện dừng vòng lặp. Có thể dùng điều kiện khác như `(i<=100, i==100)`

- `(i++)` là tăng bước nhảy


<a name="1"></a>
####1. Một số cách sử dụng vòng lặp for:

- Lặp với bước nhảy tăng lên 1 đơn vị:

```
var i;
for( i = 0; i < 10; i++){
	document.write(i + '<br/>');
}
```

Kết quả trả về như sau:

![a](https://github.com/TrinhTu/web_developer/blob/master/Task09_Javascript_Course_01/Bai06_for/image/a.png)

- Lặp với bước nhảy giảm n đơn vị:

```
	var i;
	var n = 2;
	for(i = 20; i > 0 ; i-=n){
		document.write(i + '<br/>');
	}
```

Ta có kết quả như sau:

![b](https://github.com/TrinhTu/web_developer/blob/master/Task09_Javascript_Course_01/Bai06_for/image/b.png)

Ngoài ra ta còn có thể khai báo biến i bên trong vòng lặp như sau:

```
	for(var i = 0; i < 10; i++){
	document.write(i + '<br/>');
	}
```
<a name="2"></a>
####2. Lặp vô hạn với vòng lặp for:

Khi sử dụng vòng lặp for nếu sử dụng sai sẽ dẫn đến lặp vô hạn. Ví dụ như:

```
		for( var i = 0; i < 10; i--){
			document.write(i+ '<br/>');
		}
```
<a name="3"></a>
####3. Vòng lặp for lồng nhau:

Cũng tương tự như lệnh trong if else. Ta có cấu trúc của nó như sau:

```
for ( var i = 0; i < 10; i++);
{
	for ( var j=0; j < 10; j++);
}
```

Ví dụ nhé: Viết chương trình in ra 1 ma trận 10x10

```
for (var i = 0; i <= 9; i++)
{
    for (var j = 0; j <= 9; j++){
        // In ra vị trí của ma trận [i][j]
        document.write("(["+i+"]["+j+"])");
    }
    // Xuống hàng
    document.write("<br/>");
}
```
Kết quả thu được:

![c](https://github.com/TrinhTu/web_developer/blob/master/Task09_Javascript_Course_01/Bai06_for/image/c.png)

<a name="4"></a>
####4. Bài tập thực hành:

1. Vòng lặp trong javascript in ra các số từ 1 đến 100:

```
<script language="javascript">
	var i;
	for( i=1; i<=100, i++){
		document.write(i + '-');
	}
</script>
```

2. In ra các số chia hết cho 3 trong khoảng từ 0 - 100:

```
for (var i = 0; i <= 100; i++){
    if (i % 3 == 0){
        document.write(i + ' - ');
    }
}
```

![d](https://github.com/TrinhTu/web_developer/blob/master/Task09_Javascript_Course_01/Bai06_for/image/d.png)
