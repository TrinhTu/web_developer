## HTML & CSS

### FLASH, VIDEO & AUDIO

> Chương 9: FLASH, VIDEO & AUDIO
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 02/02/2017

## Mục lục:

[1. Cách thêm flash movie vào website của bạn](#1)

[2. Cách thêm video và audio vào website của bạn](#2)

[3. HTML5 phần tử `<video>` và `<audio>`](#3)

[Tài liệu tham khảo](#4)

***

Flash là công nghệ được sử dụng rất phổ biến để tạo sự sinh động, video, và audio trong website. Trong chương này chúng ta sẽ học về:

- Cách sử dụng Flash trong website

- Cách sử dụng HTML5 phần tử `<video>` và `<audio>`

- Khi để lưu trữ video và audio và khi sử dụng 1 dịch vụ như YouTube

<a name="1"></a>
### 1. Cách thêm Flash movie và website của bạn:

#### Cách làm việc của Flash:

- Nếu muốn tạo Flash movie riêng cho mình thì phải mua các thiết kế Flash môi trường từ Adobe.Tuy nhiên 1 số công ty cung cấp flash hình ảnh động và trình chiếu, cũng như âm thanh và video người dùng có thể sử dụng mà không cần mua công cụ này.

- Khi tạo 1 tập tin flash nó được lưu với file `.fla`. Để sử dụng tập tin này trong trang web nó được lưu với định dạng khác là `SWF` (với đuôi mở rộng là `.swf`)

- Khi xuất phim thành định dạng SWF, flash tạo mã code có thể sử dụng đẻ nhúng phim flash vào trang của bạn. Trước đây, mã này sử dụng thẻ HTML `<object>` và `<embed>`, nhưng bây giờ thì sử dụng javascript thông dụng hơn.

- Để xem flash, trình duyệt cần sử dụng plugin (thêm 1 phần mềm chạy trong trình duyệt) được gọi là Flash Player. 98% các trình duyệt trên máy tính để bàn có cài đặt Flash. 

#### Sử dụng Flash:

- Khi flash được phát hành đầu tiên, nó được phát triển để tạo ra hình ảnh động, khi công nghệ ngày càng được phát triển thì nó sử dụng để xây dựng media player và toàn bộ trang web. Mặc dù Flash phổ biến nhưng nhiều người đã chọn lọc kĩ hơn khi sử dụng

#### Adding A Flash Movie To Your Web Page:

- Cách phổ biến nhất hiện nay để thêm Flash vào trang web đó là sử dụng Javasript. Có 1 số script cho phép thực hiện mà không cần hiểu thành thạo về ngôn ngữ Javascript. Script sử dụng thông dụng được gọi là SWFObject costheer có được bản sao miễn phí từ google.

- Kĩ thuật này sử dụng phần tử `<div>` tạo nên 1 không gian chứa Flash Movie. Phần tử `<div>` có thuộc tính `id` có giá trị được sử dụng bởi SWFObject script. Bên trong phần tử `<div>` có thể chứa các nội dung thay thế cho người dùng không thể dùng Flash. 

<a name="2"></a>
### 2. Cách thêm video audio vào website của bạn:

#### Understanding Video Formats And Players:

- Để thêm video vào trang web của bạn có 2 vấn đề cần phải hiểu rõ đó là: định dạng tập tin và video player/plugins.

	+ **Formats**: (định dạng) Về phim thì có các kiểu định dạng như BluRay, DVD, VHS. Còn trực tuyến thì bao gồm các kiểu định dạng sau AVI, Flash Video, H264, MPEQ, Ogg Theora, QuickTime, WebM, và Windows Media. Để người dùng có thể xem các video trực tuyến của bạn có thể chuyển đổi sang kiểu định dạng khác. Quá trình chuyển đổi video sang định dạng khác được gọi là "mã hóa" video. Có 1 số ứng dụng cho phép mã hóa video ví dụ như là  www.mirovideoconverter.com.

	+ **Players/ Plugins**: Lúc đầu các trình duyệt được thiết kế chỉ để hiển thị văn bản và hình ảnh. Những player và plugins chỉ hỗ trợ duy nhất định dạng video. Gần đây trình duyệt đã được cải tiến hơn được hỗ trợ HTML5 thẻ `<video>` (thay thế cho player và plugin đã bị lỗi thời)

	+ **Approach**: (tiếp cận) cách dễ dàng nhất để thêm video vào trong website của bạn là sử dụng dịch vụ như Youtube hoặc là Vimeo. Tuy nhiên trong 1 vài trường hợp việc sử dụng các dịch vụ đó là không phù hợp và bạn sẽ muốn lưu trữ các video đó vào trang web riêng của bạn. Video được tải lên cần được hiển thị ít nhất là 2 định dạng sau: WebM và MP4.

#### Using Hosted Video Services:

> Đây là cách dễ nhất để thêm video vào website của bạn là tải video lên Youtube hoặc Vimeo sử dụng các tính năng được hỗ trợ để nhúng video đó vào website của bạn

- **Ưu điểm**: Các trang web lưu trữ video như Youtube cung cấp các trình làm việc với phần lớn các web trình duyệt. Không cần quan tâm đến việc mã hóa video, các trang web cho phép tải lên nội dung trong 1 loạt định dạng, sau khi tải lên họ tự động chuyển đổi video của bạn thành các định dạng khác nhau cần thiết bởi các trình duyệt khác nhau. Các web lưu trữ của các công ty lớn thường phải trả thêm tiền băng thông và tập tin video có kích thước lớn. Nếu video của bạn được lưu trữ trên Youtube hoặc Vimeo thì bạn không cần phải trả thêm tiền cho băng thông.

- **Nhược điểm**: Video của bạn có sẵn trên các dịch vụ, nếu muốn video của bạn  hiển thị độc quyền trên mỗi trang web của bạn thì cần lưu trữ video trên máy chủ riêng và thêm player riêng vào trang. Một số dịch vụ sẽ hạn chế 1 vài tính nawg của video của bạn ví dụ như: cấm sử dụng quảng cáo đối với các video được tải lên (ngăn không cho kiếm tiền trên các nội dung đó). Một số dịch vụ sẽ đóng quảng cáo của họ trước khi bắt đầu video của bạn hoặc bao phủ chúng toàn màn hình video đang được phát và chất lượng của video cũng bị giới hạn.

- **The Alternative**: (thay thế) nếu muốn lưu trữ các video trên website riêng của bạn thay vì trên các tổ chức dịch vụ cần phải thiết lập trang web của bạn để chạy tốt các video. Chúng ta có thể nhìn thấy 2 cách khác nhau để lưu trữ video: sử dụng cả Flash Video và phần tử HTML5 `<video>`. Để đảm bảo số lượng người truy cập là tối đa cần phải sử dụng kết hợp cả 2 yếu tố trên.

#### Preparing A Flash Video For Your Site:

Có 3 bước để thêm Flash Video vào trang web của bạn:

- **Bước 1**: chuyển đổi vidoe sang định dạng FLV

	+ Để Flash Vidoe hoạt động cần chuyển đổi video của bạn sang dạng FLV. Từ Flash 6 thì môi trường Flash đã biết đến bộ mã hóa chuyển đổi video sang định dạng FLV. 1 số người sử dụng Flash video được cung cấp định dạng là H264 (cho phép chỉnh sửa video và xuất ra video trong định dạng này).Googling "FLV hay chuyển đổi H264" cho phép tìm phần mềm mã hóa thay thế.

- **Bước 2**: Tìm 1 FLV Player để phát video

	+ Cần có player viết bằng Flash với mục đích là chứa FLV movie và thêm các nút điều khiển như play/pause. Đây là 2 trang web cung cấp FLV player: www.osflv.com và www.longtailvideo.com

- **Bước 3**: Bao gồm Player Video trong trang web của bạn

	+ Có thể bao gồm các player trong trang bằng cách sử dụng kĩ thuật Javascript như SWFO. Cần khai báo với player nơi có thể tìm thấy tập tin video (một vài player có các tính năng ưu điểm như khả năng tạo danh sách nhiều video và thêm 1 số hình ảnh trước khi phát video)

#### Adding A Flash Video To Your Pages:

**Ví dụ**

```javascript
<head>
<title>Adding a Flash Video</title>
<script type="text/javascript"
src="http://ajax.googleapis.com/ajax/libs/
swfobject/2.2/swfobject.js"></script>
<script type="text/javascript">
var flashvars = {};
var params = {movie:"../video/puppy.flv"};
swfobject.embedSWF("flash/splayer.swf",
"snow", "400", "320", "8.0.0",
flashvars, params);</script>
</head>
<body>
<div id="snow"><p>A video of a puppy playing in
the snow</p></div>
</body>
```

- Trong ví dụ trên sử dụng OS FLV player để hiển thị video được gọi là `puppy.flv` chuyển đổi sang định dạng FlV. Chúng ta có thể thấy cách sử dụng SWFObject  để nhúng hình ảnh động vào trang. Trong ví dụ này player cần biết đường dẫn đến video để có thể phát video, vì vậy SWFObject sử dụng Javascript có sẵn để chuyển thông tin đến Flash movie, cung cấ 2 dòng code bắt đầu với `var`. Đường dẫn đến bộ phim được cung cấp trong biến `params`. 

- Khác nhau của video player luôn yêu cầu thông tin như đường dẫn đếnvidoe trong các định dạng khác nhau. Thường đi kèm với các ví dụ và tài liệu giúp hiểu rõ cách sử dụng chúng.

<a name="3"></a>
### 3. HTML5 phần tử video và audio:

#### HTML5: Preparing Video For Your Pages:

- Mặc dù phần tử HTML5 `<video>` là bổ sung mới gần đây nhưng nó được sử dụng rộng rãi. Dưới đây là 1 số vấn đề:

	+ **Support**: Phần tử HTML5 `<video>` được cung cấp bởi trình duyệt gần đây vì vậy có thể không cần sử dụng kĩ thuật này nếu muốn mọi người có thể nhìn thấy video của bạn

	+ **Digital Rights**: vào thời điểm gần đây phần tử `<video>` không hỗ trợ bất kì kiểu Digital Rights Management (DRM - Được gọi là bản sao bảo vệ). Nhưng theo cách riêng sẽ tìm đường xung quanh DRM.

	+ **Formats**: không phải tất cả trình duyệt hỗ trợ định dạng video giống nhau. Vì thế cần cung cấp video của bạn với nhiều định dạng khác nhau để được hỗ trợ nhiều hơn trên các trình duyệt. Nên cung cấp video với định dạng sau:

		+ H264: IE và Safari

		+ WebM: Android, Chrome, Firefox, Opera.

	+ **Controls**: Các trình duyệt cung cấp điều khiển riêng cho player và có thể thay đổi từ trình duyệt này  sang trình duyệt khác. Có thể điều khiển sự xuất hiện của các điều khiển bằng cách sử dụng Javascript.

	+ **In the Browser**: Một trong các vấn đề với player như là Flash Player là có thể hành động không nhất quán, HTML5 là lựa chọn để giải quyết vấn đề này.

#### HTML5: Adding Video To Your Pages:

- `<video>`: phần tử `<video>` có 1 số thuộc tính giá trị cho phép điều khiển phát lại video

	+ `src`: thuộc tính này xác định đường dẫn đến video. 

	+ `poster`: Thuộc tính này cho phép xác định đường dẫn đến hình ảnh hiển thị khi các video  được tải về

	+ `width, height`: thuộc tính này xác định kích thước của player là pixels.

	+ `controls`: khi sử dụng, thuộc tính chỉ ra rằng trình duyệt nên cung cấp điều khiển riêng để playback.

	+ `autoplay`: khi sử dụng thuộc tính xác định tập tin cần tự động đóng.

	+ `loop`: thuộc tính chỉ ra video nên bắt đầu phát lại khi bị tắt.

	+ `preload`: thuộc tính thông báo cho trình duyệt những điều nên làm khi tải trang, gồm có 3 giá trị:

		+ `none`: trình duyệt không nên tải video cho đến khi người dùng ấn phím play.

		+ `auto`: trình duyệt nên tải video xuống khi tải trang

		+ `metadata`: trình duyệt chỉ nên sưu tập thông tin như kích thước, tên, tên trước, tracklist, và thời gian.

#### HTML5: Multiple Video Sources:

- `<source>`: xác định nơi chứa tập tin để phát cần sử dụng phần tử `<source>` bên trong phần tử `<video>` (nên thay thế thuộc tính `src` trên thẻ mở `<video>`). Cũng có thể sử dụng nhiều phần tử `<source>` để xác định video có sẵn trong các định dạng khác nhau. 

- `src`: thuộc tính xác định đường dẫn đến video.

- `type`: nên sử dụng thuộc tính để thông báo cho trình duyệt định dạng của video. Nếu không nó sẽ tải 1 số video để xem (nhưng sẽ mất nhiều thời gian và tốn băng thông nhiều hơn)

- `codecs`: codec được sử dụng để mã hóa video trong các loại thuộc tính, chú thích được sử dụng trong ngoặc đơn, ngoặc kép bên trong các thuộc tính. Trình duyệt sẽ không cung cấp phần tử `<video>` hoặc định dạng sử dụng video, nó sẽ hiển thị mọi thứ nằm chính giữa thẻ mở và thẻ đóng `<video>`.

#### HTML5: Combining Flash & HTML5 Video:

- Bằng cách cung cấp các video trong cả HTML5 và định dạng Flash Video, có thể chắc rằng có thể được xem bởi đa số người dùng trên trang web của bạn.

- Việc lựa chọn HTML5 là lựa chọn tốt nhất còn đối với Flash Video như 1 lựa chọn dự phòng trong những trình duyệt không hỗ trợ HTML5. Vì 1 số video player cung cấp mã hóa H264 nên nếu sử dụng palyer hộ trợ định dạng này cần cung cấp video trong H264 và định dạng WebM

- Nếu bắt đầu với HTML5 bạn có thể: 

	+ Tạo điều khiển Playback

	+ Cung cấp các phiên bản khác nhau của video cho các trình duyệt có kích thước khác nhau

	+ Nói cho các phần khác nhau trong 1 trang thay đổi khi video đạt đến điểm nhất định.

#### Adding Audio To Web Pages:

Định dạng phổ biến nhất để đưa âm thanh lên trang web là MP3. Có 3 định tuyến thực hiện là: 

- **use a hosted service**: 1 số trang web cho phép tải âm thanh lên và cung cấp player có thể nhúng vào trang web như SoundCloud.com và MySpace.com

- **use flash**: 1 vài flash movie cho phép phát tập tin MP3 từ các nút đơn giản để phát 1 ca khúc, cho phép tạo danh sách hay máy hát.

- **use HTML5**: HTML5 cung cấp 1 phần tử mới là `<audio>`, các trình duyệt hỗ trợ phần tử này cung cấp các điều khiển riêng của họ.

#### Adding A Flash MP3 Player:

Có nhiều MP3 player được viết bằng Flash như:

- flash-mp3-player.net

- musicplayer.sourceforge.net

- www.wimpyplayer.com

Mỗi player có 1 tính chức năng khác nhau nên cần lựa chọn trước khi sử dụng cho trang web của bạn.

#### HTML5: Adding HTML5 Audio To Your Pages:

- `<audio>`: HTML5 giới thiệu 1 phần tử `<audio>` bao gồm file âm thanh trong trang của bạn, với video HTML5 trình duyệt hỗ trợ các định dạng khác nhau cho âm thanh. Phần tử `<audio>` có 1 số thuộc tính cho phép kiểm soát phát lại âm thanh:

	+ `src`: Thuộc tính xác định đường dẫn đến file audio

	+ `control`: thuộc tính này hiển thị các nút điều khiển cho player, nếu không sử dụng thuộc tính này thì sẽ không hiển thị các nút điều khiển mặc định, bạn chỉ có thể điều khiển bằng cách sử dụng javascript.

	+ `autoplay`: nhờ thuộc tính này chỉ ra âm thanh nên tự động phát

	+ `preload`: thuộc tính chỉ ra trình duyệt nên làm gì nếu người sử dụng không thiết lập tự động phát được.

	+ `loop`: thuộc tính xác định các track âm thanh nên phát lại khi đã kết thúc.

#### HTML5: Multiple Audio Sourses:

- `<source>`:  Chỉ ra nhiều tập tin sử dụng phần tử `<source>` ở giữa thẻ mở `<audio>` và thẻ đóng `</audio>`. Điều này quan trọng vì trình duyệt khác nhau hỗ trợ các định dạng khác nhau cho tập tin audio

	+ MP3: Safari 5+, Chrome 6+, IE9

	+ Ogg Vorbis: Firefox 3.6, Chome 6, Opera 1.5, IE9

Vậy nên cần cung cấp 2 định dạng audio để đảm bảo chạy tốt trên tất cả trình duyệt hỗ trợ phần tử `<audio>`, ngoài ra còn có thể cung cấp Flash thay thế cho trình duyệt cũ không hỗ trợ phần tử `<audio>`.

### Tóm lại:

- Flash cho phép thêm hình ảnh động, video và audio trên trang web.

- Flash không hỗ trợ trên iPhone và iPad

- HTML5 giới thiệu thêm phần tử mới `<video>` và `<audio>` để thêm video và audio vào trang web, nhưng nó không được hỗ trợ trên hầu hết các trình duyệt

- Trình duyệt cung cấp phần tử HTML5 nhưng không hỗ trợ tất cả các định dạng video và audio vậy nên cần cung cấp cho tất cả các tập tin đó nhiều định dạng khác nhau để đảm bảo rằng mọi người có thể xem được.

<a name="4"></a>
### Tài liệu tham khảo

> [1] Duckett, J. (2011). HTML and CSS: design and build websites. John Wiley & Sons. 

