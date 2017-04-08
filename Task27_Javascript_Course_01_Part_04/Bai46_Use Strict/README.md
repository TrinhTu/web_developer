## BÀI 46: USE STRICT LÀ GÌ? STRICT MODE TRONG JAVASCRIPT

> Tài liệu: Use Strict là gì? Strict Mode trong Javascript
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 08/04/2017

### Mục lục: 

- [1. Chế độ Strict Mode là gì?](#1)

- [2. Use Strict là gì?](#2)

	+ [2.1 Phạm vi Strict Mode toàn cục](#2.1)

	+ [2.2 Phạm vi strict Mode cục bộ](#2.2)

- [3. Ví dụ Use Strict trong Javascript](#3)

- [Tài liệu tham khảo](#4)

***

<a name="1"></a>
### 1. Chế độ Strict Mode là gì?

- Strict Mode là 1 khái niệm mới nhằm giải quyết các vấn đề mà lập trình viên hay mắc phải ví dụ như sử dụng biến mà chưa định nghĩa, quên đặt dấu chấm phẩy ở cuối mỗi đoạn code, có thể sử dụng tên những từ khóa để tạo tên biến.

<a name="2"></a>
### 2. Use Strict là gì?

- Use Strict là từ khóa khai báo sử dụng chế độ Strict Mode, nếu muốn sử dụng chế độ Strict Mode ở đâu thi đặt từ khóa "use strict" ở đó. Strict Mode có 2 phạm vi sử dụng là toàn cục và cục bộ. Toàn cục là đặt từ "use strict" ở ngoài hàm và nằm phía trên cùng của file --> tất cả các đoạn code bên dưới đều bị ảnh hưởng. Tính cục bộ tức là đặt "use strict" nằm trong 2 hàm nào đó thì phạm vi ảnh hưởng chỉ nằm trong hàm đó thôi.

<a name="2.2"></a>
#### 2.1 Phạm vi Strict Mode toàn cục:

- Trong ví dụ dưới đây chương trình bị sai bởi biến `domain` chưa được khởi tạo, tuy nhiên nếu bỏ `use strict` thì chương trình vẫn chạy bình thường.

```javascript
// Phía trên cùng của file
"use strict";
 
// Đoạn code này lỗi vì biến domain chưa được khởi tạo
domain = "https://freetuts.net";
 
// In ra màn hình
document.write(domain);
```

- Gom đoạn code vào trong 1 hàm.

```javascript
// Phía trên cùng của file
"use strict";
 
function show_domain(){
    // Đoạn code này lỗi vì biến domain chưa được khởi tạo
    domain = "https://freetuts.net";
 
    // In ra màn hình
    document.write(domain);
}
 
show_domain();
```

Chương trình sẽ bị lỗi bởi ta khai báo tính toàn cục cho chế độ Strict Mode.

<a name="2.2"></a>
#### 2.2 Phạm vi Strict Mode cục bộ:

- Sử dụng ví dụ trên khai báo ở trong phạm vi của hàm.

```javascript
function show_domain(){
    "use strict";    
}
 
// Đoạn code này lỗi vì biến domain chưa được khởi tạo
domain = "https://freetuts.net";
 
// In ra màn hình
document.write(domain);
```

- Đoạn chương trình trên vẫn hoạt động bình thường, tuy nhiên nếu sử dụng sai trong hàm đó thì chương trình sẽ không hoạt động.

```javascript
function show_domain(){
    "use strict";    
     
    // Đoạn code này lỗi vì biến domain chưa được khởi tạo
    domain = "https://freetuts.net";
 
    // In ra màn hình
    document.write(domain);
}
 
show_domain();
```

<a name="3"></a>
### 3. Ví dụ Use Strict trong Javascript:

Một số trường hợp bị lỗi khi chạy ở chế độ Strict mode:

- Sử dụng biến chưa định nghĩa

```javascript
"use strict";
 
// sai vì biến domain chưa được khởi tạo trừ trước
domain = 'freetuts.net';
```

- Không châps nhận delete biến: không thể xóa hàm và biến nếu chạy ở chế độ strict mode.

```javascript
"use strict";
 
var domain = 'freetuts.net'; 
 
// Sai vì không được delete
delete domain;
```

- Định nghĩa thuộc tính 2 lần: nếu trong 1 Object định nghĩa tên Key trùng sẽ bị lỗi.

```javascript
"use strict";
 
// Sai vì key email bị trùng
var info = {
    email : "thehalfheart@gmail.com",
    email : "freetuts.net@gmail.com"
};
```

- Khai báo tham số bị trùng: khai báo tham số trùng tên sẽ bị lỗi.

```javascript
"use strict";
 
// Sai vì tham số domain bị trùng
function show_domain(domain, domain){
    // do some thing
}
```

- Lỗi literals và escape với number: không được sử dụng literals và escape với kiểu number.

```javascript
"use strict";

//sai 
var x = 0100;
var y = \0100;
```

- Khai báo tên biến trùng với Key

```javascript
// Lỗi: Trùng hàm eval
var eval = 12;
 
// Lỗi: từ khóa arguments không được sử dụng làm tên biến
var arguments = 12;
 
// Lỗi: Từ khóa delete là khóa nên không được sử dụng làm tên biến
var delete = 123;
```

- Ngoài ra không được sử dụng tên biến với các từ khóa sau: `implements`, `interface`, `package`, `private`, `protected`, `public`, `static`, `yield`.

<a name="4"></a>
### Tài liệu tham khảo:

> [1] Use Strict là gì? Use Strict Mode trong Javascript. https://freetuts.net/use-strict-la-gi-strict-mode-trong-javascript-407.html

