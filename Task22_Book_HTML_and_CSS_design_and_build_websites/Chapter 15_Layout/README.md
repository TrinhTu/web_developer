## HTML & CSS

### LAYOUT

> Chương 15: LAYOUT
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 18/02/2017

## Mục lục:

[1. Kiểm soát vị trí của các phần tử](#1)

[2. Tạo bố cục của trang web](#2)

[3. Screen Sizes, Layout, CSS Framework](#3)

[Tài liệu tham khảo](#4)

***

<a name="1"></a>
### 1. Kiểm soát vị trí của các phần tử:

#### 1.1 KEY CONCEPTS IN POSITIONING ELEMENTS (cái khái niệm chính trong vị trí các phần tử):

**Building Blocks**: CSS xem mỗi phần tử HTML được đặt trong hộp riêng và hộp này có thể là block-level hoặc inline box.

> Block-level boxs luôn bắt đầu trên 1 dòng mới trong khi inline boxs nối tiếp ý giữa văn bản xung quanh. Có thể kiểm soát khoảng trống cho mỗi hộp bằng cách thiết lập độ rộng của border. Để tạo sự khác biệt cho hộp có thể sử dụng borders, margins, padding và màu nền

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task22_Book_HTML_and_CSS_design_and_build_websites/Chapter%2015_Layout/image/2.png"/></p>

#### 1.2 CONTAINING ELEMENTS:

- Nếu 1 phần tử block-level được đặt trong phần tử block-level khác thì hộp bên ngoài được gọi là phần tử chứa, hay cha mẹ của phần tử đó.

- Nó thường được sử dụng để nhóm 1 số các phần tử với nhau vào trong phần tử `<div>`. Ví dụ có thể nhóm tất cả các phần tử lại với nhau để tạo thành tiêu đề của trang web, phần tử `<div>` được chứa trong nhóm này được gọi là phần tử chứa. Một hộp có thể được lồng vào bên trong 1 số phân tử blocl-level. Phần tử chứa đó đóng vai trò là phần tử mẹ của phần tử đó.

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task22_Book_HTML_and_CSS_design_and_build_websites/Chapter%2015_Layout/image/3.png"/></p>

- Các đường màu cam trong sơ đồ này đại diện cho phần tử `<div>`. Tiêu đề là 1 phần tử `<div>`, là một trong các nội dung chính của trang, footer chính là phần...

#### 1.3 CONTROLLING THE POSITION OF ELEMENTS:

- CSS có các sơ đồ vị trí cho phép kiểm soát cách bố trí 1 trang như: normal flow, relative positioning và absolute positioning. Xác định sơ đồ vị trí bằng cách sử dụng thuộc tính trong CSS, có thể float phần tử bằng cách sử dụng thuộc tính float.

	+ **normal flow**: Mọi phần tử block-level đều xuất hiện trong 1 dòng mới, điều này làm cho các phần tử có xu hướng xuất hiện về phía dưới, mặc dù có thiết lập chiều rộng cho hộp và khoảng cách giữa 2 phần tử được đặt trong side-by-side thì 2 phần tử đó cũng không thể xuất hiện cạnh nhau được, đây là hành động mặc định của trình duyệt.

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task22_Book_HTML_and_CSS_design_and_build_websites/Chapter%2015_Layout/image/4.png"/></p>

<p align="center">Đây là đoạn paragraphs xuất hiện theo dọc theo chiều dọc của trang</p>

+ **Relative Positioning**: Cách này giúp di chuyển phần tử rời khỏi vị trí bình thường của nó, có thể di chuyển lên trên, sang phải, trái và xuống dưới nơi muốn đặt nó. Điều này thì không là ảnh hưởng đến các phần tử xung quanh.

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task22_Book_HTML_and_CSS_design_and_build_websites/Chapter%2015_Layout/image/5.png"/></p>

<p align="center">Đoạn paragraph này đã bị đẩy xuống bên dưới và về phía bên phải so với vị trí ban đầu của nó</p>

+ **Absolute Positioning**: Đây là vị trí các phần tử trong quan hệ chứa các phần tử khác, nó khác với vị trí thông thường, không làm ảnh hưởng đến các phần tử xung quanh nó. Vị trí các phần tử tuyệt đối di chuyển như người sử dụng kéo lên kéo xuống trang.

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task22_Book_HTML_and_CSS_design_and_build_websites/Chapter%2015_Layout/image/6.png"/></p>

<p align="center">Vị trí tiêu đề được đặt ở trên về phía bên phải và paragraph thì xuất hiện phía trên cùng màn hình</p>

- Để xác định nơi đặt box thì cần sử dụng thuộc tính `box ofset` để nói với trình duyệt nên đặt nó như thế nào.

	+ **Fixed Positioning**: Dưới đây là form liên quan đến vị trí tuyệt đối của các phần tử trong cửa sổ trình duyệt, phần tử với vị trí đã được fixes sẽ không làm ảnh hưởng đến các phần tử xung quanh và nó cũng sẽ không bị di chuyển khi người dùng kéo trang lên xuống.

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task22_Book_HTML_and_CSS_design_and_build_websites/Chapter%2015_Layout/image/7.png"/></p>

- **Floating elements**: 1 phần tử floating cho phép đưa phần tử đó ra khỏi vị trí ban đầu của nó, đặt nó về phía bên trái hoặc bên phải của hộp chứa. Khi float 1 phần tử thì phần tử đó sẽ trở thành phần tử block-level với các nội dung khác có thể flow.

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task22_Book_HTML_and_CSS_design_and_build_websites/Chapter%2015_Layout/image/8.png"/></p>

**Khi di chuyển bất kì phần tử nào khỏi vị trí bình thường của nó thì các boxs có thể bị chồng chéo lên nhau, thuộc tính `z-index` cho phép kiểm soát sự xuất hiện của các boxs theo cách tốt nhất.**

<a name="2"></a>
### 2. Tạo bố cục của trang web:

#### 2.1 NORMAL FLOW:

- **position: static**: Theo cách thông thường thì mỗi phần tử block-level đầu tiên kế tiếp phần tử trước, điều này được mặc định bởi trình duyệt đối với các phần tử HTML, cú pháp là: 

`position: static;`

- Không cần xác định chiều rộng của thuộc tính cho phần tử tiêu đề, vậy nên có thể thấy cách kéo giãn chiều rộng mặc định của toàn bộ cửa sổ trình duyệt.

#### 2.2 RELATIVE POSITIONING** (vị trí tương đối):

**position: relative**: di chuyển 1 phần tử trong quan hệ đến nơi nó sẽ được flow thông thường. 

- Trong ví dụ dưới đây có thể di chuyển thấp hơn 10px, nó sẽ nằm trong flow thông thường hoặc sang phải 20%. 

```
p.example {
position: relative;
top: 10px;
left: 100px;}
```

- Cũng có thể chỉ định phần tử có vị trí tương đối bằng sử dụng thuộc tính position với giá trị là relative. Di chuyển hộp lên xuống bằng cách sử dụng thuộc tính top bottom. Di chuyển hộp theo chiều ngang bằng cách sử dụng thuộc tính left right, giá trị của thuộc tính có đơn vị là pixels, tỉ lệ phần trăm hoặc ems.

#### 2.3 ABSOLUTE POSITIONING (vị trí tuyệt đối):

**position: absolute**: Khi thuộc tính position cho 1 giá trị cố định thì box được thoát ra khỏi flow thông thường và không làm ảnh hưởng đến các thuộc tính khác trong trang

- Box sẽ bù lại thuộc tính để xác định phần tử nên xuất hiện trong phần tử quan hệ của nó đang chứa (top hoặc bottom và left hoặc right). 

```
h1 {
position: absolute;
top: 0px;
left: 500px;
width: 250px;}
p {
width: 450px;}
```

- Theo như ví dụ trên thì tiêu đề sẽ được đặt ở đầu trang và cách vào 500px tính từ cạnh bên trái, chiều rộng của tiêu đề được thiết lập là 250px. Thuộc tính chiều rộng cũng được áp dụng đối với các phần tử `<p>` để ngăn không cho các văn bản chồng chéo lên nhau không đọc được.

- Theo mặc định hầu hết các trình duyệt sẽ thêm margin-top cho các phần tử `<h1>`, đó là lí do tại sao có 1 khoảng cách giữa đầu trình duyệt và phần tử `<h1>` đang chứa trong hộp, nếu muốn loại bỏ margin này thì sau phần tử `<h1>` kiểu quy tắc sau: `margin: 0px`

#### 2.4 FIXED POSITIONING (vị trí cố định):

**position: fixed**: đây là 1 kiểu của absolute positioning, đòi hỏi thuộc tính position có 1 giá trị cố định, khi người dùng đi chuyển trang lên xuống thì vị trí của nó cũng không bị thay đổi. Để kiểm soát vị trí cố định của box xuất hiện trong cửa sổ trình duyệt thì box sẽ sử dụng thêm 1 vài thuộc tính cơ bản.

**Ví dụ**:

```
h1 {
position: fixed;
top: 0px;
left: 50px;
padding: 10px;
margin: 0px;
width: 100%;
background-color: #efefef;}
p.example {
margin-top: 100px;}
```

- Trong ví dụ này ta có tiêu đề được đặt trên cùng về bên trái trong góc của cửa sổ trình duyệt. Khi người dùng kéo trang xuống, các đoạn paragraphs sẽ biến mất phía sau tiêu đề. 

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task22_Book_HTML_and_CSS_design_and_build_websites/Chapter%2015_Layout/image/9.png"/></p>

#### 2.5 OVERLAPPING ELEMENTS: 

**z-index**: Khi sử dụng relative, fixed, hay absolute positioning thì hộp có thể bị chồng chéo lên nhau, các yếu tố xuất hiện sau trong đoạn code HTML sẽ được đặt lên trên các yếu tố xuất hiện trước nó. Nếu muốn kiểm soát phần tử nào được đặt trước thì sử dụng thuộc tính `z-index`, với giá trị là 1 con số và phần tử nào có số lớn hơn thì được đặt trước. Đôi khi thuộc tính `z-index` còn được gọi là `stacking context`.

#### 2.6 FLOATING ELEMENTS:

**float**: Thuộc tính float cho phép đặt phần tử theo thông thường và về phía bên trái hoặc bên phải của phần tử chứa nó càng tốt. Bất cứ nội dung nào chứa trong phần tử chứa sẽ flow xung quanh phần tử được floated.

- Khi sử dụng thuộc tính float nên sử dụng thuộc tính width để xác định độ rộng để chỉ ra độ rộng mà phần tử sẽ float. Nếu không kết quả sẽ không phù hợp, box có thể mất đi toàn bộ chiều rộng của phần tử đang chứa.

#### 2.7 USING FLOAT TO PLACE ELEMENTS SIDE-BY-SIDE: 

- Một vài hộp được bố trí vị trí cạnh nhau, thuộc tính float sử dụng để đạt giải quyết vấn đề này. Khi phần tử bị float thì chiều cao của hộp có thể ảnh hưởng đến các phần tử trong nó. Trong ví dụ bên dưới có thể thấy 6 đoạn văn, và mỗi đoạn đều được thiết lập chiều rộng và thuộc tính float.

```
body {
width: 750px;
font-family: Arial, Verdana, sans-serif;
color: #665544;}
p {
width: 230px;
float: left;
margin: 5px;
padding: 5px;
background-color: #efefef;}
```

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task22_Book_HTML_and_CSS_design_and_build_websites/Chapter%2015_Layout/image/10.png"/></p>

- Trong đó đoạn thứ tư lại không hiển thị về bên trái của trang mà lại nằm dưới đoạn thứ 3. Để giải quyết vấn đề này thì thiết lập chiều cao của đoạn văn trùng với độ dài cao nhất, nhưng nó không phù hợp lắm. Vậy cách phổ biến hơn hết là sử dụng thuộc tính `clear` để giải quyết vấn đề này.

#### 2.8 CLEARING FLOATS:

**clear**: thuộc tính này xác định 2 bên của phần tử (left, right) nơi mà phần tử float không được phép float sang trái hay sang phải. Thuộc tính gồm có các giá trị sau:

- **left**: không được float về phía bên tay trái

- **right**: không được float về phía bên tay phải

- **both**: không được float về phía cả 2 bên

- **none**: có thể float được cả 2 bên

##### 2.9 CREATING MULTI-COLUMN LAYOUTS WITH FLOATS:

- Nhiều trang web sử dụng nhiều cột trong thiết kế của họ, để làm được điều này cần phải sử dụng phần tử `<div>` đại diện cho mỗi cột, đây là 3 thuộc tính CSS được sử dụng đểv xác định vị trí cho các cột:

	+ **width**: thiết lập chiều rộng cho cột

	+ **float**: vị trí cho các cột nối tiếp sau đó

	+ **margin**: tạo khoản cách giữa các cột

<a name="3"></a>
### 3. Screen sizes, layout, CSS Framework:

#### 3.1 SCREEN SIZES:

- Khách truy cập đến website của bạn sẽ sử dụng các thiết bị có kích thước màn hình khác nhau để hiển thị thông tin, vì vậy thiết kế phải phù hợp với 1 loạt màn hình có kích thước khác nhau.

- Khi thiết kế dành cho việc in ấn thì cần biết kích thước của giấy mà thiết kế của bạn sẽ được in trên đó. Kích thước màn hình người sử dụng ảnh hưởng lớn đến việc họ có thể mở cửa sổ trình duyệt và trang mà họ sẽ thấy.

#### 3.2 SCREEN RESOLUTION (Độ phân giải màn hình):

- Độ phân giải đề cập đến số lượng các chấm trên màn hình hiển thị trên mỗi inch. Một số thiết bị có độ phân giải cao hơn máy tính để bàn và nhất là các hệ điều hành cho phép người sử dụng chỉnh độ phân giải trên màn hình của họ.

#### 3.3 PAGE SIZES:

- Vì kích thước màn hình và độ phân giải khác nhau vì vậy các nhà thiết kế web thường tạo ra các trang có độ rộng là 960-1000 pixels (hầu hết người dùng có thể nhìn thấy thiết kế này trên màn hình của họ)

- Để người dùng có thể nhìn thấy toàn bộ nội dung trang mà không cần kéo trang xuống là 1 điều vô cùng khó. Các nhà thiết kế cho rằng người dùng có thể nhìn thấy 570-600 pixels trong 1 trang mà không cần kéo xuống, và cố gắng fit toàn bộ thông điệp chính vào khu vực này.

- Các khu vực trong trang mà người dùng không có chức năng cuộn lại được gọi là "above the fold". Nó được thừa nhận rằng nếu như người dùng quan tâm đến nội dung của trang, họ có thể cuộn xuống để xem nhiều thông tin hơn. Người dùng có khả năng đánh giá 1 trang, vậy nên điều này quan trọng là cung cấp cho khác truy cập thông tin cần thiết, khiến trang web này thật sự hữu ích đối với họ.

#### 3.4 FIXED WIDTH LAYOUTS:

Dùng để cố định chiều rộng của bố cục không được thay đổi kích thước bằng cách tăng hoặc giảm kích thước của cửa sổ trình duyệt.

- **Ưu điểm**: Giá trị pixel là được sử dụng chính xác để kiểm soát kích thước và vị trí của phần tử. Có thể kiểm soát độ dài của các dòng văn bản bất kì của kích thước cửa sổ của người sử dụng. Kích thước của ảnh sẽ tương đối giống với phần còn lại của trang.

- **Nhược điểm**: Có thể kết thúc bằng cách khoảng cách lớn xung quanh các cạnh của trang. Nếu như màn hình của người dùng có độ phân giải cao hơn màn hình của người sử dụng thì trang đó sẽ trông nhỏ hơn và văn bản trở nên khó đọc hơn. Nếu người dùng tăng kích thước của chữ thì văn bản có thể sẽ không phù hợp với không gian được phân bố.

#### 3.5 LIQUID LAYOUTS: 

**Liquid Layout** được thiết kế để người dùng có thể tăng hoặc giảm kích thước của cửa sổ trình duyệt và thường được sử dụng với tỉ lệ phần trăm.

- **Ưu điểm**: Trang sẽ được mở rộng ra để lấp đầy khoảng trống của cửa số trình duyệt vì vậy sẽ không tồn tại các khoảng trống xung quanh trang trên 1 màn hình rộng. Nếu như cửa sổ người sử dụng nhỏ thì trang có thể thu lại phù hợp mà không cần người dùng phải kéo xuống. Thiết kế cho phép người dùng thiết lập kích thước font lớn hơn so với chỉ định của người thiết kế.

- **Nhược điểm**: Nếu không kiểm soát chiều rộng của các phần trong trang thì thiết kế sẽ trở nên khác so với dự định của bạn, sẽ xuất hiện những khoảng trống xung quanh các phần tử hoặc các mục có thể bị trùng lên nhau. Nếu như người dùng có cửa sổ rộng thì các dòng trong văn bản sẽ trở nên dài hơn và khiến văn bản trở nên khó đọc hơn. Còn đối với cửa sổ hẹp thì chữ có thể sẽ bị ghi đè lên nhau và có thể chỉ có vài từ trên mỗi dòng. Nếu như thiết lập chiều rộng cố định cho vài mục trong 1 hộp quá nhỏ để chứa nó thì các mục đó (ví dụ như hình ảnh) có thể sẽ bị tràn ra ngoài văn bản.

#### 3.6 A FIXED WIDTH LAYOUT: 

- Dùng để tạo chiều rộng cố định của bố cục, chiều rộng của phần chính bên trong hộp trong trang thường xác định với đơn vị là pixels. Thật ra thì kết quả của fixed và liquid layout là giống nhau, vậy nên để có thể thấy rõ cách hoạt động của chúng thì xem cách chúng trong các trình duyệt, và phản ứng khi điều chỉnh kích thước của các cửa sổ trình duyệt. Fixed width layout là giống nhau không gặp vấn đề gì trong cửa sổ trình duyệt, còn chiều với Liquid Layout sẽ căng ra hoặc thu nhỏ lại để vừa màn hình.

#### 3.7 A LIQUID LAYOUT:

- Liquid Layout sử dụng phần trăm để xác định chiều rộng của mỗi hộp vì vậy các thiết kế sẽ được căng ra để vừa với kích thước của màn hình.

```
body {
width: 90%;
margin: 0 auto;}
#content {overflow: auto;}
#nav, #feature, #footer {
margin: 1%;}
.column1, .column2, .column3 {
width: 31.3%;
float: left;
margin: 1%;}
.column3 {margin-right: 0%;}
li {
display: inline;
padding: 0.5em;}
#nav, #footer {
background-color: #efefef;
padding: 0.5em 0;}
#feature, .article {
height: 10em;
margin-bottom: 1em;
background-color: #efefef;}
```

- Trong ví dụ trên phần tử `<body>` thiết lập chiều rộng của trang là 90% --> có 1 khoảng cách nhỏ giữa bên trái và bên phải cửa sổ trình duyệt với nội dung chính.

- 3 cột điều được cho margin là 1% và chiều rộng là 31.3% --> chiều rộng của phần tử `<body>` lên đến 99.9% vậy nên trình duyệt sẽ không căng hoàn toàn về phía bên phải của cột thứ 3 với các phần tử khác trong trang

- Phần tử `<div>` bao gồm navigation, feature, và footer sẽ căng ra để lấp đầy chiều rộng của phần tử đang chứa trong `<body>`. Chúng có margin là 1% để căng chỉnh với cột. Thuộc tính `min-width` và `max-width` giúp tạo các ranh giới mà layout có thể kéo căng ra.

#### 3.8 LAYOUT GRIDS: 

Bố cục dạng lưới rất quan trọng trong mỗi thiết kế, nếu muốn có được bố cục chặt chẽ rõ ràng thì không thể bỏ qua Layout Grids. Lưới được thiết lập tỉ lệ phù hợp với khoảng cách giữa các mục để tăng sự chuyên nghiệp cho thiết kế. Trong mạng lưới đó có hạn chế đó là:

- Tạo sự liên tục giữa 2 trang khác nhau sử dụng thiết kế khác nhau.

- Giúp người đọc tra cứu tìm kiếm thông tin trên trang.

- Dễ dàng hơn trong việc thêm mới 1 nội dung phù hợp.

#### 3.9 CSS FRAMEWORKS:

- CSS Frameworks giúp bạn dễ dàng hơn trong việc thiết kế bằng cách cung cấp code cho các nhiệm vụ thông thường như là: tạo layout grids, tạo kiểu cho forms... Có thể áp dụng CSS Framwork trong các dự án thiết kế của bạn hơn là viết CSS từ đầu.

	+ **Ưu điểm**: Tiết kiệm được các đoạn mã giống nhau với cùng 1 mục đích. Đã được test qua các phiên bản trình duyệt khác nhau để tránh lỗi của trình duyệt.

	+ **Nhược điểm**: Thường yêu cầu sử dụng tên class trong các mã HTML để kiểm soát sự trình bày của trang.

#### 3.10 MULTIPLE STYLE SHEETS:

**import**: 1 vài tác giả trang web thì chia quy tắc CSS style của họ thành style sheets riêng biệt, họ có thể sử dụng style sheet để kiểm soát bố cục, màu sắc, font chữ,... Có 2 cách để thêm nhiều style sheet cho 1 trang web:

1. Trang HTML của bạn có thể liên kết đến 1 style sheet và stylesheet sử dụng `@import` để import vào trong trang.

2. Trong HTML sử dụng một phần tử `<link>` riêng biệt cho mỗi style sheet

#### 3.11 MULTIPLE STYLE SHEETS:

**LINK**

```
<head>
<title>Multiple Style Sheets - Link</title>
<link rel="stylesheet" type="text/css"
href="css/site.css" />
<link rel="stylesheet" type="text/css"
href="css/tables.css" />
<link rel="stylesheet" type="text/css"
href="css/typography.css" />
</head>
```

- Ở phía trên có thể thấy sử dụng các kĩ thuật khác nhau bao gồm nhiều style sheets, bên trong phần tử `<head>` là các phần tử `<link>` riêng biệt và cho mỗi style sheet. Nội dung của site.css hoàn toàn giống với style.css ngoại trừ đoạn code không chứa quy tắc `@import`. Như đối với tất cả style sheet, nếu có 2 quy tắc được áp dụng cho cùng 1 phần tử thì quy tắc sau sẽ được ưu tiên trước. Vậy đối với ví dụ này thì `typography.css` sẽ được ưu tiên trước.

<a name="4"></a>
### Tài liệu tham khảo

> [1] Duckett, J. (2011). HTML and CSS: design and build websites. John Wiley & Sons. 

