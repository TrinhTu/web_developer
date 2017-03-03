## DATA TAMPERING

> Tài liệu: DATA TAMPERING
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 03/03/2017

### Mục lục:

- [1. POST, GET, sự khác nhau và ứng dụng của chúng](#1)

- [2. Tìm hiểu về Data Tampering](#2)

- [3. Cài đặt Addon/Extension dùng để Tamper Data trên Firefox/Chrome](#3)

- [Tài liệu tham khảo](#4)

***

<a name="1"></a>
### 1. POST, GET:

#### 1.1 Khái niệm:

**POST:** Một yêu cầu POST được sử dụng để gởi dữ liệu tới Server ví dụ như thông tin khách hàng, file tải lên,... sử dụng các mẫu HTML

**GET:**Phương thức GET được sử dụng để lấy thông tin từ Server đã cung cấp bởi sử dụng 1 URL đã cung cấp, các yêu cầu sử dụng GET chỉ nhận dữ liệu nên không làm ảnh hưởng tới dữ liệu.

#### 1.2 So sánh:

- **Giống nhau:** Đều gởi dữ liệu tới server để xử lí sau khi người dùng nhập thông tin vào Form và thực hiện lệnh Submit

- **Khác nhau:**

	+ Phương thức POST được bảo mật hơn GET vì nếu dữ liệu gởi nhầm thì sẽ không xuất hiện trên URL

	+ GET: dữ liệu được gởi đi tường minh hơn hiện trên URL, kém bảo mật hơn so với POST

	+ GET thực thi nhanh hơn POST vì những dữ liệu được gởi đi luôn được trình duyệt web cached lại

	+ Khi dùng phương thức POST thì server luôn thực thi kết quả trả về cho client, còn đối với phương thức GET thì trình duyệt web sẽ xem trong cached có kết quả tương ứng với yêu cầu đó hay không và trả về ngay mà không cần thực thi các yêu cầu đó ở server.

	+ Đối với những dữ liệu luôn được thay đổi thì nên sử dụng phương thức POST, còn dữ liệu ít được thay đổi thì sử dụng phương thức GET để truy xuất và xử lí nhanh hơn.

<a name="2"></a>
### 2. Data Tampering:

- Đây là công cụ chặn dữ liệu để Hack Website. Nó được sử dụng để giả mạo hay làm thay đổi dữ liệu của HTTP request (or reponse) trược khi người nhận xem nó . Sử dụng nó để làm xáo trộn thay đổi dữ liệu dựa trên phương thức POSt. Giả mạo URL, host, referrer, user agent, accept encoding, cookie trước khi được gởi đến máy chủ. Dữ liệu giả mạo POST bằng cách đẩy vào trong SQL và SSL. User-Agent và referrer cũng được sử dụng để tấn công website.

- Tamper Data rất dễ để sử dụng thêm vào trong Firefox dùng để giả mạo dữ liệu, nó bắt được tất cả HTTP request và HHTP reponse. Khi khởi động tampering nó bắt từng yêu cầu HTTP nếu bạn muốn thay đổi dữ liệu hay submit yêu cầu. Nếu muốn giả mạo thì Tamper Data sẽ phân tích các yêu cầu HTTP và tạo ra form có thể chỉnh sửa các thông số của HTTP request. 

<a name="3"></a>
### 3. Cài đặt Add-on dùng để Tamper Data::

#### 1. Firefox:

- Download Tamper Data tại đây và restart lại trình duyệt: https://addons.mozilla.org/En-us/firefox/addon/tamper-data/

- Sau khi cài đặt trong thanh công cụ **Tool** chọn **Tamper Data** sẽ hiện lên các thông số như sau:

[1]

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

[2]

- Dựa vào thông tin trên ta biết được Host mà ta đăng nhập, user agent, email và hiển thị cả Password... Sử dụng Tamper Data ta có thể thay đổi các thông tin (HTTP request) ví dụ như ở đây ta có thể thay đổi Password or email để cho không thể login thành công.

#### 2. Chrome:

- Download: https://chrome.google.com/webstore/detail/tamper-chrome-extension/hifhgpdkfodlpnlmlnmhchnkepplebkb/related?hl=vi

- Sau khi cài đặt ta vào trong More Tools --> developer tools để chỉnh sửa 1 vài chỗ như sau:

[3]

- Ngay sau khi chỉnh sửa thì công cụ sẽ hiện lên các thông tin sau:

[4]

<a name="4"></a>
### Tài liệu tham khảo:

> [1] HTTP Data Tampering. https://toschprod.wordpress.com/2011/10/13/http-data-tampering/ 
>
> [2] Basic Hacking with firefox data intercepting. https://www.cybrary.it/0p3n/basic-hacking-with-firefox-part-2-data-intercepting/
>
> [3] Change Form Post Data using Firefox Plugin Tamper Data. https://www.youtube.com/watch?v=xjOqcHvfjLU
>
> [4] How to use Tamper Data. https://www.youtube.com/watch?v=EcTTNWVYOiA