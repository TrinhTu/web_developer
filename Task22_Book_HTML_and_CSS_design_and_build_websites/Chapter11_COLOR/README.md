## HTML & CSS

### COLOR

> Chương 11: COLOR
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 08/02/2017

## Mục lục:

[1. FOREGROUND COLOR & BACKGROUND COLOR](#1)

[2. Độ tương phản và độ mờ](#2)

[3. CSS3 color](#3)

[Tài liệu tham khảo](#4)

***

<a name="1"></a>
### 1. FOREGROUND COLOR & BACKGROUND COLOR:

#### FOREGROUND COLOR (Màu nền):

- **color**: Thuộc tính màu sắc cho phép bạn xác định màu sắc cho văn bản nằm bên trong thẻ. Có thể chỉ định bất kì màu trong CSS bằng 1 trong 3 cách sau:

	+ **RGB values**: những màu sắc rõ ràng trong quy định bao nhiêu màu đỏ, xanh lá cây, xanh da trời được sử dụng để thể hiện nó. Ví dụ: rgb(100,100,90)

	+ **Hex codes**: đây là mã gồm 6 chữ số đại diện cho số lượng màu đỏ, xanh lá cây, xanh da trời trong 1 màu sắc bởi kí hiệu #. Ví dụ: #ee3e80

	+ **Color names**: Có 147 tên màu được được xác định và công nhận bởi trình duyệt. Ví dụ: Dark Cyan

#### BACKGROUND COLOR:

**background-color**

- CSS đối với mỗi phần tử HTML như là xuất hiện trong 1 hộp và thuộc tính background-color thiết lập màu nền cho hộp đó.

- Có thể lựa chọn màu nền bằng 1 trong 3 cách, có thể chỉ định foreground color: giá trị RGB, mã hex và tên màu

- Nếu không xác định màu nền thì màu nền sẽ trong suốt, theo mặc định hầu hết các cửa sổ trình duyệt có màu nền là màu trắng, nhưng người sử dụng có thể thiết lập lại màu nền cho cửa sổ của họ, vì vậy nếu không muốn màu nền là màu trắng thì cần thêm thuộc tính background-color trong thẻ `<body>`

#### UNDERSTANDING COLOR: 

Mỗi màu sắc trên màn hình máy tính được tạo ra bằng cách trộn một lượng màu đỏ, xanh lá cây và xanh nước biển. Để tìm được màu bạn muốn có thể sử dụng bảng chọn màu.

- Màn hình máy tính được tạo thành từ hàng ngàn ô vuông nhỏ gọi là điểm ảnh (nếu nhìn kĩ thì có thể thấy nó). Khi màn hình không bật nó là màu đen vì không phát ra ánh sáng nào. Khi nó mở mỗi điểm ảnh có màu sắc khác nhau tạo thành 1 bức ảnh.

- Màu sắc của mỗi điểm ảnh trên màn hình được thể hiện trong các quy định kết hợp màu đỏ, xanh lá cây, xanh nước biển tương tự như trên màn hình ti vi. Công cụ chọn màu có sẵn trong các trình sửa ảnh Photoshop và GIMP. CÓ thể nhìn thấy giá trị RGB quy định bên cạnh các nut radio gọi là R,G,B. Công cụ chọn màu sắc tại: colorschemedesigner.com

<a name="2"></a>
### 2. Độ tương phản và độ mờ:

#### CONTRAST (tương phản):

- Khi chọn foreground và background điều quan trọng là đảm bảo độ tương phản cho văn bản dễ đọc.

	+ Văn bản khó đọc khi độ tương phản giữa background và foreground thấp. Sự thiếu độ tương phản là vấn đề đặc biệt đối với người khiếm thị mà mù màu, bên cạnh đó còn ảnh hưởng đến màn hình độ phân giải kém và ánh sáng mặt trời chiếu trực tiếp lên thiết bị họ sử dụng.

	+ Văn bản dễ đọc khi có sự tương phản cao giữa foreground và background color. Khi người đọc đọc quá nhiều trang trên trang web của bạn sự tương phản làm cho việc đọc trở nên khó khăn hơn.

	+ Đối với các văn bản có khoảng cách dài, giảm độ tương phản sẽ giúp văn bản dễ đọc hơn. Có thể sử dụng văn bản màu xám đậm trên nền trắng hoặc văn bản trắng trên nền tối.

#### CSS3: OPACITY (làm mờ):

**opacity, rgba**:

- CSS3 giới thiệu thuộc tính làm mờ cho phép xác định làm mờ của phần tử và bất cứ phần tử con nào nằm trong đó. Giá trị là 1 số từ 0.0 và 1.0 (vì vậy giá trị của 0.5 là 50% opacity và 0.15 và 15% opacity) 

- Thuộc tính CSS3 rgba cho phép chỉ định màu sắc như 1 giá trị RGB nhưng thêm giá trị nữa để chỉ định độ mờ, giá trị này là alpha và 1 số nằm giữa 0.0 và 1.0. Các giá trị rgba sẽ ảnh hưởng đến phần tử mà nó được áp dụng

- Bởi vì 1 số trình duyệt sẽ không nhận ra màu RGBA nên cần cung cấp màu dự phòng để hiển thị màu tốt nhất. Nếu như sử dụng 2 quy tắc cho cùng 1 phần tử, phần tử đầu sẽ được ưu tiên sử dụng. Để tạo ra dự phòng có thể chỉ định màu sắc bằng mã hex, tên màu, giá trị RGB tiếp theo là chỉ định giá trị RGBA. Nếu như trình duyệt hỗ trợ màu RGBA thì nó sẽ áp dụng quy tắc đó

<a name="3"></a>
### 3. CSS3 color:

#### CSS3: HSL COLORS

CSS3 giới thiệu 1 cách hoàn toàn mới và trực quan để xác định màu sắc sử dụng hue, độ bão hòa, độ sáng

- **HUE**: trong màu HSL màu sắc thường biểu diễn trong vòng tròn màu, ngoài ra còn hiển thị trên thanh trượt với giá trị từ 0->360.

- **Saturation**: là lượng màu xám trên màu sắc. Saturation được biểu diễn theo tỉ lệ phần trăm 100% là đầy saturation và 0% là bóng màu xám

- **Lightness**: lightness là hầu hết màu trắng và màu đen trong 1 màu được biểu diễn theo tỉ lệ phần trăm 0% là lightness đen, 100% là lightness trắng, 50% là bình thường. Lightness được gọi là độ sáng.

#### CSS3: HSL & HSLA:

- Thuộc tính màu sắc `hsl` đã giới thiệu thêm 1 cách chỉ định màu sắc bằng CSS3, giá trị của thuộc tính bắt đầu với kí hiệu hsl, tiếp theo bởi thuộc tính riêng nằm bên trong như: 
	+ **Hue**: được thể hiện bằng góc (từ 0 đến 360 độ)

	+ **Saturation**: điều này được thể hiện bằng tỷ lệ phần trăm 

	+ **Lightness**: thể hiện theo tỷ lệ phần trăm với 0% là màu trắng, 50% là bình thường và 100% là màu đen. thuộc tính màu HSLA cho phép chỉ định thuộc tính màu sắc sử dụng hue, saturation và lightness với 4 giá trị đại diện như thuộc tính property.

	+ **alpha**: thể hiện như số giữa 0 và 1.0. Ví dụ: 0.5 đại diện 50% trong suốt, 0.75 đại diện cho 75% trong suốt.

### Tóm lại: 

- Màu sắc không chỉ mang lại sức sống cho website của bạn mà còn truyền đạt tâm trạng và gợi lên những phản ứng.

- Có 3 cách chỉ định màu sắc trong CSS: Giá trị RGB, mã hex, và tên màu.

- Color pickers giúp tìm được màu sắc bạn muốn

- Để đảm bảo đử độ tương phản giữa văn bản và màu nền (nếu không mọi người sẽ không thể đọc được nội dung trong website của bạn)

- CSS3 giới thiệu giá trị tăng thêm cho màu RGB để chỉ định độ mờ, đólà RGBA.

- CSS3 cũng cho phép chỉ định màu như các giá trị HSL với giá trị opacity tùy chọn, đó là HSLA

<a name="4"></a>
### Tài liệu tham khảo

> [1] Duckett, J. (2011). HTML and CSS: design and build websites. John Wiley & Sons. 

