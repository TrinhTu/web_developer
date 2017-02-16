## HTML & CSS

### LAYOUT

> Chương 15: LAYOUT
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 16/02/2017

## Mục lục:

[1. Kiểm soát vị trí của các phần tử](#1)

[2. Tạo bố cục của trang web](#2)

[3. Thiết kế cho màn hình có kích thước khác nhau](#3)

***

#### KEY CONCEPTS IN POSITIONING ELEMENTS (cái khái niệm chính trong vị trí các phần tử):

**Building Blocks**: CSS xem mỗi phần tử HTML được đặt trong hộp riêng và hộp này có thể là block-level hoặc inline box.

> Block-level boxs luôn bắt đầu trên 1 dòng mới trong khi inline boxs nối tiếp ý giữa văn bản xung quanh. Có thể kiểm soát khoảng trống cho mỗi hộp bằng cách thiết lập độ rộng của border. Để tạo sự khác biệt cho hộp có thể sử dụng borders, margins, padding và màu nền

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task22_Book_HTML_and_CSS_design_and_build_websites/Chapter15_LAYOUT/image/2.png"/></p>

#### CONTAINING ELEMENTS:

- Nếu 1 phần tử block-level được đặt trong phần tử block-level khác thì hộp bên ngoài được gọi là phần tử chứa, hay cha mẹ của phần tử đó.

- Nó thường được sử dụng để nhóm 1 số các phần tử với nhau vào trong phần tử `<div>`. Ví dụ có thể nhóm tất cả các phần tử lại với nhau để tạo thành tiêu đề của trang web, phần tử `<div>` được chứa trong nhóm này được gọi là phần tử chứa. Một hộp có thể được lồng vào bên trong 1 số phân tử blocl-level. Phần tử chứa đó đóng vai trò là phần tử mẹ của phần tử đó.

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task22_Book_HTML_and_CSS_design_and_build_websites/Chapter15_LAYOUT/image/3.png"/></p>

- Các đường màu cam trong sơ đồ này đại diện cho phần tử `<div>`. Tiêu đề là 1 phần tử `<div>`, là một trong các nội dung chính của trang, footer chính là phần...

- 

#### CONTROLLING THE POSITION OF ELEMENTS:

- CSS có các sơ đồ vị trí cho phép kiểm soát cách bố trí 1 trang như: normal flow, relative positioning và absolute positioning. Xác định sơ đồ vị trí bằng cách sử dụng thuộc tính trong CSS, có thể float phần tử bằng cách sử dụng thuộc tính float.

	+ **normal flow**: Mọi phần tử block-level đều xuất hiện trong 1 dòng mới, điều này làm cho các phần tử có xu hướng xuất hiện về phía dưới, mặc dù có thiết lập chiều rộng cho hộp và khoảng cách giữa 2 phần tử được đặt trong side-by-side thì 2 phần tử đó cũng không thể xuất hiện cạnh nhau được, đây là hành động mặc định của trình duyệt.

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task22_Book_HTML_and_CSS_design_and_build_websites/Chapter15_LAYOUT/image/4.png"/></p>

<p align="center">Đây là đoạn paragraphs xuất hiện theo dọc theo chiều dọc của trang</p>

	+ **Relative Positioning**: Cách này giúp di chuyển phần tử rời khỏi vị trí bình thường của nó, có thể di chuyển lên trên, sang phải, trái và xuống dưới nơi muốn đặt nó. Điều này thì không là ảnh hưởng đến các phần tử xung quanh.

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task22_Book_HTML_and_CSS_design_and_build_websites/Chapter15_LAYOUT/image/4.png"/></p>

<p align="center">Đoạn paragraph này đã bị đẩy xuống bên dưới và về phía bên phải so với vị trí ban đầu của nó</p>

	+ **Absolute Positioning**: Đây là vị trí các phần tử trong quan hệ chứa các phần tử khác, nó khác với vị trí thông thường, không làm ảnh hưởng đến các phần tử xung quanh nó. Vị trí các phần tử tuyệt đối di chuyển như người sử dụng kéo lên kéo xuống trang.

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task22_Book_HTML_and_CSS_design_and_build_websites/Chapter15_LAYOUT/image/6.png"/></p>

<p align="center">Vị trí tiêu đề được đặt ở trên về phía bên phải và paragraph thì xuất hiện phía trên cùng màn hình</p>

- Để xác định nơi đặt box thì cần sử dụng thuộc tính `box ofset` để nói với trình duyệt nên đặt nó như thế nào.

	+ **Fixed Positioning**: Dưới đây là form liên quan đến vị trí tuyệt đối của các phần tử trong cửa sổ trình duyệt, phần tử với vị trí đã được fixes sẽ không làm ảnh hưởng đến các phần tử xung quanh và nó cũng sẽ không bị di chuyển khi người dùng kéo trang lên xuống.

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task22_Book_HTML_and_CSS_design_and_build_websites/Chapter15_LAYOUT/image/7.png"/></p>

	+ **Floating elements**: 1 phần tử floating cho phép đưa phần tử đó ra khỏi vị trí ban đầu của nó, đặt nó về phía bên trái hoặc bên phải của hộp chứa. Khi float 1 phần tử thì phần tử đó sẽ trở thành phần tử block-level với các nội dung khác có thể flow.

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task22_Book_HTML_and_CSS_design_and_build_websites/Chapter15_LAYOUT/image/8.png"/></p>

**Khi di chuyển bất kì phần tử nào khỏi vị trí bình thường của nó thì các boxs có thể bị chồng chéo lên nhau, thuộc tính `z-index` cho phép kiểm soát sự xuất hiện của các boxs theo cách tốt nhất.**

#### NORMAL FLOW:

- **position: static**: Theo cách thông thường thì mỗi phần tử block-level đầu tiên kế tiếp phần tử trước, điều này được mặc định bởi trình duyệt đối với các phần tử HTML, cú pháp là: 

`position: static;`

- Không cần xác định chiều rộng của thuộc tính cho phần tử tiêu đề, vậy nên có thể thấy cách kéo giãn chiều rộng mặc định của toàn bộ cửa sổ trình duyệt.

#### RELATIVE POSITIONING** (vị trí tương đối):

**position: relative**: di chuyển 1 phần tử trong quan hệ đến nơi nó sẽ được flow thông thường. 

- Trong ví dụ dưới đây có thể di chuyển thấp hơn 10px, nó sẽ nằm trong flow thông thường hoặc sang phải 20%. 

```
p.example {
position: relative;
top: 10px;
left: 100px;}
```

- Cũng có thể chỉ định phần tử có vị trí tương đối bằng sử dụng thuộc tính position với giá trị là relative. Di chuyển hộp lên xuống bằng cách sử dụng thuộc tính top bottom. Di chuyển hộp theo chiều ngang bằng cách sử dụng thuộc tính left right, giá trị của thuộc tính có đơn vị là pixels, tỉ lệ phần trăm hoặc ems.

#### ABSOLUTE POSITIONING (vị trí tuyệt đối):

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

#### FIXED POSITIONING (vị trí cố định):

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

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task22_Book_HTML_and_CSS_design_and_build_websites/Chapter15_LAYOUT/image/9.png"/></p>

#### OVERLAPPING ELEMENTS: 

**z-index**: Khi sử dụng relative, fixed, hay absolute positioning thì hộp có thể bị chồng chéo lên nhau, các yếu tố xuất hiện sau trong đoạn code HTML sẽ được đặt lên trên các yếu tố xuất hiện trước nó. Nếu muốn kiểm soát phần tử nào được đặt trước thì sử dụng thuộc tính `z-index`, với giá trị là 1 con số và phần tử nào có số lớn hơn thì được đặt trước. Đôi khi thuộc tính `z-index` còn được gọi là `stacking context`.

#### FLOATING ELEMENTS:

**float**: Thuộc tính float cho phép đặt phần tử theo thông thường và về phía bên trái hoặc bên phải của phần tử chứa nó càng tốt. Bất cứ nội dung nào chứa trong phần tử chứa sẽ flow xung quanh phần tử được floated.

- Khi sử dụng thuộc tính float nên sử dụng thuộc tính width để xác định độ rộng để chỉ ra độ rộng mà phần tử sẽ float. Nếu không kết quả sẽ không phù hợp, box có thể mất đi toàn bộ chiều rộng của phần tử đang chứa.

#### USING FLOAT TO PLACE ELEMENTS SIDE-BY-SIDE: 

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

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task22_Book_HTML_and_CSS_design_and_build_websites/Chapter15_LAYOUT/image/10.png"/></p>

- Trong đó đoạn thứ tư lại không hiển thị về bên trái của trang mà lại nằm dưới đoạn thứ 3. Để giải quyết vấn đề này thì thiết lập chiều cao của đoạn văn trùng với độ dài cao nhất, nhưng nó không phù hợp lắm. Vậy cách phổ biến hơn hết là sử dụng thuộc tính `clear` để giải quyết vấn đề này.

#### CLEARING FLOATS:

**clear**: thuộc tính này xác định 2 bên của phần tử (left, right) nơi mà phần tử float không được phép float sang trái hay sang phải. Thuộc tính gồm có các giá trị sau:

- **left**: không được float về phía bên tay trái

- **right**: không được float về phía bên tay phải

- **both**: không được float về phía cả 2 bên

- **none**: có thể float được cả 2 bên

##### CREATING MULTI-COLUMN LAYOUTS WITH FLOATS:

- Nhiều trang web sử dụng nhiều cột trong thiết kế của họ, để làm được điều này cần phải sử dụng phần tử `<div>` đại diện cho mỗi cột, đây là 3 thuộc tính CSS được sử dụng đểv xác định vị trí cho các cột:

	+ **width**: thiết lập chiều rộng cho cột

	+ **float**: vị trí cho các cột nối tiếp sau đó

	+ **margin**: tạo khoản cách giữa các cột

#### SCREEN SIZES:

- Khách truy cập đến website của bạn sẽ sử dụng các thiết bị có kích thước màn hình khác nhau để hiển thị thông tin, vì vậy thiết kế phải phù hợp với 1 loạt màn hình có kích thước khác nhau.

- Khi thiết kế dành cho việc in ấn thì cần biết kích thước của giấy mà thiết kế của bạn sẽ được in trên đó. Kích thước màn hình người sử dụng ảnh hưởng lớn đến việc họ có thể mở cửa sổ trình duyệt và trang mà họ sẽ thấy.

#### SCREEN RESOLUTION (Độ phân giải màn hình):

- Độ phân giải đề cập đến số lượng các chấm trên màn hình hiển thị trên mỗi inch. Một số thiết bị có độ phân giải cao hơn máy tính để bàn và nhất là các hệ điều hành cho phép người sử dụng chỉnh độ phân giải trên màn hình của họ.

#### PAGE SIZES:

- Vì kích thước màn hình và độ phân giải khác nhau vì vậy các nhà thiết kế web thường tạo ra các trang có độ rộng là 960-1000 pixels (hầu hết người dùng có thể nhìn thấy thiết kế này trên màn hình của họ)

- Để người dùng có thể nhìn thấy toàn bộ nội dung trang mà không cần kéo trang xuống là 1 điều vô cùng khó. Các nhà thiết kế cho rằng người dùng có thể nhìn thấy 570-600 pixels trong 1 trang mà không cần kéo xuống, và cố gắng fit toàn bộ thông điệp chính vào khu vực này.

- Các khu vực trong trang mà người dùng không có chức năng cuộn lại được gọi là "above the fold". Nó được thừa nhận rằng nếu như người dùng quan tâm đến nội dung của trang, họ có thể cuộn xuống để xem nhiều thông tin hơn. Người dùng có khả năng đánh giá 1 trang, vậy nên điều này quan trọng là cung cấp cho khác truy cập thông tin cần thiết, khiến trang web này thật sự hữu ích đối với họ.

<a name="4"></a>
### Tài liệu tham khảo

> [1] Duckett, J. (2011). HTML and CSS: design and build websites. John Wiley & Sons. 

