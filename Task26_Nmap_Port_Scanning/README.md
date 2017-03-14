## NMAP PORT SCANNING

> Tài liệu: Nmap Port Scanning
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 13/03/2017

## Mục lục:

***

### Cách sử dụng Nmap để scan mở port trong VPS:

### Ports là gì?

- Có nhiều lớp trong mô hình OSI, lớp vận chuyển là lớp chính kết nối thông tin liên lạc giữa các dịch vụ và ứng dụng khác nhau. Đây là lớp chính liên kết giữa các cổng.

### Định nghĩa Port:

- **Port**: Là 1 địa chỉ mạng được sử dụng bên trong hoạt động của các hệ điều hành giúp phân biệt lưu lượng dành cho các ứng dụng hoặc dịch vụ khác nhau.

- **Internet Sockets**: đây là 1 tập tin dùng để mô tả các địa chỉ IP hay các cổng có liên quan cũng như các giao thức truyền tải sẽ được sử dụng để xử lí dữ liệu.

- **Binding**: Quá trình nay diễn ra khi 1 ứng dụng hoặc dịch vụ sử dụng Internet socket để xử lí dữ liệu đầu vào và đầu ra.

- **Listening**: 1 dịch vụ được gọi là "listening" trên 1 cổng khi nó được liên kết với 1 địa chỉ cổng/giao thức/IP trong khi chờ đợi các yêu cầu từ phía client.

Khi nhận được yêu cầu, nó thiết lập kết nối với client bằng cách sử dụng cùng 1 cổng đã lắng nghe, bởi internet sockets được sử dụng để liên kết bởi 1 địa chỉ IP client xác định, điều này không ngăn chặn máy chủ lắng nghe và gởi các yêu cầu cùng 1 lúc cho client.

- **Port Scanning**: là quá trình cố gắng kết nối với 1 số các cổng liên tiếp nhằm mục đích thu thập thông tin về dịch vụ cũng như hệ điều hành được sử dụng.

### Các Port thông thường:

Ports được xác định bởi 1 dãy số từ 1 tới 65535:

- Các cổng dưới 1024 được liên kết với các dịch vụ như hệ điều hành Linux và Unix, những cổng này phải có quyền truy cập `root` để có thể khởi chạy dịch vụ.

- Các Ports ở khoảng giữa từ 1024-49151 được coi là đã được đăng kí, có nghĩa là chúng đã được dành riêng cho các dịch vụ nhất định bằng cách gởi yêu cầu đến IANA (Internet Assigned Numbers Authority)

- Port giữa 49152 - 65535 không thể đăng kí và được đề nghị sử dụng cho các mục đích cá nhân, không thể kết nối thành mạng lưới.

Sau đây là danh sách các cổng phổ biến hiện nay:

- 20: FTP data

- 21: FTP control port

- 22: SSH

- 23: Telnet 

- 25: SMTP

- 43: WHOIS protocol

- 53: DNS services

- 67: DHCP server port

- 68: DHCP client port

- 80: HTTP 

- 110: POP3 mail port

- 113: Ident authentication services on IRC networks

- 143: IMAP mail port

- 161: SNMP

- 194: IRC

- 389: LDAP port

- 443: HTTPS <= Secure web traffic

- 587: SMTP 

- 631: CUPS printing daemon port

- 666: DOOM 

Trên đây chỉ là các dịch vụ thông thường được liên kết với ports, dựa vào đó có thể tìm được các cổng thích hợp với các ứng dụng phục vụ cho việc tìm hiểu.

Hầu hết các dịch vụ có thể được cấu hình để sử dụng các cổng khác với mặc định nhuwg cần đảm bảo cả client và server đều được cấu hình để sử dụng 1 cổng non-standard. Có thể thấy 1 danh sách ngắn các cổng thông dụng bằng cách gõ:

`less /etc/services`

Nó sẽ cung cấp 1 danh sách các cổng thông dụng và các dịch vụ có liên quan của họ:

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task26_Nmap_Port_Scanning/image/1.png"/></p>

### Cách kiểm tra cổng mở riêng:

Có 1 số công cụ được sử dụng để quét cổng mở hầu hết được phân phối trên Linux `netstat`, có thể phát hiện được các dịch vụ đang chạy bằng cách sử dụng câu lệnh sau:

`sudo netstat -plunt`

Bằng cách này cho ta thấy các cổng đang được lắng nghe liên kết với các dịch vụ và cả giao thức đang được sử dụng là TCP hay UDP.

### Cài đặt Nmap:

Nmap (Network Mapper) là 1 công cụ quét, theo dõi đánh giá bảo mật mạng. Nmap là 1 phần mềm mã nguồn mở, có các chức năng như: phát hiện host trong mạng, liệt kê các port đang được mở trên 1 host, xác định các dịch vụ chạy trên port đó, cấc phần mềm và phiên bản đang sử dụng, xác định hệ điều hành của thiết bị...

Đây là 1 phần trong việc đảm bảo mạng an toàn tránh bị tấn công bằng cách xâm nhập vào trong mạng của bạn và tìm ra những điểm yếu trong đó theo cách mài các attacker sử dụng. Trong tất cả các công cụ thì **Nmap** là công cụ mạnh và phổ biến nhất.

Có thể cài đặt Nmap trên Ubuntu hay Debian bằng cách nhập:

```
sudo apt-get update
sudo apt-get install nmap
```

Một trong những lợi ích của phần mềm này là cung cấp 1 bản đồ tập tin ngày càng được cải thiện. Có thể thấy được mối liên hệ rộng hơn giữa port và services bằng cách sử dụng câu lệnh: `less /usr/share/nmap/nmap-services`

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task26_Nmap_Port_Scanning/image/2.png"/></p>

Bên cạnh 2 ngàn dòng thì file này thêm vào các trường ví dụ như ở cột thứ 3 - 1 danh sách các cổng mở được phát hiện ra trong quá trình nghiên cứu scan trên Internet.

### Cách Scan Ports với Nmap:

Nmap được sử dụng để thu thập nhiều thông tin của máy chủ, ngoài ra còn cho quản trị viên hệ thống phát hiện được ai đang có các ý định hành vi xấu, vậy nên chỉ nên sử dụng Nmap cho máy chủ của bạn hoặc trong nhưng trường hợp đã thông báo cho chủ sở hữu.

Dưới đây là 1 số trường hợp phổ biến có thể được thực hiện với Nmap. Tất cả các lệnh sẽ được chạy với sudo privileges để tránh điều hướng truy vấn lại kết quả. Một vài lệnh có thể mất 1 thời gian dài để hoàn thành.

**Scan hệ điều hành của máy chủ:**

`sudo nmap -0 remote_host`

- Bỏ qua các phần phát hiện mạng , giả mạo host thì điều này rất hữu ích nếu nhận được câu: `Note: Host seems downs` trong các thử ngiệm của bạn.  Có thể thêm điều này vào trong các lựa chọn khác:

`sudo nmap -PN remote_host`

- Chỉ định 1 dãy có phạm vi từ "-" hoặc "/24" để scan 1 số lượng host trong cùng 1 lúc.

`sudo nmap -PN xxx.xxx.xxx.xxx-yyy`

- Scan 1 dãy mạng các dịch vụ có sẵn:

`sudo nmap -sP network_address_range`

- Scan mà không tra cứu DNS, điều này làm tăng tốc độ trả về kết quả trong hầu hết các trường hợp.

`sudo nmap -n remote_host`

- Scan 1 ports xác định thay vì các port thông thường:

`sudo nmap -p port_number remote_host`

- Scan kết nối TCP, nmap sẽ scan bắt tay 3 bước, với mục tiêu là các cổng. Ví dụ:

`sudo nmap -sT remote_host`

- Để scan kết nối UDP:

`sudo nmap -sU remote_host`

- Scan mọi giao thức TCP và UDP:

`sudo nmap -n -PN -sT -sU -p- remote_host`

- Để thực hiện scan SYN:

`sudo nmap -sS remote_host`

- Để xem phiên bản của 1 dịch vụ đang chạy trên máy chủ sủ dụng lệnh:

`sudo nmap -PN -p port_number -sV remote_host`

Việc làm này giúp khám phá các lỗ hổng mạng của bạn.