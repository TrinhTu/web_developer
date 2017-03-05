## DATA TAMPERING

> Tài liệu: DATA TAMPERING
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 03/03/2017

### Mục lục:

- [1. POST & GET](#1)

- [2. Data Tampering](#2)

- [3. Cài đặt Addon/Extension dùng để Tamper Data trên Firefox/Chrome](#3)

	- [3.1 Firefox](#3.1)

		+ [3.1.1 Tamper Data](#3.1.1)

		+ [3.1.2 Httprequester](#3.1.2)

	- [3.2 Chrome](#3.2)

		+ [3.2.1 Tamper Chrome application](#3.2.1)

		+ [3.2.2 Web-sniffer](#3.2.2)

- [Tài liệu tham khảo](#4)

***

<a name="1"></a>
### 1. POST & GET:

- 2 phương thức thường được sử dụng cho request và reponse giữa client và server là GET và POST.

	- GET: Các yêu cầu dữ liệu từ 1 nguồn chỉ định

	- POST: gởi dữ liệu để xử lý tới 1 nguồn nhất định

- Phương thức GET:

	+ Lưu ý chuỗi truy vấn (tên/ giá trị) được gởi từ URL của yêu cầu GET: `/test/demo_form.php?name1=value1&name2=value2`

	+ GET requests có thể được lưu giữ

	+ GET requests vẫn được lưu lại trong lịch sử trình duyệt

	+ GET requests có thể được bookmarked (đánh dấu lưu lại)

	+ GET requests không nên sử dụng để gởi các dữ liệu nhạy cảm

	+ GET requests có hạn chế về chiều dài dữ liệu

	+ GET requests được sử dụng để lấy lại dữ liệu

- Phương thức POST: 

	+ Lưu ý chuỗi truy vấn (tên/giá trị) được gởi đi trong thông điệp của HTTP của POST request.
 
		`POST /test/demo_form.php HTTP/1.1
Host: w3schools.com
name1=value1&name2=value2`

	+ POST requests không được lưu trữ

	+ POST requests không lưu lại trong lịch sử trình duyệt

	+ POST requests không thể bookmarked

	+ POST requests không bị giới hạn về chiều dài dữ liệu

- So sánh giữa GET và POST:

|   	|  GET 	|  POST 	|
|---	|---	|---	|
|   Khi tải lại trang hoặc nhấn nút back	|   	Không ảnh hưởng|  Dữ liệu sẽ được gởi thêm 1 lần nữa 	|
|   Bookmarked	|   Có thể bookmarked	|   Không thể bookmarked	|
|   Cached	|   Có thể được lưu trữ	|   Không thể được lưu trữ	|
|  Kiểu Encoding 	|  application/x-www-form-urlencoded 	| application/x-www-form-urlencoded or multipart/form-data. Sử dụng mã hóa dữ liệu theo nhị phân  	|
|  History 	|  Các thông số vẫn được lưu lại trong trình duyệt 	|   Các thông số không được lưu lại trong trình duyệt	|
|   	Giới hạn độ dài dữ liệu|   Khi gởi dữ liệu bằng phương thức GET thì sẽ thêm dữ liệu vào trong URL và độ dài tối đa của URL là 2048 kí tự	|   Không bị giới hạn	|
|   Hạn chế trong kiểu dữ liệu	|   Chỉ cho phép bảng mã ASCII	|   Không bị hạn chế, cho phép cả dữ liệu nhị phân	|
|   Security	|   GET kém bảo mật hơn so với POST vì dữ liệu hiển thị 1 phần trong URL nên không dùng GET để gởi những dữ liệu mang tính nhạy cảm	|   POST an toàn hơn so với GET vì thông số không được lưu trữ trong trình duyệt	|
| Visibility  	| Dữ liệu được hiển thị trong URL  	|   Dữ liệu không được hiển thị trong URL	|


<a name="2"></a>
### 2. Data Tampering:

- Đây là công cụ chặn dữ liệu để Hack Website. Nó được sử dụng để giả mạo hay làm thay đổi dữ liệu của HTTP request (or reponse) trược khi người nhận xem nó . Sử dụng nó để làm xáo trộn thay đổi dữ liệu dựa trên phương thức POSt. Giả mạo URL, host, referrer, user agent, accept encoding, cookie trước khi được gởi đến máy chủ. Dữ liệu giả mạo POST bằng cách đẩy vào trong SQL và SSL. User-Agent và referrer cũng được sử dụng để tấn công website.

- Tamper Data rất dễ để sử dụng thêm vào trong Firefox dùng để giả mạo dữ liệu, nó bắt được tất cả HTTP request và HHTP reponse. Khi khởi động tampering nó bắt từng yêu cầu HTTP nếu bạn muốn thay đổi dữ liệu hay submit yêu cầu. Nếu muốn giả mạo thì Tamper Data sẽ phân tích các yêu cầu HTTP và tạo ra form có thể chỉnh sửa các thông số của HTTP request. 

<a name="3"></a>
### 3. Cài đặt Add-on dùng để Tamper Data::

<a name="3.1"></a>
#### 1. Firefox:

<a name="3.1.1"></a>
**1.1 Tamper Data:**

- Download:

- Sau khi cài đặt trong thanh công cụ **Tool** chọn **Tamper Data** sẽ hiện lên các thông số như sau:

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task24_Data_Tampering/1.png"/></p>

- Các thông số này có ý nghĩa như sau:

	+ Time: Thời gian yêu cầu xảy ra

	+ Duration: thời gian nhận được yêu cầu

	+ Total Duration: tổng thời gian bao gồm yêu cầu và trả về

	+ Size: kích thước của nội dung nhận được

	+ Method: phương thức thực hiện

	+ Status: mã trạng thái HTTP nhận được hoặc tải từ bộ nhớ cache

	+ Content Type: Kiểu dữ liệu nhận được

	+ URL:

	+ Load Flags: bổ sung thông tin HTTP được sử dụng

- Ví dụ như khi ta đăng nhập vào 1 trang web và start Tamper Data lên ta có được thông tin như sau:

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task24_Data_Tampering/2.png"/></p>

- Dựa vào thông tin trên ta biết được Host mà ta đăng nhập, user agent, email và hiển thị cả Password... Sử dụng Tamper Data ta có thể thay đổi các thông tin (HTTP request) ví dụ như ở đây ta có thể thay đổi Password or email để cho không thể login thành công.

<a name="3.1.2"></a>
**1.2 Httprequester:**

- Download: https://addons.mozilla.org/vi/firefox/addon/httprequester/

- Cũng tương tự như công cụ trên, ta chỉ việc mở 1 trang web bất kì và dán URL vào:

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task24_Data_Tampering/2-1.png"/></p>

<a name="3.2"></a>
#### 2. Chrome:

<a name="3.2.1"></a>
**2.1 Tamper Chrome (application):**

- Download: https://chrome.google.com/webstore/detail/tamper-chrome-extension/hifhgpdkfodlpnlmlnmhchnkepplebkb/related?hl=vi

- Sau khi cài đặt ta vào trong More Tools --> developer tools để chỉnh sửa 1 vài chỗ như sau:

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task24_Data_Tampering/3.png"/></p>

- Ngay sau khi chỉnh sửa thì công cụ sẽ hiện lên các thông tin sau:

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task24_Data_Tampering/4.png"/></p>

<a name="3.2.2"></a>
**2.1 Web-sniffer:**

- Download: https://chrome.google.com/webstore/detail/web-sniffer/ndfgffclcpdbgghfgkmooklaendohaef

- Mở công cụ lên và chạy nó:

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task24_Data_Tampering/4-2.png"/></p>

<a name="4"></a>
### Tài liệu tham khảo:

> [1] HTTP Data Tampering. https://toschprod.wordpress.com/2011/10/13/http-data-tampering/ 
>
> [2] Basic Hacking with firefox data intercepting. https://www.cybrary.it/0p3n/basic-hacking-with-firefox-part-2-data-intercepting/
>
> [3] Change Form Post Data using Firefox Plugin Tamper Data. https://www.youtube.com/watch?v=xjOqcHvfjLU
>
> [4] How to use Tamper Data. https://www.youtube.com/watch?v=EcTTNWVYOiA
>
> [5] HTTP method. https://www.w3schools.com/tags/ref_httpmethods.asp