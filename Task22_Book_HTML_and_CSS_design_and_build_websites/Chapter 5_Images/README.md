## HTML & CSS

### Images

> Chương 5: Images
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 20/01/2017

## Mục lục:

[1. How to add images to pages](#1)

[2. Choosing the right format](#2)

[3. Optimizing images for the web](#3)

[Tài liệu tham khảo](#4)

***

<a name="1"></a>
### 1. Cách thêm hình ảnh vào trang web:

Có 1 số điều cần lưu ý khi chuẩn bị thêm ảnh vào website của bạn, nó sẽ giúp cho trang web trong hấp dẫn và chuyên nghiệp hơn:

- Bao gồm 1 hình ảnh trong trang web sử dụng HTML

- Định dạng hình ảnh để sử dụng

- Hiển thị hình ảnh theo đúng kích thước

- Tối ưu hóa hình ảnh trên trang web để các trang tải nhanh hơn

#### Chọn hình ảnh cho website (Choosing Images For Your Site):

Hình ảnh có vai trò rất quan trọng trong trang web, bởi thông qua hình ảnh có thể nói lên nhiều điều, tạo sự khác biệt cho trang web của bạn.

- Hình ảnh được sử dụng để làm cho trang Web trở nên sinh động hơn, có những hình ảnh muốn sử dụng cần phải trả tiền, và không nên tự tiện lấy hình ảnh có bản quyền từ 1 trang wev khác.

- Hình ảnh cần liên quan với nội dung, mang ý nghĩa truyền đạt thông tin, phù hợp với tông màu sử dụng.

#### Lưu trữ hình ảnh của bạn trong website (Storing Images On Your Site): 

- Nếu như bắt đàu xây dựng 1 trang web, nên thực hành tạo ra 1 thư mục chứa tất cả hình ảnh sử dụng cho trang web.

- Trong 1 trang web lớn bạn có thể thêm các thư mục con chứa thư mục hình ảnh.

#### Thêm hình ảnh (Adding Images):

- Để thêm hình ảnh vào trang web cần sử dụng yếu tố `<img>`. Thẻ này không có thẻ đóng. Nó gồm có 2 giá trị:

	+ `<src>`: dùng để thông báo cho trình duyệt nơi để thư mục hình ảnh. Nó thường là URL trỏ đến hình ảnh trên trang web của bạn.

	+ `alt`: Cung cấp 1 văn bản mô tả hình ảnh, nhưng không hiển thị nó.

	+ `title`: Cũng có thể sử dụng thuộc tính title trong thẻ `<img>` cung cấp thêm thông tin về hình ảnh. Hầu hết trình duyệt sẽ hiển thị nội dung của thuộc tính này khi người dùng rê chuột vào hình ảnh.

	+ Văn bản sử dụng thuộc tính alt thường được gọi là alt văn bản, nó sẽ mô tả chính xác nội dung hình ảnh. 

```javascript
<img src="http://image.com" alt="picture of me" title="the picture can not be displayed" />
```

### Chọn đúng định dạng cho hình ảnh (Choosing The Right Format)

#### Chiều dài và chiều rộng hình ảnh (Height & Width Of Images):

Yếu tố `<img>` thường đi kèm với 2 thuộc tính kích thước:

- `height`: thiết lập chiều dài của ảnh với đơn vị là pixels (px).

- `width`: Thiết lập chiều rộng của ảnh với đơn vị là px. Hình ảnh thường tốn nhiều thời gian để tải hơn so với mã HTML. Vậy nên cần xác định kích thước của hình ảnh để trình duyệt có thể làm việc 1 cách dễ dàng hơn.

- Kích thước của hình ảnh khuyến khích sử dụng CSS hơn là HTML.

#### Nơi để hình ảnh trong đoạn mã (Where To Place Images In Your Code):

- Nơi để hình ảnh trong đoạn mã có ảnh hưởng đến cách hiển thị. Trình duyệt cho thấy các phần tử HTML hiển thị theo 1 trong 2 cách:

	+ Hiển thị trên 1 dòng mới

	+ Hiển thị chung dòng với văn bản, không tạo dòng mới

#### Sắp xếp hình ảnh theo chiều ngang (Old Code: Aligning Images Horizontally):

- `align`: Thuộc tính căn chỉnh thường sử dụng để chỉ ra cách hiển thị các bộ phận khác của 1 trang xung quanh hình ảnh.

	+ `left`: Căn chỉnh hình ảnh về phía bên trái cho phép đoạn văn hiển thị về phía tay phải..


	+ `right`: Căn chỉnh hình ảnh về phía bên phải cho phép đoạn văn hiển thị về phía tay trái.

#### Sắp xếp hình ảnh theo chiều dọc (Old COde: Aligning Image Vertically)

- Có 3 giá trị dùng để điều chỉnh hình ảnh sắp xếp theo chiều dọc với các văn bản bao quanh nó.

	+ `top`: Điều chỉnh dòng đầu tiên của văn bản ở phía trên của hình ảnh.

	+ `middle`: Điều chỉnh dòng đầu của văn bản ở chính giữa hình ảnh.

	+ `bottom`: Điều chỉnh dòng đầu của văn bản hiển thị bên dưới hình ảnh.

[1]

- Ở ví dụ trên giá trị của dòng đầu của văn bản hiển thị gần đỉnh phía trên của hình ảnh và dòng tiếp theo thì xuất hiện phía dưới hình ảnh.

[2]

- Ở ví dụ trên giá trị của dòng đầu của văn bản hiển thị ở gần giữa hình ảnh theo chiều dọc và dòng tiếp theo thì xuất hiện phía dưới hình ảnh.

[3]

- Ở ví dụ trên giá trị của dòng đầu tiên của văn bản hiển thị ở gần phía dưới của hình ảnh và dòng tiếp theo của văn bản thì hiển thị phía dưới của hình ảnh.

<a name="3"></a>

### Tối ưu hóa hình ảnh cho website (Optimizing images for the web):

#### Ba quy tắc để tạo hình ảnh (Three Rules For Creating Images)

Ba quy tắc cần lưu ý khi thêm hình ảnh khi thêm hình ảnh cho Website theo nguyên tắc dưới đây. 

- **Lưu hình ảnh đúng định dạng**: Website chính sử dụng hình ảnh có định dạng là `jpeg`, `gif`, `png`. Nếu chọn định dạng hình ảnh sai thì hình ảnh đó sẽ không thể hiển  thị, và website tải chậm.

- **Lưu hình ảnh theo đúng kích thước**: Nên lưu hình ảnh theo đúng kích thước chiều dài và chiều rộng nó sẽ hiển thị tốt hơn trên trình duyệt. Nếu hình ảnh nhỏ hơn chiều dài hoặc chiều rộng được chỉ định thì hình ảnh có thể bị bóp méo và kéo dài. Còn nếu hình ảnh lớn hơn chiều dài và chiều rộng đã chỉ định thì sẽ mất nhiều thời gian để hiển thị lên trang.

- **Sử dụng đúng độ phân giải**: Hầu hết các màn hình máy tính chỉ hiển thị trang web ở 72px trên mỗi ich

#### Công cụ điều chỉnh và lưu hình ảnh (Tools To Edit & Save Images):

Có 1 số công cụ có thể sử dụng để chỉnh sửa và lưu hình ảnh để đảm bảo hình ảnh hiển thị đúng size, định dạng và độ phân giải.

- Công cụ phổ biến nhất là Adobe Photoshop, trong thực tế các nhà thiết kế web thường sử dụng phần mềm này để thiết kế toàn bộ trang web. Ngoài ra còn có các phần mềm khác như là: Adobe Fireworks, Pixelmator, PaintShop Pro, Paint.net... Các công cụ trực tiếp như là: `www.photoshop.com`, `www.pixlr.com`...

- Hình ảnh định dạng `JPEG`: Bất cứ khi nào bạn có nhiều màu sắc khác nhau trong 1 bức ảnh nên sử dụng JPEG.

- Hình ảnh định dạng `GIF`: Sử dụng định dạng `GIF` hoặc `PNG` khi lưu hình ảnh với vài màu sắc hoặc khu vực có cùng màu sắc lớn.

- Khi 1 hình ảnh trong khu vực được điền với chính xác 1 màu sắc thì nó được gọi là flat màu. Trong logo, hình ảnh minh họa, sơ đồ thường sử dụng flat màu. 

#### Kích thước hình ảnh (Image Dimensions):

- Đối với hình ảnh sử dụng trên website nên lưu lại với chiều dài và chiều rộng mong muốn hiển thị trên website.

Ví dụ nếu thiết kế 1 trang bao gồm hình ảnh dài 150px và rộng 300px thì hình ảnh bạn nên sử dụng là 300x150 px. Bạn cần sử dụng công cụ để chỉnh sửa lại hình ảnh.

#### Cẳt hình ảnh (Cropping Images):

Khi cắt hình ảnh quan trọng là không được đánh mất giá trị thông tin. Tốt nhất là nên để đúng hình dạng của nó.

#### Độ phân giải hình ảnh (Image Resolution):

- Hình ảnh được tạo cho trang web nên lưu lại với độ phân giải là 72 ppi. Độ phân giải cao hơn kích thước của hình ảnh và lớn hơn kích thước của tệp.

- JPGs, GIFs và PNGs thuộc về loại định dạng hình ảnh dưới dạng bitmap. Chúng được tạo thành từ nhiều ô vuông nhỏ. Độ phân giải của hình ảnh là số ô vuông phù hợp trong 1 khu vực hình vuông

- Hình ảnh xuất hiện trên máy tính được tạo thành từ các hình vuông nhỏ gọi là điểm ảnh. Một bộ phận nhỏ của hình ảnh đã được phóng to để hiển thị sao cho tạo thành từ các các điểm ảnh


#### Vector hình ảnh (Vector Images):

- Vector hình ảnh thì khác với bitmap và là độ phân giải độc lập. Vector hình ảnh được tạo ra trong các chương trình như Adobe Illustrator.

- Khi hình ảnh là một nét vẻ (như biểu tượng, hình minh họa hoặc biểu đồ), nhà thiết kế thường tạo ra nó trong định dạng vector. Định dạng của vector hình ảnh thì khác với hình ảnh bitmap.

- Vetor hình ảnh được tạo ra bởi các điểm trên giao diện và vẽ các đường giữa những điểm. Sau đó 1 màu sắc có thể thêm vào "fill in" trong dòng đã được tạo ra.

- Ưu điểm của việc tạo ra dòng vẽ ở định dạng vector là có thể tăng kích thước của hình ảnh mà không ảnh hưởng đến chất lượng của nó.

- Phương pháp sử dụng vector hình ảnh để hiển thị trên các trang web liên quan đến việc tiết kiệm phiên bản bitmap của bản gốc hình ảnh vector và sử dụng nó.

#### Ảnh động (Animated GIFS):

- Ảnh động GIFs hiển thị 1 số khung của hình ảnh trong trình tự do đó có thể được sử dụng để tạo ra ảnh động đơn giản.

- Một số ứng dụng chỉnh sửa hình ảnh như Adobe Photoshop cho phép tạo ra ảnh động.  

#### Ví dụ (Examining Images On The Web):

- Nếu đang truy cập 1 trang web có thể kiểm tra kích thước của hình ảnh trước khi tạo ra cái mới để thay thế nó. Có thể được tạo ra bằng cách kích chuột phải vào hình ảnh và chọn 

#### Hình và chú thích hình (HTML5: Figure And Figure Caption):

- `<figure>`: Hình ảnh thường đi với chú thích. HTML5 đã giới thiệu thêm 1 thuộc tính mới `<figure>` để chứa hình ảnh và chú thích. Có thể có nhiều hơn hình ảnh bên trong `<figure>` sao cho chúng có cùng chú thích.

- `<figcaption>`: Cho phép tác giả thêm chú thích cho hình ảnh. Trước khi có yếu tố này thì không có cách nào để kết hợp thẻ `<img>` với chú thích của nó. Với các trình duyệt cũ không hỗ trợ HTML5 thì bỏ qua các yếu tố đó và hiển thị nội dung của chúng.

### Tóm lại: 

- Yếu tố `img` sử dụng để thêm hình ảnh vào trang web

- Phải luôn xác định thuộc tính `src` của hình ảnh và `alt` mô tả nội dung hình ảnh

- Nên lưu hình ảnh với kích thước sao cho phù hợp, và sử dụng định dạng thích hợp.

- Hình ảnh sẽ hiển thị tốt nhất với `JPEGs`, hoặc logo sử dụng màu flat được lưu tốt hơn với GIFs.

<a name="4"></a>
### Tài liệu tham khảo

> [1] Duckett, J. (2011). HTML and CSS: design and build websites. John Wiley & Sons.

