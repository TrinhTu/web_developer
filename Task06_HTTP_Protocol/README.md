### Giao thức HTTP

> Tài liệu: Giao thức HTTP
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 4/11/2016

### Mục lục:

[1.Khái niệm cơ bản về giao thức HTTP](#1)

[2. HTTP request Methods](#2)

- [2.1 Verb](#2.1)

- [2.2 URLs](#2.2)

[3. HTTP response](#3)

- [3.1 HTTP Status Code](#3.1)

  + [3.1.1 Thông tin:1xx](#3.1.1)

  + [3.1.2 Thành công: 2xx](#3.1.2)

  + [3.1.3 Sự điều hướng lại: 3xx](#3.1.3)
   
  + [3.1.4 Lỗi Client: 4xx](#3.1.4)
   
  + [3.1.5 Lỗi Server: 5xx](#3.1.5)

- [3.2 HTTP Response Header Fields](#3.2)

- [3.3 Gói tin HTTP](#3.3)

[4. Encrypted connection](#4)

[5. HTTP Caching](#5)


### Nội dung:

<a name="1"></a>
#### 1. Khái niệm cơ bản về giao thức HTTP: 

HTTP là viết tắt của HeyperText Transfer Protocol đây là giao thức truyền tải siêu văn bản là 1 trong 5 giao thức chuẩn về mạng internet, được dùng để liên hệ thông tin giữa máy cung cấp dịch vụ (web server) và máy sử dụng dịch vụ( web client)

Là giao thức nằm ở tầng ứng dụng của bộ giao thức TCP/IP (giao thức nền tảng cho internet) Sử dụng kết nối TCP cổng 80. HTTP hoạt động dựa trên mô hình client-server dựa vào 1 cặp request/response, sử dụng kiểu truyền đáng tin cậy là TCP, trình duyệt client thực hiện yêu cầu nhận và hiển thị đối tượng web bao gồm dữ liệu HTML và hình ảnh  JPEG, Java applet, video... Trong khi web server sẽ gửi trả lời  khi nhận được yêu cầu từ client.

HTTP request gồm 2 thành phần: URL và Verb (phương thức) được client gởi. Còn server sẽ trả vể HTTP response chưa Status code và Message body.

<a name="2"></a>
#### 2. HTTP Request methods:

Có 2 loại kết nối HTTP đó là kết nối bền vững và kết nối bền vững và kết nối không bền vững.

> Kết nối bền không bền vững: sau khi server gởi đi 1 đối tượng thì kết nối TCP sẽ được đóng, kết nối TCP chỉ truyền 1 lần duy nhất từ client và nhận lại thông điệp từ server. Các bước hoạt động của kết nối HTTP không bền vững:

![1](http://3.bp.blogspot.com/-ymSDuIleghQ/U51YlvZ1EdI/AAAAAAAAAFU/Kw0qZgTHDCM/s1600/1.PNG)

- Bước 1: client khởi tạo kết nối TCP bằng việc yêu cầu server, server nhận được yêu cầu và chấp nhận kết nối bằng việc gởi trả lời về cho client, nếu sau khoảng thời gian RTT mà không nhận được trả lời  từ phía server thì client sẽ gởi lại yêu cầu.

- Bước 2: sau khi kết nối được thiết lập, client sẽ gởi thông điệp yêu cầu chứa tên đường dẫn đến server. Server nhận được thông điệp yêu cầu và tiến hành  lấy ra các đối tượng được yêu cầu. Sau đó các đối tượng được đóng gói thành thông điệp trả lời và gởi đến client.

- Bước 3: server đóng kết nối TCP khi chắc chắn rằng client đã nhận được câu trả lời.

- Bước 4: client nhận thông điệp trả lời chứa tập tin HTML và hiển thị các đối tượng.

- Bước 5: lặp lại các bước từ 1-4 cho các đối tượng khác. 

> Kết nối bền vững: server sẽ duy trì kết nối TCP cho việc gởi nhiều đối tượng có nghĩa là 1 client có thể gởi nhiều yêu cầu đến server trong cùng 1 kết nối

<a name="2.1"></a>
##### 2.1 HTTP Request Methods:

 Chỉ phương thức để được thực hiện trên nguồn được nhận diện bởi Request URL đã cung cấp.Bắt đầu của HTTP Request sẽ là dòng Request-Line bao gồm 3 thông tin đó là:

- Method: là phương thức mà HTTP Request này sử dụng, thường là GET, POST, ngoài ra còn một số phương thức khác như HEAD, PUT, DELETE, OPTION, CONNECT.

- URI: là địa chỉ định danh của tài nguyên.

- HTTP version: là phiên bản HTTP đang sử dụng.

Tiếp theo là các trường request-header, cho phép client gửi thêm các thông tin bổ sung về thông điệp HTTP request và về chính client. Một số trường thông dụng như:

- Accept: loại nội dung có thể nhận được từ thông điệp response. Ví dụ: text/plain, text/html…

- Accept-Encoding: các kiểu nén được chấp nhận. Ví dụ: gzip, deflate, xz, exi…

- Connection: tùy chọn điều khiển cho kết nối hiện thời. Ví dụ: keep-alive, Upgrade…

- Cookie: thông tin HTTP Cookie từ server.

- User-Agent: thông tin về user agent của người dùng.

  Client gửi request tới server bằng một số các phương thức thường dùng như:

- GET: được sử dụng để lấy thông tin từ server đã cung cấp bởi sử dụng 1 URL đã cung cấp, các yêu cầu sử dụng GET nên chỉ nhận dữ liệu và không có ảnh hưởng gì tới dữ liệu.

- HEAD: truyền tải dòng trạng thái và khu vực Header.

- PORT: sử dụng để gởi dữ liệu tới server

- PUT: thay đổi tất cả đại diện của nguồn mục tiêu được tải lên

- DELETE: gỡ bỏ các đại diện hiện tại của nguồn mục tiêu bởi URL

- CONNECT: thiết lập 1 tunnel tới server đc xđ bởi URL đã cung cấp

- OPTIONS: miêu tả chức năng giao tiếp cho nguồn mục tiêu.

- TRACE: trình bày vòng lặp kiểm tra thông báo song song với path tới nguồn mục tiêu.

<a name="2.2"></a>
##### 2.2 URLs: Viết tắt của Uniform Resourse Locators 

Cấu trúc của URL:

![2](http://expressmagazine.net/sites/default/files/images/2013/07/08/http1-url-structure.png)

- protocol: HTTP và HTTPS

- host: tên miền server

- port: mặc định là 80

- resourse path: đường dẫn tới resource trên server

- query: truy vấn


<a name="3"></a>
#### 3. HTTP response:

Cấu trúc cảu HTTP response:

![anh](http://4.bp.blogspot.com/-6MzisogRE1I/U51YmWRQalI/AAAAAAAAAFI/AlztIUBFZFw/s1600/4.PNG)

<a name="3.1"></a>
##### 3.1 HTTP Status Code:

 Là mã trạng thái HTTP được server phản hồi lại mỗi khi nhận được HTTP resquest 

Yếu tố Status là 1 số nguyên có 3 kí tự, trong đó kí tự đầu tiên được mã hóa trạng thái định nghĩa hạng phản hồi và hai kí tự cuối không có vai trò phân loại nào. 5 giá trị của kí tự đầu tiên:

<a name="3.1.1"></a>
##### 1xx-thông tin: 

Yêu cầu được chấp nhận và đang tiến trình tiếp tục

- 100 (continue): máy chủ trả về nói rằng nó đã nhận được 1 phần request và chờ đợi gởi thêm phần còn lại

- 101( Switching protocol): request đã hỏi server vể việc thay đổi protocol và server đã chấp nhận

<a name="3.1.2"></a>
##### 2xx-thành công: 

Nghĩa là hoạt động đã được nhận, hiểu và chấp nhận thành công.

- 200 (successfull): các server xử lý yêu cầu thành công

- 201 ( Created) : yêu cầu thành công, máy chủ tạo ra 1 nguồn tài nguyên mới.

- 202 ( Accepted): máy chủ đã chấp nhận yêu cầu nhưng chưa xử lí nó.

- 203 ( Non-authoritative information): máy chủ xử lí yêu cầu nhưng đang quay trở lại thông tin có thể từ 1 nguồn khác.

- 204 (No content ):  máy chủ xử lí yêu cầu thành công nhưng không thấy bất kì nội dung nào.

- 205 (Reset content): các máy chủ yêu cầu nhưng không thấy nội dung nào không giống như 1 phản ứng 204, phản ứng này đòi hỏi người yêu cầu phải thiết lập lại tài liệu.

- 206( Partial content): Máy chủ xử lí thành công 1 phần của yêu cầu.

<a name="3.1.3"></a>
##### 3xx-sự điều hướng lại): 

Hoạt động phải được thực hiện để hoàn thành yêu cầu.

- 301 (Moved permanently): các trang web yêu cầu đã bị di chuyển vĩnh viễn tới URL mới.

- 302( Moved temporarily): các trang web yêu cầu đã được di chuyển tạm thời tới URL mới.

- 304 ( Not modified): các yêu cầu đã không được sửa đổi kể từ khi yêu cầu cuối cùng. Khi máy chủ trả về phản hồi này nó không trả lại các nội dung của trang.

<a name="3.1.4"></a>
##### 4xx- lỗi Client: 

Yêu cầu có cú pháp không chính xác hoặc không thể thực hiện.

- 400 ( Bad request): máy chủ không hiểu yêu cầu.

- 401 (Not authorized): đề nghị xác thực, máy chủ gởi về yêu cầu xác minh tài khoản và mật khẩu nếu client gởi request1 trang đăng nhập.

- 403 ( Forbidden): máy chủ từ chối yêu cầu( thường thì khi đăng nhập không thành công)

- 404(Not found ): máy chủ không tìm thấy trang yêu cầu.

- 405( method not allowed): phương thức xác định trong yêu cầu là không được cho phép.

- 406 ( Not acceptable): server chỉ có thể tạo phản hồi mà không được cháp nhận bởi Client.

- 407( Proxy authentication required):  yêu cầu client xác thực sử dụng proxy, khi máy chủ trả về phản hồi này nó cũng chỉ ra proxy mà người yêu cầu phải sử dụng.

- 408( Request time out): hết thời gian chờ, request tốn thời gian dài hơn thời gian server phản hồi.

- 409 ( Conflict): các server gặp phải conflict ( xung đột) khi thực hiện request. Các server phải bao gồm các thông tin về conflict trong các phản ứng. Máy chủ có thể trả về mã này để đáp ứng với yêu cầu PUT xung đột với các yêu cầu trước đó với cột danh sách khác biệt giữa các yêu cầu. 

- 410( Gone): server trả về yêu cầu này khi tài nguyên request đã bị delete viễn viễn tương ứng với 404 ( không tìm thấy mã), nên dùng 301 để xác định vị trí mới của tài nguyên.

- 411( length requied): content-length không đc xác định rõ server sẽ không chấp nhận request mà không có nó.

- 412( Precondition failed): các máy chủ không thể đáp ứng yêu cầu tiên quyết mà người yêu cầu đưa vào yêu cầu.

- 413( Request entily too large): máy chủ không thể xử lý yêu cầu vì nó quá lớn.

- 414( Requested URL is too long): URL yêu cầu là quá dài đối với máy chủ để xử lí.

- 416 ( Requested range not satisfiable): server trả về mã trạng thái này nếu yêu cầu cho 1 vi phạm không có sẵn cho trang.

- 417( Expectation failed): server không thể đáp ứng yêu cầu của các trường yêu cầu.

<a name="3.1.5"></a>
##### 5xx- Lỗi server:

 Server thất bại với việc thực hiện yêu cầu khả thi

- 500( Internal server error): server gặp lỗi không thể thực hiện yêu cầu

- 501( Not implemented): các máy chủ không có chức năng thực hiện cầu.( không nhận ra phương thức yêu cầu)

- 502( Bad gateway): server đã hoạt động như 1 gateway or proxy và nhận được 1 phản ứng không hợp lệ từ máy chủ.

- 503(Service unavailable): máy chủ hiện không có sẵn( đây là trạng thái tạm thời)

- 504( Gateway timeout): Các máy chủ đã hoạt động như một gateway hoặc proxy và đã không nhận được yêu cầu kịp thời từ máy chủ ngược.

- 505(HTTP version not supported): server không hỗ trợ phiên bản giao thức HTTP đưuọc sử dụng trong yêu cầu

<a name="3.2"></a>
##### 3.2 HTTP Response Header Fields

Các trường Header phản hồi cho phép Server truyền thông tin thêm về phản hồi mà không thể được đặt trong dòng Status-Line. Những trường Header này cung cấp thông tin về Server và về truy cập từ xa tới nguồn được xác định bởi Request-URI:

```
response-header = Accept-Ranges           ; 
                       | Age                     ; 
                       | ETag                    ; 
                       | Location                ; 
                       | Proxy-Authenticate      ; 
                       | Retry-After             ; 
                       | Server                  ;
                       | Vary                    ; 
                       | WWW-Authenticate        ;
```

<a name="3.3"></a>
#### 3.3. Gói tin HTTP:

Mở Wireshark lên ta có thể thấy được 1 số thông tin sau:

![anh](http://i.imgur.com/PnHQr69.png)

Các mã hồi đáp có nghĩa như sau:

- Ta đang sử dụng HTTP phiên bản là 1/1, dns port là http(80), dùng phương thức GET.

- Địa chỉ ip nguồn là: 192.168.1.103

- Địa chỉ ip đích là 182.161.72.71

- 200 OK


<a name="4"></a>
#### 4. Encrypted connections:

Có 2 cách thường dùng để mã hóa kết nối HTTP là HTTP secure ( là HTTPS + SSL) hoặc kết hợp HTTP và Transport Layer Securerity (TLS)

<a name="5"></a>
#### 5. HTTP Caching:

HTTP thường sử dụng cho các hệ thống thông tin phân phối nơi hiệu suất được cải thiện bằng việc sử dụng bộ nhớ đệm. Mục đích của bộ nhớ đệm là loại bỏ sự cần thiết phải gởi yêu cầu trong nhiều trường hợp, và loại bỏ sự cần thiết phải gởi phản hồi 1 cách đầy đủ trong nhiều trường hợp khác để tiết kiệm tài nguyên. Caching sẽ vô ích nếu như không được cải thiện hiệu suất.

### Tài liệu tham khảo:

https://www.stdio.vn/articles/read/202/http-request-va-http-response

http://hatangmang.blogspot.com/2014/06/giao-thuc-http.html

http://expressmagazine.net/development/2160/http-giao-thuc-ma-moi-lap-trinh-vien-nen-biet

https://vi.wikipedia.org/wiki/Hypertext_Transfer_Protocol


