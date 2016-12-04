##Bài 19: HÀM ADDEVENTLISTENER() TRONG JAVASCRIPT

>Tài liệu: Hàm addeventListener() trong Javasscript
>
>Người thực hiện: Lê Tú Trinh
>
>Cập nhập lần cuối: 04/12/2016

### Mục lục:

[1. Hàm addEventListener() trong Javascript](#1)

[2. Thêm sự kiện cho đối tượng window](#2)

[3. Truyền tham số vào Event trong hàm addEventListener()](#3)

###Nội dung:

<a name="1"></a>
####1. Hàm addEventListener() trong javascript:

Để thêm sự kiện cho đối tượng HTML thì sử dụng cú pháp sau:

```javascript 
	elementOject.eventName = function(){
		//do something
	}
```

Nhưng nếu sử dụng hàm `addEventListener() thì cú pháp như sau:

```javascript
	elementObject.addEventListener('eventName', function(e){
		//do something
	});
```

Trong đó:

-  **eventName: là tên của sự kiện bỏ đi chữ `on`, ví dụ `click`, `change`,...

- function ở tham số thứ 2 là hàm sẽ được chạy khi sự kiện eventName kích hoạt.

Ví dụ: Xây dựng chức năng nhập dữ liệu vào ô input thì hiển thị giá trị o input đó ra ngoài:

```javascript
<input type="text" id="ok" value="" />
<div id="result"></div>
<script language="javascript">
    var input = document.getElementById("ok");
	input.addEventListener('keyup', function(){
      	document.getElementById('result').innerHTML = input.value;
    });
</script>
```

Xem kết quả: 

![1](https://github.com/TrinhTu/web_developer/blob/master/Task15_Javascript_Course_01_Part_02/Bai_19_Ham%20addEventListener/image/1.png)

Ví dụ 2: Bổ sung thêm chiều dài kí tự vào ví dụ trên, nếu nhập nhiều hơn 5 kí tự thì hiển thị thông báo

```javascript
<input type="text" id="ok" value="" />
<div id="result"></div>
<script language="javascript">
    var input = document.getElementById("ok");
	input.addEventListener('keyup', function(){
      	document.getElementById('result').innerHTML = input.value;
      	if(input.value.length>5){
      		alert('Không vượt quá độ dài 5 kí tự');
      	}
    });
</script>
```

![2](https://github.com/TrinhTu/web_developer/blob/master/Task15_Javascript_Course_01_Part_02/Bai_19_Ham%20addEventListener/image/2.png)


<a name="2"></a>
####2. Thêm sự kiện cho đối tượng window:

Sử dụng hàm `addEventListener()` để tạo sự kiện cho window

```javascript
<h2>hãy zoom trình duyệt</h2>
<div id="result"></div>
<script language="javascript">
    window.addEventListener("resize", function(){
    	document.getElementById('result').innerHTML="bạn vừa zoom trình duyệt"
    });
</script>
```

![3](https://github.com/TrinhTu/web_developer/blob/master/Task15_Javascript_Course_01_Part_02/Bai_19_Ham%20addEventListener/image/3.png)

<a name="3"></a>
####3. Truyền tham số vào Event trong hàm addEventListener():

Nếu muốn truyền tham số vào thì bắt buộc phải tạo 1 hàm khác rồi gọi nó từ hàm `addEventListener()`

Ví dụ:

```javascript
var buton = document.getElementById('ok');
button.addEventListener('click', function(){
	object(2,3);
});
	function object(a, b)
	{
	alert(a+b);
	}
```

![4](https://github.com/TrinhTu/web_developer/blob/master/Task15_Javascript_Course_01_Part_02/Bai_19_Ham%20addEventListener/image/4.png)
