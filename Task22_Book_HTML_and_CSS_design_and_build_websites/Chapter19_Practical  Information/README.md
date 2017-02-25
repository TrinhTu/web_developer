## HTML & CSS

### PRACTICAL INFORMATION

> Chương 18: PRACTICAL INFORMATION
>
> Người thực hiện: LÊ TÚ TRINH
>
> Cập nhập lần cuối: 24/02/2017

## Mục lục:

[1. Search engine optimization](#1)

[2. Using analytics to understand visitors](#2)

[3. Putting your site on the web](#3)

[Tài liệu tham khảo](#4)

***

<a name="1"></a>
### 1. SEARCH ENGINE OPTIMIZATION (SEO) (tối ưu hóa công cụ tìm kiếm):

#### 1.1 SEO:

Sau đây là các khái niệm quan trọng giúp cải thiện khả năng hiển thị của website trên các công cụ tìm kiếm.

- **The basics**:

	+ Tối ưu hóa công cụ tìm kiếm (SEO) là cố gắng giúp cho website của bạn xuất hiện gần đầu của kết quả tìm kiếm khi mọi người tìm kiếm các chủ đề trang web của bạn. Trọng tâm của SEO là làm việc với mục đích của người tìm kiếm trang web của bạn, sử dụng với mục đích đúng và tăng cơ hội cho các công cụ tìm kiếm hiển thị liên kết đến trang web của bạn trong kết quả tìm kiếm của họ.

	+ Để mọi người đến với kết quả đầu tiên trong việc tìm kiếm thì không chỉ nhìn vào sự xuất hiện trên trang web của bạn mà còn xem xét có bao nhiêu liên kết đến trang web của bạn (và cách liên kết). Vì lí do đó SEO được phân chia thành 2 khu vực: kĩ thuật on-page và off-page.

- **On-page techniques**:

	+ Kĩ thuật on-page sử dụng trên trang web của bạn nhằm cải thiện xếp hạng của họ trên công cụ tìm kiếm. Thành phần chính của việc tìm kiếm đó chính là nhìn vào từ khóa mà họ nhập vào công cụ tìm kiếm nếu muốn tìm trang web của bạn, nó bao gồm các văn bản và code HTML để công cụ tìm kiếm biết rằng trang web của bạn bao gồm các chủ đề gì.

	+ Công cụ tìm kiếm sẽ dựa vào văn bản trong trang web của bạn điều này rất quan trọng, mục đích mọi người tìm kiếm được chứa trong văn bản. Phải đảm bảo bất cứ hình ảnh nào cũng có nội dung giá trị phù hợp cho các thuộc tính của họ giúp cho công cụ tìm kiếm hiểu được nội dung của hình ảnh.

- **Off-page techniques**:

	+ Các trang web khác liên kết tới bạn là rất quan trọng như kĩ thuật on-page. Công cụ tìm kiếm sẽ giúp xác định xếp hạng của trang web bằng cách nhìn vào số trang web khác liên kết đến bạn. Trong trang web họ quan tâm đặc biệt đến nội dung có liên quan tới bạn.

	+ Công cụ tìm kiếm cũng nhìn vào từ khóa giữa thẻ mở `<a>` và thẻ đóng `</a>` trong liên kết. Nếu như văn bản trong liên kết có chứa từ khóa (không cần thiết là phải click vào trang web của bạn) nó có thể sẽ được xem xét để lựa chọn sao cho phù hợp. Những từ khó xuất hiện trong liên kết của bạn cũng sẽ xuất hiện trong các văn bản của các trang mà trang web liên kết đến.

#### 1.2 ON-PAGE SEO:

Trong mỗi trang web thì 7 vị trí trọng tâm nơi từ khóa có thể xuất hiện để cải thiện khả năng tìm kiếm nó.

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task22_Book_HTML_and_CSS_design_and_build_websites/Chapter19_Practical%20%20Information/1.png"/></p>

1. **Page Title**: Tiêu đề của trang xuất hiện phía trên đầu cửa sổ trình duyệt hoặc xuất hiện trên tab của trình duyệt. Nó được xác định trong phần tử `<title>` được đặt bên trong phần tử `<head>`.

2. **URL/WEB Address**: Tên file là đường dẫn của URL, nơi có thể sử dụng từ khóa trong tên file.

3. **Headings**: nếu như từ khóa nằm trong phần tử tiêu đề `<hn>` thì công cụ tìm kiếm sẽ biết được trang web này nói về chủ đề gì và sẽ đánh giá trang cao hơn các trang khác. 

4. **Text**: Đặt ở những nơi cần thiết nó giúp cho các từ khóa trong nội dung chính được lặp lại 2,3 lần

5. **Link text**: Sử dụng các từ khóa trong văn bản mà tạo liên kết giữa các trang thay vì sử dụng từ khóa thông thường là bấm vào đây.

6. **Image Alt Text**: độ tin cậy của công cụ tìm kiếm dựa vào cung cấp mô tả chính xác về hình ảnh trong văn bản, điều này cũng giúp cho hình ảnh của bạn hiển thị trong kết quả tìm kiếm.

7. **Page Descriptions**:  Phần mô tả cũng nằm trong phần tử `<heaa>` và sử dụng để xác định thẻ `<meta>`, là 1 câu dùng để mô tả nội dung của trang

#### 1.3 HOW TO IDENTIFY KEYWORDS AND PHRASES (cách xác định từ khóa và cụm từ):

Xác định từ khóa để sử dụng trong website của bạn là 1 trong những việc khó khăn nhất trong SEO, sau đây là 6 bước xác định từ khóa cụm từ thích hợp cho trang web:

1. **Brainstorm**: Liệt kê danh sách những từ mà 1 người nào đó có thể gõ vào Google để tìm kiếm trang web của bạn, danh sách đó phải bao gồm các chủ đề khác nhau, các sản phẩm hoặc địch vụ liên quan đến trang web của bạn, danh sách có thể bao gồm các cụm từ khóa, nếu như website của bạn có 1 chủ đề thì hãy mô tả nó bới nhiều từ khác nhau.

2. **Organize**: Nhóm các từ khóa vào các danh sách riêng tùy thuộc vào từng vùng chọn, hoặc thể loại trang của website của bạn. Đối với các trang web lớn có thể chia nhỏ thành nhiều mục nhỏ

3. **Research**: Có 1 vài công cụ cho phép nhập từ khóa vào và họ sẽ đề nghị thêm 1 vài từ khóa để bạn xem xét, ví dụ như:

	+ adwords.google.co.uk/

	+ select/KeywordToolExternal

	+ www.wordtracker.com

	+ www.keyworddiscovery.com

4. **Compare**: Nó không đảm bảo trang web của bạn sẽ xuất hiện đầu tiên bởi công cụ tìm kiếm cho mọi từ khóa, điều này đúng cho các tiêu đề có nhiều sự cạnh tranh. Việc tìm kiếm bằng từ khóa cho bạn biết có bao nhiêu người đã tìm kiếm 1 từ khóa cụ thể và biết được có bao nhiêu sự cạnh tranh đối với điều khoản đó. Ngoài ra còn có thể sử dụng tính năng tìm kiếm nâng cao của Google để tìm các title của trang web, nó sẽ giúp xác định có bao nhiêu trang web có từ khóa trong title của họ.

5. **Refine**: Cần phải chọn các từ khóa trọng tâm có liên quan mật thiết tới các phần trong trang web của bạn. Nếu như có 1 cụm từ rất liên quan tới trang web của bạn nhưng có rất nhiều sự cạnh tranh thì vẫn nên sử dụng nó. Để trang web của bạn dễ được tìm kiếm có thể xem xét các cụm từ khác có thể phù hợp hơn.

6. **Map**: Khi có danh sách các từ khóa chính bao gồm từ khóa có sự cạnh tranh nhất và từ khóa liên quan nhiều nhất với trang web của bạn, nên bắt đầu với việc chọn từ khóa để sử dụng cho mỗi trang. Chọn 3-5 từ hoặc cụm từ cho bản đồ để mỗi trang sử dụng từ khóa phù hợp. Không nên lặp lại cùng 1 từ khóa trên tất cả các trang

<a name="2"></a>
### 2. Using analytics to understand visitors:

#### 2.1 ANALYTICS: LEARNING ABOUT YOUR VISITORS:

Khi người khác truy cập vào trang web của bạn có thể phân tích làm thế nào để tìm thấy họ, và họ tìm kiếm điều gì và tại vị trí nào mà họ rời đi. Một trong những công cụ tốt nhất để làm điều này là Google Analytics.

- **Signing up**: Dịch vụ Google Analytics dựa trên việc đăng kí 1 tài khoản. Các trang web sẽ cung cấp cho bạn các mã theo dõi để đặt vào các trang web của bạn.

- **How It Works**: Mỗi lần có người tải trang web của bạn mã theo dõi se gởi dữ liệu về cho máy chủ Google, nơi nó được lưu trữ, Google sẽ cung cấp 1 giao diện webbased cho phép bạn thấy được cách mà khách truy cập sử dụng website của bạn.

- **The Tracking Code**: Các mã theo dõi được cung cấp bởi Google Analytics cho mỗi trang web mà bạn đang theo dõi. Nó được đặt trước thẻ đóng `</head>`. Đoạn mã sẽ không làm thay đổi sự xuất hiện của trang web của bạn.

#### 2.2 HOW MANY PEOPLE ARE COMING TO YOUR SITE:

Trang tổng quan cung cấp 1 bản chụp các thông tin quan trọng mà bạn muốn biết bao gồm có bao nhiêu người truy cập vào trang web của bạn.

- **Visits**: đây là 1 con số tại 1 thời điểm nào đó mọi người truy cập vào trang web của bạn. Nếu người nào đó ngừng hoạt động trên trang web của bạn 30 phút và vào 1 trang khác trên trang web của bạn thì sẽ được xem là lần truy cập mới.

- **Unique Visits**: Đây là tổng số người đã truy cập vào trang web của bạn so với thời gian quy định. Số lượng truy cập này sẽ thấp hơn so với số lần truy cập nếu như 1 người có thể truy cập trở lại nhiều hơn 1 lần trong thời gian quy định.

- **Page Views**: tổng số trang khách truy cập đã xem trên trang web của bạn.

- **Page Per Visit**: Số lượng trang trung bình mỗi khách truy cập xem trên trang web của bạn trong mỗi lần truy cập.

- **Average Time On Site**: thời gian trung bình mà mỗi người dùng bỏ ra mỗi lần trên trang web.

- **Date Selector**: Sử dụng chọn ngày trên góc phải của trang web có thể thay đổi thời gian báo cáo hiển thị.

#### 2.3 WHAT ARE YOUR VISITORS LOOKING AT:

Các nội dung liên kết cho phép bạn biết được khách truy cập nhìn thấy gì khi đến với trang web của bạn.

- **Pages**: Cho biết trang nào được khách truy cập tìm kiếm nhiều nhất và trang nào được họ dành nhiều thời gian quan tâm nhất.

- **Landing Pages**: Đây là những trang được tìm đến đầu tiên khi truy cập trang web, nó đặc biệt hữu ích bởi có thể thấy rằng nhiều người không phải lúc nào cũng truy cập vào trang chủ của bạn trước.

- **Top Exit Pages**: Cho thấy trang nào ít được quan tâm nhiều và khách truy cập thường xuyên rời đi, và có thể nên xem xét thay đổi hay cải thiện trang đó.

- **Bounce Rate**: cho biết số lượng người còn lại trên cùng 1 trang khi họ truy cập. Khi tỉ lệ rời đi cao có thể nội dung đó không phải là họ đnag tìm kiếm. 1 lần thoát được tính như sau:

	+ Click đến 1 trang web khác

	+ Click vào 1 quảng cáo

	+ Nhập 1 URL mới

	+ Dùng nút trở lại

	+ Đóng trình duyệt

#### 2.4 WHERE ARE YOUR VISITORS COMING FROM

Liên kết nguồn cho biết khách truy cập đang truy cập từ đâu.

- **Referrers**: hiển thị các trang web có liên kết đến bạn và số lượng người đã thăm trang web.

- **Direct**: hiển thị cách truy cập đến trang web của bạn không thông qua 1 liên kết trong trang web khác, có thể nhập URL vào trình duyệt sử dụng 1 trình duyệt bookmark hoặc click vào liên kết trong email, PDF hoặc tài liệu Word.

- **Search Terms**: cho thấy mục đích của người sử dụng nhập vào công cụ tìm kiếm để tìm trang web của bạn. Điều này giúp bạn học cách mô tả với khách truy cập những gì họ đang tìm kiếm, giúp chỉnh sửa nội dung và từ khóa SEO.

- **Advanced Features**: có thể thiết lập các mục tiêu đường dẫn mà bạn muốn mọi người lấy, làm đường dẫn cho họ để đến với trang web của bạn, xem cách họ truy cập vào trang web thông qua cách nào, điều này đặt biệt hữu ích để thu thập dữ liệu từ người dùng.

<a name="3"></a>
### 3. Putting your site on the web:

#### 3.1 DOMAIN NAME & HOSTING:

Để đưa trang web của bạn lên trên website thì cần có tên miền và web hosting.

- **Domain Names**: Tên miền là địa chỉ trang web của bạn, có rất nhiều trang web cho phép đăng kí tên miền và phải trả 1 khoản phí hàng năm để duy trì nó. Các trang web này thường chứa 1 form cho phép kiểm tra các tên miền ưu thích có sẵn, có rất nhiều tên miền đã được đăng kí vậy nên sẽ mất 1 thời gian để tìm thấy 1 tên miền phù hợp, 1 số trang web cung cấp tên miền cũng cung cấp web hosting.

- **Web Hosting**: để mọi người có thể nhìn thấy trang web của bạn cần tải nó lên 1 máy chủ web. Máy chủ web là máy tính đặc biệt liên tục kết nối internet, được thiết lập để phục vụ các trang web khi được yêu cầu. Trừ các trang web lớn thì hầu hết các trang web đều tồn tại trên máy chủ web chạy bởi web hosting công ty, điều này rẻ hơn và tin cậy hơn.

#### 3.2 FTP & THIRD PARTY TOOLS:

- Để truyền code hay hình ảnh từ máy tính của bạn tới hosting company thì sử dụng giao thức truyền file gọi là FTP. Có nhiều chương trình FTP cung cấp 1 giao diện đơn giản hiển thị file trên máy tính 1 bên và 1 bên là máy chủ web của bạn, bạn chỉ việc kéo thả từ máy tính lên máy chủ và ngược lại.

- Một số công ty Hosting cũng cung cấp các công cụ để tải file lên máy chủ của họ sử dụng 1 trình duyệt web, nhưng phổ biến và nhanh hơn thì vẫn là chương trình FTP. Khi mua web hosting bạn sẽ được cung cấp chi tiết về FTP mà bạn nhập vào chương trình FTP để kết nối đến máy chủ. Thường thì nó là 1 địa chỉ, tên người dùng và mật khẩu. Cần bảo mật thông tin này ngăn chặn người lạ tiếp cận đến máy chủ của bạn. Đây là 1 loạt các trang web cung cấp dịch vụ được tạo bởi các nhà phát triển web:

	- **Danh sách các ứng dụng FTP phổ biến**: FileZilla, FireFTP, CuteFTP, SmartFTP, Transmit...

	- **Danh sách công cụ bên thứ 3 phổ biến**: Blogs, E-commerce, Email Newsletters, Social Networking Sharing Buttons.

<a name="4"></a>
### Tài liệu tham khảo

> [1] Duckett, J. (2011). HTML and CSS: design and build websites. John Wiley & Sons. 

