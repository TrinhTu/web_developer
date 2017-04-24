## Bài 06: XỬ LÍ FILE VĂN BẢN

> Tài liệu: Xử lí file văn bản
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 23/04/2017

### Mục lục:

[1. Xem nội dung file văn bản](#1)

[2. Xử lí các luồng dữ liệu văn bản](#2)

[3. Tìm kiếm nội dung trong file văn bản](#3)

[4. Một số tiện ích khác](#4)

[Tài liệu tham khảo](#5)

***

<a name="1"></a>
### 1. Xem nội dung file văn bản:

- File văn bản có thể đọc được thông qua việc sử dụng các lệnh 'cat', 'more' và 'less'

- Cú pháp: $cat[more/less]ten_file

- Lệnh 'cat' sẽ gởi toàn bộ nội dung file văn bản ra ngoài màn hình

![1.1]()

- Lệnh 'more' cho phép xem nội dung của các file văn bản và định dạng kết quả hiện ra dưới dạng các trang

- <enter> để trượt xuống theo từng dòng

- <space> để trượt xuống theo từng trang

- Cú pháp: $more ten_file

![1.2]()

- Lệnh 'less' hiển thị toàn bộ nội dung file văn bản ra màn hình

- <enter> để trượt xuống theo từng dòng

- <space> để trượt xuống theo từng trang

- Dùng các phím lên xuống để xem xét nội dung file

- Có thể tìm kiếm trong 1 file hoặc mở 1 file để chỉnh sửa bằng tiện ích vi

![1.3]()

<a name="2"></a>
### 2. Xử lí các luồng dữ liệu văn bản:

- Luồng dữ liệu có thể được định hướng tới hoặc từ 1 file

- STDIN có thể được định hướng từ đầu ra của 1 file thành đầu vào của 1 chương trình

- STDOUT và STDERR có thể được gởi tới 1 file thay vì gởi tới console hoặc được gởi đi như là đầu vào của 1 chương trình

- Biểu tượng định hướng:

	+ < (định hướng đầu vào)

	+ > (định hướng stout hoặc stderr tới 1 file)

- Ví dụ: $less myfile > newfile

- '>' sử dụng để định hướng stout là mặc định, '2>' sử dụng để định hướng stderr

- Có thể định hướng tới 1 file riêng biệt hoặc vừa tới file và vừa ra màn hình

- Có thể định hướng tới /dev/null để loại bỏ kết quả

- '>' gởi kết quả tới 1 file và ghỉ đè file đó nếu tồn tại

- '>>' thêm stout hoặc stderr vào nội dung 1 file có sẵn

![1.4]()

<a name="3"></a>
### 3. Tìm kiếm nội dung trong file văn bản:

- Lệnh 'grep' cho phép tìm kiếm 1 xâu kí tự trong 1 file

- Có rất nhiều tùy chọn khác nhau cho mục đích tìm kiếm

- $grep noi_dung_xau ten_file. Tìm kiếm xâu noi_dung_xau trong file có thể ten_file

- Các tùy chọn có thể sử dụng để xét đến hoặc không xét đến chữ hoa và chữ thường

- Có thể sử dụng dạng cơ bản của grep hoặc sử dụng dạng nâng cao

- 2 lệnh thường sử dụng trong việc tìm kiếm nâng cao là 'egrep' và 'fgrep'

- Regular expressions cho phép tìm kiếm các nội dung văn bản mà không cần biết chính xác xâu kí tự muốn tìm kiếm

- Sử dụng 1 số kí tự đặc biệt để thay thế cho 1 hoặc vài kí tự không rõ

- Kí tự `*` đại diện cho 1 hoặc 1 vài kí tự. Ví dụ: re*. mọi xâu kí tự với độ dài bất kì bắt đầu với cụm chữ cái 're'

- Kí tự `.` đại diện cho bất cứ 1 kí tự đơn nào. Ví dụ: `r.d` mọi xâu kí tự có độ dài bằng 3, bắt đầu xâu là chữ `r` và kết thúc xâu là chữ `d`

<a name="4"></a>
### 4. Một số tiện ích khác:

- Lệnh 'sort' in nội dung của 1 file theo trình tự sắp xếp các chữ cái

- Lệnh 'uniq' lấy 1 file có nội dung đã được sắp xếp theo thứ tự chữ cái hoặc luồng dữ liệu, loại bỏ các dòng trùng nhau và hiện thị ra màn hình

- Lệnh 'wc' thực hiện đếm số dòng, số từ và số byte trong đầu ra nội dung của 1 file hoặc của 1 luồng dữ liệu đầu vào

- Lệnh 'head' hiển thi nội dung mười dòng đầu tiên của 1 file hoặc 1 luồng dữ liệu

- Lệnh 'tail' hiển thị nội dung mười dòng cuối cùng của 1 file hoặc 1 luồng dữ liệu

- Lệnh 'tac' tương tự lệnh 'cat' nhưng hiển thị nội dung theo trình tự ngược lại

- Lệnh 'cut' sử dụng để lấy và hiển thị 1 trường trong luồng kết quả có được

- Lệnh 'nl' sử dụng để thêm vào đầu mỗi dòng của kết quả hiển thị ra số

- Lệnh 'echo' hiển thị 1 nội dung ra màn hình hoặc có thể định hướng vào 1 file

- Lệnh 'tee' cho phép hiển thị nội dung của 1 luồng đầu vào vào cả 1 file lẫn ra màn hình

<a name="5"></a>
### Tài liệu tham khảo:

> [1] Xử lí file văn bản.FLV. https://www.youtube.com/watch?v=o75TLZ52sHA&index=24&list=PLF09AC5E5EAC05E52