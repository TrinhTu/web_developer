##Bài 15: RETURN TRUE/FALSE CỦA EVENTS TRONG JAVASCRIPT

>Tài liệu: Return True/False của Events trong javascript
>
>Người thực hiện: Lê Tú Trinh
>
>Cập nhập lần cuối: 04/12/2016

### Mục lục:

[1. Return true/false của events trong javascript](#1)

[2. Bài tập validate form đơn giản với event và DOM](#2)

###Nội dung

<a name="1"></a>
####1. Return true/false của events trong javascript:

Return của events trong javascript dùng để xác nhận 1 sự kiện nào đó có được thực hiện thành công hay không, để từ đó đối tượng HTML sẽ cho phép xử lí hoặc không cho phép thực hiện thao tác đó.

Trong 1 sự kiện sẽ có 2 trạng thái TRUE/FALSE, để hiển thị 2 trạng thái này ta sử dụng cú pháp `return TRUE/FALSE` trong funtion của event. 2 cách return thông dụng nhất:

- Cách 1: return tại đoạn code event trong HTML :

```javascript
	<input type="text" onkeypress="return false" />
```

- Cách 2: Tạo 1 hàm xử lí sự kiện:

```javascript
<script language="javascript">
function check()
{
	return false;
}
</script>
<input type="text" onkeypress="return check()"/>
```

<a name="2"></a>
###2. Bài tập validate form đơn giản với event và DOM:

Ta có đoạn code HTML như sau:

```javascript
 <form method="post" action="">
    Username: <input type="text" value="" name="username" id="username"/> <br/>
    Password: <input type="text" value="" name="password" id="password"/> <br/>
    Re Password: <input type="text" value="" name="re-password" id="re-password"/> <br/>
    <input type="submit" value="Register" onclick="return validate()" />        
</form>
```

Xem hiển thị:

![1](https://github.com/TrinhTu/web_developer/blob/master/Task15_Javascript_Course_01_Part_02/Bai_15_Return%20TRUE%20FALSE/1.png)

**Yêu cầu bài tập:**

- Tên đăng nhập không được để trống

- Mật khẩu không được để trống

- Mật khẩu nhập lại phải trùng với mật khẩu ở trên

**Cách thực hiện:**

 - Tạo 1 javascript funtion `validate()`

 - Sử dụng hàm `return validate()` trong sự kiện `onclick` của button register

 - Trong hàm `validate()` sử dụng DOM để lấy giá trị các ô input, kiểm tra các giá trị và return về true/false


 ```javascript
 <script language="javascript">
    function validate()
        {
            var username = document.getElementById("username").value;
            var password = document.getElementById("password").value;
            var re_password = document.getElementById("re-password").value;
            if (username == ""){
              alert("Bạn chưa nhập tên đăng nhập");
              return false;
            }
          
            if (password == ""){
              alert("Bạn chưa nhập mật khẩu");
              return false;
            }
            if (password != re_password){
              alert("Mật khẩu nhập lại không đúng");
              return false;
            }
            return true;
          }
</script>
```

Kiểm tra kết quả tại đây: http://tutrinh01.chuyengiaseoweb.net/javascript11.html


Ví dụ 2:

```javascript
<script language="javascript">
    function validate()
    {
        var host = document.getElementById("host").value;
        var username = document.getElementById("username").value;
        var password = document.getElementById("password").value;
        var port = document.getElementById("port").value;
        if(host== ""){
            alert("Bạn chưa nhập giá trị")
        }
        if (username == ""){
            alert("Bạn chưa nhập tên đăng nhập");
        	return false;
        }
          
        if (password == ""){
            alert("Bạn chưa nhập mật khẩu");
            return false;
        }
        if (port==""){
            alert("Bạn chưa nhập cổng");
            return false;
        }
        return true;
        }
</script>
		 <form method="post" action="">
            Host: <input type="text" value="" name="host" id="host"/><br/>
            Username: <input type="text" value="" name="username" id="username"/><br/>
            Password: <input type="text" value="" name="password" id="password"/><br/>
            Port: <input type="text" value="" name="port" id="port"/><br/>
            <input type="submit" value="Quickconnect" onclick="return validate()" />        
        </form>
```

 Xem kết quả: http://tutrinh01.chuyengiaseoweb.net/javascript15.html
