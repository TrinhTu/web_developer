## Bài 03: TIẾN TRÌNH KHỞI ĐỘNG

> Tài liệu: Tiến trình khởi động
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 16/03/2017

### Mục lục:

[1. Boot loader](#1)

[2. LILO](#2)

[3. GRUB](#3)

[4. File FSTAB](#4)

[5. Hồ sơ đăng nhập người dùng](#5)

[6. Xử lí sự cố trong quá trình khởi động Linux](#6)

[Tài liệu tham khảo](#7)

***

<a name="1"></a>
### 1. Boot loader:

- Nạp vào các file khởi động cần thiết và Linux Kernel

- Nằm trong vùng Master Boot Record hoặc sector đầu tiên của phân vùng Linux

- Có hai trình boot loader được sử dụng phổ biến nhất trong các bản phân phối

- LILO (Linux Loader)

- GRUB (Grand Unified Boot loader)

- Kiểm soát các tùy chọn khởi động

- Có thể quản lí việc khởi động của các hệ điều hành khác như Microsoft Windows

- Được cài đặt khi Linux được cài đặt, có thể thay đổi và cấu hình lại sau khi cài đặt

<a name="2"></a>
### 2. LILO:

- LILO không phụ thuộc vào hệ thống file nào, có thể khởi động 1 hệ điều hành từ đĩa mềm hoặc đĩa cứng

- Cho phép lựa chọn 16 hệ thống khởi động khác nhau

- Gồm 2 thành phần:

	+ Chương trình thực thi /sbin/lilo: được sử dụng để cấu hình LILO và ghi LILO vào MBR/boot sector đầu tiên

	+ File cấu hình /etc/lilo.conf: chứa các thông số cấu hình của LILO

- **Trình tự cấu hình LILO**

	+ Chương trình /sbin/lilo đọc file lilo.conf để lấy các thông tin cấu hình

	+ Các file kernel được định vị vào tạo file boot image

	+ File boot image được sao chép vào MBR/boot sector

	+ /sbin/lilo thoát ra

	+ Máy tính sử dụng bản boot image mới cho việc khởi động

- **Trình tự khởi động LILO**:

	+ Pha đầu tiên được thực thi: đọc thông tin từ boot loader hoặc MBR để nạp vào file boot image (hiển thị kí tự "L" lên màn hình)

	+ Pha đầu tiên kết thúc (hiển thị "LI" trên màn hình) chuyển sang pha thứ 2

	+ Pha thứ 2 được gọi thực hiện (hiển thị "LIL" trên màn hình): bootloader được nạp vào và kiểm tra trạng thái

	+ Pha thứ 2 kết thúc (hiển thị chữ "LILO" trên màn hình) bootloader được nạp và kiểm tra thành công. LILO được kích hoạt thành công.

- **File cấu hình LILO**:

	+ Lilo.conf tương tự như file boot.ini được sử dụng trong Windows

	+ Lilo.conf được chia làm 2 phần:

		+ Toàn cục (phần đầu tiên) chứa các thông số cấu hình chung cho LILO

		+ Phần toàn cục chứa thông tin về các lời nhắc, khoảng thời gian chờ, file image khởi động mặc định và 1 số thông số khác

	+ Image session bao gồm các thông số khởi động của OS và các thông số hiển thị menu

	+ Danh sách OS có thể bao gồm: Linux. tùy chọn failsafe và Windows

	+ Cấu hình OS bao gồm vị trí của Kernel và nhân menu

	+ prompt hiển thị dấu nhắc cho phép người dùng lựa chọn các hệ điều hành muốn làm việc

	+ timeout=50 chỉ ra khoảng thời gian LILO đợi sự lựa chọn của người dùng, nếu không có sự lựa chọn nào sẽ chọn default

	+ default=linux chỉ ra hệ điều hành mặc định LILO sẽ trao đổi quyền khởi động khi không có sự lựa chọn của người dùng.

	+ image=boot/vmliniuz-2.4.0-0.43.6 chỉ ra linux kernel dùng để khởi động khi được lựa chọn

	+ lable=linux chỉ ra hệ điều hành mà người dùng sẽ chọn để làm việc

	+ initrd=boot/initrd-2.4.0-0.43.6.img là initial ram disk iamge được kernel sử dụng trong quá trình khởi động để khởi tạo các thiết bị mà có thể khởi động cùng kernel. Ví dụ: SCSI card, hard drive...

	+ root=/dev/hda5 thông báo cho LILO biết đâu là phân vùng root

	+ File cấu hình có thể chỉnh sửa bằng các công cụ như vi hoặc trình soạn thảo văn bản khác

	+ Chạy lại file /sbin/lilo để cập nhập các thông tin đã thay đổi trong file cấu hình

	+ Chạy lại file /sbin/lilo sau khi thực hiện việc cập nhập nhân hoặc thay đổi phân vùng.

- **/sbin/lilo các tùy chọn nâng cao**: chạy lilo với các tùy chọn 

	+ -b thiết lập thiết bị khởi động sẽ được sử dụng

	+ -c sử dụng file cấu hình khác thay vì lilo.conf

	+ -R <lệnh> sử dụng để chạy lệnh với lilo

<a name="3"></a>
### 3. GRUB:

- Là trình quản lí khởi động mới hơn LILO

- Được sử dụng rộng rãi hơn trong các bản phân phối mới gần đây hơn là LILO

- Có khả năng cập nhập GRUB mà không cần đọc file cấu hình cũng như khởi động lại hệ thống

- **So sánh giữa LILO và GRUB**:

	+ LILO hỗ trợ tới 16 tùy chọn boot khác nhau, GRUB hỗ trợ không giới hạn

	+ LILO không thể khởi động lại từ mạng, GRUB có thể

	+ LILO phải được ghi lại cứ mỗi khi chỉnh sửa file cấu hình, GRUB không cần

	+ LILO không cso chế độ tương tác lệnh, GRUB có

- File cấu hình của GRUB là /boot/grub/grub.conf

- GRUB được cấu hình thông qua việc sử dụng grub-install script hoặc lệnh grub

- Sử dụng lệnh grub để tìm lỗi quá trình cài đặt

- **Các pha hoạt động của GRUB**

	+ Stage 1: được cài đặt trong MBR và trỏ tới Stage 2

	+ Stage 2: trỏ tới file cấu hình, trong trường hợp không xác định được vị trí file cấu hình thì command line sẽ xuất hiện để người dùng cấu hình thủ công

	+ Sử dụng lệnh grub để tìm lỗi trong quá trình cài đặt

<a name="4"></a>
### 4. File FSTAB:

- Là file văn bản đặt tại /etc/stab

- Được nạp vào trong suốt quá trình cài đặt cũng như khởi động hệ thống để chỉ ra hệ thống file nào sẽ được gắn kết vào trong quá trình khởi động và hệ thống file nào có thể được gắn vào bởi root hay người dùng.

- 6 cột thông tin cấu hình cho file hệ thống bao gồm

	+ Device: file device của hệ thống file, ví dụ: /dev/hda

	+ Điểm gắn kết: điểm gắn kết file hệ thống, ví dụ: /mnt/hda1 hoặc /media/cdrom

	+ Dạng file hệ thống dạng của file hệ thống trên thiết bị, ví dụ: vfat, ext2, ext3...

	+ Tùy chọn: rất nhiều tùy chọn liên quan tới việc gắn kết hệ thống file (ví dụ: `rw` cho quyền đọc ghi, `ro` cho quyền chỉ đọc...)

	+ `dump type` phục vụ cho việc sao lưu hệ thống file

	+ Trình tự `fsck` để kiểm tra hệ thống file khi có lỗi

- **Ví dụ**: Xem nội dung file FSTAB bằng câu lệnh `more /etc/fstab`. Nội dung file này cung cấp cho chúng ta tất cả các thông tin về các thiết bị sẽ được gắn kết trong quá trình khởi động.

![1]()

- Ngoài ra còn có thể xem thông tin nằm trong thư mục `more /etc/mtab`. File `mtab` này chứa tất cả các thông tin về các thiết bị đã được mount vào trong hệ thống.

![2]()

<a name="5"></a>
### 5. Hồ sơ đăng nhập người dùng:

- Script profile được kích hoạt khi 1 người dùng đăng nhập vào hệ thống

- `/etc/profile` ảnh hưởng tới mọi người dùng - file cấu hình toàn cục được kích hoạt trước script profile của người dùng

- `~/.bash_profile script` được kích hoạt tiếp theo (nếu tồn tại)

- `~/.bash_profile` chứa các biến và các thông số chỉ ảnh hưởng đến môi trường làm việc của người dùng

- Có thể đặt tên là bash_login hoặc .profile

- Tiếp đến là gọi file `~/.bashrc`

- `~/.bashrc` thiết lập các thông số về shell và tùy chọn, lời nhắc, các định dạng và các hàm

- File script.bash_logout được chạy khi người dùng đăng xuất khỏi hệ thống - xóa bỏ các biến và văn bản

<a name="6"></a>
### 6. Xử lí sự cố trong quá trình khởi động Linux:

- Sử dụng lệnh `dmesg` để xem lại các thông báo của hệ thống trong quá trình khởi động - nhằm mục đích tìm lỗi

- Các thông báo khởi động được lưu trong `/var/log/dmesg`

- Hiểu được các thông báo lỗi của LILO và GRUB

- Sử dụng failsafe hoặc chế độ rescue để giải quyết vấn đề

- Sử dụng /sbin/lilo để cấu hình lại LILO nếu sự cố xảy ra

- Hiểu các thông số của lệnh grub để sử dụng cho việc tìm lỗi

- Thay đổi runlevel về 3 để thực hiện khởi động vào chế độ văn bản nhằm tìm lỗi của X-window

- Khi gặp sự cố trong quá trình khởi động chúng ta có thể xem lại nhật kí để tìm hiểu xem lỗi ở đâu, có 2 cách để xem lại nhật kí là 	

	+ Xem lại nội dung nằm trong file `dmesg` nằm trong thư mục: `more /var/log/dmesg`

	+ Cách 2 có thể dùng lệnh `dmesg | more`

![3]()

- Có 6 mức khởi động trong linux (run level)

	– Run level 0 (init 0): chế độ tắt máy.

	– Run level 1 (init 1): chế độ này chỉ sử dụng được 1 người dùng.

	– Run level 2 (init 2): chế độ đa người dùng nhưng không có dịch vụ NFS.

	– Run level 3 (linit 3): chế độ đa người dùng, có đầy đủ các dịch vụ.

	– Run level 4 (linit 4): chưa được sử dụng.

	– Run level 5 (linit 5): chế độ đồ họa.

	– Run level 6 (linit 6): khởi động lại máy.

- **to do**

<a name="7"></a>
### Tài liệu tham khảo:

> [1] Tiến trình khởi động (3.1).FLV. https://www.youtube.com/watch?v=vloigWDUxVs&list=PLF09AC5E5EAC05E52&index=12
>
> [2] Tiến trình khởi động (3.2).FLV. https://www.youtube.com/watch?v=xXPsbfEhShc&list=PLF09AC5E5EAC05E52&index=13
>
> [3] Tiến trình khởi động (3.3).FLV. https://www.youtube.com/watch?v=kNe-VyU55sc&list=PLF09AC5E5EAC05E52&index=14
>
> [4] Tiến trình khởi động (3.4).FLV. https://www.youtube.com/watch?v=ozUwfIiWKFk&index=15&list=PLF09AC5E5EAC05E52

