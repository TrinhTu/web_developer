##Bài: CRAWLER AND SPIDER

>Tài liệu: Crawler and Spider
>
>Người thực hiện: Lê Tú Trinh
>
>Cập nhập lần cuối: 12/12/2016

###Mục lục:

[1. Các khái niệm cơ bản](#1)

[2. Cách thức để thực hiện Crawler](#2)

[3. Cách thức hoạt động của Google search](#3)

[4. Tài liệu tham khảo](#4)

###Nội dung:

<a name="1"></a>
####1. Các khái niệm cơ bản:

- **Spider** hay **Crawler** đều là những phần mềm (công cụ) dùng để thu thập dữ liệu cho các công cụ tìm kiếm, chúng có tên gọi chung là Web Crawler. Phần mềm này được thiết kế để có thể duyệt website trên World Wide Web 1 cách có hệ thống với mục đích thu thập thông tin của trang web đó về công cụ tìm kiếm

- **Crawler** là phần mềm có khả năng tự động lấy dữ liệu như hình ảnh, text..., chức năng chính của nó là tự động phân tích dữ liệu từ nguồn nội dung sau đó bóc tách những thông tin cần thiết theo tiêu chí mà lập trình viên hệ thống thiết lập. Đây chính là chức năng của Web Crawler. 

Crawler được viết bởi rất nhiều ngôn ngữ: python, C#, java, PHP,... 

- **Spider**(nhện): có chức năng và nhiệm vụ len lỏi vào từng ngóc ngách trên trang và truy cập vào từng liên kết có trên trang, tạo liên kết giữa 2 trang với nhau. Từ 1 website ban đầu, Spider có thể kết nối thêm nhiều website lại thành 1 mạng lưới chằng chịt.

<a name="2"></a>
####2. Cách thực hiện Crawler:

Cách xây dựng mô hình crawler đơn giản nhất:

- Chọn URL khởi đầu

- Sử dụng HTML protocol để lấy trang web

- Trích xuất ra các link, lưu lại trong database

- Lặp đi lặp lại 2 bước trên

**Công việc của Web Crawler:**

- Đầu tiên Spider sẽ phải ghé thăm trang web nào đó, sau đó tìm kiếm tập tin `robots.txt`, tập tin này sẽ hướng dẫn spider cần lấy phần nào và bỏ qua phần nào( tức là những phần nào mà chủ trang web đó không cho phép công cụ tìm kiếm đụng đến sẽ bị spider bỏ qua). Việc sử dụng crawler truy cập vào các trang web thường gây ra tình nghẽn mạch, nên các website thường có qui định dành riêng cho các crawler và thường được lưu dưới dạng văn bản `robots.txt` ngay dưới thư mục gốc.

<a name="3"></a>
####3. Cách thức hoạt động của Googe search:

Google search gồm 3 bộ phận chính.

- Bộ phận thu thập dữ liệu: gồm google spider, crawler, bot.... Spider đi từ trang này trong trang khác để khám phá nội dung và các liên kết trong trang web. Google bot là 1 chương trình thu thập dữ liệu và phát hiện ra các trang web mới, thay đổi các trang web hiện có và các liên kết không tồn tại, các dữ liệu này được sử dụng để cập nhập cho các chỉ mục của google.

- Bộ phận lập chỉ mục: Đây là quá trình xây dựng cơ dữ liệu của các từ khóa, cụm từ, các trang web và các liên quan đến 1 lĩnh vực nào đó

- Bộ phận xử lí tính toán: Đây là quá trình tính toán của google nhằm cung cấp kết quả cho người tìm kiếm. Có hơn 200 yếu tố để xác định trang web, yếu tố quan trọng nhất để xếp hạng là dựa trên chất lượng nội dung của những liên kết đến trang web

Cơ chế hoạt động của Google Search:

- Search Engine sử dụng Web Crawler để khám phá và tìm hiểu thông tin trên các trang web, các công cụ tìm kiếm thông tin như Spider hay Crawler sẽ vào từng trang web và dò tìm theo từng liên kết có trong trang web đó. Nó sẽ đánh chỉ mục các từ khóa trên trang và theo các liên kết tìm thấy bên trong trang web. 

- Tiếp theo đó thì Google sẽ xây dựng chỉ mục để giúp cho các thông tin được tìm thấy 1 cách nhanh chóng, việc tìm kiếm thông tin trên trang web là 1 quá trình không bao giờ kết thúc bởi vì quản trị web luôn thay đổi thông tin, và cập nhập thông tin 1 cách liên tục.

- Sau khi thiết lập chỉ mục xong thì Google sẽ xử lí và tính toán mã hóa thông tin để lưu trữ trong cơ sở dữ liệu.

<a name="4"></a>
###Tài liệu tham khảo:

[1] Anh. Crawler

Online: http://viet.jnlp.org/tai-nguyen-ngon-ngu-tieng-viet/ke-hoach-xay-dung-tu-dong-corpus-tu-nguon-web/crawler

[2] Đào Tú. Thuật ngữ spider, crawler, bot.

Online: http://dautuseo.com/thuat-ngu-spider-crawler-bot-la-gi/

[3] Chia sẻ số. Crawler thu thập thông tin tự động là gì?

Online: http://chiaseso.vn/crawler-thu-thap-thong-tin-tu-dong-la-gi/

[4] Anh Diệp. Curl PHP

Online: https://www.youtube.com/watch?v=vTPoNYgFzTI

[5] Anh Diệp. Giới thiệu về Crawler

Online: https://www.youtube.com/watch?v=ywtIokgCCR8
