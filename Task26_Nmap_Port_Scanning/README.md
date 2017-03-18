## NMAP PORT SCANNING

> Tài liệu: Nmap Port Scanning
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 14/03/2017

## Mục lục:

- [1. Port](#1)

	[1.1 Định nghĩa port](#1.1)

	[1.2 Các port thông thường](#1.2)

	[1.3 Cách kiểm tra các cổng mở riêng](#1.3)

- [2. Nmap](#2)

	- [2.1 Cài đặt Nmap](#2.1)

	- [2.2 Cách scan port với Nmap](#2.2)

- [3. Kĩ thuật scan port được sử dụng phổ biến trong Nmap](#3)

	- [3.1 TCP scan](#3.1)

	- [3.2 UDP scan](#3.2)

- [Tài liệu tham khảo](#4)

***

<a name="1"></a>
### 1. Port:

<a name="1.1"></a>
#### 1.1 Định nghĩa Port:

- Có nhiều lớp trong mô hình OSI, lớp vận chuyển là lớp chính kết nối thông tin liên lạc giữa các dịch vụ và ứng dụng khác nhau. Đây là lớp chính liên kết giữa các cổng.

- **Port**: Là 1 địa chỉ mạng được sử dụng bên trong hoạt động của các hệ điều hành giúp phân biệt lưu lượng dành cho các ứng dụng hoặc dịch vụ khác nhau.

- **Internet Sockets**: đây là 1 tập tin dùng để mô tả các địa chỉ IP hay các cổng có liên quan cũng như các giao thức truyền tải sẽ được sử dụng để xử lí dữ liệu.

- **Binding**: Quá trình nay diễn ra khi 1 ứng dụng hoặc dịch vụ sử dụng Internet socket để xử lí dữ liệu đầu vào và đầu ra.

- **Listening**: 1 dịch vụ được gọi là "listening" trên 1 cổng khi nó được liên kết với 1 địa chỉ cổng/giao thức/IP trong khi chờ đợi các yêu cầu từ phía client.

Khi nhận được yêu cầu, nó thiết lập kết nối với client bằng cách sử dụng cùng 1 cổng đã lắng nghe, bởi internet sockets được sử dụng để liên kết bởi 1 địa chỉ IP client xác định, điều này không ngăn chặn máy chủ lắng nghe và gởi các yêu cầu cùng 1 lúc cho client.

- **Port Scanning**: là quá trình cố gắng kết nối với 1 số các cổng liên tiếp nhằm mục đích thu thập thông tin về dịch vụ cũng như hệ điều hành được sử dụng.

<a name="1.2"></a>
### 1.2 Các Port thông thường:

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

<a name="1.3"></a>
### 1.3  Cách kiểm tra cổng mở riêng:

Có 1 số công cụ được sử dụng để quét cổng mở hầu hết được phân phối trên Linux `netstat`, có thể phát hiện được các dịch vụ đang chạy bằng cách sử dụng câu lệnh sau:

`sudo netstat -plunt`

Bằng cách này cho ta thấy các cổng đang được lắng nghe liên kết với các dịch vụ và cả giao thức đang được sử dụng là TCP hay UDP.

<a name="2"></a>
### 2. Nmap:

<a name="2.1"></a>
### 2.1 Cài đặt Nmap:

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

<a name="2.2"></a>
#### 2.2 Cách Scan Ports với Nmap:

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

<a name="3"></a>
### 3. Kĩ thuật Scan Port được sử dụng phổ biến trong Nmap:

<a name="3.1"></a>
#### 3.1  TCP scan:

3.1.1 TCP SYN scan:

- TCP SYN scan `-sS`: Đây là mặc định và là lựa chọn hợp lí nhất bởi nó được thực hiện 1 cách nhanh chóng, quét hàng ngàn cổng mỗi giây trên 1 mạng không bị hạn chế và cản trở bởi tường lửa. Kĩ thuật này thường được gọi là `half-open` scanning bởi nó không mở 1 kết nối TCP đầy đủ. Khi gởi 1 gói tin SYN tức là đã mở 1 kết nối và đợi trả lời. Nếu nhận được ACK_SYN thì port đó ở trạng thái mở, Nmap sẽ gởi gói tin RST để đóng kết nối thay vì gởi ACK để hoàn thành quá trình bắt tay 3 bước. Nếu nhận được RST thì port đó ở trạng thái đóng. Sau 1 số lần gởi mà không nhận được trả lời hoặc nhận được ICMP type 3 thì port đó đã bị firewall chặn. Lợi thế của việc này là ít bị phát hiện bởi hệ thống IDS hơn là đăng nhập cố gắng tấn công hoặc kết nối

3.1.2 TCP connect scan:

- TCP connect scan `-sT`: kĩ thuật này được sử dụng trong trường hợp khi người dùng không có quyền truy cập raw packet để thực hiện SYN scan. Thay vì viết các raw packet như các máy quét khác thì nmap sẽ yêu cầu hệ điều hành thiết lập kết nối với các máy tính và cổng bằng cách khởi tạo các kết nối. Thay vì đọc các raw packet phản hồi thì nmap sử dụng API để thu thập tình trạng thông tin trên mỗi kết nối. Do thực hiện kết nối đầy đủ nên kĩ thuật này dễ bị phát hiện bởi hệ thống log của mục tiêu do đó thường sử dụng SYN scan hơn để tránh bị phát hiện.

3.1.3 TCP ACK scan:

- TCP ACK scan `-sA`: Khác với các kĩ thuật trên thì kĩ thuật này sẽ gởi đi 1 gói tin TCP với flag ACK. Nếu nhận phản hồi là RST thì port đó không bị chặn (unfiltered), còn nếu không nhận được trả lời hoặc ICMP (type 3, code 1,2,3,9,10,13) thì port đó đã bị chặn bởi firewall.

Cả TCP SYN và TCP connect đều cho ra kết quả giống nhau, nhưng thông thường thường sử dụng TCP SYN là kĩ thuật hiệu quả nhất và không để lại log, nhưng đối với kĩ thuật này cần phải có quyền truy cập root, nếu không có quyền này thì phải sử dụng đến kĩ thuật TCP connect, còn riêng đối với TCP ACK dùng để kiểm tra firewall.

3.1.4 Windows scan: đây là loại scan tương tự như ACK và cũng có phát hiện các cổng mở

<a name="3.2"></a>
#### 3.2 UDP scan:

3.2.1 UDP scan:

- UDP scan `-sU`: trong khi các dịch vụ phổ biến trên Internet chạy trên nên giao thức TCP, dịch vụ UDP được triển khai rộng rãi. DNS, SNMP và DHCP (đăng kí các port 53, 161/162 và 67/68) là 3 giao thức phổ biến. Bởi vì scan UDP quét thường chậm hơn và khó khăn hơn so với TCP.

UDP scan được kích hoạt với các tùy chọn `-sU`, có thể được kết hợp với kiểu TCP scan như SYN scan (`sS`) để kiểm tra cả 2 giao thức trong cùng quá trình chạy. Nmap gởi gói tin UDP tới port của mục tiêu nếu nhận được gói tin ICMP port unreachable error (type 3, code 3) thì port đó ở trạng thái đóng. Nếu nhận được ICMO unreachable error (type 3, codes 1,2,9,10, hoặc 13) thì port đó ở trạng thái filtered. Nếu không nhận được gì thì port ở trạng thái open| filtered. Nếu nhận được gói tin UDP thì port đó ở trạng thái open.

3.2.2 TCP Null, FIN và Xmas scans:

- TCP NULL `-sN`: gởi gói tin TCP mà không kèm bất kì flag nào

- TCP FIN `-sF`: gởi gói tin TCP với flag FIN

- TCP Xmas `-sX`: gởi gói tin TCP với các flag PSH, URG và FIN.

Các kĩ thuật này sẽ cho ra 1 kết quả giống nhau nên tùy theo mục đích mà chọn NULL, FIN, Xmas.

Lựa chọn port và thứ tự quét: mặc định nmap sẽ quét 1000 port phổ biến nhất với thứ tự ngẫu nhiên. 

- Tùy chọn -p: lựa chọn chính xác các port cần quét, nếu quét đồng thời nhiều giao thức thì thêm các chữ cái đứng trước số port. T: TCP, U: UDP, S: SCTP, hay P: IP Protocol.

- Tùy chọn -F (Fast scan): nmap quét 100 port phổ biến nhất thay vì mặc định 1000 port.

- Tùy chọn -top-port: quét n port phổ biến nhất

- Tùy chọn -r: thứ tự quét các port từ thấp lên cao thay vì mặc định là ngẫu nhiên.

<a name="4"></a>
### Tài liệu tham khảo:

> [1] Nmap port scanning. https://nmap.org/book/man-port-scanning-techniques.html
>
> [2] How to use nmap to scan for open ports on your vps. https://www.digitalocean.com/community/tutorials/how-to-use-nmap-to-scan-for-open-ports-on-your-vps