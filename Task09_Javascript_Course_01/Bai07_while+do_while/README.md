## Bài 7: Vòng lặp While- do while

> Tài liệu: Vòng lặp While- do while
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 12/11/2016

### Mục lục:

[1. Vòng lặp While](#1)

[2. Vòng lặp do while](#2)

[3. Vòng lặp while-do while lồng nhau](#3)

[4. Bài tập thực hành](#4)

### Nội dung:

<a name="1"></a>
#### 1. Vòng lặp While:

Cấu trúc vòng lặp While:

```
while (condition){
	//do something
}
```

`condition` là điều kiện dừng vòng lặp, condition đúng thì vòng lặp được thực hiện đến khi nào condition có giá trị sai thì dừng, nếu condition luôn đúng thì sẽ dẫn tới lặp vô hạn.

Ví dụ dùng while lặp từ 1 đến 10

```
var i = 1;
while (i <= 10){
    document.write(i + '<br/>');
    i++; 
}
```

Ta phải tăng i lên để tránh lặp vô hạn

![1](https://github.com/TrinhTu/web_developer/blob/master/Task09_Javascript_Course_01/Bai07_while%2Bdo_while/image/(1).png)

- Trường hợp lặp vô hạn lấy thông tin: Ví dụ nhập đúng các số trong trong khoảng từ 1 -> 20 thì dừng:

```
var a = null;	
	while (a < 1 || a > 20){
   		a = prompt("Nhập vào số từ 1 -> 20");
	}
	alert("Số bạn vừa nhập là " + a);
```

![2](https://github.com/TrinhTu/web_developer/blob/master/Task09_Javascript_Course_01/Bai07_while%2Bdo_while/image/(2).png)

<a name="2"></a>
#### 2. Vòng lặp do while:

Vòng lặp này có 1 đặc điểm là thực thi lệnh  rồi mới kiểm tra điều kiện, vậy nên vòng lặp này luôn được thực hiện ít nhất 1 lần. Cấu trúc của vòng lặp này là:

```
do {
	// some thing
}
while (condition);
```

`condition` là điều kiện dừng vòng lặp. Ví dụ: nhập các số từ 1 đến 10

```
<script language="javascript">
	var a=null;
	do {
		a= prompt("Nhập vào các số từ 1 đến 10");
	}
	while (a <1 || a>10);
	alert("Số bạn vừa nhập là"+ a);
</script>
```

<a name="3"></a>
#### 3. Vòng lặp while- do while lồng nhau:

Tương tự như vòng lặp for trong vòng lặp while và do while ta có thể lồng nhiều vòng lặp vào nhau. Ví dụ sử dụng vào lặp while hoặc do while để xây dựng ma trận 6x6

```
var i=0;
	while(i<=5){
		var j=0;
		while(j<=5){
			document.write('['+i+']['+j+']');
			j++;
		}
		document.write('<br/>');
		i++;
	}
```

![3](https://github.com/TrinhTu/web_developer/blob/master/Task09_Javascript_Course_01/Bai07_while%2Bdo_while/image/(3).png)

<a name="4"></a>
#### 4. Bài tập thực hành:

In ra các số từ 1->100 bằng vòng lặp while và do while:

- Sử dụng vòng lặp while:

```
var i=1;
while(i<=100){
	document.write(i + '<br/>');
	i++;
}
```

- Sử dụng vòng lặp do while:

``` 
var i=1;
do {
	document.write(i +'<br/>');
	i++;
}
while(i<=100);
```
