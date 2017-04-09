### Bài 9: Tạo form nhập liệu

> Tài liệu: Tạo form nhập liệu
> 
> Thực hiện: **Lê Tú Trinh**
> 
> Cập nhật lần cuối: **16/10/2016**

#### Mục lục

[1. Các thuộc tính trong thẻ `<form>`](#01)

[2. Các thuộc tính trong thẻ `<input>`](#02)

### Nội dung

Để tạo form chúng ta sử dụng cặp thẻ `<form>` `</form>` thẻ này chứa vài thuộc tính quan trọng và nội dung bên trong cặp thẻ đó là các thẻ `<input>` để khai báo các trường nhập liệu

<a name="01"></a>
#### 1. Các thuộc tính trong thẻ `<form>`:

- `action` : đường  dẫn đến 1 trang xử lí dữ liệu sau khi người dùng ấn nút gởi dữ liệu

- `method`: phương thức gởi dữ liệu

- `name`: tên của form

Tạm thời thì chưa cần quan tâm đến 3 thuộc tính đó nhưng cần phải khai báo chúng khi tạo form

![anh](http://i.imgur.com/s8sXGsV.png)

<a name="02"></a>
#### 2. Các thuộc tính trong thẻ `<input>`:

Thẻ này đại diện cho các trường nhập dữ liệu, mỗi thẻ là 1 trường khác nhau, kiểu nhập liệu của mỗi thẻ là khác nhau dựa vào thuộc tính `type` bên trong nó, hiện nay HTML hỗ trợ đến 23 kiểu nhập liệu tương ứng với 23 giá trị của thuộc tính `type`

Danh sách các giá trị của thuộc tính type:

- button

- checkbox

- color

- date

- datetime

- datetime-local

- email

- file

- hidden

- image

- month

- number

- password: thường sử dụng ( trường nhập mật khẩu nó sẽ tự động mã hóa mật khẩu bằng kí tự *)

- radio

- range

- reset

- search

- submit: thường sử dụng ( trường tạo nút gởi dữ liệu đi)

- tel

- text: thường sử dụng ( trường nhập liệu dạng chữ và số)

- time

- url

- week

[Xem thêm về thuộc tính của thẻ `<input>`](http://www.w3schools.com/tags/tag_input.asp)

Đây là ví dụ cho những thuộc tính vừa nói:

![anh](http://i.imgur.com/xMACVRR.png)

Thu được kết quả như sau:

![anh](http://i.imgur.com/IQBvAjy.png)

### Tài liệu tham khảo

[Học HTML cơ bản toàn tập](http://thachpham.com/web-development/html-css/gioi-thieu-serie-hoc-html-co-ban.html)

[Video hướng dẫn học HTML cơ bản](https://www.youtube.com/playlist?list=PLl4nkmb3a8w135_M4YRPzYD9_6tERz3ce)






