##Bài 24: BIẾN TOÀN CỤC VÀ BIẾN CỤC BỘ TRONG JAVASCRIPT

>Tài liệu: Biến toàn cục và biến cục bộ trong javascript
>
>Người thực hiện: Lê Tú Trinh
>
>Cập nhập lần cuối: 07/12/2016

### Mục lục:

[1. Biến cục bộ trong javascript](#1)

[2. Biến toàn cục trong javascript](#2)

[3. Một số ví dụ](#3)

###Nội dung:

<a name="1"></a>
####1. Biến cục bộ trong javascript:

Là biến nằm bên trong 1 hàm nào đó, không sử dụng được nếu ở bên ngoài hàm đó.

Ví dụ: 

```javascript
function add_comment()
{
	var comment = "Nội dung";
	// đoạn code này đúng là biến comment đã được định nghĩa
	alert(comment);
}
alert(comment); //đoạn code này sai vì biến comment chưa được định nghĩa
```

<a name="2"></a>
####2. Biến toàn cục trong javascript:

Biến toàn cục là biến khai báo bên ngoài và không nằm trong 1 hàm cụ thể nào.

Ví dụ:

```javascript
//biến toàn cục
var comment = "Nội dung";
//hàm sử dụng biến toàn cục
function add_comment()
{
	alert(commnet);
}
//in biến toàn cục
alert(comment); //đoạn code này vẫn đúng vì biến comment đã được định nghĩa
```

<a name="3"></a>
####3. Một số ví dụ:

```javascript
  <script language="javascript">
          
          // Biến toàn cục
          var comment = "Nội dung comment toàn cục";
          
           // Hàm có sử dụng biến toàn cục
          function add_comment()
          {
             var comment = "Nội dung comment cục bộ";
          	alert(comment);
          }
          
          // Gọi fuction comment
          add_comment();
          // In biến toàn cục
          alert(comment);
          
    </script>
```

Nếu không sử dụng từ khóa `var` để tạo tên biến thì nó sẽ sử dụng biến toàn cục. Nên mọi thay đổi bên trong hàm đó sẽ ảnh hưởng ra ngoài hàm.

Xem hiển thị kết quả: http://tutrinh01.chuyengiaseoweb.net/javascript24.html

Ví dụ 2: Không sử dụng từ khóa `var` cho biến cục bộ:

```javascript
 		  // Biến toàn cục
          var comment = "Nội dung chưa bị thay đổi";
          
           // Hàm có sử dụng biến toàn cục
          function add_comment()
          {
            comment = "Nội dung đã bị thay đổi";
            alert(comment);
          }
          
          // Gọi fuction comment
          add_comment();
           // In biến toàn cục
          alert(comment);
```

Xem kết quả: http://tutrinh01.chuyengiaseoweb.net/javascript.html
          
