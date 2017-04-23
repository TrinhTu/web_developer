## Bài 05: QUẢN LÍ FILE

> Tài liệu: Quản lí file
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 23/04/2017

### Mục lục:

[1. Quy cách đặt tên file](#1)

[2. Các dạng file](#2)

[3. Cơ bản việc quản lí file](#3)

[4. Hard và Symbolic Links](#4)

[5. Tìm kiếm file](#5)

[Tài liệu tham khảo](#6)

***

<a name="1"></a>
### 1. Quy cách đặt tên file:

- File là tập hợp các thông tin có quan hệ với nhau mà thể hiện dưới góc nhìn của người dùng chỉ là 1 khối đơn lẻ

- Một tên sẽ được gán cho 1 file để cho phép người dùng có thể dễ dàng định danh và làm việc với file

- Các hệ điều hành khác nhau có những quy định khác nhau về cách thức đặt tên file

- Tên file trong linux bao gồm mọi kí tự trừ dấu: `(/)`, kí tự null, dấu cách không bị cấm sử dụng nhưng hạn chế sử dụng

- Tên file thường bao gồm: chữ cái (thường ở dạng chữ thường), gạch chân, dấu gạch nối, dấu chấm (phân cách phần)

- Tên file ở dạng chữ hoa thường là các file văn bản đi kèm ví dụ: README, INSTALL, NEWS...

- Tên file có chiều dài tối thiểu là 1 và tối đa là 255

- Tên file có thể gồm nhiều phần hoặc không nhiều phần

- Tên file có thể bắt đầu bằng chữ số, phần mở rộng của file không bắt buộc, file ẩn là file được bắt đầu bằng *.*- trên thực tế không hoàn toàn ẩn (ví dụ: .bash_profile)

![2]()

- Chữ cái hoa hay chữ cái thường đều được chấp nhận

- Có phân biệt chữ hoa và chữ thường

- Một số câu lệnh cơ bản:

	+ Tạo mới 1 file: `touch name`

	+ Xem nội dung file: `less name`

	+ Tạo file có dấu cách ở giữa: `touch test\ so\ 1`

	+ Ẩn file: `mv name .name`

	+ Xem file đã bị ẩn: `ls -la`

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task29_Linux_Course_01/B%C3%A0i%205_Qu%E1%BA%A3n%20l%C3%AD%20file/image/1.png"/></p>

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task29_Linux_Course_01/B%C3%A0i%205_Qu%E1%BA%A3n%20l%C3%AD%20file/image/2.png"/></p>

<a name="2"></a>
### 2. Các dạng file:

- Trên 1 hệ thống Unix/Linux, tất cả mọi thứ đều là file, nếu có gì đó không phải là file thì đó là tiến trình

- File trong Linux được chia làm 3 dạng chính

	+ File chứa dữ liệu thông thường

	+ Thư mục

	+ Tập tin thiết bị

	+ Ngoài ra còn có link và pipe là các file đặc biệt

- **File chứa dữ liệu thông thường:**

	+ Là file thông thường dùng để chứa dữ liệu thông thường

		+ File văn bản

		+ File script thực thi được

		+ Các ứng dụng

		+ Đầu vào và đầu ra cho 1 chương trình

	+ Được lưu trên các thiết bị lưu trữ như đĩa cứng, CD-ROM,...

	+ Ví dụ: README, timer.sh

- **Thư mục**:

	+ Không chứa dữ liệu

	+ Chứa các file và các thư mục con trong nó

	+ Thư mục chứa 2 trường của 1 file

		+ Tên file

		+ Inode number

	+ Ví dụ: /bin, /home/hanv

- **Tập tin thiết bị**:

	+ Trên Unix và Linux mọi thiết bị được xem như các file

	+ Làm việc với các thiết bị thực ra là làm việc với các file thiết bị tương ứng

	+ Ví dụ: /dev/cdrom, /dev/vtty0,...

- Trong Linux không quan tâm tới phần mở rộng của file

- Linux tham chiếu vào định dạng của file nhận định đó là file gì

- Để xác định file trên Linux có thể dùng lệnh file, lệnh file dùng 3 bài kiểm tra

	+ Filesystem test: xác định xem file thuộc dạng socket, symbolic links, pipe hoặc file rỗng

	+ Magic number test: kiểm tra xem file nhị phân thực thi được dịch từ mã nguồn

	+ Language test: kiểm tra có phải file văn bản với các định dạng ngôn ngữ khác nhau

<a name="3"></a>
### 3. Cơ bản việc quản lí file:

- File có thể được tạo lập, sao chép, di chuyển và xóa

- Tạo lập bởi chương trình, hệ điều hành, ứng dụng người dùng

- Có thể được tạo bởi lệnh 'touch', nếu file chưa tồn tại thì sẽ tạo 1 file mới, file có rồi touch sẽ thay đổi lại nhãn thời gian trên file. Lệnh kiểm tra nhãn thời gian: `ls -l name`

- Thư mục có thể được tạo bởi lệnh `mkdir`

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task29_Linux_Course_01/B%C3%A0i%205_Qu%E1%BA%A3n%20l%C3%AD%20file/image/3.png"/></p>

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task29_Linux_Course_01/B%C3%A0i%205_Qu%E1%BA%A3n%20l%C3%AD%20file/image/4.png"/></p>

- Sao chép file:

	+ Lệnh `cp` thường được sử dụng trong việc sao chép các file - có thể sử dụng để sao chép thư mục

	+ Ví dụ: $cp old_file /dir/new_file

	+ Rất nhiều các switch cho nhiều tùy chọn

- Di chuyển file:

	+ Lệnh `mv` sử dụng để di chuyển file

	+ Có thể được sử dụng đê di chuyển 1 thư mục

	+ Sẽ hỏi xác nhận trong trường sẽ ghi đè file cũ trừ khi tùy chọn -f được sử dụng

	+ Có thể được sử dụng để đặt lại tên file

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task29_Linux_Course_01/B%C3%A0i%205_Qu%E1%BA%A3n%20l%C3%AD%20file/image/5.png"/></p>

- Xóa thư mục và các file nằm trong thư mục: `rm -rf name`

<a name="4"></a>
### 4. Hard và Symbolic Links:

- Link cho phép tạo ra các đường dẫn tắt tới 1 đối tượng trên hệ thống file của linux

- Có 2 dạng link chính là: symbolic (soft) link và hard link

- Hai dạng link cơ bản được phân biệt với nhau giữa vào cách thức sw dụng inode để tham chiếu tới đối tượng được link tới

- Các đường link có thể được tạo ra bằng lệnh ln

- **Inode**:

	+ Lưu trữ những thông tin về file trên hệ thống file của linux

	+ Các thông tin:

		+ Loại file và quyền truy cập

		+ Chủ sở hữu

		+ Kích thước file và số lượng hard link trỏ đến

		+ Nhãn thời gian

		+ Vị trí lưu nội dung file trên hệ thống vật lí

	+ Dùng ls -i để xem thông tin về inode

- **Symbolic Links**: tương tự như khái niệm shortcuts trên Windows

	+ Soft link không được dùng để tránh file đối tượng trỏ đến bị xóa, khi file đối tượng bị xóa soft link là không có giá trị

	+ Soft link có thể tham chiếu tới thư mục và file

	+ Tạo ra bằng lệnh ln -s

- **Hard Links**:

	+ Hard Links là các liên kết trỏ tới cùng 1 nội dung vật lí (nội dung file) với các giá trị inode giống nhau

	+ Nọi dung vật lí sẽ tồn tại trên hệ thống cho tới khi hard link cuối cùng bị xóa bỏ

	+ Hard link chỉ tham chiếu tới file mà không sử dụng được với thư mục

	+ Hard link được tạo bởi lệnh ln

<a name="5"></a>
### 5. Tìm kiếm file:

- **Locate**:
	
	+ Là công cụ tìm kiếm có tốc độ làm việc nhanh

	+ Sử dụng 1 tập cơ sở dữ liệu về hệ thống các file có trong hệ thống để thực hiện việc tìm kiếm

	+ Cơ sở dữ liệu về hệ thống các file được cập nhập thông qua việc sử dụng lệnh `slocate -u` hoặc `updatedb`

	+ Không hiện thị các kết quả mà người thực hiện việc tìm kiếm không có quyền quy cập

	+ Cú pháp:

		+ $locate ten_file: tìm file

		+ $locate -i text_string: tìm một chuỗi text trong tên file

- Trước khi thực hiện lệnh `locate` nên chạy lệnh `updatedb`

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task29_Linux_Course_01/B%C3%A0i%205_Qu%E1%BA%A3n%20l%C3%AD%20file/image/6.png"/></p>

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task29_Linux_Course_01/B%C3%A0i%205_Qu%E1%BA%A3n%20l%C3%AD%20file/image/7.png"/></p>

- **Find**:

	+ Đây là công cụ tìm kiếm chính xác nhất tuy nhiên mất nhiều thời gian cho việc xử lí

	+ Đi kèm với nhiều tùy chọn cho phép điều khiển để tìm được chính xác đối tượng mong muốn

	+ Có thể tìm kiếm file dựa trên các đường dẫn cụ thể, tên người dùng, nhóm sở hữu...

	+ Một số tùy chọn khác:

		+ `-type`: d- tìm thư mục,  f- tìm file thông thường, s- tìm socket

		+ `-user`: tìm user chủ sở hữu file

		+ `-size`: tìm kích thước

		+ `-perm`: tìm theo quyền

		+ `-name`: tìm theo tên file không phân biệt chữ hoa và chữ thường

		+ `-iname`: tìm tên file có phân biệt chữ hoa chữ thường

	+ Which kiểm tra 1 chương trình có trong các thư mục được chỉ ra bởi biến $PATH hay không

	+ Where: tìm kiếm các thông tin có liên quan đến vị trí chương trình nhập vào

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task29_Linux_Course_01/B%C3%A0i%205_Qu%E1%BA%A3n%20l%C3%AD%20file/image/8.png"/></p>

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task29_Linux_Course_01/B%C3%A0i%205_Qu%E1%BA%A3n%20l%C3%AD%20file/image/9.png"/></p>

<a name="6"></a>
### Tài liệu tham khảo:

> [1] Quản lý file (5.1).FLV. https://www.youtube.com/watch?v=VnNtBcgkX5Y&list=PLF09AC5E5EAC05E52&index=20
>
> [2] Quản lý file (5.2).FLV. https://www.youtube.com/watch?v=S6EMFz4tnN4&index=21&list=PLF09AC5E5EAC05E52
>
> [3] Quản lý file (5.3).FLV. https://www.youtube.com/watch?v=qoJfrlr5_64&list=PLF09AC5E5EAC05E52&index=22
>
> [4] Quản lý file (5.4).FLV. https://www.youtube.com/watch?v=em2TKNpJkYU&list=PLF09AC5E5EAC05E52&index=23



