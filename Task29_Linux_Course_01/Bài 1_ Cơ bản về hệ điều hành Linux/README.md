## BÀI 1: CƠ BẢN HỆ ĐIỀU HÀNH LINUX (1.1).FLV

> Tài liệu: Cơ bản hệ điều hành Linux (1.1).FLV
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 11/04/2017

### Mục lục: 

[1. Giới thiệu chung về hệ điều hành linux](#1)

[2. Các tính năng của hệ điều hành linux](#2)

[3. Mã nguôn mở và giấy phép GNU](#3)

[4. Linux Kernel](#4)

[5. Các bản phân phối của hệ điều hành Linux](#5)

[6. Khởi động song song cùng Windows](#6)

[Tài liệu tham khảo](#7)

***

<a name="1"></a>
### 1. Giới thiệu chung về hệ điều hành Linux:

- Là hệ điều hành có chức năng tuwogn tự như Window, Unix,...

- Có khả năng chạy trên nhiều môi trường khác nhau (phần cứng, CPU...)

- Là hệ điều hành đa người dùng, đa nhiệm

- Có lượng phần mềm hỗ trợ đông đảo và đa dạng

- Giá thành rẻ có khả năng thay thế tốt cho các hệ điều hành khác

- Mã nguồn mở GNU

- Giá thành rẻ, tính ưu việt cao, tương tự như Unix..

- ...

<a name="2"></a>
### 2. Các tính năng của hệ điều hành Linux:

- Đa người dùng đa nhiệm

- Tính bảo mật cao - ít bị ảnh hưởng bởi các lổ hổng thông thường thường gặp trong windows

- Số lượng phần mềm tương thích đa dạng và phong phú

- Mã nguồn mở - mã nguồn luôn được cung cấp kèm theo

- Giá thành rẻ - có thể tải về miễn phí

- Hướng tới nhiều lớp người dùng khác nhau - sử dụng đồ họa, sử dụng giải trí, sử dụng làm công cụ bảo mật...

- Có khả năng cài đặt và sử dụng trên các hệ thống phần cứng cũ- giúp giảm thiểu chi phí cập nhập hay nâng cấp.

<a name="3"></a>
### 3. Mã nguồn mở và giấy phép GNU:

- Mã nguồn mở là việc truy cập và sử dụng mã nguồn của các phần mềm 1 cách miễn phí - người dùng có thể thay đổi, sửa chữa mà không bị giới hạn.

- Được quyền đóng gói và phân phối (bán hoặc gởi đi) các bản phần mềm mà không bị giới hạn gì.

- Mã nguồn được phổ biến miễn phí tự do cho việc phân phối, phát triển và tiếp tục quảng bá.

- Giấy phép công cụ GNU là 1 khái niệm mã nguồn mở hợp pháp

- Được sử dụng để gán giấy phép sử dụng cho đa số các sản phẩm phần mềm thuộc Free Software Foundations và bất cứ phần mềm nào được bảo vệ 1 cách hợp pháp về phần mềm, tác giả và quyền sử dụng.

<a name="4"></a>
### 4. Linux Kernel:

- Là nhân của hệ điều hành Linux ở mức độ thấp nhất

- Đóng vai trò là lớp giao tiếp cho các ứng dụng của người dùng trong quá trình liên lạc với hệ thống phần cứng.

- Điều khiển file, ổ đĩa, phần cứng, quản lí bộ nhớ, phân bổ việc xử dụng và chiếm hữu bộ vi xử lí.

- Kernel có kiến trúc module

- Có khả năng biên dịch nhằm đáp ứng các nhu cầu sử dụng khác nhau

- ĐIều khiển file, ổ đĩa, phần cứng, quản lí bộ nhớ

- Được phát triển và bổ sung mới các chức năng cũng như sửa chữa những vấn đề phát sinh về tính bảo mật

- Phiên bản của Linux kernel được định dạng theo khuôn mẫu major.minor.patch (vd 2.6.2)

    + Nếu minor là chẵn, kernel được coi là ổn định và sẽ được sử dụng trong các sản phẩm đề ra

    + Nếu minor là lẻ kernel đang trong quá trình phát triển và kiểm tra

<a name="5"></a>
### 5. Các bản phân phối của hệ điều hành Linux:

- Là bản đóng gói hoàn chỉnh bao gồm Linux Kernel, các tiện ích, các file cài đặt, hệ thống quản lí giao diện đồ họa

- Đi kèm với logo của sản phẩm và 1 số tính năng đặc biệt tương ứng với bản phân phối đó

- Các bản phân phối thường gặp là Red Hat. Debian, Slackware

- Đa số các lệnh cơ bản, các tiện ích có được trong hệ điều hành Linux là không phụ thuộc vào bản phân phối

- Đa số các bản phần mềm được viết cho 1 bản phân phối có thể làm việc với các bản phân phối khác

<a name="6"></a>
### 6. Khởi động song song cùng Windows:

- Một số yêu cầu về phân hoạch ổ cứng trước khi cài đặt:

    + Ổ cứng lưu trữ cần có dung lượng trống khoảng 5GB (chưa được định dạng và chưa phân vùng) để phục vụ cho việc sao chép các file trong quá trình cài đặt

    + RAM tối thiểu 256MB

    + Bộ vi xử lí tối thiểu 400MHz

    + Các phân vùng được quy hoạch thành dạng cây, với phân vùng root(/) có tại điểm bắt đầu của cây

    + Các phân vùng khác được nối tiếp với phân vùng root

    + Các phân vùng khác bao gồm

        + /boot-lưu trữ các file khởi động thường có kích thước < 500MB

        + /home - lưu trữ các thư mục home của người dùng

        + /swap - sử dụng các file swap

    + Fdisk là tiện ích đi kèm có mặt trong đa số các bản phân phối Linux

        + Là công cụ ở dạng chạy dòng lệnh

        + Sử dụng để thủ công việc phân hoạch ổ cứng

        + Có nhiều tùy chọn khác nhau

    + Disk Druid thường đi kèm với các bản phân phối của Red Hat

        + Có giao diện đồ họa để thao tác phân hoạch

        + Được dùng để phân hoạch ổ cứng trong suốt quá trình cài đặt

        + Là công cụ dễ sử dụng nhất

    + Cfdisk thường đi kèm trong các bản phân phối của Debian Linux

        + Cho phép phân hoạch ổ cứng thủ công

        + Thao tác qua hệ thống menu ngữ cảnh

- Linux và Windows có thể tồn tại song song trên cùng 1 hệ thống

- Đòi hỏi phải có các vùng tách biệt

- Nạp Windows trước, nạp linux sau

- Cho phép sử dụng quản lí khởi động của Linux để quản lí việc khởi động

- Trình quản lí khởi động sẽ cung cấp menu lựa chọn việc khởi động vào hệ điều hành nào, thứ tự khởi động có thể thay đổi.

- Sẽ có 1 hệ điều hành được chọn làm mặc định để khởi động lên nếu không có sự lựa chọn nào từ phía người dùng trong 1 khoảng thời gian chờ

- Có thể tạo đĩa khởi động riêng của Linux trong quá trình cài đặt, đĩa được sử dụng để khởi động thẳng vào Linux mà không cần thay đổi bản ghi khởi động hoặc quá trình quản lí khởi động.

- Trình khởi động của Windows vẫn quản lí việc khởi động vào hệ điều hành Windows.

<a name="7"></a>
### Tài liệu tham khảo:

> [1] Cơ bản hệ điều hành Linux (1.1).FLV. https://www.youtube.com/watch?v=IBY4BvBSA00&list=PLF09AC5E5EAC05E52&index=1
>
> [2] Cơ bản hệ điều hành Linux (1.2).FLV. https://www.youtube.com/watch?v=p_a4t0QL6Ow&index=2&list=PLF09AC5E5EAC05E52
>
> [3] Cơ bản hệ điều hành Linux (1.3).FLV. https://www.youtube.com/watch?v=lPLrZSLYfjM&list=PLF09AC5E5EAC05E52&index=3
> 
> [4] Cơ bản hệ điều hành Linux (1.4).FLV. https://www.youtube.com/watch?v=o0pppNUYcDc&list=PLF09AC5E5EAC05E52&index=4
> 
> [5] Cơ bản hệ điều hành Linux (1.5).FLV. https://www.youtube.com/watch?v=b4ecJXvbOR0&index=5&list=PLF09AC5E5EAC05E52
> 
> [6] Cơ bản hệ điều hành Linux (1.6).FLV. https://www.youtube.com/watch?v=qYsr7AJ9bPI&list=PLF09AC5E5EAC05E52&index=6
