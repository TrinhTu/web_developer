##Bài 22: Hàm removeEventListener() trong javascript

>Tài liệu:  Hàm removeEventListener() trong javascript
>
>Người thực hiện: Lê Tú Trinh
>
>Cập nhập lần cuối: 04/12/2016

### Mục lục:

[1. Hàm removeEventListener() trong javascript](#1)

[2. Ví dụ](#2)

###Nội dung:

<a name="1"></a>
####1. Hàm removeEventListener() trong javascript:
 
Sử dụng hàm `removeEventListener()` để xóa đi hành động validate. Cú pháp:

```javascript
		object.removeEventListener("click", some_action);
```

Để xóa hành động đó phải biết tên hành động đó và đặt nó trong 1 hàm để nhận diện. Ví dụ như sau:

```javascript
// Lấy đối tượng
var object = document.getElementById("something");
 
// Hành động validate
function do_validate()
{
// do something
}
 
// Thêm hành động vào sự kiện click
object.addEventListener("click", do_validate);
 
// Xóa hành động validate vào sự kiện click
object.removeEventListener("click", do_validate);
```

<a name="2"></a>
####2. Ví dụ:

Ví dụ: Xây dựng 1 ứng dụng di chuyển chuột thì sẽ xuất hiện 1 dãy số ngẫu nhiên, nếu click vào button **Stop Random** thì sẽ dừng random dãy số đó.

```javascript
 		<div id="result"></div>
        <input type="button" value="Stop Random" id="stop_random" />
        <script language="javascript">
            // Lấy các đối tượng
            var result = document.getElementById("result");
            var button = document.getElementById("stop_random");
            var html = document.getElementsByTagName("html")[0];
           
            //Định nghĩa hành động hiển thị dãy số random
            function do_random()
            {
                var randomString = Math.random();
                result.innerHTML = randomString;
            }
             
            //Thêm hành động do_random cho sự kiện mousemove thẻ <html>, 
            html.addEventListener("mousemove", do_random);
           
            //Thêm sự kiện click cho button
            button.addEventListener("click", function(){
                // Xóa hành động do_random khỏi sự kiện mousemove
                html.removeEventListener("mousemove", do_random);
            });     
        </script>
```

![1](https://github.com/TrinhTu/web_developer/blob/master/Task15_Javascript_Course_01_Part_02/Bai_22_Ham%20removeEventListener/1.png)

Xem kết quả: http://tutrinh01.chuyengiaseoweb.net/javascript22.html
