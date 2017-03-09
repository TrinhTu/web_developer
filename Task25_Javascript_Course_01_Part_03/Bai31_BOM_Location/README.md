## Bài 31: BOM - LOCATION ĐIỀU HƯỚNG VÀ XỬ LÝ URL TRONG JAVASCRIPT

> Tài liệu: BOM - Location điều hướng và xử lý URL trong Javascript
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 09/03/2017

## Mục lục:

- [1.Location trong Javascript](#1)

- [2. Các phương thức của Location](#2)

	- [2.1 window.location.reload(url) - tải lại trang web](#2.1)

	- [2.1 window.location.replace(urr) - ghi đè trang web](#2.2)

	- [2.3 window.location.assign(url) - load 1 trang mới](#2.3)

- [3. Các thuộc tính của Location](#3)

- [Tài liệu tham khảo](#4)

***

<a name="1"></a>
### 1. Location trong Javascript:

Location là 1 thuộc tính của window nên khi sử dụng phải thông qua đối tượng window, nên không cần phải khai báo. `window.location`

<a name="2"></a>
### 2. Các phương thức của Location:

3 phương thức chính nằm trong đối tượng location là: `reload()`, `replace()`, `assign()`

<a name="2.1"></a>
#### 2.1 window.location.reload(url) - tải lại trang web:

Để tải lại trang web cách thông thường là nhấn F5 trên bàn phím hoặc dịch chuột chọn **Refresh page**, nhưng nếu refresh bằng Javascript thì vẫn được bằng cách sử dụng phương thức `reload()`.

**Ví dụ:**

```javascript
<body>
		<h1> Vui lòng tải lại trang web </h1>
		<button onclick= "refreshPage()"> Refresh</button>
		<script language="javascript">
			function refreshPage()
			{
				window.location.reload();
			}
		</script>
</body>
```

<a name="2.2"></a>
#### 2.2 window.location.replace(urr) - ghi đè trang web:

Phương thức này ít khi được sử dụng thay vào đó là sử dụng cú pháp `window.location.href="url"`. Sự khác biệt của 2 cách này:

- Đối với `replace()` trình duyệt sẽ không đưa vào lịch sử

- Đối với `location()` trình duyệt sẽ đưa vào lịch sử

**Ví dụ:**

```javascript
<body>
      Click vào để chuyển hướng đến github.com
      <button onclick="replacePage()">replace()</button>
      <button onclick="hrefPage()">location.href</button>
      <script language="javascript">
        function replacePage()
        {
          window.location.replace('http://github.com'); 
        }
        
        function hrefPage()
        {
          window.location.href = 'http://github.com';
        }
      </script>
</body>
```
<a name="2.3"></a>
#### 2.3 window.location.assign(url) - load 1 trang mới:

Cách này về công dụng tương tụ như 2 cách trên nhưng có đặc điểm giống với location.href

**Ví dụ:**

```javascript
	<body>
      Click vào để chuyển hướng trang web
      <button onclick="assignPage()">replace()</button>
      <script language="javascript">
        function assignPage()
        {
          window.location.assign('http://github.com'); 
        }
      </script>
    </body>
```

<a name="3"></a>
### 3. Các thuộc tính của Location:

Ngoài các phương thức trên thì có thể sử dụng `Location` để xử lý các thành phần liên quan đến URL như `hash`, `search`. Dưới đây là danh sách các thuộc tính đầy đủ cho đối tượng `location`:

- **hash**: thiết lập hoặc lấy phần sau dấu `#` của URL

- **host:** thiết lập hoặc lấy hostname và port number của URL

- **hostname:** thiết lập hoặc lấy hostname

- **href:** thiết lập hoặc lấy URL

- **origin:** trả về protocal, hostname và port number của URL

- **pathname:** thiết lập hoặc lấy path name của URL

- **port:** thiết lập hoặc lấy port của URL

- **search:** lấy phần query string của URL

**Các thuộc tính trên có thể dùng để lấy (get) hoặc thiết lập (get)

**Ví dụ:**

```javascript
	<script language="javascript">
        document.write("hash:" +window.location.hash + "<br/>");
        document.write("host:" +window.location.host + "<br/>");
        document.write("hostname:" +window.location.hostname + "<br/>");
        document.write("href:" +window.location.href + "<br/>");
        document.write("origin:" +window.location.origin + "<br/>");
        document.write("pathname:" +window.location.pathname + "<br/>");
        document.write("port:" +window.location.port + "<br/>");
        document.write("search:" +window.location.search + "<br/>");
    </script>
```

<a name="4"></a>
### Tài liệu tham khảo:

> [1] BOM - Location điều hướng và xử lý URL trong Javascript. http://freetuts.net/bom-location-dieu-huong-va-xu-ly-url-trong-javascript-386.html