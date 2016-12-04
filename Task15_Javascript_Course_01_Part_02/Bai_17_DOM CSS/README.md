##Bài 17: DOM CSS trong Javascript

>Tài liệu: DOM CSS trong Javascript
>
>Người thực hiện: Lê Tú Trinh
>
>Cập nhập lần cuối: 04/12/2016

### Mục lục:

[1. Thay đổi CSS bằng Javascript](#1)

[2. Ví dụ thay đổi CSS bằng Javascript](#2)

###Nội dung:

<a name="1"></a>
####1. Thay đổi CSS bằng Javascript:

Đối tượng `style` sẽ chứa tất cả các thuộc tính của CSS và chúng ta dễ dàng thao tác với chúng bằng cú pháp riêng đó là thiết lập CSS và lấy giá trị CSS:

Cú pháp thiết lập CSS bằng Javascript:

```javascript
	document.getElementById("object").style.cssName= 'something';
```

Cú pháp lấy giá trị CSS bằng Javascript:

```javascript
	var value =document.getElementById("object").style.cssName;
```

Trường hợp thuộc tính có dấu gạch ngang như: `font-size`, `line-height`, `margin-bottom` thì thuộc tính đó trong `style` sẽ có tên là `fontSize`, `lineHeight`, `marginBottom`, bỏ dấu gạch ngang và viết hoa kí tự đầu tiên của chữ thứ hai.

<a name="2"></a>
####2. Ví dụ thay đổi CSS bằng Javascript:

Ví dụ 1: Viết 1 chương trình gồm 4 button và 1 thẻ div, khi click vào từng button thì nó sẽ thiết lập màu sắc, background, chiều cao, font size của thẻ div:

```javascript
<script language="javascript">
	function change_background(){
         document.getElementById("content").style.background='aqua';
    }
    function change_color(){
         document.getElementById("content").style.color='tomato';
    }
         	
    function change_height(){
        document.getElementById("content").style.height='400px';
    }
    function change_fontsize(){
        document.getElementById("content").style.fontSize='100px';
    }
</script>
<div id="content">Nội dung</div>
<input type="button" value="Background" onclick="change_background()"/>
<input type="button" value="Color" onclick="change_color()"/>
<input type="button" value="Height" onclick="change_height()"/>
<input type="button" value="Font size" onclick="change_fontsize()"/>
```
 Xem kết quả: http://tutrinh01.chuyengiaseoweb.net/javascript17.html

Ví dụ 2: Viết chương trình đăng nhập và validate thông tin username, password. Nếu nhập không đủ thông tin sẽ hiển thị thẻ div màu đỏ, còn ngược lại thì có thông báo validate thành công chữ màu xanh.

```javascript
<script language="javascript">
	function validate(){
		var box1 = document.getElementById("box1").value;
        var box2 = document.getElementById("box2").value;
        var message = document.getElementById("message");
        if(box1 =="" || box2 ==""){
         	message.innerHTML= "Bạn chưa nhập đủ thông tin!";
         	message.style.color=" red";
        }
        else{
         	message.innerHTML="Bạn đã đăng nhập thành công!";
         	message.style.color="blue";
        }
    }
</script>
Username:<input type="text" value="" id="box1"/> <br/>
Password:<input type="password" value="" id="box2" /> <br/>
<div id="message"></div><br/>
<input type="button" value="Login" onclick="validate()"/>
```

Kết quả:

![1](https://github.com/TrinhTu/web_developer/blob/master/Task15_Javascript_Course_01_Part_02/Bai_17_DOM%20CSS/1.png)

![2](https://github.com/TrinhTu/web_developer/blob/master/Task15_Javascript_Course_01_Part_02/Bai_17_DOM%20CSS/2.png)


