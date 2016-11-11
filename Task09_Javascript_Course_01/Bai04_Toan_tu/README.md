##BÀi 4: Các toán tử toán học và toán tử gán trong Javascript

>Tài liệu: Các toán tử toán học và toán tử gán trong Javascript
>
>Người thực hiện: Lê Tú Trinh
>
>Cập nhập lần cuối: 11/11/2016

###Mục lục:

[1. Toán tử toán học trong Javascript](#1)

[2.Toán tử gán trong Javascript](#2)

[3. Bài tập thực hành](#3)

###Nội dung:

<a name="1"></a>
####1. Toán tử toán học trong JS

- Phép cộng: (+) nếu là số thì nó sẽ cộng 2 số đó lại, còn nếu là chuỗi thì sẽ nối chuỗi.

```
 var a = 20;
 var b = 30;
 var c = a + b;
```
 - Tương tự ta có được phép trừ (-), phép nhân (*) và phép chia (/) dùng với number:

 ```
 var a = 10;
 var b = 5;
 var c = a - b;
 var d = a *b;
 var e = a / b;
 ```

- Phép chia lấy phần dư: là kết quả của bài toán là phần dư của 2 số đem chia cho nhau:

```
var a = 10;
var b = 5;
var c = a % b;
```

- Phép tăng giá trị hiện tại lên 1 đơn vị(++). Có 2 cách sử dụng là đặt nó trước biến và đặt nó sau biến

 Khi đặt nó trước biến:

 ```
 var c = 10;
 alert(++c); //giá trị nó là 11
 alert(c);// giá trị của c bây giờ là 11
```

 Khi đặt nó sau biến:

 ```
 var c = 10;
 alert(c++); //giá trị của nó là 10
 alert(c); // giá trị của c là 11
 ``` 

 Tương tự ta có phép giảm giá trị xuống 1 đơn vị (--). Tương tự như trên


<a name="2"></a>
####2. Toán tử gán trong JS:

- Toán tử (=):

Ví dụ: x=y

Giá trị của biến x bằng giá trị của biến y.

```
var x = 10;
var y = x; // y = 10
```

- Toán tử (+=):

Ví dụ: x +=y

Tương đương với x = x + y

```
var x = 10;
var y = 5;
x +=y; // tương đương x = x + y
```

- Toán tử (-=)

Ví dụ: x -= y

Tương đương với x = x -y

```
var x = 20; 
var y = 10;
x -= y; //tương đương x = x - y

- Tương tự ta áp dụng cho các toán tử (*=), (/=) và (%=)

<a name="3"></a>
####3. Bài tập thực hành: 

Thực hiện cộng trừ nhân chia và chia lấy dư của 2 số a và b sau đó hiển thị kết quả ra màn hình:

```
<!DOCTYPE html>
<html lang="vi">
	<head>
		<meta charset="utf-8"/>
		<title>Trinh</title>
		<script language="javascript">
			// khai báo 2 biến a và b
			var a;
			var b;
			var tong;
			var hieu;
			var tich;
			var thuong;
			var du;
			//gán giá trị, lấy thông tin
			a= prompt("Nhập giá trị của số a", "0"); //kiểu string
			b=prompt("Nhập giá trị của số b", "0"); //kiểu string
			a= parseInt(a);
			b=parseInt(b);
			tong= (a+b);
			hieu= (a-b);
			tich= (a*b);
			thuong= (a/b);
			du= (a%b)
			document.write("Giá trị tổng của a và b là " + tong + "<br/>");
			document.write("Giá trị hiệu của a và b là " + hieu + "<br/>");
			document.write("Giá trị tích của a và b là " + tich + "<br/>");
			document.write("Giá trị thương của a và b là " + thuong + "<br/>");
			document.write("Giá trị phần dư khi a chia b là " + du + "<br/>");
		</script>
	</head>
</html>
```

Kết quả:

![20](http://i.imgur.com/mFeRKrN.png)
