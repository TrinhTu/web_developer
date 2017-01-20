## HTML & CSS

### Links

> Chương 4: Links
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 16/01/2017

## Mục lục:

[1. Creating links between pages](#1)

[2. Linking to other sites](#2)

[3. Email links](#3)

[Tài liệu tham khảo](#4)

***

<a name="1"></a>
### 1. Creating Link Between Pages:

Liên kết là những tính năng xác định của các trang web cho phép di chuyển từ trang web này đến 1 trang web khác. Chúng ta thường gặp các loại liên kết sau đây:

- Liên kết từ 1 trang web khác

- Liên kết từ trang này đến trang khác trên cùng 1 trang web

- Liên kết từ 1 phần của 1 trang web đến 1 phần khác cùng 1 trang

- Liên kết từ email của bạn đến địa chỉ email mới của ai đó

### Writing Links (tạo liên kết):

- Liên kết có thể tạo bằng cách sử dụng thẻ `<a>` người sử dụng có thể ghi bất cứ điều gì vào giữa thẻ mở và thẻ đóng `<a>`. Xác định trang web muốn liên kết đến bằng thuộc tính href.

`<a href="http://google.com">Hihi</a>`

- Văn bản nằm trong cặp thẻ `<a>` gọi là liên kết văn bản, khi nhấp vào văn bản đó nó sẽ liên kết đến 1 trang web khác thay vì nói rằng "Nhấp chuột vào đây". Nhiều người điều hướng các trang web bằng cách quét các văn bản. Các liên kết văn sẽ giúp người sử dụng tìm thấy những nội dung mà họ muốn. Điều này sẽ cung cấp cho người dùng ấn tượng tốt về trang web đó khuyến khích truy cập vào.

- Để viết 1 trang web hay thì cần suy nghĩ từ khóa nào sẽ sử dụng khi tìm kiếm đến các trang mà bạn liên kết đến.

<a name="2"></a>
### 2. Linking to other sites (Liên kết đến các trang web khác):

- Tạo liên kết bằng yếu tố thẻ `<a>` với thuộc tính giá trị `href`. Giá trị của thuộc tính href là trang mà bạn muốn mọi người liên kết đến khi họ click vào link.

- Người sử dụng có thể click vào bất kì chỗ nào xuất hiện ở giữa cặp thẻ `<a>` và sẽ đưa đến trang được xác định trong thuộc tính `href`.

- Khi liên kết đến 1 trang Web khác, giá trị của thuộc tính href sẽ hiển thị đầy đủ địa chỉ của trang web đó (URL)

- Trình duyệt sẽ hiển thị liên kết màu xanh da trời và mặc định là gạch chân ở dưới.

#### Linking to other pages on the same site (Liên kết đến 1 trang khác trong cùng 1 trang web)

- Khi liên kết đến 1 trang khác trong cùng 1 trang web bạn không cần xác định tên miền trong URL. Bạn có thể sử dụng cách viết tắt biết đến như URL tương đối.

- Nếu tất cả trang trong trang web nằm trong cùng thư mục và giá trị của thuộc tính href chỉ tên của file

- Nếu bạn có trang khác của website khác thư mục, bạn có thể sử dụng cú pháp phức tạp hơn để chỉ ra nơi liên kết đến trang hiện tại

- Nếu nhìn vào code của mỗi trang thì sẽ thấy rằng tập tin `index.html` chứa liên kết sử dụng URL tương đối.

#### Relative URLs:

- Khi liên kết đến trang khác trong cùng 1 trang web, có thể sử dụng các URL tương đối. Đây là kiểu viết tắt mà URL mà không cần chỉ định tên miền.

- URL tương đối giúp xây dựng trang web trong máy tính của bạn bởi vì chỉ cần tạo liên kết bất kì giữa trang mà không cần chuẩn bị tên miền của bạn hoặc nơi lưu trữ.

#### Directory Structure:

Trong các Website lớn đó là ý tưởng tốt để tổ chức mã của bạn bằng cách đặt các đoạn mã của trang web vào thư mục khác nhau

**Structure:**

- Mỗi phần của trang web đều được đặt trong các thư mục riêng biệt, giúp cho việc quản lí file 1 cách dễ dàng hơn. Các trang và hình ảnh trên website đều có URL. URL chính là đường dẫn đến trang hoặc hình ảnh đó.

- Thư mục gốc có chứa:

	+ File `index.html` là trang chủ cho toàn bộ website.

	+ Thư mục cá nhân chứa hình ảnh, âm thanh...Các thành phần khác tạo nên trang web.

**Relationships:**

- Quan hệ giữa tập tin và thư mục trong website được mô tả bằng cách sử dụng thuật ngữ thân thuộc.

**Homepages:**

- Khi bạn chỉnh sửa các tập tin mẫu có thể dẫn đến việc thay đổi toàn bộ các trang sử dụng mẫu đó, nếu như thay đổi mã HTML đồng nghĩa với việc phá vỡ nội dung ban đầu.

#### Relative URLs:

- Relative URL có thể được sử dụng khi liên kết đến 1 trang trong trang web riêng của bạn trên website. Họ cung cấp cách ngắn gọn nói cho trình duyệt nơi đặt file của bạn.  

- Đây là 1 điều đặc biệt giúp tạo 1 trang web mới hoặc tìm hiểu về HTML bởi về có thể tạo 1 liên kết ở giữa trang chỉ sử dụng máy tính cá nhân (đã có tên miền và đã tải liên web). Không cần đặt lại tên miền với mỗi liên kết.

- Khi tất cả tập tin trong trang web nằm trong 1 thư mục chỉ cần sử dụng tên file cho trang đó. Nếu trang web của bạn được sắp xếp thành các thư mục riêng thì cần thông báo cho trình duyệt cách hiện lên trang web mà muốn liên kết tới.

<a name="3"></a>
### 3. Email Links

- Để tạo ra liên kết mà khởi động chương trình email của người dùng và đến 1 địa chỉ mail xác định, có thể sử dụng thẻ `<a>`. Cú pháp này bắt đầu `mailto` và theo sau là địa chỉ mà muốn email gởi tới.

`a href="mailto:letutrinh.ktmm@gmail.com">Email Trinh</a>`

#### Opening Links In A New Window

- Khi muốn liên kết được mở trong cửa sổ mới thì sử dụng thuộc tính target bên trong thẻ mở `<a>`. Với giá trị là `_blank`.

- Tác giả hi vọng sau khi liên kết đến trang web khác trong tab mới thì người dùng sẽ quay trở lại trang chủ của họ và xem tiếp nội dung khác.

- Nên tránh mở liên kết trong cửa sổ mới, nếu như sử dụng cần tạo thêm thông báo là thông tin sẽ được mở trong cửa sổ mới trước khi họ click vào.

#### Linking To A Specific Part Of The Same Page

- Ở phần mục lục hoặc phía trên cùng của 1 trang dài ta cần sử dụng 1 danh sách các liên kết đến các trang phía dưới để tiết kiệm thời gian, người dùng có thể dễ dài lấy thông tin cần thiết mà không cần kéo xuống toàn bộ trang đó.

- Để tạo liên kết đến trang cần xác định các vị trí mà liên kết sẽ đi đến bằng thuộc tính `id`. 

- Giá trị của thuộc tính nên là kí tự hay gạch dưới... không nên sử dụng chữ số, hoặc thứ gì khác. Không được có 2 thuộc tính `id` giống nhau.

- Để thuộc tính `id` được áp dụng 1 cách chính xác thì phải sử dụng thẻ `<a>` nhưng giá trị thuộc tính href bắt đầu với kí tự `#` và tiếp đến là giá trị của thuộc tính `id` mà bạn muốn liên kết đến

#### Linking To A Specific Part Of Another Page

- Nếu muốn liên kết đến 1 phần cụ thể của trang web khác thì cũng sử dụng kĩ thuật tương tự.

- Xác định phần cụ thể của trang, thêm cùng cú pháp để phía sau liên kết đến trang đó. Thuộc tính `href` bây giờ sẽ chứa URL của trang đó sau đó là kí tự `#` và giá trị của thuộc tính `id`. 

### Tóm lại:

- Để tạo liên kết thì sử dụng thẻ `<a>`

- Yếu tố `<a>` sử dụng thuộc tính `href` để xác định trang muốn liên kết tới.

- Nếu muốn liên kết tới trang nằm trong cùng trang web của bạn thì sử dụng liên kết quan hệ hơn là URL

- Có thể tạo liên kết mở chương trình mail với địa chỉ mail nằm trong "to".

- Có thể sử dụng thuộc tính `id` để liên kết với các yếu tố nằm trong cùng 1 trang. 

<a name="4"></a>
### Tài liệu tham khảo:

> [1] Duckett, J. (2011). HTML and CSS: design and build websites. John Wiley & Sons.


