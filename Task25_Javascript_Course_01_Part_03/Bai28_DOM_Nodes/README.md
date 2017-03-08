## Bài 28: DOM NODES TRONG JAVASCRIPT

> Tài liệu: DOM Nodes trong Javascript
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 08/03/2017

## Mục lục:

- [1. DOM Node - document.createElement()](#1)

- [2. DOM Node - document.createTextNode()](#2)

- [3. DOM Node - Các phương thức khác](#3)

	- [3.1 Phương thức appendChild()](#3.1)

	- [3.2 Phương thức insertBefore()](#3.2)

	- [3.3 Phương thức removeChild()](#3.3)

	- [3.4 Phương thức replaceChild()](#3.4)

- [Tài liệu tham khảo](#4)

***

<a name="1"></a>
### 1. DOM Node - document.createElement():

Khi sử dụng DOM element để truy vấn tới đối tượng HTML thì kết quả nhận được sẽ là 1 `object` và `object` đó gọi là DOM Nodes.

**Ví dụ**: `var mode = document.getElementById("some-id");`

`var node = document.getElementById("some-id");`

Đối với cách này bắt buộc phải tồn tại 1 đối tượng HTML đang hiển thị trên website thì mới có thể khởi tạo thành công. Nếu muốn tạo 1 Node mới không liên quan gì đến các thẻ HTML đang hiển thị trên website thì sử dụng phương thức `document.creatElement()` với tham số truyền vào là tên của thẻ HTML cần tạo.

`var p = document.creatElement("p");`

Sau khi khởi tạo xong có thể sử dụng các phương thức thuộc tính của DOM HTML, DOM CSS

` p.innerHTML = "Học DOM Nodes"`

Để thêm Node này vào trang web thì sử dụng phương thức `appendChild`. Giả sử muốn thêm vào thẻ `boby`:

`document.getElementsByTagName('body')[0].appendChild(p);`

**Ví dụ:**

```javascript
<script language="javascript">
          
    // Tạo mới một thẻ h1
    var h1 = document.createElement("h1");
          
    // Thêm nội dung HTML vào thẻ h1
    h1.innerHTML = "Học DOM Nodes"
          
    // Đưa thẻ h1 vào trong thẻ body
    document.getElementsByTagName('body')[0].appendChild(h1);
          
</script>
```

<a name="2"></a>
### 2. DOM Node - document.createTextNode():

Text node là 1 node đặc biệt, không phải là 1 thẻ HTML thường mà là 1 chuỗi (string) nên thường sử dụng nó để thay thế cách gán thông thường `node.innerHTML`.

**Ví dụ:**

```javascript
<script language="javascript">
          
    // Tạo mới một thẻ h1
    var h1 = document.createElement("h1");
          
    // Tạo text node
    var text = document.createTextNode("Học DOM Nodes");
          
    // Thêm nội dung HTML vào thẻ h1
    h1.appendChild(text);
          
    // Đưa thẻ h1 vào trong thẻ body
    document.getElementsByTagName('body')[0].appendChild(h1);
          
        </script>
```
<a name="3"></a>
### 3. DOM Node - Các phương thức khác:

<a name="3.1"></a>
#### 3.1 Phương thức appendChild():

Để bổ sung vào vị trí cuối cùng của đối tượng thẻ HTML nào đó. Ta có ví dụ:

```javascript
	<div id="TOP">Chào các bạn</div>
	<input type="button" value="click here" id="01"/> //tạo button
	<script language="javascript">
			var button = document.getElementById("01"); //lấy button
			button.addEventListener("click", function(){ //thêm sự kiện click cho button
			var h1 = document.createElement("h1"); //tạo thẻ h1 mới
			h1.innerHTML = "Thật bất ngờ" //thêm nội dung vào thẻ h1
			document.getElementById('TOP').appendChild(h1); //thêm thẻ h1 vào thẻ div có id=TOP
		});
	</script>
```

[1]

<a name="3.2"></a>
#### 3.2 Phương thức insertBefore():

- **Phương thức insertBefore()**: Được sử dụng để thêm vào phía trước 1 node nào đó. Có 2 tham số truyền vào `insertBefore(node_insert, node_child)` trong đó: 

	+ `node_insert`: là node bạn muốn thêm vào

	+ `node_child`: là node mà muốn thêm vào phía trước nó

**Ví dụ:**

```javascript
	<div id="TOP">
			<h4>Chào các bạn</h4>
			<h4>Một ngày vui vẻ</h4>
	</div>
	<input type="button" value="click here" id="01"/> 
	<script language="javascript">
			var button = document.getElementById("01"); //lấy button
			button.addEventListener("click", function(){ //thêm sự kiện click cho button
			var h1 = document.createElement("h1"); //tạo thẻ h1 mới
			h1.innerHTML = "Thật bất ngờ" //thêm nội dung vào thẻ h1
			var element = document.getElementById("TOP");
			var element_child = document.getElementsByTagName("h4")[1];
			element.insertBefore(h1,element_child);
		});
	</script>
```

[2]

<a name="3.3"></a>
#### 3.3 Phương thức removeChild():

Dùng để xóa 1 node con ra khỏi node hiện tại.

```javascript
	<div id="content">
		<h4>Chúc các bạn một buổi tối vui vẻ</h4>
	</div>
	<input type="button" value="delete" id="01"/>
	<script language="javascript">
		var button = document.getElementById("01");
		button.addEventListener("click", function(){
			var need_remove = document.getElementsByTagName("h4")[0];
			document.getElementById("content").removeChild(need_remove);
		});
	</script>
```
<a name="3.4"></a>
#### 3.4 Phương thức replaceChild():

Dùng để replace 1 node con nào đó bằng 1 node mới khác.

```javascript
	<div id="content">
          	<h5>chúc học bài vui vẻ</h5>
    </div>
      
    <input type="button" value="Replace" id="btn-replace"/>
      
    <script language="javascript">
    // Lấy button
    var button = document.getElementById("btn-replace");
          
    // Thêm sự kiện click cho button
    button.addEventListener("click", function(){
          	
    	// Tạo mới một thẻ
    	var p = document.createElement("h1");
    	p.innerHTML = "Xin chào!";
                
    	// Lấy thẻ cần replace
    	var replace = document.getElementsByTagName("h5")[0];
            
    	// Replace
    	document.getElementById("content").replaceChild(p, replace);
    });
     </script>
```
<a name="4"></a>
### Tài liệu tham khảo:

> [1] DOM Nodes. http://freetuts.net/dom-nodes-trong-javascript-383.html