## Bài 08: CẤU HÌNH CÁC THIẾT BỊ PHẦN CỨNG

> Tài liệu: Cấu hình các thiết bị phần cứng
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 06/05/2017

### Mục lục:

[1. Thu thập thông tin về phần cứng](#1)

[2. Cấu hình các thiết bị ngoại vi](#2)

[3. Cấu hình các thiết bị trao đổi thông tin](#3)

[4. Cấu hình các thiết bị lưu trữ](#4)

[5. Cấu hình các thiết bị plug and play](#5)

[Tài liệu tham khảo](#6)

***

<a name="1"></a>
### 1. Thu thập thông tin về phần cứng:

- Có 2 cách thức để có được thông tin về các thiết bị phần cứng có trong hệ thống

- Tập lệnh 'ls' bao gồm: các lệnh trên sẽ hiển thị thông tin về các thiết bị mà hệ thống nhận diện được: **lsdev, lsusb, lsmode, lsraid, lspci**

- lsdev thu thập thông tin về các thiết bị phần cứng được sử dụng trong hệ thống, các thông tin bao gồm: địa chỉ I/O, số hiệu ngắt IRQ và kênh DMA

- lsusb thu thập và hiện thị thông tin về các bus USB có trong hệ thống và các thiết bị USB kết nối tới chúng

- Với lsusb và các thiết bị usb thì hệ thống nên có kernel linux hỗ trợ giao tiếp /proc/bus/usb. Ví dụ: kernel 2.3.15 hoặc mới hơn

- lsmode thu thập và hiện thị thông tin về các modules đã được nạp vào trong hệ thống

- lsraid thu thập và hiện thị thông tin về các thiết bị raid trong hệ thống linux (thiết bị md)

- lspci thu thập và hiện thị thông tin về các bus PCI cũng như các thiết bị kết nối với nó trong hệ thống

- Thu thập thông tin có trong hệ thống file ảo /proc

- Hệ thống file ảo /proc được tạo lập cứ mỗi khi hệ thống khởi động

- Thông tin về hệ thống có thể được kiểm tra thông qua các file có trong /proc

- Các file này bao gồm interupts, pci, dma

- Ví dụ để xem các thông tin hiện tại thông qua lệnh `ifconfig`:

![1]()

Các thông số này có thể thay đổi được, ví dụ thay đổi địa chỉ IP bằng lệnh:

`ifconfig ens33 192.168.0.200 netmask 255.255.255.0 up`

![2]()

- Để thực hiện việc cấp phát động địa chỉ IP thực hiện lệnh: `dhclient`

- Việc gán địa chỉ IP tĩnh bằng tay chỉ tồn tại trong phiên làm việc hiện tại khi khởi động lại hệ thống sẽ bị mất đi

- Để xem các file cấu hình cho thiết bị:

![3]()


- Chỉnh sửa nội dung file cấu hình gán địa chỉ IP:

![4]()

Khởi động lại các dịch vụ mạng bằng câu lệnh `service network restart`. Địa chỉ IP đã được gán:

![5]()

<a name="2"></a>
### 2. Cấu hình các thiết bị ngoại vi:

- **Thiết bị ngoại vi** là tên gọi chung cho 1 số thiết bị bên ngoài thùng máy được gắn kết với máy tính với tính năng nhập xuất (IO) hoặc mở rộng khả năng lưu trữ (như 1 bộ nhớ phụ)

- Thiết bị ngoại vi của máy tính có thể là:

	+ Thiết bị cấu thành máy tính và không thể thiếu ở 1 số loại máy tính

	+ Thiết bị có mục đích mở rộng tính năng hoặc khả năng của máy tính

- Một số thiết bị ngoại vi thường gặp

	+ Ổ cứng gắn ngoài hoặc ổ cứng di động

	+ Chuột (máy tính)

	+ Bàn phím máy tính

	+ Máy in

- Để có thể cấu hình và làm việc được với các thiết bị ngoại vi cần nắm 3 thông số cơ bản sau:

	+ Số hiệu ngắt (IRQ)

	+ Direct memory access (DMA)

	+ Địa chỉ cổng I/O

- Số hiệu ngắt:

	+ Ngắt là khả năng yêu cầu CPU tạm dừng công việc hiện tại để phục vụ cho 1 công việc khác, sau khi thực hiện xong sẽ quay lại hoàn thành công việc còn lại

	+ Mỗi máy tính đề hỗ trợ các công gắn thiết bị ngoại vi, các cổng này tương ứng với tín hiệu ngắt được đánh số từ 0-15

	+ Ngắt là nguyên nhân gây ra xung đột trong hệ thống máy tính, ví dụ như 2 thiết bị phần cứng cùng chung 1 số hiệu ngắt khi gắn kết vào trong 1 hệ thống máy tính.

	+ Thu thập thông tin có trong hệ thống file ảo /proc

	+ Hệ thống file ảo /proc được tạo lập mỗi khi hệ thống khởi động

	+ Thông tin về hệ thống có thể được kiểm tra thông qua các file có trong /proc

	+ Các file này bao gồm interrupts, pci, dma

- **DMA**:

	+ Direct memory access là tính năng của các hệ thống máy tính mới cho phép các thiết bị ngoại vi có khả năng truy cập trực tiếp vào bộ nhớ hệ thống để đọc hoặc ghi mà không phụ thuộc vào sự điều khiển của CPU

	+ Có thể xem thông tin về DMA cho các thiết bị ngoại vi trong hệ thống tại file /proc/dma

- **Địa chỉ cổng I/O**:

	+ Địa chỉ cổng I/O là phương thức cho phép thực hiện vào ra dữ liệu giữa CPU với các thiết bị ngoại vi trong máy tính

	+ Không có khái niệm "port" giống như trên windows, thay vào đó là các port COM1, COM3, COM4 tương ứng với các file /dev/tty0, /dev/tty1, /dev/tty2, /dev/tty3.

	+ LPT port trên windows tương ứng với /dev/lp trên linux (LPT1= /dev/lp0)

	+ Có thể xem thông tin về địa chỉ cổng I/O tại file /proc/oports

- Để lấy thông tin về số hiệu ngắt bằng cách xem thông tin file `interrupts`:

![6]()

- Để thu thập thông tin cổng I/O xem nội dung file `ioports`

![7]()

- Để thu thập thông tin về các kênh DMA được phân bố trong hệ thống xem nội dung file `dma`

![8]()

<a name="3"></a>
### 3. Cấu hình các thiết bị trao đổi thông tin:

- 2 thiết bị chính thường được dùng để truyền thông dữ liệu khi máy tính hoạt động trong 1 hệ thống mạng: 

	+ Card mạng

	+ Modems

- **Card mạng**:

	+ Có thể xem các thông số cấu hình làm việc của card mạng thông qua lệnh 'ifconfig'. Các thông số bao gồm:

		+ Địa chỉ IP

		+ Subnetmask

		+ Địa chỉ MAC

	+ Card mạng đầu tiên trong hệ thống được gán tên /dev/eth0

	+ Card mạng không dây được cấu hình thông qua lệnh ifconfig

	+ Có 3 cách để thay đổi thông số hoạt động của card mạng trong hệ thống

		+ Lệnh ifconfig để gán tĩnh cho 1 phiên làm việc

		+ Lệnh dhclient để gán động cho 1 phiên làm việc

		+ Thay đổi file cấu hình tương ứng

	+ Cú pháp lệnh ifconfig như sau:

		`ifconfig <interface> <ip_address> netmask <subnetmask> [up/down]`

	+ Gán động thông số hoạt động cho card mạng dùng lệnh `dhclient`

	+ Sử dụng được khi trong hệ thống có mặt dịch vụ dhcp client và trong mạng có 1 dhcp server

	+ Thông số gán vào chỉ có giá trị trong phiên làm việc hiện tại và mất khi khởi động lại hệ thống

- **Modem**:

	+ Modem được đăng kí trong hệ thống là 1 thiết bị truyền nối tiếp (ví dụ: /dev/tty0) và được ánh xạ vào file /dev/modem

	+ Modem có thể được cấu hình thông qua lệnh 'setserial' hoặc thông qua script/etc/rc.local/rc.serial

	+ Winmodems không thường sử dụng trong linux

<a name="4"></a>
### 4. Cấu hình các thiết bị lưu trữ:

- CÓ 2 dạng thiết bị lưu trữ chính:

	+ Các thiết bị lưu trữ theo chuẩn USB

	+ Các thiết bị lưu trữ theo chuẩn SCSI

- **USB** (Universal Serial Bus) là 1 chuẩn kết nối tuần tự trong máy tính. USB sử dụng để kết nối các thiết bị ngoại vi với máy tính, thường được thiết kế dưới dạng các đầu cắm cho các thiết bị tuân theo chuẩn cắm-là-chạy (plug-and-play) với tính năng gắn nóng (hot swapping) thiết bị cắm và ngắt các thiết bị không cần phải khởi động lại hệ thống.

- Đa số các bản phân phối linux mới đều tự động nhận diện và gắn kết thiết bị USB 1 cách tự động

- Các thiết bị USB thường được gắn kết vào các thiết bị theo chuẩn SCSI

- Trình điều khiển USB thường nằm trong hệ thống file /proc/bus/usb

- Lệnh 'usbmg' được sử dụng để thiết lập thông số hoạt động của các thiết bị USB nếu chúng không được nhận dạng 1 cách tự động

- Trình điều khiển /proc/bus/usb và /proc/bus/usb/devices sẽ hiển thị mọi thông tin về các thiết bị USB

<a name="5"></a>
### 5. Cấu hình các thiết bị plug and play:

- Plug and play là các thiết bị được thiết kế theo cấu trúc cho phép hệ điều hành có khả năng tự phát hiện sự có mặt của các thiết bị, thay đổi các thông số hệ thống sao cho người dùng có thể sử dụng trực tiếp thiết bị mà không tác động vào hệ thống

- Kernel đọc thông số của các thiết bị PnP chủ yếu từ BIOS

- 'isapnp' là công cụ chủ yếu được sử dụng nhằm phát hiện các thiết bị PnP có trong hệ thống

- Sử dụng file /etc/isapnp.conf cho cấu hình ISA bus

- Các thiết bị card âm thanh PnP có thể được cấu hình thông qua lệnh 'sndconfig'

<a name="6"></a>
### Tài liệu tham khảo:

> [1] Cấu hình thiết bị phần cứng (8.1). https://www.youtube.com/watch?v=Hu0fEr2DofU&list=PLF09AC5E5EAC05E52&index=27
>
> [2] Cấu hình thiết bị phần cứng (8.2 end). https://www.youtube.com/watch?v=ksmwbykL1_s&index=28&list=PLF09AC5E5EAC05E52