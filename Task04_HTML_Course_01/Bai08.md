###Bài 8: Chèn tập tin kĩ thuật số vào Web

> Tài liệu: Chèn tập tin kĩ thuật số vào Web
> 
> Thực hiện: **Lê Tú Trinh**
> 
> Cập nhật lần cuối: **16/10/2016**

####Mục lục

[1. Chèn ảnh vào HTML](#01)

[2. Chèn video](#02)

[3. Chèn âm thanh, nhạc](#03)

[4. Chèn đối tượng kĩ thuật số với thẻ `object`](#04)

[5. Nhúng tài liệu HTML vào Web](#05)

###Nội dung

<a name="01"></a>
####1. Chèn ảnh vào HTML:

Để chèn ảnh vào HTML chúng ta sử dụng thẻ `img` với các tham số bắt buộc, và thẻ này không có thẻ đóng. Thẻ `img` có các thuộc tính sau:

- `src`: là đường dẫn đến tập tin hình ảnh, liên kết hình ảnh phải là 1 liên kết trực tiếp.

- `alt`: đoạn mô tả hình ảnh mà không hiển thị ra

- `title`: tiêu đề của hình ảnh mà khi rê chuột vào nó sẽ hiển thị ra

- `width`: chiều rộng của hình ảnh sao cho phù hợp

- `height`: là chiều cao của ảnh, nên để **auto** để tự động chỉnh sao cho phù hợp với chiều rộng.

![anh](http://i.imgur.com/qfDGcQr.png)

![anh](http://i.imgur.com/Sc74xzt.png)

<a name="02"></a>
####2. Chèn video:

Sử dụng thẻ `<video>` `</video>` trong HTML5. Trong `video` còn có các thuộc tính như `width` là chiều rộng video, `height` chiều dài, ngoài ra còn 1 thẻ mà chỉ có trong  HTML5 nhưng chúng ta vẫn có thể sử dụng được đó là thẻ `controls` để hiển thị lên các nút lệnh tùy chỉnh video.

Trong thẻ `video` còn có 1 thẻ nữa là thẻ `<source>` với các thuộc tính nhằm khai báo đường dẫn đến video. Để đảm bảo tất cả các trình duyệt có thể đọc được, chỉ nên chèn video định dạng MP4.

![anh](http://i.imgur.com/WowRhgl.png)

![anh](http://i.imgur.com/1pXIbjb.png)

Còn nếu muốn chèn video trên **Youtube** thì chỉ cần vào **chia sẻ**->**nhúng** và copy mã đó bỏ vào là xong, ví dụ:

![anh](http://i.imgur.com/NC3d0rd.png)

và xong khi tải lên đọc bằng trình duyệt:

![anh](http://i.imgur.com/zQ0FLor.png)

<a name="03"></a>
####3. Chèn âm thanh, nhạc:

Giống như thẻ `<video>` để chèn âm thanh nhạc sử dụng thẻ `<audio>`

![anh](http://i.imgur.com/6F4xA0Z.png)

![anh](http://i.imgur.com/64vvMaT.png)

<a name="04"></a>
####4. Chèn đối tượng kĩ thuật số với thẻ `object`:

Ngoài các thẻ đặc trưng cho từng loại tập tin ở trên thì bạn còn có một cách khác để chèn các đối tượng kỹ thuật số vào tài liệu HTML đó là dùng thẻ `<object>`, đây là một thẻ có thể giúp bạn chèn các loại đối tượng kỹ thuật số như Flash, Java, Audio, Video, PDF, ActiveX. Nhưng thông thường thì các loại mã nhúng của một số website cho phép sử dụng mã nhúng như Youtube họ sẽ dùng thẻ này để bạn chèn đối tượng vào web.

Thẻ này có khá nhiều thuộc tính nên bạn có thể tham khảo [thêm](http://www.w3schools.com/tags/tag_object.asp)

<a name="05"></a>
####5. Nhúng tài liệu HTML vào Web:

Nếu muốn nhúng thẳng 1 trang nào đó vào tài liệu HTML có thể sử dụng thẻ `<iframe>`

![anh](http://i.imgur.com/Rsyjjin.png)

Trong thẻ `<iframe>` có các thuộc tính như 

- **src** là đường dẫn trang mà bạn muốn nhúng vào bài.

- **width** chiều rộng của trang đó

- **height** chiều dài trang hiển thị

![anh](http://i.imgur.com/S8oY5At.png)

Ngoài ra bạn có thể tạo 1 liên kết khác trong thẻ `<iframe>` bằng cách sử dụng thẻ `<a>` và các thuộc tính **target**, **name**, **href**.

Cú pháp như sau:

![anh](http://i.imgur.com/DcttNwE.png)

Nhớ phải thêm thuộc tính `name` vào bên dưới sao cho nôi dung trùng với phần `target`

![anh](http://i.imgur.com/vaH9dhz.png)





