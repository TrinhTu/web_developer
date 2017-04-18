## Bài 04: CƠ BẢN VỀ HỆ LỆNH

> Tài liệu: Cơ bản về hệ lệnh
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 18/03/2017

### Mục lục:

[1. Shell lệnh](#1)

[2. Cấu trúc lệnh và cú pháp](#2)

[3. Các trang trợ giúp Help và MAN](#3)

[4. Các lệnh làm việc với thư mục](#4)

[Tài liệu tham khảo](#5)

***

<a name="1"></a>
### 1. Shell lệnh:

- Shell lệnh cung cấp cho người dùng các lệnh có thể tương tác với Kernel

- Môi trường mà các lệnh được nhập vào và thực thi

- Ngôn ngữ lệnh cho phép lập trình tạo các trình tiện ích nhỏ

- Điều khiển môi trường làm việc

- Thay đổi các biến và tên file dùng trong hệ thống

- Định hướng xuất nhập vào ra

- Shell còn được gọi là Command Line Interface (CLI)

- Các loại Shell

	+ C Shell (CSH)

	+ Korn Shell (KSH)

	+ Bourne Shell

- Các loại shell khác nhau có 1 số tính năng chung và 1 số tính năng riêng

- **C Shell**

	+ Có cú pháp tương tự ngôn ngữ C

	+ Ví dụ:

```javascript
if ( ! -e mylife ) echo mytext > mylife
	if ( ! -e mylife ) then
		echo mytext > mylife
	endif
```

- **Korn Shell**

	+ Tương thích với Bourne Shell 

	+ Có nhiều thuộc tính tương tự như C Shell. Ví dụ: Command history

	+ Được sử dụng như 1 ngôn ngữ lập trình để tạo ra các tiện ích nhỏ

- **Bourne Again Shell (BASH)**

	+ Được sử dụng phổ biến nhất trong các bản phân phối

	+ Được phát triển từ Bourne shell

	+ Có nhiều tính năng mới

		+ Điều khiển các tiến trình

		+ Các lệnh history

		+ Tên file dài

		+...

- Dấu nhắc trong Shell thường là $ thì là user thông thường, còn # là user root.

- Một số câu lệnh:

	+ Kiểm tra đang làm việc với shell nào sử dụng câu lệnh: `echo $SHELL`

	+ Tất cả các shell được đặt trong thư mục `bin`: `ls /bin | more`

	+ Có thể chuyển từ shell này sang shell khác bằng cách thay đổi tên, về cấu trúc các lệnh cơ bản vẫn như cũ.

![1](https://github.com/TrinhTu/web_developer/blob/master/Task29_Linux_Course_01/B%C3%A0i%204_%20C%C6%A1%20b%E1%BA%A3n%20v%E1%BB%81%20h%E1%BB%87%20l%E1%BB%87nh/image/1.png)

<a name="2"></a>
### 2. Cấu trúc lệnh và cú pháp:

- Lệnh để thực hiện gọi 1 chương trình, ứng dụng, script hoặc các tiện ích

- Lệnh được nhập tại dấu nhắc shell

- Cú pháp cho 1 lệnh trong linux

	+ command [options][expression][filenames] Trong đó:

		+ `command`: tên của lệnh hoặc tiện ích sẽ được sử dụng

		+ `option`: các tùy chọn đi kèm với lệnh hoặc tiện ích, ảnh hưởng đến quá trình thực thi của lệnh

		+ `expresstion`: một số lệnh hoặc tiện ích đòi hỏi có các biểu thức điều kiện để thực thi


		+ `file`: 1 số lệnh hoặc tiện ích yêu cầu 1 hoặc nhiều đối tượng cần có để áp dụng tính năng được thực thi

- Chính tả và cú pháp là rất quan trọng

- Linux là hệ thống phân biệt các trường hợp (case sentive)

- Các lệnh có rất nhiều tùy chọn khác nhau được gọi là switch

- Các switch được phân cách với nhau trong các câu lệnh bởi dấu (-).

- Các switch có thể được xâu chuỗi lại. (Ví dụ: ls -al)

![2](https://github.com/TrinhTu/web_developer/blob/master/Task29_Linux_Course_01/B%C3%A0i%204_%20C%C6%A1%20b%E1%BA%A3n%20v%E1%BB%81%20h%E1%BB%87%20l%E1%BB%87nh/image/2.png)

- Khi gõ 1 lệnh thì Linux sẽ thực hiện việc tìm kiếm trong các thư mục

![3]()

<a name="3"></a>
### 3. Các trang trợ giúp Help và MAN

- Có 3 cách để có được sự hộ trợ bổ sung hoặc các thông tin cần thiết từ 1 lệnh, các sử dụng và các switch

	+ --help switch

	+ Lệnh info

	+ MAN page

- **--help switch**

	+ --help switch là tùy chọn sẵn cps trong 1 số lệnh. Ví dụ: ls -help

	+ Hiển thị các thông số cho biết tính năng của lệnh, cú pháp của lệnh, các switch và vai trò của các switch có thể đi kèm với lệnh

	+ Không được hỗ trợ trong tất cả các lệnh hoặc bản phân phối

![4]()

- **Lệnh info**:

	+ Một số bản phân phối Linux đi kèm rất nhiều các trang thông tin (info page) về các loại khái niệm Linux và lệnh

	+ Lệnh info cho phép truy xuất các trang thông tin đi kèm trong các bản phân phối để lấy thông tin về lệnh hoặc khái niệm muốn nắm được

	+ Lệnh info không có trong tất cả các lệnh và các bản phân phối

	+ Cú pháp lệnh sử dụng: $info command_name. Ví dụ: $info mkdir

![5]()

- **MAN page** (manual pages)

	+ MAN page là tài liệu hỗ trợ mở rộng đi kèm trong các bản phân phối

	+ MAN pages bao gồm các thông tin đầy đủ về các thành phần của bản phân phối: kernel, tiện ích cũng như các lệnh

	+ Thông qua MAN có thẻ truy xuất được thông tin sử dụng của các lệnh cần thiết

	+ Cách sử dụng: $MAN <command>

	+ MAN page chia thành các chủ đề (session) khác nhau:

		+ Session 1 - User command: các lệnh thông thường của hệ điều hành

		+ Session 2 - System call: các thư viện kernel của hệ thống

		+ Session 3 - Subroutines: các hàm thư viện lập trình

		+ Session 4 - Devices: các hàm truy xuất file và thiết bị

		+ Session 5 - File format: các hàm định dạng file

		+ Session 6 - Games: các hàm liên quan đến trò chơi

		+ Session 7 - Miscell: các hàm khác

		+ Session 8 - Sys Admin: các hàm quản trị hệ thống

		+ **Ví dụ**: $man echo: xem các thông tin về hàm echo dùng trong lập trình

		+ Mặc định là session 1

		+ Để xem trang man pages theo từng trang ấn Space

		+ Thoát khỏi man pages ấn q

![6]()

<a name="4"></a>
### 4. Các lệnh làm việc với thư mục:

- Các file được lưu trong các thư mục

- Tương tự như khái niệm thư mục trong Windows

- Các thư mục có dạng thức phân cấp hoặc cây

- Thư mục trên cùng là thư mục root (`/`)

- Cây thư mục được tham khảo bởi 1 đường dẫn

- Thư mục có thể thư mục nhánh hoặc là thư mục của 1 thư mục khác

- Tất cả các thư mục đều là thư mục con của thư mục root

- **/bin**

	+ Chứa các lệnh có thể được sử dụng bởi người dùng có quyền quản lí cũng như người dùng thông thường

	+ Các lệnh thông thường chứa trong bin gồm: ls, cp, rm, ...

	+ Không có thư mục con bên trong thư mục bin

![9]()

- **/sbin**

	+ Chứa các tiện ích của người quản lí hệ thống

	+ Các tiện ích (file nhị phân) cần thiết cho quá trình khởi động, khôi phục sửa chữa hay phục hồi lại hệ thống

	+ Ngoài ra còn có các tiện ích tương tự trong các thư mục /usr/sbin và /usr/local/bin

![8]()

- **/dev**

	+ Nơi chứa các file thiết bị hoặc các file đặc biệt

	+ Có thể là 1 thiết bị ổ cứng IDE: /dev/hda /dev/hdb

	+ Có thể là 1 thiết bị ổ cứng SCSI: /dev/sda /dev/sdb

	+ Có thể là thiết bị âm thanh: /dev/audio /dev/dsp

	+ Có thể là thiết bị terminal: /dev/tty0 /dev/tty1

	+ Có thể là 1 số cổng terminal: /dev/ttyS0 cho COM 1, /dev/ttyS1 cho COM 2

	+ Có thể là đĩa mềm: /dev/fd*

	+ ...

![11]()

- **/home**

	+ Thư mục chứa các file cá nhân của người dùng thông thường trên hệ thống

	+ Các cấu hình liên quan đến thư mục home có thể khác nhau trên các hệ thống khác nhau vậy nên không nên để các chương trình thực thi trong thư mục này.

![10]()

- **/boot**

	+ Chứa tất cả các file cần thiết cho quá trình khởi động

	+ Kernel của hệ điều hành phải được đặt tại `/` hoặc `/boot`

![7]()

- **/etc**:

	+ Thư mục này chứa các file cấu hình cần thiết cho hệ thống

		+ File cấu hình là các file chứa các thông tin được sử dụng để điều khiển hoạt động của 1 chương trình

		+ File cấu hình là các file tĩnh

	+ Các file cấu hình về mật khẩu người dùng,boot, device, mạng và các cấu hình khác nằm ở đây

	+ Nhiều file trong /etc được sử dụng để định ra 1 thiết bị phần cứng

		+ /etc/X11 chứa các file cấu hình cho card đồ họa

	+ Không nên đặt file nhị phân nào trong thư mục /etc

![12]()

- **lib**

	+ Thư mục này chứa các mã của các thư viện chia sẻ cần thiết cho việc khởi động hệ thống và chạy các lệnh trên hệ thống file root

	+ Các file trong thư mục này nên ở dạng tĩnh

	+ Các thư mục thư viện có thể bao gồm các thư viện liên kết tĩnh hoặc chia sẻ (/usr/lib)

![13]()

- **/root**

	+ Đây là thư mục home của người dùng root

	+ Đối với 1 số hệ thống thì thư mục này không cần thiết

- **/usr**

	+ Là thư mục lớn chứa cấu trúc tương tự `/`

	+ Đa phần hệ thống Linux nằm trong thư mục `/usr`

	+ Có nhiều thư mục con nằm trong bao gồm:

		+ /local: ho phép administrator có thể cài đặt các phần mềm của họ

		+ /bin: chứa các lệnh của người dùng

		+ /include: chứa các header file được sử dụng bởi ngôn ngữ C

		+ /man: chứa các man pages

		+ ...

![14]()

- **/var**: 

	+ Chứa các file dữ liệu là biến của các chương trình chạy: bao gồm spool, các file quản lí và file nhật kí, các file tạm.

	+ Nên đặt /var ra 1 phân vùng độc lập trong quads trình cài đặt

![15]()

- **/tmp**:

	+ Là nơi chứa các file tạm trong quá trình người dùng làm việc

	+ Bất kì người dùng nào đều có thể đọc và ghi trong thư mục /tmp nhưng không thể truy cập đến các file khác trong thư mục này

	+ Đa số các bản phân phối sẽ dọn dẹp trong thư mục /tmp trong quá trình khởi động

	+ Không để các file quan trọng trong thư mục /tmp

	+ Một vài chương trình sử dụng thư mục này như vùng làm việc tạm

![16]()

- Để tham chiếu tới 1 thư mục sử dụng 2 dạng đường dẫn: đường dẫn tuyệt đối và đường dẫn tương đối

- Đường dẫn tuyệt đối tham chiếu tới đường dẫn đầy đủ của 1 thư mục bắt đầu từ thư mục root.

- Đường dẫn tương đối tham chiếu tới tới đường dẫn tắt của 1 thư mục trong ngữ cảnh của thư mục hiện tại

- Một số lệnh thông thường dùng làm việc với thư mục:

	+ $pwd: hiển thị đường dẫn của thư mục hiện tại mà người dùng đang làm việc

	+ $cd: chuyển đến thư mục khác

	+ $ls: liệt kê nội dung của thư mục với rất nhiều switch

![17]()

<a name="5"></a>
### Tài liệu tham khảo:

> [1] Cơ bản về hệ lệnh (4.1).FLV. https://www.youtube.com/watch?v=CgZgRD6v-j8&index=16&list=PLF09AC5E5EAC05E52
>
> [2] Cơ bản về hệ lệnh (4.2).FLV. https://www.youtube.com/watch?v=-w-S8YMrezU&index=17&list=PLF09AC5E5EAC05E52
>
> [3] Cơ bản về hệ lệnh (4.3).FLV. https://www.youtube.com/watch?v=OPbw2ys-6CQ&index=18&list=PLF09AC5E5EAC05E52
> 
> [4] Cơ bản về hệ lệnh (4.4).FLV. https://www.youtube.com/watch?v=TEjLCOccfHI&index=19&list=PLF09AC5E5EAC05E52