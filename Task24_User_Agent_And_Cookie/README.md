## USER AGENT AND COOKIE

> Tài liệu: USER AGENT AND COOKIE
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 01/03/2017

### Mục lục:

[1. User agent](#1)

[2. Cookie](#2)

[Tài liệu tham khảo](#3)

***

<a name="1"></a>
### 1. User agent:

#### 1.1 Khái niệm:

- Trong máy tính user agent hoạt động như 1 phần mềm thay thế cho người sử dụng. Thông thường được sử dụng cho mục đích để trình duyệt web khai báo thông tin của trang web tới trình duyệt và hệ thống. Điều này cho phép các trang web tùy chỉnh nội dung theo khả năng của các thiết bị chi tiết.

- Các công dụng khác user agent chằng hạn như: 1 trình đọc mail được gọi là `mail user agent`. Trong nhiều trường hợp khác thì 1 user agent được xem như là 1 client trong 1 giao thức mạng được sử dụng trong giao tiếp trong hệ thống phân phối máy tính client-server. Điều đặc biệt ở đây là giao thức HTTP được coi như là phần mềm client khởi tạo yêu cầu, sử dụng 1 user-agent header trong khi client không được điều khiển bởi người dùng

- Nói tóm lại thì user agent là 1 chuỗi nhận dạng khi trình duyệt gởi yêu cầu đến máy chủ web. Khi truy cập vào 1 trang web bất kì thì trình duyệt sẽ gởi 1 HTTP Request bao gồm cả User Agent đến máy chủ web. Nội dung của User Agent thì còn tùy thuộc vào trình duyệt đang sử dụng, các trình duyệt khác nhau thì có User Agent khác nhau.

#### 1.2 User Agent Identification (Xác định tác nhân người dùng):

- Khi 1 software agent hoạt động trong 1 giao thức mạng thì nó thường nhận diện được chính nó, kiểu ứng dụng, hệ điều hành, phiên bản phần mềm... bằng cách submit 1 chuỗi kí tự nhận dạng để nó hoạt động. Trong giao thức HTTP, SIP và NNTP nhận dạng được truyền trong 1 trường tiêu đề là `User-Agent`. Chẳng hạn như thu thập thông tin Web (Web crawlers) thì thường bao gồm URL và e-mail address để quản lí các trang web có thể tương tác với với hệ điều hành (Operator) của bot.

#### 1.3 Use In HTTP:

- Trong HTTP thì chuỗi User-Agent được sử dụng để trao đổi nội dung, tại nơi các máy chủ gốc chọn nội dung thích hợp hoặc các thông số hệ điều hành cho phần trả lời. Chuỗi User-Agent có thể được nhận dạng bởi máy chủ web để lựa chọn các thay đổi cơ bản phù hợp với phiên bản phần mềm client. 

- Chuỗi User-Agent là 1 trong các tiêu chuẩn để ngăn chặn các Web crawler vào 1 số nội dung của trang web bằng cách sử dụng Robots Exclusion Standard (robots.txt file). Thông tin trong chuỗi User Agent đóng góp vào thông tin mà client muốn gởi tới server, các chuỗi này có thể biến đổi đáng kể từ người dùng này tới người dùng khác.

#### 1.3.1 Format For Human-operated Web Browsers:

Định dạng chuỗi User-Agent trong HTTP là 1 danh sách các product tokens (từ khóa) với các ý kiến tùy chọn. Ví dụ như, product của người dùng là WikiBrowser thì chuỗi user agent có thể là WikiBrowser/1.0 Gecko/1.0, các product quan trọng nên được liệt kê ở đầu tiên.

- Các thành phần của chuỗi này như sau:

	+ Name và version (WikiBrowser/1.0)

	+ Cách sắp xếp bố cục và version (Gecko/1.0)

- Hầu hết các trình duyệt web đều sử dụng chuỗi User-Agent có giá trị như sau:

`Mozilla/[version] ([system and browser information]) [platform] ([platform details]) [extensions]`

Ví dụ trên Safari dành cho Ipad sử dụng: `Mozilla/5.0 (iPad; U; CPU OS 3_2_1 like Mac OS X; en-us) AppleWebKit/531.21.10 (KHTML, like Gecko) Mobile/7B405`

Trong đó: 

+ Mozilla/5.0: để chỉ khả năng tương thích giữa các công cụ Mozilla

+ (iPad; U; CPU OS 3_2_1 like Mac OS X; en-us): các chi tiết về các trình duyệt đang chạy.

+ AppleWebkit/531.21.10: Nền tảng trình duyệt sử dụng

+ (KHTML. like Gecko): Chi tiết về trình duyệt

+ Mobile/7B405: được trình duyệt sử dụng để chỉ ra những thay đổi cải tiến trong trình duyệt hay thông qua 1 bên thứ 3.

#### 1.3.2 Format Automated Agents (bots)

Công cụ tìm kiếm Web tự động có thể sử dụng để rút gọn hình thức, nơi mà các trường quan trọng trao đổi thông tin trong các trường hợp có vấn đề. Theo quy định thì từ `bot` được bao gồm trong tên của agent, ví dụ như:

`Googlebot/2.1 (+http://www.google.com/bot.html)`

Các tác nhân tự động này phải tuân theo các quy định được xác định trong tập tin `robots.txt`. 

#### 1.3.3 User Agent Spoofing (Giả mạo User-agent):

1.4 User Agent Sniffing:

1.5 Encryption Strength Notations:

- Sử dụng các chữ U, I, N để xác định chuỗi mã hóa để mã hóa user agent. 


- Để kiểm tra user agent hiện tại có thể vào trang (What's My User Agent)[http://www.whoishostingthis.com/tools/user-agent/] Và user agent hiện tại của mình như sau: 

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task24_User_Agent_And_Cookie/image/1.png"/></p>

#### 1.4 Cách cài đặt User agent cho chrome

- Tải về: 

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task24_User_Agent_And_Cookie/image/2.png"/></p>

- Vào opition để tạo mới user agent:

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task24_User_Agent_And_Cookie/image/3.png"/></p>

- Sau khi tạo xong sẽ thấy xuất hiện user agent vừa tạo:

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task24_User_Agent_And_Cookie/image/4.png"/></p>

- Kiểm tra sau khi thêm:

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task24_User_Agent_And_Cookie/image/5.png"/></p>

#### 1.5 Cách tạo user agent cho Firefox:

- Tải về:

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task24_User_Agent_And_Cookie/image/6.png"/></p>

- Tạo thêm user agent mới:

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task24_User_Agent_And_Cookie/image/7.png"/></p>


- Chọn user agent. khi nào thấy quả cầu màu xanh là được:

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task24_User_Agent_And_Cookie/image/8.png"/></p>

<a name="2"></a>
### 2. Cookie:

- Khái niệm: Cookie là 1 dạng bản ghi được tạo ra và lưu lại trên trình duyệt khi người dùng truy cập 1 trang web. Nó là 1 bộ nhắc nhỏ mà website lưu trữ trên máy tính của bạn có thể định danh cho bạn, khi truy cập vào 1 trang web thay vì việc thường xuyên hỏi lại các thông tin như nhau thì chương trình trên website đó sẽ lưu thông tin vào cookie khi cần thiết sẽ tự động truy vấn cookie. 

- Nếu không có cookie thì mỗi lần truy cập vào trang web đó đều phải tự nhập lại thông tin. Thông tin mà cookie lưu trữ là thông tin người dùng cung cấp với website tạo ra cookie. Tuy nhiên những thông tin do cookie ghi nhận không được tiết lộ rộng rãi, chỉ có website chứa cookie mới có thể xem được những thông tin này. Cookie là 1 phần không thể thiếu với những website có khối lượng dữ liệu lớn, có số người dùng đông và sử dụng những chức năng đi kèm với đăng kí thành viên, đa phần cacs website đó là website thương mại điện tử.

- Cookie có thể được tạo bằng PHP hoặc Javascript. Có các loại cookie sau:

	+ Session Cookie: được lưu trong bộ nhớ của máy tính chỉ chỉ trong phiên trình duyệt web và sẽ tự động xóa khi đóng trình duyệt. Cookie này thường lưu trữ dưới dạng ID, cho phép nhanh chóng chuyển tơi 1 trang web mới mà không cần đăng nhập lại

	+ Persistent Cookie: được lưu trữ trên ổ cứng của máy tính và không bị xóa khi trình duyệt đóng lại, cho phép sử dụng mà không cần đăng nhập lại thông tin trong các lần truy cập tiếp theo. Được web server sử dụng để nhận dạng bạn trong những lần truy cập tới

Cookie thường có 6 tham số để truyền dữ liệu gồm: 

1. Tên cookie

2. Giá trị của cookie

3. Ngày hết hạn của cookie

4. Đường dẫn hợp lệ - là 1 tập hợp các URL trong cookie. Các website không có tên trong danh sách này sẽ không được sử dụng cookie.

5. Domain hợp lệ - giúp cho cookie có thể được truy cập bởi các trang web trên server bất kì trong trường hợp 1 website chạy nhiều server dưới 1 tên miền duy nhất.

6. Công tắc bảo mật - quyết định xem cookie sẽ được sử dụng khi và chỉ khi kết nối đó được bảo mật (ví dụ như SSL)

**Lợi ích của Cookie**: 

- Được sử dụng trong các dịch vụ thương mại điện tử để hỗ trợ chức năng mua hàng trực tuyến, máy chủ có thể theo dõi khách hàng và sao lưu các giao dịch của họ.

- Đối với doanh nghiệp có thể biết được 1 số thông tin về những người đang truy cập web của mình, biết được mức độ thường xuyên truy cập và chi tiết về thời gian truy cập. Lưu dữ thông tin khách hàng giúp cho những lần truy cập sau sẽ được thuận tiện hơn. Điều chỉnh quản cáo của mình, cung cấp những quản cáo phù hợp

- Đối với người dùng thì sẽ truy cập web nhanh hơn không phải nhập lại thông tin nhiều lần.

**Rủi ro**:

- Ảnh hưởng đến sự riêng tư của người dùng, rò rỉ thông tin cá nhân, tăng nguy cơ mất thông tin đăng nhập nếu người khác sử dụng máy tính của bạn, hoặc máy tính bị đánh cắp và xâm nhập.

Vậy nên cần thiết lập chế độ bảo mật cho trình duyệt, xóa cookie định kì trên máy tính, session cookie được tự động xóa khi hoàn thành 1 giao dịch sẽ làm giảm nguy cơ lạm dụng thông tin lưu trữ trong cookie, giữ cho trình duyệt được tự động update các bản vá lỗi, cập nhập phần mềm chống phần mềm giả mạo chỉ truy cập vào các trang web tin cậy...

### Tài liệu tham khảo:

