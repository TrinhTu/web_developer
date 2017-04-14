## Bài 2: CÀI ĐẶT HỆ ĐIỀU HÀNH LINUX

> Tài liệu: Cài đặt hệ điều hành Linux
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 13/04/2017

### Mục lục:

[1. Chế độ cài đặt](#1)

[2. Các bước cài đặt](#2)

[3. Cài đặt Fedora for Linux 25.0](#3)

[Tài liệu tham khảo](#4)

***

<a name="1"></a>
### 1. Chế độ cài đặt:

- Các bản phân phối có 1 số chế độ cài đặt

- Chế độ đồ họa (mặc định) - quá trình cài đặt được thực hiện thông qua giao diện tương tác đồ họa

- Chế độ văn bản - sử dụng hệ thống menu ngữ cảnh văn bản, tương tác với trình cài đặt thông qua nhập vào các thông số cài đặt từ bàn phím.

- Các tham số "lores" hoặc "nofb" được sử dụng cho các hệ thống có card đồ họa giới hạn về mặc tính năng

- Tham số 'linux noprobe' tắt bỏ chức năng tự động dò tìm cấu hình phần cứng

- Tham số 'linux mediacheck' được thực hiện kiểm tra đĩa cài đặt để phát hiện các lỗi vật lí có thể ảnh hưởng đến quá trình cài đặt

- Tham số 'linux rescue' được sử dụng phục hồi và sửa chữa các bản cài đặt bị lỗi.

- Tham số 'linux dd' được dùng để yêu cầu nhập vào các trình điểu khiển tương ứng với các thiết bị phần cứng

- Các tùy chọn khác bao gồm các phím chức năng để mô tả các chế độ cài đặt khác nhau:

	+ F1 - màn hình khởi động chính

	+ F2 - Các tùy chọn chính

	+ F3 - mô tả các tùy chọn đối với chế độ kernel

	+ F4 - mô tả các tùy chọn với chế độ 'linux rescue'

- Quá trình cài đặt Linux bắt đầu sau khi việc chọn tùy chọn được thực hiện, tùy chọn mặc định (chế độ đồ họa) sẽ bắt đầu sau 1 khoảng thời gian trễ (thông thường 30s)


<a name="2"></a>
### 2. Các bước cài đặt:

- Chỉnh thông số BIOS để thực hiện khởi động từ đĩa CD

- Chọn chế độ cài đặt và truyền vào các tham số cài đặt trong trường hợp cần thiết

- Kiểm tra chất lượng của thiết bị lưu trữ chứa bộ cài đặt

- Lựa chọn ngôn ngữ hệ thống sẽ được sử dụng:

	+ Mặc định là Tiếng Anh

	+ Có hỗ trợ Tiếng Việt

- Lựa chọn chế độ bàn phím sẽ được sử dụng với mặc định là U.S Enghlish

- Đặt tên cho máy (hostname)

- Chọn múi giờ làm việc cho hệ thống

- Thiết lập mật khẩu cho tài khoản root

- Khởi tạo phân hoạch đĩa cứng với các chế độ

	+ Xóa bỏ toàn bộ phân vùng và phân hoạch theo mặc định

	+ Xóa bỏ toàn bộ phân vùng linux và phân hoạch theo mặc định

	+ Thay đổi lại kích thước một phân vùng đã có và phân hoạch theo mặc định trên vùng không gian rỗi

	+ Sử dụng vùng không gian rỗi và phân hoạch theo mặc định

	+ Tùy chỉnh việc phân hoạch

- Kích thước phân vùng cho linux

	+ Phân vùng gốc (/) kích thước > 5GB, với định dạng file hệ thống ext2 hoặc ext3.

	+ Phân vùng khởi động (boot) kích thước 50-100M, với định dạng file hệ thống ext2 hoặc ext3

	+ Phân vùng nháp (swap) kích thước gấp đôi dung lượng RAM. Ví dụ: RAM 256MB cần swap có kích thước 512MB

- Lựa chọn kết nơi lưu trữ (repositories) bộ cài đặt của các phần mềm muốn cài đặt vào trong hệ thống linux với 2 dạng:

	+ Repo tại local nằm trên đĩa CD

	+ Repo trong mạng LAN hoặc trên Internet

- Các gói phần mềm:

	+ Office and Productivity

	+ Software Development

	+ Web server

- Chế độ cài:

	+ Lựa chọn cài đặt phần mềm sau khi cài hệ điểu hành Linux

	+ Lựa chọn cài đặt phần mềm trong quá trình cài hệ điều hành

- Thực hiện cấu hình sau khi cài đặt

- Xem xét giấy phép sử dụng

- Tạo tài khoản người dùng để sử dụng trong hệ thống

- Cấu hình thông số thời gian, ngày tháng trong hệ thống

	+ Chỉnh theo thời gian hệ thống máy cục bộ

	+ Đồng bộ thời gian theo máy chủ trong mạng LAN hoặc Internet

- Login vào hệ thống và kết thúc quá trình cài đặt

<a name="3"></a>
### 3. Cài đặt Fedora for Linux 25.0:

- Tải phiên bản mới nhất của [Fedora](http://taimienphi.vn/download-fedora-for-linux-8898)

- Tiến hành cài đặt 

- Sau khi cài đặt xong

![1](https://github.com/TrinhTu/web_developer/blob/master/Task29_Linux_Course_01/B%C3%A0i%202_%20C%C3%A0i%20%C4%91%E1%BA%B7t%20h%E1%BB%87%20%C4%91i%E1%BB%81u%20h%C3%A0nh%20Linux/1.png)

<a name="4"></a>
### 4. Tài liệu tham khảo:

> [1] Cài đặt hệ điều hành (2.1).FLV. https://www.youtube.com/watch?v=tqvV1hGjBNI&index=7&list=PLF09AC5E5EAC05E52
>
> [2] Cài đặt hệ điều hành (2.2).FLV. https://www.youtube.com/watch?v=J74eHIL7C4c&list=PLF09AC5E5EAC05E52&index=8
>
> [3]  Cài đặt hệ điều hành (2.3).FLV. https://www.youtube.com/watch?v=MOadkW0NhHY&index=9&list=PLF09AC5E5EAC05E52
>
> [4]  Cài đặt hệ điều hành (2.4).FLV. https://www.youtube.com/watch?v=n_cajmuBTTE&index=10&list=PLF09AC5E5EAC05E52
>
> [5]  Cài đặt hệ điều hành (2.5).FLV. https://www.youtube.com/watch?v=ARBgNEbApv4&list=PLF09AC5E5EAC05E52&index=11