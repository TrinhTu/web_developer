##Bài 13: DOM Element trong javascript

>Tài liệu: DOM Element trong javascript
>
>Người thực hiện: Lê Tú Trinh
>
>Cập nhập lần cuối: 03/12/2016

###Mục lục:

[1. Tìm thẻ HTML theo ID](#1)

[2. Tìm thẻ HTML theo tên của thẻ HTML](#2)

[3. Tìm thẻ HTML theo tên class](#3)

[4. Tìm thẻ HTML theo cú pháp selector CSS](#4)

###Nội dung:

<a name="1"></a>
####1. Tìm thẻ HTML theo ID:

Để truy xuất tới thẻ HTML theo id ta sử dụng cú pháp sau:

```javascript
var element = document.getElementById('idname');
```

Ví dụ:

```javascript
<input type="text" value="Tú Trinh" id="box"/>
<script language="javascript">
	var element= document.getElementById('box');
	document.write(element.value);
</script>
```

Xem kết quả:

![1](https://github.com/TrinhTu/web_developer/blob/master/Task15_Javascript_Course_01_Part_02/Bai_13_DOM%20Element/image/1.png)

<a name="2"></a>
####2. Tìm thẻ HTML theo tên của thẻ:

Tên thẻ HTML là các thẻ như: `div`, `p`, `a`... Cú phá truy xuất tới các thẻ đó như sau:

```javascript
var element = document.getElementByIdName('tagname');
```

Ví dụ:

```javascript
<input type="text" value="Element"/>
<script language="javascript">
	var element= document.getElementsByTagName('input');
	document.write(element[0].value);
</script>
```
Xem kết quả:

![2](https://github.com/TrinhTu/web_developer/blob/master/Task15_Javascript_Course_01_Part_02/Bai_13_DOM%20Element/image/2.png)

<a name="3"></a>
####3. Tìm thẻ HTML theo tên class:

Ta sử dụng cú pháp sau:

```javascript
var element = document.getElementsByClassName('input');
```

Ví dụ:

```javascript
<input type="text" value="Tú Trinh" class="box"/>
<script language="javascript">
var element = document.getElementsByClassName('box');
document.write(element[0].value);
</script>
```

<a name="4"></a>
####4. Tìm thẻ HTML theo cú pháp selector CSS:

Cú pháp sử dụng:

```javascript
var element = document.querySelectorAll("selector.css");
```

Ví dụ:

```javascript
<html>
  <body>
    <input type="text" value="thẻ không cần lấy" class="box"/>
    <div>
        <input type="text" value="Thẻ Cần Lấy" class="box"/>
        <input type="text" value="thẻ không cần lấy"/>
    </div>
    <script language="javascript">
    var element = document.querySelectorAll("div input.box");
    document.write('<h3>Nội dung cần lấy là:'+ element[0].value + '</h3>');
    </script>
  </body>
</html>
```

Xem kết quả:

![3](https://github.com/TrinhTu/web_developer/blob/master/Task15_Javascript_Course_01_Part_02/Bai_13_DOM%20Element/image/3.png)

