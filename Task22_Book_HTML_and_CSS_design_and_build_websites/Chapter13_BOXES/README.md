## HTML & CSS

### BOXES

> Chương 13: BOXES
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 11/02/2017

## Mục lục:

[1. Điều chỉnh kích thước của hộp](#1)

[2. Mô hình Box model cho đường viền, margin và padding](#2)

[3. Hiển thị và ẩn hộp](#3)

[4. Tài liệu tham khảo](#4)

***

<a name="1"></a>
### 1. Điều chỉnh kích thước của hộp

#### BOX DIMENSIONS (kích thước của hộp):

**width, height**

- Mặc định thì kích thước của hộp chỉ đủ chứa nội dung bên trong, ta có thể thiết lập kích thước cho hộp bằng cách sử dụng thuộc tính chiều dài và chiều rộng. Cách phổ biến để xác định kích thước cho hộp là sử dụng pixels, phần trăm.

-  Khi sử dụng tỉ lệ phần trăm kích thước của hộp là tỉ lệ phần trăm của hộp chứa nó. Khi sử dụng `ems` kích thước của hộp dựa trên kích thước của văn bản trong nó. Gần đây thì các nhà thiết kế sử dụng tỉ lệ phần trăm và ems nhiều hơn để đo lường chính xác khi tạo và thiết kế các linh hoạt các thiết bị có kích thước màn hình khác nhau

#### LIMITING WIDTH (giới hạn chiều rộng):

**min-width, max-width**

- 1 vài trang được thiết kế theo kiểu dãn ra và co lại để fit cho vừa kích thước với màn hình người sử dụng. Trong khi thiết kế, thuộc tính min-width xác định kích thước nhỏ nhất của hộp có thể hiển thị khi cửa sổ trình duyệt thu nhỏ lại và thuộc tính max-width xác định kích thước chiều rộng tối đa mà hộp có thể dãn ra khi cửa sổ trình duyệt phóng to ra.

- Đây là các tính chất rất hữu ích để chắc rằng nội dung của trang sẽ hiển thị dễ đọc (đặc biệt đối với màn hình các thiết bị cầm tay nhỏ hơn). Ví dụ có thể sử dụng thuộc tính max-width để đảm bảo rằng các dòng trong văn bản không hiển thị quá rộng trong cửa sổ trình duyệt lớn và thuộc tính min-width củng đảm bảo rằng các dòng trong văn bản không hiển thị quá chen chúc khi thu nhỏ cửa sổ trình duyệt lại.

#### LIMITING HEIGHT (giới hạn chiều cao):

**min-height, max-height**

- Trong cùng 1 phương pháp có thể vừa giới hạn chiều rộng và vừa giới hạn chiều cao, để đạt được điều này cần sử dụng thuộc tính min-height và max-height. Nếu như 1 cái hộp không đủ lớn để chứa toàn bộ nội dung thì nội dung sẽ bị tràn ra bên ngoài và trông rất hỗn độn, để giải quyết vấn đề này có thể sử dụng thuộc tính overflow.

#### OVERFLOWING CONTENT (tràn nội dung):

**overflow**: thuộc tính này thông báo cho trình duyệt biết phải xử lí như thế nào khi nội dung chứa bên trong hộp lớn hơn so với hộp, gồm 1 trong 2 giá trị:

- **hidden**: ẩn bất kì nội dung bổ sung nào mà không fit chúng vừa hộp

- **scroll**: thêm thanh cuộn vào trong hộp để người sử dụng có thể di chuyển để xem các nội dung còn thiếu. 

Thuộc tính overflow rất tiện dụng bởi vì 1 vài trình duyệt cho phép người dùng điều chỉnh kích thước của văn bản để xuất hiện rộng ra hay thu nhỏ lại theo ý muốn. Nếu các văn bản được thiết lập quá lớn thì sẽ khó đọc, ẩn nội dung bị tràn ra trong hộp sẽ giúp ngăn chặn việc chồng chéo nội dung trên trang.

<a name="2"></a>
### 2. Mô hình Box model cho đường viền, margin và padding:
#### BORDER, MARGIN & PADDING

Mỗi hộp có sẵn 3 thuộc tính có thể được điều chỉnh để kiểm soát sự xuất hiện. 

1. **Border**: Mỗi hộp điều có 1 đường viền giúp ngăn cách các cạnh của hộp với các nội dung khác

2. **Margin**: Margins được đặt trong các cạnh của hộp, có thể thiết lập chiều rộng của margin để tạo 1 khoảng trống giữa đương viền của 2 hộp kề nhau

3. **Padding**: padding là khoảng cách giữa đường viền của hộp và bất kì nội dung nào được chứa bên trong hộp, thêm padding giúp trong nội dung trở nên dễ đọc hơn.

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task22_Book_HTML_and_CSS_design_and_build_websites/Chapter13_BOXES/1.png"/></p>

#### WHILE SPACE & VERTICAL MARGIN:

Thuộc tính padding và margin rất hữu ích trong việc thêm khoảng cách giữa các mục trong 1 trang này:

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task22_Book_HTML_and_CSS_design_and_build_websites/Chapter13_BOXES/2.png"/></p>

Nếu như bottom margin của hộp bất kì trùng với top margin của hộp khác thì trình duyệt sẽ không hiển thị cả 2 giá trị, 2 margin có kích thước giống nhau thì nó chỉ hiển thị 1.

#### BORDER WIDTH: 

**border-width**

- Thuộc tính border-width được sử dụng để điều chỉnh chiều rộng của hộp giá trị của thuộc tính có thể được cho bởi pixel hoặc sử dụng các giá trị sau: thin, medium, thick. Ta sẽ không thấy sử dụng tỉ lệ phần trăm đối với thuộc tính này. Có thể kiểm soát riêng đường viền cá nhân bằng việc sử dụng 4 thuộc tính riêng biệt:

	+ border-top-width

	+ border-right-width

	+ border-bottom-width

	+ border-left-width

Ngoài ra cũng có thể chỉ định độ rộng khác nhau cho 4 cạnh đường viền trong 1 thuộc tính như sau: `border-width: 2px 1px 1px 2px;` giá trị xuất hiện lần lượt là: top, right, bottom, left.

#### BORDER STYLE

**border-style**: có thể kiểm soát phong cách của đường viền bằng việc sử dụng border-style. Thuộc tính bao gồm các giá trị:

- **solid**: 1 dòng đơn

- **dotted**: gồm 1 loạt các dấu chấm đơn 

- **dashed**: 1 loạt các đoạn thẳng ngắn

- **double**: có 2 dòng đơn

- **hidden/none**: không hiển thị đường viền xung quanh

Bên cạnh đó có thể thay đổi phong cách riêng của từng đường viền sử dụng:

	+ border-top-style

	+ border-left-style

	+ border-right-style

	+ border-bottom-style

#### BORDER COLOR: 

**border-color**: có thể xác định màu cho đường viền sử dụng giá trị RGB và mã code hoặc tên màu CSS. Ngoài ra cá nhân còn có thể kiểm soát màu sắc trên các đường viền trong hộp bằng cách sử dụng: 

	+ border-top-color

	+ border-right-color

	+ border-bottom-color

	+ border-left-color

Cũng có thể sử dụng kí hiệu ngắn gọn kiểm soát màu của 4 đường viền trong 1 thuộc tính: `border-color: darkcyan deeppink darkcyan deeppink;`

#### SHORTHAND 

**border**

Thuộc tính border cho phép xác định chiều rộng, phong cách và màu sắc của đường viền chỉ trong 1 thuộc tính (các giá trị phải đươc sắp xếp theo thứ tự cụ thể)

```
p {
width: 250px;
border: 3px dotted #0088dd;}
```

#### PADDING 

**padding**

- Thuộc tính padding cho phép chỉ định không gian xuất hiện giữa nội dung của phần tử và đường viền. Giá trị của thuộc tính thường được xác định theo pixels (mặc dù nó vẫn có thể sử dụng tỉ lệ phần trăm hoặc ems). Nếu xác định chiều rộng cho hộp thì padding được thêm vào chiều rộng của hộp.

- Ngoài ra cũng có thể xác định các giá trị khác nhau cho mỗi cạnh trong hộp:

	+ padding-top

	+ padding-right

	+ padding-bottom

	+ padding-left

Hoặc sử dụng các ghi tắt ngắn gọn hơn: `padding: 10px 5px 3px 1px;`. Giá trị của thuộc tính padding không áp dụng cho các phần tử con giống như giá trị màu trong thuộc tính font-family vậy nên cần phải xác định padding cho từng yếu tố cần sử dụng nó.

#### MARGIN 

**margin**

- Thuộc tính margin kiểm soát khoảng cách trong hộp, giá trị của nó thường là pixels mặc dù cũng có thể sử dụng tỉ lệ phần trăm hoặc ems. Xác định giá trị cho mỗi cạnh trong hộp bằng cách sử dụng:

	+ margin-top

	+ margin-right

	+ margin-bottom

	+ margin-left

Bên cạnh đó còn có thể sử dụng cách viết ngắn gọn bao gồm tất cả các giá trị: top, right, bottom, left: `margin: 1px 2px 3px 4px;`, Hoặc thiết lập giá trị cho left right là 10px, top bottom là 20px thì viết như sau: `margin: 10px 20px;`. Cách viết này cũng áp dụng tương tự cho padding. Giá trị của margin cũng không áp dụng cho các phần tử con, vậy nên cần xác đinh margin cho các phần tử cần sử dụng nó.

<a name="3"></a>
### 3. Hiển thị và ẩn hộp:

#### CENTERING CONTENT:

- Khi muốn hộp được hiển thị giữa trang cần thiết lập left-margin và right-margin tự động, bên cạnh đó cần thiết lập thêm chiều rộng cho hộp nếu không nó sẽ chiếm hết chiều rộng của trang. Một khi đã thiết lập chiều rộng cho hộp, thiết lập margin left right thì tự động trình duyệt sẽ cân bằng khoảng cách mỗi bên của hộp, đặt hộp chính giữa trang. Để thuận tiện cho các trình duyệt làm việc, các phần tử này bên trong hộp có 1 thuộc tính là text-align với giá trị của nó được thiết lập dùng để căn giữa.

- Thuộc tính text-align cho phép thừa hưởng bởi các phần tử con vậy nên cần xác định thuộc tính text-align trên hộp trung tâm nếu không muốn các văn bản bên trong đó cũng được đặt trung tâm.

#### CHANGE INLINE/BLOCK: 

**display**: display là thuộc tính cho phép chuyển từ phần tử inline thành block hoặc ngược lại hay được sử dụng để ẩn phần tử trên trang. Giá trị của thuộc tính bao gồm:

- **inline**: 1phần tử block-level hoạt động như 1 phần tử inline

- **block**: 1 phần tử inline hoạt động như 1 phần tử block-level

- **inline-block**: 1 phần tử block-level hoạt động như phần tử inline trong khi vẫn giữ lại tính năng của phần tử block-level

- **none**: ẩn các phần tử trong trang, tức là phần tử đó vẫn tồn tại mặc dù nó không xuất hiện trên trang (người dùng sẽ thấy nội dung trong hộp nếu xem source). Nếu sử dụng thuộc tính này điều quan trọng là hộp inline không cung cấp tạo ra phần tử block-level.

#### HIDING BOXES:

**visibility**: thuộc tính này cho phép ẩn hộp nhưng sẽ để lại 1 khoảng trống tại nơi phần tử bị ẩn. Thuộc tính có 2 giá trị:

- **hidden**: ẩn phần tử

- **visible**: Hiển thị phần tử. Khi khả năng nhìn thấy của phần tử được thiết lập để ẩn phần tử đi thì 1 khoảng trống sẽ xuất hiện tại vị trí của nó. Nếu không muốn xuất hiện khoảng trống đó có thể sử dụng thuộc tính display với giá trị là none.

> Không bất cứ ai có thể nhìn thấy nội dung của phần tử được thiết lập để ẩn đi bằng cách xem source.

#### CSS3: BORDER IMAGES:

**border-image**

- Đây là thuộc tính áp dụng cho hình ảnh khi tạo thành viền của hộp. Thuộc tính này yêu cầu 3 thông tin:

1. URL của hình ảnh

2. Nơi cắt hình ảnh

3. Những điều cần làm với những cạnh thẳng, các giá trị có thể là:

	+ `stretch`: căng hình ảnh

	+ `repeat`: lặp lại hình ảnh

	+ `round`: tương tự như repeat nhưng sẽ không fit chính xác tỉ lệ hình ảnh. 

Hộp phải có độ rộng của đường viền cho hình ảnh để hiển thị

#### CSS3: BOX SHADOWS:

**box-shadow**: đây là thuộc tính cho phép tạo bóng đổ xung quanh hộp, nó làm việc như thuộc tính text-shadow, sử dụng ít nhât 1 trong 2 giá trị và 1 màu sắc.

- **horizontal offset**: giá trị âm là bóng sẽ đổ về bên trái hộp

- **vertical offset**: giá trị âm là bóng sẽ đổ về phía trên cùng của hộp

- **blur distance*: nếu bỏ qua thì bóng sẽ là 1 khối thẳng như đường viền.

- **spread of shadow**: sẽ làm cho bóng mở rộng ra theo tất cả các hướng, và giá trị âm sẽ làm cho nó co lại. Các từ khóa inset có thể được sử dụng phía trước của thuộc tính này tạo thành inner-shadow

#### CSS3: ROUNDED CORNERS: 

**border-radius**

- CSS3 giới thiệu thuộc tính border-radius để bo góc tròn xung quanh hộp, giá trị xác định kích thước của radius là pixels. 

- Các thuộc tính `-moz-border-radius` và `webkit-border-radius` không được xác định trong CSS, tuy nhiên có thể sử dụng các phiên bản của Chrome, Firefox và Safari để hỗ trợ cho kiểu này.

- Có thể xác định giá trị riêng sử dụng cho mỗi góc trong hộp:

	+ border-top-right-radius

	+ border-bottom-right-radius

	+ border-bottom-left-radius

	+ border-top-left-radius

Ngoài ra còn sử dụng cách viết ngắn gọn cho 4 thuộc tính theo thứ tự: top, right, bottom, left: `border-radius: 5px, 10px, 5px, 10px;`

#### CSS3: ELLIPTICAL SHAPES (hình elip)

**border-radius**

- Để tạo ra 1 hình dạng phức tạp hơn có thể xác đinh các khoảng cách khác nhau cho chiều ngang và chiều dọc của góc hình tròn. Ví dụ tạo ra góc bo với chiều rộng lớn hơn chiều cao:

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task22_Book_HTML_and_CSS_design_and_build_websites/Chapter13_BOXES/3.png"/></p>

- Khi mục tiêu là thay đổi 1 góc thì nên sử dụng thuộc tính riêng: `border-top-left-radius: 80px 50px;`. Cũng có thể viết ngắn gọn cho tất cả 4 góc chỉ trong 1 câu lệnh, đầu tiên là xác định 4 giá trị ngang sau đó là 4 giá trị dọc. Có thể tạo ra 1 vòng tròn bằng cách lấy hộp hình vuông tạo border-radius trùng với chiều cao của hình vuông.

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task22_Book_HTML_and_CSS_design_and_build_websites/Chapter13_BOXES/4.png"/></p>

<a name="4"></a>
### Tài liệu tham khảo

> [1] Duckett, J. (2011). HTML and CSS: design and build websites. John Wiley & Sons. 

