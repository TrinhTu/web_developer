## Bài 30: BOM - WINDOW TRONG JAVASCRIPT

> Tài liệu: BOM - Window trong javascript
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 08/03/2017

## Mục lục:

- [1. Xác định kích thước của trình duyệt](#1)

- [2. Thao tác với 1 cửa sổ của window](#2)

	+ [2.1 Mở cửa sổ với lệnh window.open()](#2.1)

	+ [2.2 Đóng cửa sổ với lệnh window.close()](#2.2)

	+ [2.3 Di chuyển cửa sổ với lệnh window.moveTo()](#2.3)

	+ [2.4 Resize cửa sổ với lệnh window.resizeTo()](#2.4)

- [Tài liệu tham khảo](#3)

***

<a name="1"></a>
### 1. Xác định kích thước của trình duyệt:

Để lấy kích thước chiều cao và chiều rộng của trình duyệt thì chúng ta sử dụng đối tượng `window`, với mỗi trình duyệt có những cách lấy khác nhau.

**Đối với Internet Explorer, Chrome. Firefox, Opera, và Safari cú pháp như sau:**

```
var heightBrowser = window.innerHeight;
var widthBrowser = window.innerWidth;
```

**Đối với Internet Explore các vesion 5,6,7,8 cú pháp như sau**

```
// Lấy chiều cao
var height = document.documentElement.clientHeight;
// hoặc
var height = document.body.clientHeight;
 
// Lấy chiều rộng
var width = document.documentElement.clientWidth;
// hoặc
var width = document.body.clientWidth;
```

Cách ngắn gọn để tương thích với các trình duyệt:

```
var width = window.innerWidth
        || document.documentElement.clientWidth
        || document.body.clientWidth;
 
var height = window.innerHeight
        || document.documentElement.clientHeight
        || document.body.clientHeight;
```

Dấu `||` nghĩa là nếu vế trái không thực hiện được sẽ lấy vế phải, đến khi lấy được thì dừng.

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task25_Javascript_Course_01_Part_03/Bai30_BOM_window/3.png"/></p>

<a name="2"></a>
### 2. Thao tác với 1 cửa sổ của window:

Một số phương thức giúp thao tác với trình duyệt dễ dàng hơn là:

<a name="2.1"></a>
#### 2.1 Mở cửa sổ với lệnh window.open():

**Cú pháp**: `window.open(url, name, options)`

**Trong đó**: 

- **url**: đường dẫn tới website muốn mở

- **name**: tên đặt cho cửa sổ

- **option**: chuỗi các thông số cách nhau bởi dấu phẩy, các thông sô thông dụng:

	+ **height=pixels**: chiều cao cửa sổ

	+ **width=pixels**: chiều rộng cửa sổ

	+ **top=pixels**: vị trí hiển thị so với lề trên

	+ **left=pixels**: vị trí hiển thị so với lề trái

	+ **menubar=yes|no|1|0**: có hiển thị thanh menu hay không

	+ **resizable=yes|no|1|0**: có hiển thị biểu tượng resize cửa sổ hay không

	+ **scrollbars=yes|no|1|0**: có hiển thị thanh cuộn hay không

	+ **status=yes|no|1|0**: có hiển thị thanh trạng thái hay không

	+ **titlebar=yes|no|1|0**: có hiển thị titlebar hay không

	+ **toolbar=yes|no|1|0**: có hiển thị toolbar hay không

	+ **fullscreen=yes|no|1|0**: có hiển thị biểu tượng fullscreen hay không

**Ví dụ**:

```javascript
<body>
      <script language="javascript">
        var windowChild = null;
        function openWindow()
        {
          windowChild = window.open('http://github.com', "windowChild ", "width=500, height=500");
        	return false;
        } 
      </script>
      <a href="#" onclick="return openWindow()">Open</a>
</body>
```

<a name="2.2"></a>
#### 2.2 Đóng cửa sổ với lệnh window.close():

Ta sử dụng lệnh `windowObj.close()` trong đó `windowObj` là cửa sổ mà sử dụng lệnh `window.open()` tạo ra.

**Ví dụ:**

```javascript
<script language="javascript">
        
        var windowChild = null;
        
        function openWindow()
        {
          	windowChild = window.open('http://freetuts.net', "windowChild", "width=500, height=500");
        	return false;
        }
        
        function closeWindow()
        {
          	windowChild.close()
        	return false;
        }
</script>
<a href="#" onclick="return openWindow()">Open</a>
<a href="#" onclick="return closeWindow()">Close</a>
```

<a name="2.3"></a>
#### 2.3 Di chuyển cửa số với lệnh window.moveTo():

Di chuyển cửa sổ sử dụng lệnh `windowObj.moveTo(top,left)`

+ **top**: số pixels so với lề trên

+ **left**: số pixels so với lề trái

**Ví dụ:**

```javascript
 <script language="javascript">
         
        var windowChild = null;
         
        function openWindow()
        {
            windowChild = window.open('http://freetuts.net', "windowChild", "width=500, height=500");
            return false;
        }
         
        function moveWindow()
        {
            windowChild.moveTo(500, 100);
            windowChild.focus();
            return false;
        }
</script>
<a href="#" onclick="return openWindow()">Open</a>
<a href="#" onclick="return moveWindow()">Move</a>
```

<a name="2.4"></a>
#### 2.4 Resize cửa số với lệnh window.resizeTo():

Nếu muốn thay đổi thiết lập chiều cao chiều rộng cho window thì sử dụng hàm `windowObj.resizeTo(width,height)`

**Ví dụ:**

```javascript
<script language="javascript">
         
        var windowChild = null;
         
        function openWindow()
        {
            windowChild = window.open('http://freetuts.net', "windowChild", "width=500, height=500");
            return false;
        }
         
        function resizeWindow()
        {
            windowChild.resizeTo(1000, 1000);
            windowChild.focus();
            return false;
        }
</script>
<a href="#" onclick="return openWindow()">Open</a>
<a href="#" onclick="return resizeWindow()">Resize</a>
```

<a name="3"></a>
### Tài liệu tham khảo:

> [1] BOM - Window trong javascript. http://freetuts.net/bom-window-trong-javascript-385.html