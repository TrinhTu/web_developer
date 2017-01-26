## HTML & CSS

### FORMS

> Chương 7: FORMS
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 23/01/2017

## Mục lục:

[1. Cách thu thập thông tin từ khách truy cập](#1)

[2. Sự khác nhau của form control](#2)

[3. Điều khiển dạng HTML5](#3)

[Tài liệu tham khảo](#4)

***

Theo truyền thống, các thuật ngữ "hình thức" đã đề cập đến 1 tài liệu chứa khoảng trống để điền thông tin vào. Trình duyệt HTML lấy khái niệm của yếu tố khác cho phép thu thập thông tin từ người truy cập đến trang web của bạn. Trong chương này chúng ta sẽ tìm hiểu: 

- Cách tạo form trong website

- Sự khác nhau của các công cụ thu thập dữ liệu

- Form HTML5 mới

<a name="1"></a>
### 1. Cách thu thập thông tin từ khách truy cập:

#### Tại sao cần sử dụng Forms?

- Có lẽ chúng ta đã quen với các hộp tìm kiếm được đặt chính giữa trang chủ tìm kiếm của Google. Ngoài việc cho phép người dùng tìm kiếm thông tin thì bên cạnh đó form này còn cho phép người dùng thực hiện các tính năng trực tuyến khác. Khi đăng kí là thành viên trên website nào đó, khi mua sắm trực tuyến...

#### Form controls:

Một số loại form dùng để thu thập thông tin từ người truy cập đến trang web:

- **Adding Text**: 

	+ `Text input`: Được sử dụng cho 1 dòng của văn bản như địa chỉ mail, và tên

	+ `Password input`: Gồm 1 cái hộp chứa dòng văn bản và kí tự nhập vào sẽ được mã hóa.

	+ `Text area`(multi-line): Dùng chứa văn bản dài như tin nhắn hoặc bình luận.

- **Making Choices**: 

	+ `Radio button`: Sử dụng khi người sử dụng phải chọn 1 trong số các tùy chọn.

	+ `Checkboxes`: Khi người dùng chọn và bỏ chọn 1 hoặc lựa chọn nhiều hơn.

	+ `Drop-down boxes`: Khi người dùng phải chọn 1 trong số các lựa chọn từ danh sách.

- **Submitting Forms**:

	+ `Submit button`: dùng để gởi dữ liệu từ biểu mẫu của bạn đến 1 trang web khác.

	+ `Image buttons`: tương tự như submit button nhưng cho phép bạn sử dụng hình ảnh.

	+ `File upload`: Cho phép người dùng tải tập tin lên website.

#### Cách thức làm việc của biểu mẫu:

- Người dùng sẽ điền vào biểu mẫu và sau đó nhấn vào 1 cái hộp để tải thông tin lên server.

- Một biểu mẫu thì có nhiều hình thức điều khiển, mỗi cái thì thu thập thông tin khác nhau. Các máy chủ cần xác định được dữ liệu đầu vào tương ứng với các yếu tố  của biểu mẫu.

- Để phân biệt sự khác nhau của dữ liệu đầu vào thông tin sẽ được gởi từ trình duyệt đến máy chủ sử dụng các cặp tên/giá trị. 

#### Cấu trúc của Form:

- `<form>`: form control tồn tại bên trong phần tử `<form>~. Phần tử này đi kèm với thuộc tính hành động, thường sẽ có 1 phương thức hành động và  thuộc tính id.

	+ `action`: mọi phần tử `<form>` yêu cầu thuộc tính hành động, giá trị của nó là URL của trang trên máy chủ sẽ nhận thông tin trong biểu mẫu khi được tải lên.

	+ `method`: Biểu mẫu có thể được gởi bằng cách sử dụng 1 trong 2 phương thức sau: get hoặc post.

	+ Với phương thức `get` thì giá trị của biểu mẫu được thêm vào cuối của URL được chỉ định trong thuộc tính hành động. Phương thức `get` sử dụng tốt cho:

		+ Biểu mẫu ngắn (như hộp tìm kiếm)

		+ Chỉ có thể lấy dữ liệu từ máy chủ web

	+ Với phương thức `post` giá trị được gởi với tiêu đề HTTP. Như 1 phương thức quan trọng nên sử dụng phương thức `post` trong biểu mẫu trong trường hợp:

		+ Cho phép người sử dụng tải tập tin

		+ Sử dụng cho các biểu mẫu dài

		+ Chứa dữ liệu quan trọng (ví dụ như mật khẩu)

		+ Cho biết thông tin hoặc xóa thông tin từ cơ sở dữ liệu

	+ `id`: Giá trị của thuộc tính sử dụng để xác biểu mẫu rõ ràng từ các yếu tố khác trên trang, thường được sử dụng bởi các script chẳng hạn như kiểm tra xem có thu thập thông tin vào các trường đòi hỏi giá trị.

<a name="2"></a>
### 2. Sự khác nhau của form control:

#### Text Input:

- `<input>`: Yếu tố `<input>` sử dụng để tạo 1 số điểm khác biệt để kiểm soát biểu mẫu. Giá trị của các kiểu thuộc tính xác định kiểu đầu vào mà bạn sẽ tạo.


- `type="text"`: Khi khách truy cập nhập thông tin vào biểu mẫu, máy chủ cần kiểm soát từng từng phần dữ liệu đã nhập vào (Ví dụ: Khi đăng nhập vào biểu mẫu máy chủ cần biết những gì được nhập vào như tên người dùng, mật khẩu). Vì vậy mỗi biểu mẫu kiểm soát đòi hỏi phải có tên thuộc tính, giá trị của thuộc tính cho phép kiểm soát biểu mẫu và gởi cùng với các thông tin được nhập vào máy chủ.


- `maxlength`: Bạn có thể sử dụng thuộc tính chiều dài tối đa giới hạn số lượng người dùng truy cập vào trường văn bản. Giá trị của nó là số kí tự mà họ có thể nhập. Ví dụ nếu yêu cầu là **Năm** thì thuộc tính chiều dài tối đa của giá trị là `4`.

#### Password Input:

- `<input>`

	+ `type="password"`: Các loại thuộc tính có giá trị là mật khẩu tạo ra trong 1 hộp văn bản hoạt động như là văn bản 1 dòng, không cho phép thấy các dữ liệu bí mật như mật khẩu.

	+ `name`: Thuộc tính `name` dùng chỉ định tên của mật khẩu vào, gởi lên trình duyệt với mật khẩu người dùng nhập vào.

	+ `size, maxlength`: nó có thể mang các kích thước và thuộc tính `maxlength` như một dòng văn bản nhập vào.

- Mặc dù mật khẩu được ẩn trên màn hình, nó không có nghĩa là mật khẩu sẽ được gởi an toàn đến máy chủ, không nên sử dụng cho việc gởi dữ liệu quan trọng như số thẻ tín dụng.

- Để đảm bảo an toàn, máy chủ cần thiết lập giao tiếp với trình duyệt người sử dụng (SSL).

#### Text Area

- `<textarea>`: Yếu tố `<textarea>` sử dụng để tạo đầu vào văn bản có nhiều dòng, không giống như các yếu tố đầu vào khác, nó không phải là phần tử rỗng, nó gồm có thẻ mở và thẻ đóng.

- Nhiều đoạn văn viết giữa thẻ mở `<textarea>` và thẻ đóng `</textarea>` thì sẽ xuất hiện trong hộp khi tải trang.

- Nếu người sử dụng không xóa đoạn văn bản nằm giữa thẻ thì tin nhắn này sẽ được gởi lên máy chủ cùng với bất cứ điều gì khi người dùng đã gõ (1 số trang web sẽ sử dụng javascript để xóa thông tin này khi người dùng click vào vùng văn bản)

- Khi tạo biểu mẫu nên sử dụng CSS để kiểm soát chiều dài và chiều rộng của `<textarea>`. Tuy nhiên, nếu nhìn vào các mã cũ bạn có thể thấy các thuộc tính hàng và cột sử dụng phần tử này.

#### Radio Button: 

- `type="radio"`: nút radio cho phép người dùng lựa chọn 1 trong số các tùy chọn.

- `name`: thuộc tính `name` dùng để gởi lên máy chủ với giá trị mà người sử dụng lựa chọn. Khi câu hỏi yêu cầu người sử dụng lựa chọn câu trả lời trong biểu mẫu, giá trị của thuộc tính `name` tạo nút radio để trả lời câu hỏi đó.

- `value`: thuộc tính giá trị xác định giá trị gởi lên máy chủ cho các tùy chọn được chọn. Giá trị được chọn là khác nhau (để máy chủ biết lựa chọn mà người dùng đã chọn)

- `checked`: kiểm tra thuộc tính có thể được sử dụng để chỉ ra giá trị (nếu có) cần chọn khi tải trang. Giá trị của thuộc tính này cần kiểm tra, chỉ 1 nút radio trong nhóm nên sử dụng thuộc tính này.

#### Checkbox:

- `type="checkbox"`: Checkbox cho phép người sử dụng chọn 1 hay nhiều lựa chọn hơn để trả lời cho câu hỏi.

- `name`: Thuộc tính `name` gởi lên máy chủ với giá trị mà người dùng đã chọn. Khi câu hỏi cung cấp cho người sử dụng những lựa chọn trả lời biểu mẫu dưới dạng hộp kiểm tra, giá trị tên của thuộc tính nên tương tự với các nút trả lời câu khỏi đó.

- `value`: Thuộc tính giá trị xác định giá trị gởi đến máy chủ nếu checkbox được kiểm tra.

- `checked`: Thuộc tính checked chỉ ra hộp cần kiểm tra khi tải trang

#### Drop Down List Box

- `<select>`: Hộp danh sách đổ xuống cho phép người dùng chọn 1 trong các lựa chọn từ danh sách đổ xuống. Yếu tố `<select>` dùng để tạo hộp danh sách đổ xuống, bao gồm 2 hoặc nhiều lơn `<option>` phần tử.

- `name`: Thuộc tính name chỉ định tên kiểm soát biểu mẫu gởi lên máy chủ, với giá trị người dùng chọn.

- `option`: Phần tử `<option>` sử dụng xác định các tùy chọn mà người dùng có thể lựa chọn. Từ nằm giữa thẻ mở `<option>` và thẻ đóng `</option>` sẽ hiển thị cho người dùng trong hộp danh sách thả đổ xuống.

- `value`: Phần tử `<option>` sử dụng thuộc tính giá trị chỉ định giá trị gởi lên máy chủ với tên điều khiển nếu tùy chọn này được chọn.

- `selected`: Thuộc tính được chọn có thể được sử dụng để chỉ định các tùy chọn nên chọn khi tải trang. Giá trị của thuộc tính này nên được chọn. Nếu thuộc tính này không được sử dụng thì tùy chọn đầu tiên sẽ hiển thị khi tải trang. Nếu người sử dụng không chọn các tùy chọn thì mục đầu tiên sẽ được gởi đến máy chủ như là giá trị để kiểm soát. Chức năng của hộp danh sách đổ xuống giống như nút radio (trong đó có 1 tùy chọn có thể được chọn). Có 2 yếu tố quan trọng trong việc lựa chọn:

	+ Nếu người dùng cần xem tất cả các tùy chọn trong nháy mắt, thì radio button là thích hợp hơn.

	+ Nếu có 1 danh sách dài (như tên quốc gia), thì hộp danh sách đổ xuống làm việc tốt hơn.

#### Multiple Seclect Box:

- `size`: Có thể bật tùy chọn đổ xuống thành 1 hộp hiển thị nhiều tùy chọn hơn bằng cách thêm thuộc tính kích thước. Giá trị của nó nên là con số tùy chọn nếu muốn hiển thị cùng lúc

- `multiple`: Có thể cho phép người dùng chọn nhiều lựa chọn từ danh sách bằng cách thêm nhiều thuộc tính với giá trị của multiple. 

- Nó là ý tưởng tốt để nói với người dùng họ có thể chọn nhiều hơn 1 lựa chọn trong cùng 1 thời gian, nó cũng giúp chỉ định trên PC rằng nên nhấn phím điều khiển trong khi lựa chọn nhiều tùy chọn

#### File Input Box: 

Nếu muốn cho phép người dùng tải tập tin (hình ảnh, video, mp3 hoặc PDF) bạn cần sử dụng tập tin đầu vào của hộp.

- `type="file"`: đây là loại đầu vào tạo ra 1 cái hộp giống như văn bản vào tiếp đến là nút duyệt. Khi người dùng click vào nút duyệt thì cửa sổ mở lên cho phép chọn 1 file từ máy tính của họ và tải lên website. Khi cho phép người dùng tải file, thuộc tính phương thức trong phần tử `<form>` phải có giá trị là post (không nên gởi file sử dụng phương thức get HTTP). Khi người dùng click vào nút duyệt thì bày ra cửa sổ cho phép duyệt file muốn tải lên phù hợp, không thể kiểm soát sự xuất hiện của cửa sổ.

#### Submit Button:

- `type="submit"`: Submit button dùng để gởi biểu mẫu lên máy chủ.

- `name`: Có thể sử dụng thuộc tính name nhưng nó không cần thiết lắm

- `value`: Thuộc tính giá trị sử dụng kiểm soát sự xuất hiện của văn bản chính xác, nó rất cần thiết để xác định từ mà bạn muốn xuất hiện chính xác, theo mặc định thì giá trị của nút trên trình duyệt là "gởi và truy vấn", nó không phù hợp cho tất cả các loại biểu mẫu.

#### Image Button:

- `type="image"`: Nếu muốn thêm hình ảnh trong nút có thể sử dụng kiểu thuộc tính giá trị hình ảnh trong các giá trị: `src`, `width`, `height` và các thuộc tính alt.

#### Button & Hidden Controls:

- `<button>`: Phần tử `<button>` cho phép người dùng kiểm soát sự xuất hiện của các nút, và các phần tử bên trong nó. Tức là có thể phối hợp đoạn văn và hình ảnh nằm giữa thẻ mở `<button>` và thẻ đóng `</button>`.

- `type="hidden"`: Trong ví dụ cho thấy việc kiểm soát biểu mẫu nhưng không hiển thị lên trang. Nó cho phép tác giả của trang web thêm giá trị lên biểu mẫu mà người dùng không thể nhìn thấy được. Ví dụ: Tác giả sử dụng trường ẩn để xác định trang người sử dụng cản khi họ gởi biểu mẫu.

#### Labelling Form Controls:

- `<label>`: Phần tử `<label>` được sử dụng bằng 2 cách: 

	+ Hiển thị xung quanh các mô tả văn bản và đầu vào của biểu mẫu 

	+ Tách chúng với form control và sử dụng thuộc tính để chỉ ra form control như là 1 nhãn dán (tương tự như radio button)

- `for`: Giá trị của thuộc tính sao cho phù hợp với thuộc tính `id` trong form control chính là nhãn dán. Kĩ thuật này sử dụng `for` và thuộc tính `id` có thể sử dụng form control. Khi phần tử `<label>` sử dụng `checkbox` hoặc radio button thì người sử dụng có thể chọn form control hoặc nhãn dán. Việc mở rộng khu vực chọn làm cho các biểu mẫu dễ sử dụng hơn, vị trí của nhãn là rất quan trọng nếu người dùng không biết nơi để nhập thông tin hoặc điền thông tin gì thì việc sử dụng biểu mẫu sẽ trở nên khó khăn hơn.

- Sau đây là quy tắc chủ chốt về nơi tốt nhất để đặt nhãn dán:

	+ Ở trên hoặc bên trái:

		+ Nhập văn bản

		+ Khu vực văn bản

		+ Chọn khung

		+ Tải tập tin

	+ Ở bên phải:

		+ Kiểm tra hộp hộp cá nhân

		+ Nút radio cá nhân

#### Grouping Form Elements:

- `<fieldset>`: có thể tạo nhóm liên quan đến việc kiểm soát biểu mẫu trong phần tử `<fieldset>` nó rất hữu ích sử dụng trong thời gian dài. Hầu hết các trình duyệt sẽ hiển thị fieldset với 1 đường xung quanh cạnh để cho thấy rõ mối quan hệ, sự xuất hiện của đường đó có thể được điều chỉnh bằng cách sử dụng CSS.

- `<legend>`: Phần tử `<lengend>` có thể được sử dụng trực tiếp sau thẻ mở `<fieldset>` và nội dung của chú thích giúp chỉ định mục đích của nhóm hình thức điều khiển

<a name="3"></a>
### 3. Điều khiển dạng HTML5:

#### HTML5: Form Validation:

- Nếu như người sử dụng không điền đầy đủ thông tin thì sẽ nhận được 1 tin nhắn thông báo, hình thức này được gọi là hình thức xác nhận. Lúc trước hình thức xác nhận được thực hiện bằng Javascript nhưng đối với HTML5 thì giới thiệu xác nhận và công việc cho các trình duyệt. Hình thức xác nhận này đảm bảo cho người dùng đăng nhập thông tin trong biểu mẫu, các máy chủ có thể hiểu các biểu mẫu khi được tải lên. Việc xác nhận nội dung trước khi đưa lên máy chủ giúp:

	+ Giảm số lượng công việc mà máy chủ đã làm

	+ Cho phép người sử dụng thấy được vấn đề của các biểu mẫu sẽ nhanh hơn khi được xác nhận là thực hiện trên máy chủ.

#### HTML5: Date Input:

- `<input>`: nhiều biểu mẫu cần thông tin như: ngày, email, địa chỉ, URLs nó thường được sử dụng khi nhập dữ liệu vào. HTML5 cung cấp dạng biểu mẫu mới để xác nhận thông tin thu thập, còn đối với trình duyệt cũ sẽ không phân biệt được dữ liệu đầu vào và xem nó như 1 dòng văn bản bình thường.

- `type="date"`: nếu yêu cầu ngày từ khách truy cập thì sử dụng phần tử`<input>` và cung cấp loại giá trị thuộc tính là ngày. Điều này tạo dữ nhập ngày nhập vào trong trình duyệt mới hỗ trợ HTML5.

#### HTML5: Email & URL Input:

- `<input>`: HTML5 cũng đã cung cấp đầu vào cho khách truy cập nhập địa chỉ email và URL/ Trình duyệt không hỗ trợ các loại đầu vào sẽ điều chỉnh như 1 hộp văn bản.

- `type="email"`: nếu muốn biết được email của người dùng có thể sử dụng email đầu vào, trình duyệt hỗ trợ HTML5 xác nhận kiểm tra thông tin người dùng đã cung cấp thông qua địa chỉ email. 

- `type="url"`: tương tự như email, nhưng kiểm tra xác nhận lại thông tin thông qua URLs.

#### HTML5: Search Input:

Nếu muốn tạo 1 dòng văn bản tìm kiếm, HTML5 cung cấp các kiểu đầu vào đặc biệt. 

- `type="search"`:  để tạo hộp tìm kiếm HTML5 nên có 1 thuộc tính giá trị tìm kiếm. trình duyệt cũ sẽ xử lí nó 1 cách dễ dàng. Các trình duyệt gần đây thêm 1 số tính năng cải thiện để dễ sử dụng

- `placeholder`: Trên bất kì đầu vào văn bản nào cũng sử dụng thuộc tính giữ chỗ giá trị tức là văn bản sẽ hiển thị trong hộp văn bản tới khi người dùng click chuột vào, đối với trình duyệt cũ sẽ bỏ ra thuộc tính này.

### Tóm lại:

- Bất cứ khi nào muốn thu thập thông tin từ khách truy cập cần sử dụng biểu mẫu với phần tử `<form>` bên trong.

- Thông tin trong biểu mẫu được gởi trong cặp tên và giá trị.

- Mỗi kiểm soát biểu mẫu đều có tên, các văn bản hoặc giá trị tùy chọn đều được gởi đến máy chủ.

- HTML5 cung cấp các yếu tố biểu mẫu mới dễ dàng sử dụng hơn cho khách truy cập.

<a name="4"></a>
### Tài liệu tham khảo

<<<<<<< HEAD
> [1] Duckett, J. (2011). HTML and CSS: design and build websites. John Wiley & Sons. 


=======
> [1] Duckett, J. (2011). HTML and CSS: design and build websites. John Wiley & Sons.
>>>>>>> c6de2caf91b78de0992dc510814a2c65dd322b2d
