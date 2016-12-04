##Bài 16: DOM HTML TRONG JAVASCRIPT

>Tài liệu: DOM HTML trong Javascript
>
>Người thực hiện: Lê Tú Trinh
>
>Cập nhập lần cuối: 04/12/2016

### Mục lục:

[1. Thay đổi và lấy nội dung bên trong thẻ HTML](#1)

[2. Thay đổi và lấy giá trị thuộc tính thẻ HTML bằng javascript](#2)

###Nội dung:

<a name="1"></a>
####1. Thay đổi và lấy nội dung bên trong thẻ HTML:


Để lấy nội dung bên trong thẻ HTML ta sử dụng cú pháp sau:

```javascript
	var html = document.getElementById("content").innerHTML
```

Để thay đổi nội dung cho thẻ HTML ta sử dụng cú pháp sau:

```javascript
	var html = document.getElementById("content").innnerHTML="<h1>Nội dung</h1>";
```

Ví dụ:

```javascript
<script language="javascript">
         	function set_content(){
         		document.getElementById("content").innerHTML="<h1>NỘI DUNG ĐÃ ĐƯỢC THAY ĐỔI</h1>";
         	}
         	function get_content(){
         		var html=document.getElementById("content").innerHTML
         		alert("Nội dung cần lấy rỗng hahaha:"+ html);
         	}
        </script>
		<div id="content">Nội dung</div>
		<input type="button" value="Nội dung cần lấy" id="get_content" onclick="get_content()"/>
		<input type="button" value="Thay đổi nội dung" id="set-content" onclick="set_content()"/>
</script>
```

![1](https://github.com/TrinhTu/web_developer/blob/master/Task15_Javascript_Course_01_Part_02/Bai_16_DOM%20HTML/image/1.png)

![2](https://github.com/TrinhTu/web_developer/blob/master/Task15_Javascript_Course_01_Part_02/Bai_16_DOM%20HTML/image/2.png)

![3](https://github.com/TrinhTu/web_developer/blob/master/Task15_Javascript_Course_01_Part_02/Bai_16_DOM%20HTML/image/3.png)

<a name="2"></a>
####2. Thay đổi và lấy giá trị thuộc tính thẻ HTML bằng javascript:

Để thay đổi giá trị 1 thuộc tính HTML bất kì ta sử dụng cú pháp:

```javascript
	document.getElementById("element").attributeName ="new value";
```

Để lấy giá trị của 1 thuộc tính HTML ta sử dụng cú pháp:

```javascript
	var value= document.getElementById("element").attributeName;
```

Ví dụ: Viết chương trình khi click và button thì nó chuyển thành textbox và khi click vào textbox nó sẽ chuyển lại thành button:

```javascript
<script language="javascript">
    function button(){
        var object= document.getElementById("object");
        var type = object.type;
        if(type=="button"){
         	object.type= 'text';
        }
         else{
         	object.type='button';
        }
        }
</script>
<input type="button" value="Click me" id="object" onclick="button()"/>
```

Kết quả: http://tutrinh01.chuyengiaseoweb.net/javascript16.html
