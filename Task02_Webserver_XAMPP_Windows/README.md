## Cài đặt webserver XAMPP trên Windows

> Tài liệu: Cài đặt webserver XAMPP trên Windows
> 
> Thực hiện: Lê Tú Trinh
> 
> Cập nhập lần cuối:26/09/2016

###Mục lục:

1. [Tìm hiểu về Localhost](#localhost) 

2. [Hướng dẫn tải về Webserver XAMPP trên Windows](#caidat)

3. [Thực hành cài đặt Webserver trên máy tính](#thuchanh)

4. [Tạo 1 trang "index.php"](#taotrang)

5. [Truy cập được từ trình duyệt "http://127.0.0.1"](#truycap) 

### II. Nội dung.

<a name="localhost"></a>
#### 1. Localhost là gì ?

> Localhost là một máy tính chủ được vận hành trên máy tính của bạn Localhost gồm nhiều ứng dụng đi kèm với nhau và tất cả các ứng dụng đó sẽ kết hợp với nhau để tạo ra mã nguồn để chạy WordPress trên máy tính của người dùng, bao gồm:

 -  Phần mềm Webserver trên Apache

 - Phần mềm PHP để xử lý mã PHP vì WordPress viết bằng ngôn ngữ PHP

 - Phần mềm MySQL server để xử lý và lưu trữ dữ liệu, do WordPress sử dụng MySQL làm nền tảng cơ sở dữ liệu(database)

 - Phần mềm PHPMyAdmin để xem và quản lý cơ sở dữ liệu MySQL.
 
> Khi cài đặt Localhost vào máy tính rồi, thì máy tính của bạn đã có một phần mềm Webserver để chạy ứng dụng website với địa chỉ là IP là http://127.0.0.1. Đây là địa chỉ IP dạng localhost, ngoài ra bạn cũng có thể chạy localhost với đường dẫn là http://localhost.

----------
<a name="caidat"></a>
#### 2 .Hướng dẫn cài đặt localhost cho Windows,và thực hành trên máy tính
	
- Nếu sử dụng windows thì dùng phần mềm XAMPP, vào trang web và download [tai_day](https://www.apachefriends.org/download.html)

Nên sử dụng phần mềm XAMPP vì nó hoàn toàn miễn phí thích hợp cho người mới học muốn tìm hiểu về chúng, ngoài ra có còn dễ sử dụng và hỗ trợ các hệ điều hành thông dụng như Windows, Linux, Mac. Tuy XAMPP chỉ hỗ trợ cho phiên bản 32bit nhưng máy 64 bit vẫn có thể sử dụng bình thường.

Trước khi tải về bạn cần làm 1 số thao tác sau:

- Nếu như máy tính có cài đặt Skype thì nên vào cài đặt để chỉnh sửa cổng cho Skype, bởi vì mặc định của Skype là chiếm cổng 80, mà cổng 80 là cổng mặc định của Webserver. Bởi vậy nên cần vào **Skype->tool->connection option** bỏ chọn *Use port 80 and 443* và nhập 1 cổng bất kì khác để Skype sử dụng

- Nếu máy tính đang bật chức năng User Account Control thì nên tắt nó đi, bằng cách vào **Control panel** tìm kiếm **control user** và khi nó hiện ra bạn sẽ chọn bên dưới mục Action Center chọn **change user account settings** và kéo thanh xuống hết mức như hình:

![hinh](http://i.imgur.com/xybhPq7.png)

 
- Còn nếu như bật tường lửa và các phần mềm antivirus thì nên tắt đi vì nó có thể chặn các phần mềm webserver và cổng 80, cách tắt tường lửa nếu chưa biết có thể xem [tat_tuong_lua](http://quantrimang.com/cach-tat-bat-windows-firewall-trong-windows-7-68908)
 
<a name="thuchanh"></a>
### Thực hành cài đặt XAMPP trên Windows

 1.  Bấm vào [đây](https://www.apachefriends.org/download.html) để download XAMPP về máy, mình sẽ tải phiên bản có PHP là 5.6.24
 
![anh](http://imageshack.com/a/img923/879/wKqiqA.png)
  
Nếu như ở phía trên bạn chưa tắt chức năng UAC  thì nó sẽ hiện ra như thế này:

![anh](http://i.imgur.com/UOsReSn.png)

Nếu như vậy nên xem lại phần phía trên để xem hướng dẫn để tắt UAC đi.

2.Sau khi download thành công ta tiến hành cài đặt phần mềm.

![anh](http://imageshack.com/a/img922/1126/2l02Xc.png)

click next để tiến hành cài đặt

![anh](http://imageshack.com/a/img924/6176/RTe3Ku.png)

Click chọn tất cả để cài đặt, sau đó tiếp tục click next tới chỗ

![anh](http://imageshack.com/a/img922/1719/WtiMiA.png)

Đó có nghĩa là XAMPP được tải về sẽ được lưu vào ổ đĩa C, mặc định là như vậy nên không nên sửa lại

Tiếp tục click next , bỏ chọn

![hinh_anh](http://thachpham.com/wp-content/uploads/2013/09/cai-dat-xampp-04.jpg)

Xong phần cài đặt để tải về, nó sẽ hiện lên như sau, bấm click chọn vào bấm finish để kết thúc phần tải về

![hinh_anh](http://imageshack.com/a/img923/9591/tuxliL.png)

3. Để khởi động localhost thì đầu tiên cần khởi động apache và MySQL. 

![anh](http://imageshack.com/a/img923/4477/MQRWXD.png)

Bấm vào start để khởi động apache và MySQL, **lưu ý** nếu như phía trên bạn không đổi cổng cho skype  hay vì lý do gì đó mà cổng 80 của bạn bị chặn nên bạn sẽ không thể khởi động được Apache thì cũng còn cách khác là bạn có thể đổi cổng cho Apache bằng cách bấm vào **config** và chọn như hình:

![anh](http://imageshack.com/a/img923/9844/2jBEW7.png)

Khi đó sẽ hiện ra 1 notepad và kéo xuống tìm chỗ **listen 80** và sửa lại thành cổng bất kì sau đó lưu lại và start để bật Apache lên lại

![anh](http://imageshack.com/a/img924/1708/pgX4yX.png)

Khi khởi động thành công thì 2 ứng dụng đó sẽ có màu xanh

![anh](http://imageshack.com/a/img924/1047/K5BOGv.png)
Đã hoàn thành xong phần cài đặt localhost trên máy tính.

<a name="taotrang"></a>
###4. Tạo 1 trang "index.php"
Vào ổ đĩa C vào **xampp**->**htdocs** tạo 1 thư mục với tên bất kì

![anh](http://imageshack.com/a/img922/7930/FyjxTA.png)

Mình sẽ tạo thư mục mới với tên của minh **TuTrinh**, sau đó mở notepad lên và paste đoạn code này vào:

    <?php
    echo '<h3>It works</h3>';
    ?>

Rồi lưu lại trong  với tên là **index.php** trong C->xampp->htdocs->tutrinh->index.php. Sau đó truy cập lại vào địa chỉ  thì nó sẽ hiển thị như sau:

![anh](http://imageshack.com/a/img923/3888/aJrYko.png)

<a name="truycap"></a>
### 5. Truy cập được từ trình duyệt (http://127.0.0.1/)

Vì mình đổi cổng cho Apache nên việc truy cập vào trình duyệt này cũng có 1 chút thay đổi, nên thay vì truy cập vào địa chỉ 127.0.0.1 thì mình sẽ truy cập vào địa chỉ là http://127.0.0.1:8888/TuTrinh/ sẽ được kết quả:

![anh](http://imageshack.com/a/img922/6799/u7C37g.png)

Tại sao bạn lại nên dùng XAMPP?

- Không mất chi phí
- Hỗ trợ đa hệ điều hành
- Dễ sử dụng nhất
- Ít gặp lỗi

### Tài liệu tham khảo

(http://thachpham.com/thu-thuat/cai-dat-localhost-xampp.html)
 
