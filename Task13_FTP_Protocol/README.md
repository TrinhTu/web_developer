## Bài : FTP protocol

> Tài liệu: FTP protocol
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 25/11/2016

### Mục lục:

[1.Khái niệm về FTP protocol](#1)

[2. Hoạt động của FTP protocol](#2)

[3. Ứng dụng](#3)

[4. Ưu điểm và nhược điểm của FTP protocol](#4)

[5. Cài đặt và dùng thử các FTP Client phổ biến](#5)

[6. Tài liệu tham khảo](#6)

### Nội dung:

<a name="1"></a>
#### 1. Khái niệm về FTP protocol

- FTP là viết tắt của File Transfer Protocol, đây là giao thức truyền tải tập tin dùng để trao đổi tập tin qua mạng lưới truyền thông sử dụng giao thức TCP/IP

- FTP thường chạy trên 2 cổng 20 và 21. Thông qua giao thức FTP người dùng có thể tải dữ liệu như hình ảnh, văn bản, các tập tin media... từ máy tính lên máy chủ đặt ở 1 nơi khác, hoặc tải tập tin trên máy chủ về máy tính cá nhân.

<a name="2"></a>
#### 2. Hoạt động của FTP protocol:

- Hoạt động của FTP cần có 2 máy tính, 1 client và 1 server. Server FTP dùng để chạy phần mềm cung cấp dịch vụ FTP, lắng nghe yêu cầu về dịch vụ của các máy tính khác trên mạng lưới gọi là trình chủ. Client chạy các phần mềm FTP dành cho người sử dụng dịch vụ gọi là trình khách.

- Trình chủ FTP lắng nghe các yêu cầu dịch vụ của các trình khách FTP trên cổng 21. Tại đây đường kết nối này tạo nên 1 dòng truyền điều khiển, cho phép các dòng lệnh được chuyển qua trình chủ FTP. Khi người dùng có yêu cầu trao đổi file, FTP mở kết nối TCP để truyền dữ liệu qua cổng 20, FTP truyền đúng 1 file qua kết nối này, sau khi truyền xong thì đóng kết nối lại, khi có 1 yêu cầu khác  thì FTP sẽ mở kết nối khác. Luồng thông tin điểu khiển được mở và tồn tại trong suốt phiên làm việc của người dùng, nhưng mỗi kết nối dữ liệu được tạo ra cho 1 yêu cầu truyền file, tức là kết nối dữ liệu là không liên tục.

Tiến trình phía server có 2 giao thức chính:

- Server Protocol Interpreter(PI): lắng nghe yêu cầu kết nối từ user trên cổng dành riêng, sau khi kết nối được thiết lập nó nhận lệnh từ phía User-PI, trả lời lại và quản lí tiến trình truyền dữ liệu trên server.

- Server Data Transfer Process(DTP): làm nhiệm vụ gởi hoặc nhận file từ User-DTP. Server-DTP vừa thiết lập kết nối dữ liệu vừa lắng nghe kết nối dữ liệu từ user. Dưới đây là mô hình đối chiếu các tiến trình vào trong mô hình FTP:

![anh](http://data.sinhvienit.net/2010/T05/img/SinhVienIT.NET---2805988391-2ec937c6dd-o.jpg)

Tiến trình từ Client:

- User Protocol Interpreter(User-PI): chịu trách nhiệm quản lí điều khiển phía client. Khởi tạo phiên kết nối FTP bằng việc phát ra yêu cầu tới Server-PI. Sau khi thiết lập kết nối. nó xử lí các lệnh nhận được trên giao diện người dùng và gởi tới Server-PI, đợi nhận phản hồi trở lại

- User Data Transfer Process(User-DTP): Có nhiệm vụ gởi nhận dữ liệu từ Server-DTP. User-DTP có thể thiết lập hoặc lắng nghe yêu cầu kết nối kênh dữ liệu trên server.

- User Interface: cung cấp giao diện xử lí cho người dùng, cho phép sử dụng các lệnh đơn giản hướng người dùng và cho phép người điều khiển phiên FTP theo dõi các thông tin kết quả xảy ra trong tiến trình.

Trình tự truy cập FTP:

- Người dùng gởi 1 username từ User-PI tới server bằng lệnh USER, sau đó password của người  dùng được gởi đi bằng lệnh PASS

- Server sẽ kiểm tra tên người dùng và password trong cơ sở dữ liệu người dùng của nó, nếu như hợp lệ thì server sẽ gởi thông báo tới người dùng là kết nối đã mở. Nếu không hợp lệ thì server sẽ yêu cầu người dùng chứng thực lại, sau 1 số lần chứng thực sai thì sẽ ngắt kết nối

<a name="3"></a>
#### 3. Ứng dụng:

FTP được sử dụng nhiều nhất vào việc truyền tải dữ liệu ( Nhất là đối với những tài liệu có dung lượng lớn mà không thể gởi qua mail hay các phương thức khác như CD USB flash).Có thể cùng lúc tải nhiều tập tin để tiết kiệm thời gian

<a name="4"></a>
#### 4. Ưu điểm và nhược điểm của FTP protocol:

Ưu điểm:

- Khuyến khích việc dùng chung tập tin (như chương trình ứng dụng hoặc dữ liệu)

- Khuyến khích việc sử dụng máy tính ở xa 1 cách gián tiếp

- Che đậy sự khác biệt về hệ thống lưu trữ tập tin giữa các máy chủ, nhằm cho người dùng không cần quan tâm đến sự khác biệt riêng của chúng

- Truyền tải dữ liệu đáng tin cậy và có hiệu quả cao.

Nhược điểm:

- Mật khẩu và nội dung của tập tin được truyền qua đường cap mạng ở dạng văn bản thường, nếu như bị chặn thì nội dung có thể bị lộ ra ngoài

- Cần thiết lập nhiều kết nối TCP/IP hơn nữa: 1 dòng dành riêng cho điểu khiển kết nối, 1 dành cho truyền tập tin lên, truyền tập tin xuống, liệt kê thư mục... Tường lửa cần phải được cài thêm những logic mới có thể lường trước được kết nối FTP.

- Tính năng ủy quyền có thể bị lạm dụng để sai khiến máy chủ gởi dữ liệu sang 1 cổng tùy chọn ở 1 máy tính thứ 3

- Khi nhận dữ liệu thì không có phương pháp để kiểm chứng toàn bộ dữ liệu truyền sang. Nếu kết nối bị ngắt khi truyền dữ liệu thì không có cách khắc phục
<a name="5"></a>
#### 5. Cài đặt và dùng thử các FTP Client phổ biến:

Trong phần trước đã thực hiện cài đặt Filezilla, vậy nên bây giờ sẽ thử sử dụng 1 phần mềm client khác nhưng cũng hoạt động tương tự đó là WINSCP. 

- Tiến hành tải về và cài đặt bình thường

- Sau đó mở lên và bắt đầu đăng nhập:

![i](https://github.com/TrinhTu/web_developer/blob/master/Task13_FTP_Protocol/image/i.png)

- sau khi đăng nhập thành công sẽ thấy giao diện WINSCP chia làm 2 phần: Bên trái là hiển thị dữ liệu trên ổ cứng của máy mình( client), còn bên phải là dữ liệu máy chủ FTP (server)

![ii](https://github.com/TrinhTu/web_developer/blob/master/Task13_FTP_Protocol/image/ii.png)

- Để truyền tải file từ máy tính lên máy chủ hoặc ngược lại chỉ cần click vào file hay folder rồi kéo thả sang khung bên cạnh, chờ cho việc truyền tải hoàn tất sẽ thấy xuất hiện tập tin vừa tải

![iii](https://github.com/TrinhTu/web_developer/blob/master/Task13_FTP_Protocol/image/iii.png)

- Truy cập vào server để kiểm tra: http://chuyengiaseoweb.net/FTP.html

<a name="6"></a>
### Tài liệu tham khảo:

> [1] Vũ Thanh Lai. Tìm hiểu về Giao thức FTP. 
> 
> Online: http://sinhvienit.net/forum/tim-hieu-ve-giao-thuc-ftp.28754.html 
> 
> [2] Wikipedia. FTP. 
> 
> Online: https://vi.wikipedia.org/wiki/FTP
