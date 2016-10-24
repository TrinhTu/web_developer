###Bài 2: Nhúng CSS vào Website

> Tài liệu: Nhúng CSS vào Website
> 
> Thực hiện: **Lê Tú Trinh**
> 
> Cập nhật lần cuối: **17/10/2016**

####Mục lục

[1. Cách nhúng CSS với Inline Styles](#01)

[2.Cách nhúng CSS với External Styles](#02)

[3. Nhúng tập tin CSS vào bên trong tập tin CSS](#03)

###Nội dung

Trước khi viết CSS để CSS có thể thực thi trên Website hoặc  tài liệu HTML thì đầu tiên phải nhúng CSS vào trong Website, có 2 cách nhúng CSS vào trong Website đó là:

- Kiểu 1: Inline Styles là chèn CSS thẳng vào trong tài liệu HTML

- Kiểu 2: Extenal Styles

<a name="01"></a>
####1. Cách nhúng CSS với Inline Styles:
 
 Trong thẻ `<head>` thêm cặp thẻ `<style>` trong thẻ `<style>` này có có 1 tham số tên là `type` và có giá trị là **text/css**

![anh](anh1.png)

![anh](anh2.png)

<a name="02"></a>
####2. Cách nhúng CSS với External Styles:

Tạo ra 1 tập tin CSS với tên bất kì có thể dùng bất cứ chường trình soạn thảo văn bản nào để tạo sau đó dán 1 đoạn CSS đơn giản vào như thế này:

```
p {
	color: blu;
}
```

Và lưu lại với dạng `tên tập tin.css` 

Và cuối cùng chèn CSS vào trong HTML sử dụng thẻ `<link>` thẻ này không có thẻ đóng và được đặt trong cặp thẻ `<head>`, cú pháp ví dụ như sau:

`<link rel="stylesheet" href="name.css" />`

`rel` là khai báo loại tập tin nhúng, `href` là đường dẫn đến tập tin .css cần nhúng vào. Ta có ví dụ:

![anh](anh3.png)

Và sau khi đã nhúng CSS vào trong tài liệu HTML ta có result như sau: 

![anh](anh4.png)

Nếu như tạo tập tin **css** mà lưu không cùng thư mục thì nên nhớ thêm đường dẫn thư mục vào `href`

<a name="03"></a>
####3. Nhúng tập tin CSS vào bên trong tập tin CSS:

Nếu có 3 tập tin CSS mà không muốn thêm cả 3 vào website mà chỉ muốn thêm 1 tập tin vào thì có thể sử dụng từ khóa `@import` và các từ khóa này phải đặt ở đầu tập tin .css ( không bao gồm các đoạn comment)

Ví dụ có thể nhúng tập tin `hoc.css` vào trong tập tin `style.css` bằng cách chèn đoạn này vào tập tin `style.css`

`@import "hoc.css";`



