## HTML & CSS

### TEXT

> Chương 12: TEXT
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 09/02/2017

## Mục lục:

[1. Kích thước, phông chữ của văn bản](#1)

[2. In đậm, in nghiêng, chữ hoa, gạch dưới](#2)

[3. Khoảng cách giữa các dòng, từ và chữ](#3)

[Tài liệu tham khảo](#4)

***

Thuộc tính cho phép ta điều chỉnh sự xuất hiện của chữ được chia là 2 nhóm sau:

- Trực tiếp ảnh hưởng đến phông chữ và sự xuất hiện của nó (bao gồm kiểu chữ, chữ thường, in đậm hay in nghiêng và kích thước của văn bản)

- Có tác dụng tương tự trên văn bản nhưng không có vấn đề về phông chữ đang sử dụng (bao gồm màu sắc của văn bản, khoảng cách giữa các từ và chữ cái)

Định dạng của vản bản có thể có tác động đáng kể để đọc được các trang của bạn.

<a name="1"></a>
### 1. Kích thước, phông chữ của văn bản:

#### Typeface Terminology (thuật ngữ về kiểu chữ):

- **serif**: phông chữ Serif có thêm kết thúc nét chính của chữ cái, được gọi là nét nhô ra.

- **san-serif**: phông chữ không có chân kết thúc chữ bằng 1 đường thẳng làm cho thiết kế gọn gàn hơn.

- **monospace**: mỗi một phông chữ đơn (hoặc chiều rộng cố định) thì có chiều rộng giống nhau (phông non-monospace có độ rộng khác nhau)

**weight**: phông weight dùng để nhấn mạnh bên cạnh đó còn ảnh hưởng đến khoảng cách và độ tương phản của trang. Bao gồm các giá trị: light, medium, bold, black.

**Style**: bao gồm các giá trị: Normal, italic, oblique. italic mang hình dáng của chữ viết ẩu đối với 1 vài chữ. Oblique (chữ xiêng) mang phong cách của chữ bình thường được đặt vào trong 1 góc.

**stretch**: condensed, regular, extended. Trong việc căng chữ làm các chữ các mỏng hơn và gần nhau hơn, trong các phiên bản mở rộng gần đay thì chữ trở nên dày hơn và xa nhau

#### Choosing A Typeface For Your Website (chọn kiểu chữ cho website của bạn):

Khi chọn kiểu chữ cho website điều quan trọng là cần hiểu rằng trình duyệt chỉ hiển thị nó khi nó cài đặt trên máy tính người dùng.

#### Speccifying Typefaces (xác định kiểu chữ):

- Thuộc tính font-family cho phép chỉ định kiểu chữ sử dụng trong văn bản với việc áp dụng các quy tắc CSS. Giá trị của thuộc tính là tên kiểu chữ muốn sử dụng. Đối với người truy cập tới trang web của bạn thì kiểu chữ bạn sử dụng cần được cài đặt trên máy họ nếu không nó sẽ không thể hiển thị.

- Bạn cũng có thể chỉ định 1 danh sách các font cách nhau bởi dấu phẩy để nếu font chữ đầu tiên chưa được cài đặt thì có thể sử dụng font chữ thay thế trong danh sách. Nếu font chữ đó dài hơn 1 từ thì nên đặt nó trong dấu ngoặc kép. Nên sử dụng không quá 3 kiểu chữ trong 1 trang.

#### Size Of Type (kích thước của kiểu chữ):

**font-size**: thuộc tính font-size cho phép chỉ ra kích thước của font, một số cách chỉ định kích thước của phông là:

- **pixels**: đây là dùng thông dụng bởi trình duyệt cho phép người thiết kế điều khiển chính xác không gian văn bản chiếm trên website của họ. Đơn vị pixel là `px`.

- **percentages** (tỉ lệ phần trăm): mặc định kích thước của văn bản được cho bởi trình duyệt là 16px vì vậy kích thước của 75% sẽ là 12px, 200% là 32px.

- **ems**: 1 em tương đương với chiều rộng của 1 chữ m.

#### More Font Choice: 

**@font-face**: @font-face cho phép bạn sử dụng 1 phông, ngay khi nó không được cài đặt trên máy tính người sử dụng, bằng việc cho phép bạn chỉ định 1 đường dẫn đến bản sao của phông chữ sẽ được tải về nếu không được cài đặt trên máy người sử dụng. Có thể thêm sử dụng @font-face như sau:

```javascript
@font-face {
font-family: 'ChunkFiveRegular';
src: url('fonts/chunkfive.eot');}
h1, h2 {
font-family: ChunkFiveRegular, Georgia, serif;}
```

- **font-family**: Dùng để chỉ định tên của font. Tên này được sử dụng như giá trị của thuộc tính font-family

- **src**: chỉ định đường dẫn đến font, để kĩ thuật này hoạt động trong tất cả các trình duyệt cần phải chỉ định đường dẫn đến 1 vài phiên bản khác nhau của font.

- **format**: xác định các định dạng được cung cấp. Nhiều nhà sản xuất kiểu chữ không cho phép sử dụng phông chữ của họ theo cách này, nhưng có font mã nguồn mở có thể sử dụng 1 cách tự do. Danh sách của họ:

	+ www.fontsquirrel.com

	+ www.fontex.org

	+ www.openfontlibrary.org

- Google cũng cung cấp mã nguồn mở cho font, thay vì thêm @font-face thì liên kết đến tập tin CSS và tập tin font trên máy chủ của họ: www.google.com/webfonts

#### Understanding Font Formats:

- Các trình duyệt khác nhau cung cấp các định dạng font khác nhau, vì vậy cần cung cấp 1 số font thay đổi để đạt được trong tất cả các trình duyệt. Nếu không có nhiều định dạng cho font của bạn có thể tải font tại: 

	+ www.fontsquirrel.com/

	+ fontface/generator

<a name="2"></a>
### 2. In đậm, in nghiêng, chữ hoa, gạch dưới:

#### Bold

**font-weight**: Thuộc tính font-weight cho phép tạo chữ in đậm, nó gồm có 2 giá trị:

- **normal**: điều này làm văn bản xuất hiện trong 1 bố cục bất kì

- **bold**: làm cho văn bản xuất hiện in đậm. 

#### Ilatic 

**font-style**: Nếu muốn tạo văn bản in nghiêng có thể sử dụng thuộc tính font-style, gồm có 3 thuộc tính giá trị sau:

- **normal**: Làm cho văn bản xuất hiện theo kiểu bình thường

- **italic**: làm văn bản xuất hiện với chữ nghiêng

- **oblique**: làm văn bản xuất hiện theo chiều xiêng

Font Italic là font chữ truyền thống dựa trên thư pháp

#### Upprecase & Lowercase (chữ hoa & chữ thường):

**text-transform**: Thuộc tính này sử dụng để thay đổi văn bản với các giá trị sau:

- **uppercase**: văn bản hiển thị theo chữ in hoa

- **lowercase**: văn bản hiển thị theo chữ thường

- **capitalize**: chữ đầu tiên viết hoa

Khi sử dụng chữ in hoa nó sẽ làm tăng khoảng cách giữa các chữ trong trang làm cho trang trở nên dễ đọc hơn.

#### Underline & Strike (gạch dưới & gạch ngang):

**text-decoration**: thuộc tính này cho phép xác định các giá trị theo sau như:

- **none**: loại bỏ bất kì sự trang trí nào được áp dụng trong văn bản

- **underline**: thêm 1 đường thẳng gạch chân dưới văn bản

- **overline**: thêm 1 đường thẳng trên đầu văn bản

- **line-through**: thêm 1 dòng băng qua các từ

- **blink**: làm cho văn bản trở nên sống động hơn tạo hiệu ứng flash mở và tắt (tuy nhiên không khuyến khích sử dụng vì khá khó chịu)

Thuộc tính này thông thường được nhà thiết kế sử dụng để loại bỏ gạch dưới được trình duyệt đặt dưới cái link.

<a name="3"></a>
### 3. Khoảng cách giữa các dòng, từ và chữ:

#### Leading:

**Line-height**: leading được xác định là term typographers sử dụng theo chiều dọc giữa các dòng trong trong văn bản. Leading được đo từ đáy của chữ trong 1 dòng đến điểm trên cùng trong dòng tiếp theo.

- Trong CSS thuộc tính `line-height` thiết lập chiều cao của các dòng trong văn bản, vì vậy sự khác nhau giữa font-size và line-height là tương đương với leading. Tăng line-height tạo khoảng cách lớn hơn giữa các dòng trong văn bản.

- Tăng leading làm cho văn bản đọc dễ dàng hơn. Khoảng cách theo chiều dọc giữa các dòng nên rộng hơn khoảng cách giữa các chữ, nó giúp việc di chuyển mắt theo chiều dọc thay vì nhìn dòng phía dưới. Thiết lập tốt nhất khoảng 1.4 đến 1.5em bởi vì người sử dụng có thể điều chỉnh kích thước mặc định của văn bản, giá trị của thuộc tính lineheight tốt nhất là `em`, vì vậy khoảng cách giữa các dòng tương đối với kích thước văn bản mà người dùng đã chọn.

#### Letter & Word Spacing (khoảng cách giữa các từ):

**letter-spacing, word-spacing**

- **Kerning**: được sử dụng cho khoảng cách giữa các chữ, bạn có thể kiểm soát khoảng cách giữa mỗi từ với thuộc tính letter-spacing. Nó rất hữa ích để tăng kerning khi tiêu đề hay câu của bạn là chữ in hoa, còn nếu văn bản của bạn là 1 câu thường thì việc tăng hoặc giảm kerning làm văn bản trở nên khó đọc hơn.

- Ngoài ra còn có thể kiểm soát khoảng trống giữa các từ bằng cách sử dụng thuộc tính word-spacing. Giá trị chỉ định của thuộc tính là `em`. Mặc định khoảng trống giữa các từ là thiết lập bởi kiểu chữ (thường là 0.25em), đối với kiểu chữ in đậm hoặc bạn có thể tăng khoảng cách giữa các chữ, sau đó tăng độ rộng giữa các chữ sẽ giúp văn bản dễ đọc hơn.

#### Alignment:

**text-align**: thuộc tính này cho phép điều chỉnh lại văn bản, gồm 4 giá trị:

- **left**: chỉ ra rằng văn bản được căng bên trái left-aligned

- **right**: chỉ ra rằng văn bản được căng bên phải right-aligned

- **center**: căng chính giữa văn bản

- **justify**: căng đều các dòng trong văn bản ngoại trừ dòng cuối.

Có 1 vài đoạn văn bản nó được xem xét là dễ đọc nhất nếu được căng về bên trái. Văn bản căng đều về 2 bên tạo nên khoảng cách bằng nhau của các từ nhưng sẽ tạo ra kết thúc với những khoảng trống lớn và khoảng trống nhỏ với 1 số từ, điều này thường xảy ra với văn bản chứa các từ dài.

#### Vertical Alignment (căng theo đoạn thẳng):

**vertical-align**: Thuộc tính này không dành cho các phần tử block như `<p>`, `<div>`... Nó được sử dụng cho phần tử inline như `<img>`, `<em>` hoặc `<strong>`. Và nó cũng có các giá trị sau: baseline, sub, super, top, text-top, middle, bottom, text-bottom. Và nó cũng có chiều dài (pixels hoặc ems) hoặc phần trăm theo chiều cao.

#### Indenting Text:

**text-indent**: đây là thuộc tính cho phép thụt đầu dòng văn bản, có 1 số cách để thụt đầu dòng nhưng thường được đưa vào pixels hoặc ems. Nhưng nó có 1 số giá trị tiêu cực là có thể đẩy văn bản ra khỏi cửa sổ trình duyệt.

#### CSS3: Drop Shadow:

**text-shadow**: Thuộc tính này được sử dụng thông dụng mặc dù không được hỗ trợ trong tất cả các trình duyệt.

- Nó được sử dụng để tạo bóng đổ, tạo ra 1 số hiệu ứng cho văn bản. Giá trị của thuộc tính này khá phức tạp vì có tới 3 độ dài và 1 màu cho 1 bóng đổ

	+ Độ dài đầu tiên chỉ ra khoảng cách bên trái hay bên phải bóng đổ

	+ Độ dài thứ 2 chỉ ra khoảng cách từ đầu đến cuối bóng đổ

	+ Độ dài thứ 3 chọn và chỉ ra độ mờ nên áp dụng để thả bóng.

	+ Giá trị thứ 4 là màu sắc bóng đổ

#### First Letter Or Line:

**:first-letter, :first-line**

- Có thể chỉ ra các giá trị khác nhau cho chữ đầu tiên hoặc dòng đầu tiên của văn bản bên trong các phần tử sử dụng :first-letter và :first-line. Về kĩ thuật thì đây không phải là thuộc tính mà được gọi là **pseudo-element**. Nó cũng được sử dụng theo cách thông thường như các phần tử khác. 

- CSS giới thiệu cả **pseudo-element** và **pseudo-class**, ta có pseudo-element đóng vai trò như phần tử thêm vào trong đoạn code. Còn pseudo-class đóng vai trò như thêm giá trị cho thuộc tính class.

#### Styling Links:

**:link, :visited**: mặc định trình duyệt thường hiển thị các liên kết màu xanh da trời và gạch chân, họ sẽ thay đổi màu sắc của liên kết đã được truy cập để giúp người dùng biết trang họ đã truy cập. Trong CSS có 2 pseudo-class cho phép thiết lập các kiểu liên kết khác nhau và truy cập hay chưa được truy cập

- **:link**: Cho phép thiết lập phong cách cho liên kết chưa được truy cập

- **:visited**: Cho phép thiết lập phong cách cho các liên kết đã được nhấp vào. Thông thường sử dụng để điều chỉnh màu cho liên kết và cũng như xuất hiện có gạch chân hay không

Thường thì các pseudo-classes như `:hover` và `:active` được sử dụng để thay đổi sự xuất hiện khi người dùng rê chuột vào vào nhập vào nó.

#### Responding To Users:

**:hover, :acctive, :focus** 

Có 3 pseudo-classes cho phép thay đổi sự xuất hiện của các phần tử khi người dùng tương tác với chúng

- **:hover**: áp dụng khi người dùng hover trên 1 phần tử, thông thường được sử dụng để thay đổi sự xuất hiện của liên kết và button khi người dùng đặt con trỏ lên chúng. Nó không hoạt động trên các thiết bị sử dụng màn hình cảm ứng (như iPad)

- **:active**: áp dụng khi phần tử được kích hoạt bởi người sử dụng, ví dụ: khi nhấn vào button hay clicked vào liên kết.

- **:focus**: áp dụng khi phần tử có tiêu điểm, bất kì phần tử nào bạn tương tác với nó chẳng hạn như có 1 liên kết bạn click vào nó hay bất kì hình thức kiểm soát có trọng tâm nào. Focus xảy ra khi trình duyệt phát hiện ra bạn tương tác với 1 phần tử trong trang. Ví dụ như khi trỏ vào form input sẵn sàng để nhập - đây cũng chính là focus. Khi pseudo-classes được sử dụng chúng sẽ xuất hiện theo thứ tự: :link, :visited, :hover, :focus, :active

<a name="4"></a>
### Tài liệu tham khảo

> [1] Duckett, J. (2011). HTML and CSS: design and build websites. John Wiley & Sons. 

