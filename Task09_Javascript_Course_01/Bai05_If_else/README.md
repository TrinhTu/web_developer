## Bài 5: Lệnh kiểm tra điều kiện if else trong javascrip

> Tài liệu: Lệnh kiểm tra điều kiện trong Javascript
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 12/11/2016

### Mục lục:

[1. Lệnh if trong Javascript](#1)

[2. Lệnh else trong Javascript](#2)

[3. Kết hợp nhiều lệnh if else trong Javascript](#3)

[4. Lệnh if else lồng nhau trong javascript](#4)

[5. Bài tập thực hành](#5)

### Nội dung:

<a name= "1"></a>
#### 1. Lệnh if trong javascript:

Cú pháp:

```
if ( condition){
	// statment
}
```
Trong đó condition là mệnh đề luôn có 2 giá trị là true/false hoặc tương đương ( 1=> true, 0=>false). Ví dụ: 

```
<script language="javascript">
	var a=10;
	var b=10;
	if (a==b){
		alert ('a và b bằng nhau');
	}
</script>
``` 

Kết quả sẽ hiển thị ra là a và b bằng nhau.

![1](https://github.com/TrinhTu/web_developer/blob/master/Task09_Javascript_Course_01/Bai05_If_else/image/1.png)

Nếu như câu lệnh bên trong là câu lệnh đơn thì có thể bỏ dấu ngoặc nhọn đi.

<a name="2"></a>
#### 2. Lệnh else trong javascript:

Lệnh else sẽ được thực hiện nếu như lệnh if không thỏa, vậy nên muốn sử dụng lệnh else thì phải có lệnh if trước nó. Ví dụ:

```
<script language="javascript">
	var a= 20;
	var b= 30;
	if (a == b){
		alert('a và b bằng nhau');
	}
	else{
		alert('a và b khác nhau');
	}
</script>
```
![2](https://github.com/TrinhTu/web_developer/blob/master/Task09_Javascript_Course_01/Bai05_If_else/image/2.png)

<a name="3"></a>
#### 3. Kết hợp nhiều lệnh if else trong javascript:

Có thể kết hợp nhiều cú pháp if else để xử lí:

```
<script language="javascript">
	var a = 20;
	if (a>20){
		alert ('a >20');
	}
	else if (a <20){
		alert('a<20');
	}
	else {
		alert('a=20');
	}
</script>
```
![3](https://github.com/TrinhTu/web_developer/blob/master/Task09_Javascript_Course_01/Bai05_If_else/image/3.png)

<a name="4"></a>
#### 4. Lệnh if else lồng nhau trong javasript:

Nghĩa là trong lệnh if sẽ chứa nhiều lệnh if khác. Ví dụ:

```
<script language="javascrip">
	var a= 20;
	if (a>10)
	{
		var b= 15;
		if(a==b)
		{
			alert('a=b');
		}
		else{
			alert('a!=b');
		}
	}
</script>
```

![4](https://github.com/TrinhTu/web_developer/blob/master/Task09_Javascript_Course_01/Bai05_If_else/image/4.png)

<a name="5"></a>
#### 5. Bài tập thực hành:

1. Tìm min max của 2 số cho trước bằng javascript

```
<script language="javascript">
	var a;
	var b;
	a= prompt ("Nhập giá trị của a", "0");
	b= prompt ("Nhập giá trị của b", "0");
	a=parseInt(a);
	b=parseInt(b);
	if(a>b){
		document.write("Max là a:" + a + "<br/>");
		document.write("Min là b:" + b);
	}
	else if(a<b){
		document.write("Max là b:" + b + "<br/>");
		document.write("Min là a:" + a);
	}
	else{
		document.write("a và b bằng nhau");
	}
</script>
```
2. Kiểm tra số chẳn lẽ:

```
<script language="javascript">
	var a;
	a = prompt ("Nhập giá trị của a", "0");
	a = parseInt(a);
	if((a%2)==0){
		document.write("a là số chẵn");
	}
	else {
		document.write("a là số lẻ");
	}
</script>
```
Thử nhập giá trị của a=5 ta có kết quả:

![5](https://github.com/TrinhTu/web_developer/blob/master/Task09_Javascript_Course_01/Bai05_If_else/image/5.png)


