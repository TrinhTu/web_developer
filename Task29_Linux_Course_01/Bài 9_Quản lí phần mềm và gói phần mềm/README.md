## Bài 09: QUẢN LÝ PHẦN MỀM VÀ GÓI PHẦN MỀM

> Tài liệu: Quản lý phần mềm và gói phần mềm
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 06/05/2017

### Mục lục:

[1. Cài đặt phần mềm từ mã nguồn](#1)

[2. Hệ thống quản lí gói phần mềm của Redhat](#2)

[3. Hệ thống quản lí gói phần mềm của Debian](#3)

[Tài liệu tham khảo](#4)

***

<a name="1"></a>
### 1. Cài đặt phần mềm từ mã nguồn:

- Đa số các phần mềm trên hệ điều hành Linux đều được cung cấp kèm cả mã nguồn mở và các tài liệu cần thiết để sử dụng.

- Mã nguồn mở có thể được biên dịch và cài đặt để trở thành các ứng dụng trong hệ thống

- Mã nguồn thường đi kèm ở dạng file nén, hay gọi là tarbal với phần đuôi là .tar hoặc .tar.gz

- Các file nén này thường bao gồm mã nguồn mở của ứng dụng, các script cấu hình, makefile và các script để cài đặt.

- Script cấu hình là các file chứa các dòng lệnh kiểm tra hệ thống nhằm thu thập các thông tin cần thiết để cấu hình cho makefiles

- Makefile là file chứa các thông số cài đặt, các biến và các lệnh cài đặt được dùng để thực hiện việc biên dịch cũng như cài đặt ứng dụng

- Các lệnh make và make install thường được sử dụng để biên dịch mã nguồn cũng như cài đặt ứng dụng

- Các phần mềm có thể sử dụng các thư viện chia sẻ - thường là các file thư viện, các file header có trong:

	+ /lib: thư mục thư viện chia sẻ chính

	+ /urs/lib: thư mục chứa các file thư viện bổ sung

	+ /urs/X11R6/lib: thư mục chứa các file thư viện cho các thành phần của X-windows

**Ví dụ**:

- Tải trực tiếp gói phần mềm về cài đặt:

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task29_Linux_Course_01/B%C3%A0i%209_Qu%E1%BA%A3n%20l%C3%AD%20ph%E1%BA%A7n%20m%E1%BB%81m%20v%C3%A0%20g%C3%B3i%20ph%E1%BA%A7n%20m%E1%BB%81m/image/1.png"/></p>

- Giải nén: `tar xzvf ftp://ftp.gnu.org/gnu/grub/grub-2.00.tar.gz`

- Kết thúc quá trình giải nén chuyển vào thư mục chứa cấu hình:

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task29_Linux_Course_01/B%C3%A0i%209_Qu%E1%BA%A3n%20l%C3%AD%20ph%E1%BA%A7n%20m%E1%BB%81m%20v%C3%A0%20g%C3%B3i%20ph%E1%BA%A7n%20m%E1%BB%81m/image/2.png"/></p>

- Xem nội dung file hướng dẫn `INSTALL`:

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task29_Linux_Course_01/B%C3%A0i%209_Qu%E1%BA%A3n%20l%C3%AD%20ph%E1%BA%A7n%20m%E1%BB%81m%20v%C3%A0%20g%C3%B3i%20ph%E1%BA%A7n%20m%E1%BB%81m/image/3.png"/></p>

- Thực hiện các bước như trong file hướng dẫn -> chạy `./configure`

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task29_Linux_Course_01/B%C3%A0i%209_Qu%E1%BA%A3n%20l%C3%AD%20ph%E1%BA%A7n%20m%E1%BB%81m%20v%C3%A0%20g%C3%B3i%20ph%E1%BA%A7n%20m%E1%BB%81m/image/4.png"/></p>

<a name="2"></a>
### 2. Hệ thống quản lí gói phần mềm của Redhat:

- Gói phần mềm là bộ cài đặt ứng dụng

- RPM sử dụng lệnh 'rpm' để thực hiện việc quản lí các gói phần mềm, lệnh này đi kèm với nhiều tùy chọn khác nhau

- Các gói phần mềm có thể có phần đuôi là rpm hoặc src.rpm tùy thuộc vào gói

- Các gói .rpm có thể được cung cấp dưới dạng các gói mã nguồn hoặc các gói thực thi

- Các gói này chứa trong đó các file, các lệnh, các script thực thi cần thiết cho việc cài đặt ứng dụng

- Sử dụng lệnh 'rpm -q <ten_goi>' để thu thập thông tin về các gói phần mềm đã được cài đặt trong hệ thống.

- Cơ sở dữ liệu RPM có chứa các thông tin về các gói phần mềm đã được cài đặt vào trong hệ thống

- Thường cơ sở dữ liệu này được lưu tại thư mục /var/lib/rpm

- Cơ sở dữ liệu này có thể bị hỏng sau nhiều lần cài đặt và gỡ bỏ, để sửa chữa dùng lệnh 'rpm -rebuilddb'

- Lệnh rpm được sử dụng để cài đặt nâng cấp và gỡ bỏ các gói phần mềm

- Có thể truy vấn cơ sở dữ liệu để lấy thông tin về các gói

- Có thể kiểm tra chữ kí đi kèm với gói bằng lệnh: `rpm -K <ten_goi>`

- **Ví dụ**: xem hướng dẫn cài đặt các gói `rpm` bằng lệnh `man`

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task29_Linux_Course_01/B%C3%A0i%209_Qu%E1%BA%A3n%20l%C3%AD%20ph%E1%BA%A7n%20m%E1%BB%81m%20v%C3%A0%20g%C3%B3i%20ph%E1%BA%A7n%20m%E1%BB%81m/image/5.png"/></p>

<a name="3"></a>
### 3. Hệ thống quản lí gói phần mềm của Debian:

- Các gói .deb có chứa danh sách các file, các file nhị phân và các file điều khiển

- Sử dụng lệnh 'dpkg' để thực hiện các tác vụ cài đặt, lệnh đi kèm với rất nhiều tùy chọn khác nhau.

- Cơ sở dữ liệu về dpkg thường đặt tại thư mục /var/lib/dpkg

- Có 3 file chính trong thư mục cần chú ý: `status, avaiable, diversion`

- 'apt-get' là hệ lệnh mới cho phép thực thi việc cài đặt các gói .deb từ các nguồn gói

- 'alien' là tiện ích cho phép chuyển đổi các định dạng gói không tuân theo chuẩn của debian sang định dạng gói của debian

<a name="4"></a>
### Tài liệu tham khảo:

> [1] Quản lí phần mềm và gói phần mềm.FLV. https://www.youtube.com/watch?v=HnCNIFJh0Go&index=29&list=PLF09AC5E5EAC05E52