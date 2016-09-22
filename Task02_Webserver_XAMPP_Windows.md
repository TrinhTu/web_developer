## Cài đặt webserver XAMPP trên Windows ##


----------
**Thực hiện**: Lê Tú Trinh
**Ngày cập nhập**: 23/09/2016


----------

 **I. Mục lục**:
---------

 1. Tìm hiểu về Localhost
 2.  Hướng dẫn cài đặt Webserver XAMPP trên Windows
 3. Thực hành cài đặt Webserver trên máy tính
 4. Tạo 1 trang "index.php"
 5. Truy cập được từ trình duyệt "http://127.0.0.1" 

 **II. Nội dung**
---------

 **1. Localhost là gì ?**

		> Localhost là một máy tính chủ được vận hành trên máy tính của bạn Localhost bao gồm nhiều ứng dụng đi kèm với nhau và tất cả các ứng dụng đó sẽ kết hợp với nhau để tạo ra một môi trường có thể chạy mã nguồn WordPress trên máy tính của chính bạn bao gồm:

>  - Phần mềm Webserver tên Apache, đây là webserver thông dụng nhất.
 - Phần mềm PHP để xử lý mã PHP vì WordPress viết bằng ngôn ngữ PHP.
 - Phần mềm MySQL Server để lưu trữ và xử lý cơ sở dữ liệu, do WordPress sử dụng MySQL làm nền tảng cơ sở dữ liệu. Cơ sở dữ liệu thường được mình viết theo chữ tiếng Anh là database.
 - Phần mềm PHPMyAdmin để xem và quản lý cơ sở dữ liệu MySQL.



----------

> Khi cài đặt Localhost vào máy tính rồi, thì máy tính của bạn đã có một phần mềm Webserver để chạy ứng dụng website với địa chỉ là IP là http://127.0.0.1. Đây là địa chỉ IP dạng localhost, ngoài ra bạn cũng có thể chạy localhost với đường dẫn là http://localhost.


----------

**2 .Hướng dẫn cài đặt localhost cho Windows,và thực hành trên máy tính**
	
> Nếu sử dụng windows thì dùng phần mềm XAMPP, vào trang web và download [tai_day](https://www.apachefriends.org/download.html) 
> Nên sử dụng phần mềm XAMPP vì nó hoàn toàn miễn phí thích hợp cho người mới học muốn tìm hiểu về chúng, ngoài ra có còn dễ sử dụng và hỗ trợ các hệ điều hành thông dụng như Windows, Linux, Mac
> Sau khi download thành công ta tiến hành cài đặt phần mềm: click next để cài đặt, nên để mặc định là c:\xampp có nghĩa là xampp này sẽ được lưu trong ổ đĩa C  
>  ![hinh_anh](http://blogloi.com/wp-content/uploads/2015/07/cai-dat-localhost-xampp-03.gif)

Tiếp tục click next , bỏ chọn
![hinh_anh](http://thachpham.com/wp-content/uploads/2013/09/cai-dat-xampp-04.jpg)
sau đó bấm finish để kết thúc phần cài đặt.


----------
Để khởi động localhost thì đầu tiên cần khởi động apache và MySQL
![hinh_anh](http://itvinh.com/wp-content/uploads/2015/05/panelxampp.png)
Nếu máy bạn có cài đặt tường lửa từ Windows hay từ một phần mềm Antivirus nào khác thì hãy tắt nó đi vì có thể nó sẽ chặn cổng 80 hoặc các ứng dụng webserver. Nếu sử dụng skype thì đổi cổng mạng bất kì cho nó, vì skype chiếm cổng 80, mà đây là cổng mặc định của webserver, hoặc có thể bạn sẽ vào config->apache(httpd.conf) sẽ hiện ra 1 bảng rồi kéo xuống chỗ listen 80 để đổi thành cổng bất kì khác
![anh](http://i.imgur.com/4dY5oJq.png)

Đã hoàn thành xong phần cài đặt localhost trên máy tính.


**4. Tạo 1 trang "index.php"**
Vào ổ đĩa C vào **xampp**->**htdocs** tạo 1 thư mục với tên bất kì

![anh](http://imageshack.com/a/img922/7930/FyjxTA.png)
trong thư mục TuTrinh tạo 1 file trống bất kì ''ahihi"
sau đó mở notepad lên ghi lại đoạn 

    <?php
    echo '<h3>It works</h3>';
    ?>


----------
rồi lưu lại trong C->xampp->htdocs->tutrinh->ahihi
sau đó truy cập lại vào địa chỉ localhost:8888/TuTrinh thì nó sẽ hiển thị như sau:
![anh](http://imageshack.com/a/img921/1627/YxtCpk.png)
 
------------
 **III. Kết luận**
---------

Tại sao bạn lại nên dùng XAMPP?

 - Không mất chi phí
 - Hỗ trợ đa hệ điều hành
 - Dễ sử dụng nhất
 - Ít gặp lỗi
------------
 **IV. Tài liệu tham khảo**
---------
(http://thachpham.com/thu-thuat/cai-dat-localhost-xampp.html)
 
