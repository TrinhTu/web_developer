## BÀI 47: ĐỐI TƯỢNG (OBJECT) TRONG JAVASCRIPT

> Tài liệu: Đối tượng (Object) trong javascript
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 08/04/2017

### Mục lục: 

- [1. Đối tượng (Object) là gì?](#1)

    + [1.1 Khởi tạo đối tượng](#1.1)

- [2. Thuộc tính và phương thức đối tượng](#2)

    + [2.1 Thuộc tính](#2.1)

    + [2.2 Phương thức](#2.2)

    + [2.3 Xem danh sách phương thức và thuộc tính](#2.3)

- [3. Thao tác với thuộc tính và phương thức đối tượng](#3)

    + [3.1 Gán giá trị cho thuộc tính](#3.1)

    + [3.2 Lấy giá trị của thuộc tính](#3.2)

    + [3.3 Gọi phương thức](#3.3)

- [4. Mảng chứa đối tượng - đối tượng chứa đối tượng](#4)

    + [4.1 Đối tượng chứa đối tượng](4.1)

    + [4.2 Mảng chứa đối tượng](#4.2)

- [Tài liệu tham khảo](#5)

***

<a name="1"></a>
### 1. Đối tượng (Object) là gì?

- Đối tượng thể hiện cho 1 đối tượng cụ thể và có sẵn ví dụ như Date, Number... Ngoài các đối tượng trên thì lập trình viên còn có thể tạo 1 đối tượng theo ý mình dựa vào yêu cầu, Ví dụ cần tạo đối tượng chuyên xử lí vấn đề về bình luận cho trang tin tức thì tạo đối tượng Commnet.

<a name="1.1"></a>
#### 1.1 Khởi tạo đối tượng:

Có 2 cách tạo đối tượng:

- **Cách 1**: Sử dụng từ khóa `new Object()`

`var Comment = new Object();`

- **Cách 2**: Sử dụng từ khóa `{}`

`var Comment = {};`

<a name="2"></a>
### 2. Thuộc tính và phương thức đối tượng:

Mỗi đối tượng sẽ bao gồm các thuộc tính và phương thức.

<a name="2.1"></a>
#### 2.1 Thuộc tính

- Thuộc tính làm những đặc điểm (biến) cần được lưu trữ trong đối tượng, ví dụ với đối tượng Comment thì cần các thuộc tính sau: title, content, fullname, email...

Có 3 cách khai báo:

- **Cách 1**: Sử dụng từ khóa `new Object`

```javascript
// Khởi tạo
var Comment = new Object();
 
// Thêm thuộc tính
Comment.title = '';
Comment.content = '';
Comment.fullname = '';
Comment.email = '';
```

- **Cách 2**: Sử dụng từ khóa `{}` và thêm thuộc tính vào lúc khai báo.

```javascript
// Khởi tạo
var Comment = {
    title : "",
    content : "",
    fullname : "",
    email : ""
};
```

- **Cách 3**: Sử dụng từ khóa `{}` và thêm thuộc tính sau đó

```javascript
// Khởi tạo
var Comment = {};
 
// Thêm thuộc tính
Comment.title = '';
Comment.content = '';
Comment.fullname = '';
Comment.email = '';
```

<a name="2.2"></a>
#### 2.2 Phương thức

- Phương thức là những hành động (hàm) của đối tượng. Ví dụ trong đối tượng Comment cần hai phương thức là: 

    + addComment()
    
    + validateComment()

Có 3 cách khai báo thuộc tính:

- **Cách 1**: Sử dụng từ khóa `new Object()`

```javascript
// Khởi tạo
var Comment = new Object();
 
// Thêm phương thức
Comment.addComment = function(){
    // do some thing
};
 
Comment.validateComment = function(){
    // do some thing
};
```

- **Cách 2**: Sử dụng từ khóa `{}` và thêm phương thức ngay lúc khai báo

```javascript
// Khởi tạo
var Comment = {
    addComment : function(){
        // do some thing
    },
    validateComment : function(){
        // do some thing
    }
};
```

- **Cách 3**: Sử dụng từ khóa `{}` và thêm phương thức sau đó

```javascript
// Khởi tạo
var Comment = {};
 
// Thêm phương thức
Comment.addComment = function(){
    // do some thing
};
 
Comment.validateComment = function(){
    // do some thing
};
```

<a name="2.3"></a>
#### 2.3 Xem danh sách phương thức và thuộc tính

- Để xem và debug đối tượng thì nên sử dụng Firebug

<a name="3"></a>
### 3. Thao tác với thuộc tính và phương thức đối tượng

- Có 2 cách sử dụng đối tượng là gọi và gán dữ liệu cho thuộc tính và phương thức.

<a name="3.1"></a>
#### 3.1 Gán giá trị cho thuộc tính

- Để gán giá trị cho thuộc tính thực hiện bằng cách sử dụng toán tử = giống như cách gán giá trị cho biến.

`Comment.title = "Tiêu đề bình luận";`

- Gọi từ một hàm trong đối tượng thì có thể sử dụng từ khóa `this`

```javascript
var Comment = {
    title : "",
    addComment : function(){
        this.title = "Tiêu đề bình luận";
    }
};
```

<a name="3.2"></a>
#### 3.2 Lấy giá trị của thuộc tính

- Thực hiện tương tự như biến.

`var title = Comment.title;`

- Gọi từ một hàm trong đối tượng thì có thể sử dụng từ khóa `this`

```javascript
var Comment = {
    title : "",
    addComment : function(){
        var title = this.title;
    }
};
```

<a name="3.3"></a>
#### 3.3 Gọi phương thức

`comment.addComment();`

- Gọi trong hàm của đối tượng.

```javascript
var Comment = {
    title : "",
    addComment : function(){
        this.validateComment();
    },
    validateComment : function(){
        // do some thing
    }
};
```

<a name="4"></a>
### 4. Mảng chứa đối tượng - đối tượng chứa đối tượng

- Mỗi đối tượng (object) trong Javascript có thể chứa các đối tượng khác hoặc một mảng có thể chứa các đối tượng.

<a name="4.1"></a>
#### 4.1 Đối tượng chứa đối tượng

- **Ví dụ 1**: Gom các thuộc tính của Comment vào một đối tượng `Info`.

```javascript
var Comment = {
    info : {
        title : "",
        content : "",
        email : "",
        fullname : ""
    }
};
```

- **Ví dụ 2**: Gom các phương thức (hàm) của Comment vào đối tượng `func`.

```javascript
var Comment = {
    func : {
        addComment : function(){
            // Something
        },
        validateComment : function(){
            // Something
        }
    },
};
```

- Để truy xuất tới các thuộc tính và phương thức sử dụng dấu chấm và bổ sung thêm một cấp nữa.

```javascript
Comment.info.title = "Comment tại freetuts.net";
Comment.func.addComment();
```

<a name="4.2"></a>
#### 4.2 Mảng chứa đối tượng

- Để gán giá trị là một đối tượng vào mảng cũng tương tự như gán các giá trị khác.

```javascript
// Đối tượng Comment
var Comment = {
    title   : "",
    content : "",
    email   : "",
    fullname : ""
};
 
// Khởi tạo mảng
var Comments = [];
 
// Gán giá trị cho phần tử mảng
Comments[0] = Comment;
 
// Gọi tới thuộc tính
Comments[0].title = "Tiêu đề bình luận";
alert(Comments[0].title);
```

Hoặc:

```javascript
// Khởi tạo mảng
var Comment = [{
    title   : "",
    content : "",
    email   : "",
    fullname : "" 
}];
 
// Sử dụng
Comment[0].title = "Tiêu đề bình luận";
alert(Comment[0].title);
```

<a name="5"></a>
### Tài liệu tham khảo:

> [1] Đối tượng (Object) trong Javascript. https://freetuts.net/doi-tuong-object-trong-javascript-408.html