## HTML & CSS

### EXTRA MARKUP

> Chương 8: Extra Markup
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 28/01/2017

## Mục lục:

[1. Giới thiệu](#1)

[2. Nhận dạng và nhóm các phần tử](#2)

[3. Nhận xét, thay đổi thông tin và iframes](#3)

***

<a name="1">
### 1. Giới thiệu:

Trong chương này chúng ta sẽ tìm hiểu các nội dung chính sau đây:

- Sự khác nhau của các phiên bản HTML và cách nhận dạng phiên bản để sử dụng

- Cách thêm chú thích khi code

- Khái niệm chung của các thuộc tính, với mỗi thuộc tính có thể  sử dụng nhiều phần tử bao gồm thuộc tính `class` và `id`.

- Cách gắn trang vào trang sử dụng iframes

- Thêm thông tin về trang web có sử dụng phần tử `<meta>`

- Thêm tác giả và biểu tượng bản quyền

#### Sự phát triền của ngôn ngữ HTML (The Evolution Of HTML):

Một vài sự khác nhau của các phiên bản HTML:

- Mỗi một phiên bản mới lại được thiết kế với nhiều cải tiến hơn các phiên bản cũ.

- Trong đó có 1 số phiên bản của mỗi trình duyệt sử dụng để trang trí trang web, nhưng nó không sử dụng cho hầu hết các trang web, có 1 vài trình duyệt cũ cài đặt cho máy tính của họ, mà không phải ai cũng có thể xem tất cả các tính năng mới nhất và đánh dấu.

- HTML4, XHTML 1.0, HTML5.

<a name="2"></a>

### 2. Nhận dạng và nhóm các phần tử:

#### DOCTYPES:

- Mỗi một trang web nên bắt đầu với một `DOCTYPE` để nói với trình duyệt là đây là trang web sử dụng ngôn ngữ HTML (trình duyệt sẽ không hiển thị nội dung đó). Việc sử dụng DOCTYPE sẽ giúp cho trình duyệt đọc trang web 1 cách chính xác nhất.

- Bởi vì XHTML được viết trong XML,đôi khi thấy các trang sử dụng XHTML DOCTYPE khởi đầu đúng khai báo tùy chọn XML. Trường hợp này được sử dụng đầu tiên trong tài liệu. Nó phải là không có gì trước đó, không được có khoảng trống.

#### Comments In HTML:

- Nếu muốn thêm chú thích bình luận trong đoạn code của bạn (nó sẽ không được hiển thị), thì cần thêm đoạn văn có dạng: `<!--comment goes here-->`

- Cách thêm chú thích vào đoạn code giúp cho việc viết trang web, chỉnh sửa nội dung trở nên dễ dàng và dễ hiểu hơn

- Mặc dù chú thích không được hiển thị để người truy cập nhìn thấy trong cửa sổ trình duyệt chính, nhưng họ có thể xem nó bất cứ lúc nào bằng cách hiển thị mã nguồn của trang.

- Trong 1 trang web dài bạn thường xuyên thấy sử dụng chú thích để chỉ định vùng chọn của trang bắt đầu và kết thúc trang, nó sẽ giúp bất cứ người nào khi nhìn vào cũng có thể hiểu đoạn code

#### Thuộc tính ID:

- Mọi phần tử HTML đều có thể mang thuộc tính `id`. Nó được sử dụng duy nhất xác định sự khác nhau của các phần tử trong trang. Giá trị của các phần tử nên bắt đầu với kí tự hoặc đường kẻ (không được là số hay các yếu tố khác). Điều quan trọng là không được có 2 phần tử giống nhau trong cùng 1 trang.

- Nếu học về Javascript (ngôn ngữ cho phép thêm sự tương tác cho trang web), thuộc tính `id` có thể sử dụng cho phép script làm việc với phần tử khác.

#### Thuộc tính `CLASS`:

- Mọi phần tử HTML đều có thể áp dụng thuộc tính `class`. Đây không phải là thuộc tính duy nhất, nó xác định cho mọi phần tử trong tài liệu. Ví dụ như có 1 đoạn văn bản chứa thông tin, muốn phân biệt các yếu tố này hoặc muốn phân biệt giữa các liên kết trỏ đến trang web khác và liên kết đó nằm ngoài trang web của bạn. Để thực hiện điều đó có thể sử dụng thuộc tính class. Giá trị của nó mô tả lớp của nó

- Thuộc tính class có thể đặt trong bất kì phần tử nào, có thể có giá trị giống nhau. Vì vậy, trong ví dụ giá trị của thuộc tính có thể sử dụng trong tiêu đề và liên kết.

- Mặc định sử dụng thuộc tính không ảnh hưởng đến cách trình bày 1 phần tử. Nó chỉ thay đổi sự xuất hiện của phần tử đó nếu nó sử dụng quy tắc CSS chỉ định 1 cách hiển thị khác.

### Block Elements:

- Một vài phần tử luôn xuất hiện trong 1 hàng riêng biệt trên cửa sổ trình duyệt. Nó được gọi là  phần tử `block level`. Ví dụ: `<h1>, <p>, <ul> và <and>`

#### Inline Elements:

- Một vài phần tử luôn xuất hiện tiếp theo trên cùng 1 hàng cùng với phần tử phía trước nó. Nó được gọi là phần tử `inline`. Ví dụ: `<a>, <b>, <em> và <img>`.

### Grouping Text & Elements In a Block:

- `<div>`: Phần tử `<div>` cho phép nhóm 1 tập hợp các phần tử với nhau trong 1 hộp block-level.

- Ví dụ: Có thể tạo 1 phần tử `<div>` chứa tất cả các phần tử tiêu đề của website của bạn hoặc tạo ra 1 phần tử `<div>` chứa bình luận của khách.

- Trong trình  duyệt nội dung của thẻ `<div>` sẽ bắt đầu trên 1 hàng mới, nhưng sẽ không có sự khác biệt về sự trình bày của trang. Sử dụng thuộc tính `id` hoặc `class` trong phần tử `<div>`, tuy nhiên nếu áp dụng quy tắc trong CSS để thay đổi sự xuất hiện của các phần tử nằm trong nó.

#### Grouping Text & Elements Inline:

- `<span>`: phần tử `<span>` hoạt động giống như phần tử `<div>`. Có 1 trong 2 cách sử dụng:

	+ Thành phần của văn bản, nơi phân biệt nó với văn bản xung quanh.

	+ Chứa các phần tử nằm trên cùng 1 hàng. Đó là lí do mà mọi người sử dụng `<span>` như họ có thể kiểm soát sự xuất hiện của nội dung của phần tử sử dụng CSS.

	+ Bạn thường thấy thuộc tính `id` hay `class` sử dụng phần tử `<span>`:

		- Để giải thích mục đích của phần tử `<span>`.

		- Vì vậy mà phong cách CSS có thể được áp dụng cho phần tử đã chỉ định giá trị cho các thuộc tính.

<a name="3"></a>
### IFRAMES, thay đổi thông tin, nhận xét:

#### IFRAMES:

- `<iframes>`: 1 iframes giống như 1 cửa sổ nhỏ đươc cắt thành trang của bạn- và trong cửa sổ đó có thể nhìn thấy 1 trang khác. Thuật ngữ iframe và viết tắt của inline frame.

- Cách sử dụng thông thường của iframes là nhúng 1 Google Map vào 1 trang. Các nội dung của iframe có thể là 1 trang HTML bất kì (nằm trên cùng 1 máy chủ hoặc 1 trang web bất kì)

- Iframe được tạo ra bằng cách sử dụng phần tử `<iframe>`. Một vài phần tử cần biết để sử dụng:

	+ **src**: Thuộc tính **src** chỉ ra URL của trang hiển thị trong frame

	+ **height**: Thuộc tính **height** chỉ ra chiều cao của iframe theo đơn vị pixels

	+ **width**: Thuộc tính **width** chỉ ra chiều rộng của iframe theo đơn vị pixels

	+ **scrolling**: Thuộc tính **scrolling** sẽ không hỗ trợ cho HTML5. Trog HTML4 và XHTML nó chỉ ra liệu iframe nên có thanh cuộn hay không Việc này rất quan trọng, nếu các trang bên trong iframe lớn hơn không gian cho phép (sử dụng thuộc tính chiều dài và chiều rộng). Thanh cuộn cho phép người dùng di chuyển xung quanh khung để xem nội dung, có thể lấy 1 hoặc 3 giá trị: yes (hiển thị thanh cuộn), no (ẩn thanh cuộn) và tự động (cho xem nếu cần).

	+ **frameborder**: Thuộc tính **frameborder** không hỗ trợ cho HTML5. Trong HTML4 và XHTML chỉ ra có nên có viền hay không. Giá trị 0 chỉ ra không hiển thị đường viền, giá trị bằng 1 chỉ ra hiển thị 1 đường viền.

	+ **seamless**: Trong HTML5 có thuộc tính mới là liền mạch được áp dụng cho iframe nơi không có thanh cuộn, nó không có giá trị, nhưng thường được cung cấp cho 1 seamless. Trình duyệt cũ không hỗ trợ seamless.

#### Information About Your Pages:

- `<meta>`: phần tử `<meta>` được sử dụng bên trong phần tử `<head>` và chứa thông tin về trang web của bạn.

- Nó không hiển thị cho người dùng nhưng đáp ứng 1 số mục đích như nói với công cụ tìm kiếm về trang web, tác giả tạo ra trang web...

- Phần tử `<meta>` không có thẻ đóng, sử dụng để chứa thông tin. Thuộc tính thông thường nhất là tên nà nội dung thuộc tính được sử dụng cùng nhau. Các thuộc tính xác định tính chất toàn bộ trang, giá trị của tên thuộc tính được thiết lập và giá trị bao gồm nội dung thuộc tính mà bạn muốn cài đặt.

- Giá trị của thuộc tính tên cho bạn bất cứ điều gì bạn muốn. Một số giá trị được định nghĩa phổ biến cho thuộc tính này là:

	+ **description**: Chứa mô tả về trang, mô tả này thông thường được dử dụng bởi các công cụ tìm kiếm để hiểu về trang đó, tối đa sử dụng 155 kí tự. Đôi khi được hiển thị trong kết quả tìm kiếm.

	+ **keyword**: Chứa 1 danh sách các từ khóa có thể được sử dụng để tìm kiếm trang

	+ **robots**: Chỉ định nơi công cụ tìm kiếm nên thêm trang này vào kết quả tìm kiếm của họ hay không.

- Các phần tử `<meta>` cũng sử dụng http-equiv và nội dụng thuộc tính trong 1 cặp, sau đây là 3 trường hợp của thuộc tính http equiv:

	+ **author**: xác định tác giả trang web

	+ **pragma**: ngăn chặn trình duyệt từ bộ nhơ đệm của trang

	+ **expires**: bởi vì trình duyệt thường lưu nội dung của trang vào bộ nhớ đệm, các tùy chọn khi hết hạn có thể được chỉ định khi trang hết hạn (không còn khoảng trống bộ nhớ cached)

#### Escape Characters:

- Có một số ký tự được sử dụng và được bảo vệ bởi mã HTML. (Ví dụ, trái và dấu ngoặc nhọn bên phải.)

- Muốn kí tự xuất hiện trên trang của bạn cần sử dụng kí tự `escape`.Ngoài ra còn các mã đặc biệc để hiển thị các kí tự bản quyền và nhãn dán hàng hóa. tiền tệ, kí tự toán học... Khi sử dụng các ký tự escape,điều quan trọng là để kiểm tra trang trong trình duyệt của bạn để đảm bảo các biểu tượng hiển thị đúng. Điều này là do một số phông chữ không hỗ trợ tất cả các kí tự và do đó cần phải xác định một phông chữ khác nhau cho những ký tự trong mã CSS của bạn.

### Tóm lại:

- DOCTYPE thông báo với trình duyệt phiên bản CSS đang sử dụng

- Có thể thêm chú thích vào giữa đoạn code: <!-- and -->

- Thuộc tính id và class cho phép xác định các phần tử đặc biệt

- Phần tử `<div>` và `<span>` cho phép nhóm các block-level và inline với nhau

- Các thẻ `<meta>` cho phép bạn để cung cấp tất cả các thông tin về trang web của bạn

- Ký tự escape được sử dụng để bao gồm các kí tự đặc biệt trong các trang của bạn như <,>, và ©.

<a name="4"></a>
### Tài liệu tham khảo

> [1] Duckett, J. (2011). HTML and CSS: design and build websites. John Wiley & Sons. 

