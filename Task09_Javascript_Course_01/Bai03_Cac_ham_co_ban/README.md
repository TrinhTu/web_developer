## Bài 3: Hàm alert()- confirm()-prompt() trong javascript

> Tài liệu:
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 11/11/2016

### Mục lục:

[1. Hàm alert() trong javascript](#1)

[2. Hàm confirm() trong javascript](#2)

[3. Hàm prompt() trong javascript](#3)

### Nội dung:

<a name="1"></a>
#### 1. Hàm alert:

Hàm có nhiệm vụ thông báo popup (cửa sổ bật lên), nó có 1 tham số truyền vào và tham số này chính là nội dung muốn thông báo với người dùng.

```
<html>
	<head>
		<meta charset="utf-8"/>
		<title>Trinh</title>
	</head>
	<body>
		<input type="button" onclick="alert('Hello every body')" valua="Click Me"/>
	</body>
</html>
```
Kết quả trả về như sau:

![1](https://github.com/TrinhTu/web_developer/blob/master/Task09_Javascript_Course_01/Bai03_Cac_ham_co_ban/image/1.png)


<a name="2"></a>
#### 2. Hàm confirm:

Hàm confirm() cũng sẽ xuất hiện 1 thông báo popup nhưng có thêm 2 sự lựa chọn là Yes và No. Nếu người dùng chọn Yes thì nó trả về TRUE và sai là FALSE. Nó cũng có 1 tham số truyền vào và tham số này chính là nội dung thông báo:

```
<html>
	<head>
		<meta charset="utf-8"/>
		<title>Trinh</title>
		<script language="javascript">
			var result= confirm('Bạn có chắc chắn muốn xóa bài viết này không?');
			if(result==true){
				alert('Bạn đã xóa thành công');
			}
			else if (result==false){
				alert('Bạn đã hủy bỏ thao tác');
			}
		</script>
	</head>
</html>
```
Kết quả như sau:

![2](https://github.com/TrinhTu/web_developer/blob/master/Task09_Javascript_Course_01/Bai03_Cac_ham_co_ban/image/2.png)

Nếu bạn click vào Ok:

![3](https://github.com/TrinhTu/web_developer/blob/master/Task09_Javascript_Course_01/Bai03_Cac_ham_co_ban/image/3.png)

Nếu click vào Cancle:

![4](https://github.com/TrinhTu/web_developer/blob/master/Task09_Javascript_Course_01/Bai03_Cac_ham_co_ban/image/4.png)

<a name="3"></a>
#### 3. Hàm prompt:

Dùng để lấy thông tin từ người dùng, gồm có 2 tham số truyền vào là nội dung thông báo và giá trị ban đầu. Nếu người dùng không nhập thì nó sẽ trả về NULL

```
<head>
		<meta charset="utf-8"/>
		<title>Trinh</title>
		<script language="javascript">
			prompt("Question", "Bạn đang làm gì đó?");
		</script>
</head>
```
Kết quả trả về như sau:

![5](https://github.com/TrinhTu/web_developer/blob/master/Task09_Javascript_Course_01/Bai03_Cac_ham_co_ban/image/5.png)

Nếu thêm hàm document.write để hiển thị nội dung ra ngoài trình duyệt thì ta có:

```
<head>
	<meta charset="utf-8"/>
	<title>Trinh</title>
	<script language="javascript">
		var name= prompt("Question", "Bạn đang làm gì đó?");
		document.write(name);
	</script>
</head>
```
Kết quả như sau:

![6](https://github.com/TrinhTu/web_developer/blob/master/Task09_Javascript_Course_01/Bai03_Cac_ham_co_ban/image/6.png)

Bài tập ví dụ nè:

```
<script language="javascript">
// khai báo 2 biến a và b
	var a;
	var b;
	var tong;
	//gán giá trị, lấy thông tin
	a= prompt("Nhập giá trị của số a", "0"); //kiểu string
	b=prompt("Nhập giá trị của số b", "0"); //kiểu string
	//chuyển sang kiểu number
	a= parseInt(a);
	b=parseInt(b);
	tong= (a+b);
	//in kết quả ra màn hình
	document.write("Giá trị tổng của a và b là " + tong);
</script>
```
Ta có kết quả lần lượt như sau:

![7](https://github.com/TrinhTu/web_developer/blob/master/Task09_Javascript_Course_01/Bai03_Cac_ham_co_ban/image/7.png)

![8](https://github.com/TrinhTu/web_developer/blob/master/Task09_Javascript_Course_01/Bai03_Cac_ham_co_ban/image/8.png)

![9](https://github.com/TrinhTu/web_developer/blob/master/Task09_Javascript_Course_01/Bai03_Cac_ham_co_ban/image/9.png)

Bài tập nhỏ: Lấy thông tin khách hàng

```
<script language="javascript">
       var name;
       var email;
       var phone;
       var address;
       var honey;
       name    = prompt("Bạn tên gì nè?");
       email   = prompt("Email của bạn là gì nè?");
       phone   = prompt("Số điện thoại của bạn là gì?");
       address = prompt("Địa chỉ của bạn là gì?");
       honey   = prompt("Bạn có người yêu chưa nè?");
        // In ra trình duyệt
       document.write("Tên bạn rất đẹp: " + name + "<br/>");
       document.write("Email của bạn rất hay: " + email + "<br/>");
       document.write("Số điện thoại của bạn đẹp quá: " + phone + "<br/>");
       document.write("Địa chỉ của bạn là: " + address + "<br/>");
       document.write("Người yêu bạn là: " + honey + "<br/>");
 </script>
 ```

![10](https://github.com/TrinhTu/web_developer/blob/master/Task09_Javascript_Course_01/Bai03_Cac_ham_co_ban/image/10.png)
