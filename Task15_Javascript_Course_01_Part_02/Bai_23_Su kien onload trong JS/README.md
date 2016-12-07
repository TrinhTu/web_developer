##Bài 22: Sự kiện onload trong javascript

>Tài liệu:  Sự kiện onload trong javascript
>
>Người thực hiện: Lê Tú Trinh
>
>Cập nhập lần cuối: 06/12/2016

### Mục lục:

[1. Quá trình biên dịch code javascript](#1)

[2. Sự kiện onload trong javascript](#2)

###Nội dung:

<a name="1"></a>
####1. Quá trình biên dịch code javascript:

Tương tự các ngôn ngữ khác, javascript sẽ chạy biên dịch từ trên xuống dưới và từ trái qua phải. Nên khi sử dụng 1 hàm mà phía trên nó không tồn tại hàm đó thì sẽ bị báo lỗi undefined, và để giải quyết vấn đề này ta sử dụng sự kiện onload trong javascript:

Ví dụ: đoạn code này sai vì hàm `do_validate` được định nghĩa nằm dưới đoạn code gọi tới nó.

```javascript
var flag = do_validate();
function do_validate()
{
	return TRUE/FALSE;
}
```

- Sửa lại đúng như sau:

```javascript
function do_validate()
{
	//return TRUE/FALSE;
}
var flag = do_validate();
```

Vậy nên khi gán 1 hàm nào đó cho sự kiện nào đó trong HTML thì phải gán hàm đã khai báo sẵn phía trên thẻ HTML. 

Ví dụ: đoạn code này cũng sai do hàm `do_validate()` ở thẻ HTML trên chưa đc định nghĩa.

```javascript
<button on click="do_validate()">Click me</button>
<script language="javascript">
function do_validate()
{
	//return TRUE/FALSE;
}
</script>
```

- Sửa lại:

```javascript
 <script language="javascript">
      function do_validate()
      {
        // return TRUE/FALSE;
      } 
 </script>
 <button onclick="do_validate()">Click me</button>
 ```

<a name="2"></a>
####2. Sự kiện onload trong javascipt:

Sự kiện `onload` có nghĩa là khi trình duyệt đã load xong mọi thứ thì code nằm bên trong đó mới chạy. Tức là nếu sử dụng `onload` cho 1 thẻ HTML thì nó chỉ có tác dụng với thẻ HTML đó thôi, còn dùng cho `window` thì sẽ có tác dụng toàn trang. Tức là những đoạn code nằm bên trong sự kiện onload sẽ chạy sau cùng.

Ví dụ: Cho hàm `do_validate()` bên trong sự kiện window.load nên mặc dù hàm validate đặt phía dưới vẫn đúng.

```javascript
window.onload = function()
{
	do_validate()
};
function do_validate()
{
	alert(1);
}
```

Ví dụ 2: 

```javascript
		<input type="text" id="ok" />
        <script language="javascript">
            alert (1);
            window.onload = function()
            {
                alert(3);
            };
            alert(2);
        </script>
```

Xem kết quả: http://localhost:81/sourse/javascript22.html
