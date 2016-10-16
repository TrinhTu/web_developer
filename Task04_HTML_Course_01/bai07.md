###Bài 3: Thẻ tạo liên kết và liên kết neo

> Tài liệu: Thẻ tạo lên kết và liên kết neo
> 
> Thực hiện: **Lê Tú Trinh**
> 
> Cập nhật lần cuối: **15/10/2016**

####Mục lục

[1. Thẻ tạo liên kết](#01)

[2. Liên kết neo (Anchor Link)](#02)

###Nội dung

<a name="01"></a>
####1. Thẻ tạo liên kết:

Thẻ tạo liên kết hay còn gọi là link trong văn bản của mình là cặp thẻ `<a>` `</a>`. Trong cặp thẻ này có những tham số quan trọng như :

- `href`: là liên kết cần trỏ về, có thể là đường dẫn thư mục hay địa chỉ website

- `title`: là tham số thiết lập tiêu đề, tiêu đề sẽ hiển thị như 1 thông tin khi rê chuột vào liên kết

- `target`: xác định nơi mở tài liệu, nó có các giá trị như là `_blank` (mở tài liệu trên cửa sổ mới) ,`_self` ( mở tài liệu trên cửa sổ hiện tại, nếu không khai báo thuộc tính `target` thì nó sẽ sử dụng giá trị này làm mặc định), `_top` ( mở tài liệu trong nội dung trang hiện tại) ,`parent` ( mở tài liệu trên khung trình duyệt mẹ của nó).

![anh](http://imageshack.com/a/img923/8646/m2OyDE.png)

Bằng cách khai báo như trên thì khi chạy bằng trình duyệt sẽ thu được result

![anh](http://imageshack.com/a/img923/8974/ibzsgv.png)

Result là 1 liên kết khi nhấn vào liên kết đó là sẽ mở ra cửa sổ như `href` khai báo.

<a name="02"></a>
####2. Liên kết neo (Anchor Link):

Liên kết neo nghĩa là 1 liên kết trong siêu văn bản sẽ dẫn đến 1 vị trí đặt biệt trong cùng tài liệu mà không phải tải lại hoặc mở 1 tài liệu mới. Một liên kết neo có 2 phần đó là 

- Khu vực được neo khai báo bằng thẻ bất kì với thuộc tính `id` :  ví dụ như `<p id="noi_dung"></p>`

- Liên kết neo được khai báo bằng thẻ `<a>` nhưng có thuộc tính `href` giá trị có dấu # và tên id của địa chỉ cần truy cập đến. Ví du: `<a href="#noi_dung">xem noi dung</a>`

![anh](http://imageshack.com/a/img923/6427/FyO6IG.png)

Result sau khi đọc bởi trình duyệt thì tại chỗ tiêu đề mà chúng ta `href` đã trở thành 1 liên kết neo mà khi ta trỏ vào đó nó sẽ tự nhảy xuống chỗ nội dung mà ta đặt liên kết.

![anh](http://imageshack.com/a/img922/3476/LsuCGY.png)



