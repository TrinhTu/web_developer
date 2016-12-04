##Bài 18: THÊM SỰ KIỆN BẰNG JAVASCRIPT

>Tài liệu: Thêm sự kiện bằng javascript
>
>Người thực hiện: Lê Tú Trinh
>
>Cập nhập lần cuối: 04/12/2016

### Mục lục:

[1. Thêm sự kiện cho 1 thẻ HTML bằng javascript](#1)

[2. Thêm sự kiện cho nhiều thẻ HTML bằng javascript](#2)

###Nội dung:

<a name="1"></a>
####1. Thêm sự kiện cho 1 thẻ HTML bằng javascript:

Để thêm sự kiện bằng javascript thì sẽ sử dụng cú pháp sau:

```javascript
	elementOject.eventName = function(){
	//do something
	};
```

Trong đó: 

- **elementObject** là đối tượng HTML mà sử dụng DOM để lấy.

- **eventName** là tên của event như onclick, onchange,...

Ví dụ: thêm sự kiện click button có `id="show-btn"`

```javascript
<input type="button" id="show-btn" value="Click me"/>
<script language="javascript">
	var button = document.getElementById('show-btn');
	button.onclick= function(){
		alert('Bạn vừa click vào button');
	}
</script>
```

![1](https://github.com/TrinhTu/web_developer/blob/master/Task15_Javascript_Course_01_Part_02/Bai_18_Them%20su%20kien%20trong%20JS/1.png)

<a name="2"></a>
####2. Thêm sự kiện cho nhiều thẻ HTML bằng javascript:

Cú pháp như sau:

```javascript
var elementObjs = document.getElementsByTagName('element');
for (var i = 0; i < elementObjs.length; i++)
{
	elementObjs[i].eventName = function()
	{
		//do something
	};
}
```

Ví dụ: Thêm sự kiện khi click vào các thẻ `a` sẽ hiện lên câu chào:

```javascript
<ul>
    <li><a href="#" class="show">Nội dung 1</a></li>
    <li><a href="#" class="show">Nội dung 2</a></li>
    <li><a href="#" class="show">Nội dung 3</a></li>
</ul>  
<script language="javascript">  
    var a_list = document.getElementsByClassName("show");
    for (var i = 0; i < a_list.length; i++){
        a_list[i].onclick = function()
        {
            alert('XIN CHÀO CÁC BẠN');
            return false
        };
    }
</script>
```

Xem kết quả:

![2](https://github.com/TrinhTu/web_developer/blob/master/Task15_Javascript_Course_01_Part_02/Bai_18_Them%20su%20kien%20trong%20JS/2.png)




