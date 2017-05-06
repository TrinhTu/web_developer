## Bài 07: CHỈNH SỬA VĂN BẢN VỚI VI

> Tài liệu: Chỉnh sửa văn bản với Vi
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 06/05/2017

### Mục lục:

[1. Tổng quan về vi - chế độ làm việc và cách thức thao tác](#1)

[2. Chèn thêm nội dung kí tự trong vi](#2)

[3. Chỉnh sửa nội dung với kí tự vi](#3)

[4. Xóa bỏ nội dung kí tự trong vi](#4)

[5. Tìm kiếm chuỗi kí tự trong vi](#5)

[6. Thiết lập các tùy chọn](#6)

[7. Lưu file và thoát khỏi vi](#7)

[Tài liệu tham khảo](#8)

***

<a name="1"></a>
### 1. Tổng quan về vi - chế độ làm việc và cách thức thao tác:

- Vi là công cụ chỉnh sửa văn bản phỏ biến trong Unix/Linux, là công cụ chạy trong shell lệnh

- Sử dụng để tạo lập và chỉnh sửa các file văn bản, file script

- Để tạo mới 1 file hoặc mở 1 file: $vi /path/file

- Để mở 1 file sau đó chuyển tới phần nội dung có chứa 1 chuỗi kí từ cụ thể

	`$vi +/search_string file`

- Để mở vi và nhảy tới 1 dòng cụ thể

	`vi + 10/path/file`

- Chế độ lệnh: thực hiện xem xét và làm việc với file (lưu file, tìm kiếm, thoát)

- Chế độ chèn: chỉnh sửa nội dung kí tự trong file

- Chuyển sang chế độ lệnh bất cứ khi nào bằng cách nhấn phím ESC

- Có thể sử dụng các phím mũi tên lên xuống để thực hiện xem xét nội dung file trong các hệ thống bàn phím mới

- Trong các hệ thống bàn phím cũ sử dụng các phím:

	+ k - di chuyển lên

	+ j - di chuyển xuống

	+ h - di chuyển sang trái

	+ l - di chuyển sang phải

- Tổ hợp các phím để trượt đi qua các trang:

	+ CTRL+F: di chuyển tới trước 1 trang

	+ CTRL+B: di chuyển về sau 1 trang

	+ CTRL+D: di chuyển tới trước 1/2 trang

	+ CTRL+U: di chuyển về sau 1/2 trang

<a name="2"></a>
### 2. Chèn thêm nội dung kí tự trong vi:

- Vi luôn bắt đầu trong chế độ lệnh - để chuyển sang chế độ chèn nhấn `INSERT`

	+ i-di chuyển tới vị trí con trỏ hiện tại và chèn kí tự vào văn bản bắt đầu từ điểm đó

	+ l-di chuyển tới vị trí đầu dòng hiện tại và chèn kí tự vào văn bản bắt đầu từ điểm đó

	+ a- di chuyển con trỏ sang bên phải 1 kí tự và chèn văn bản vào

	+ A- di chuyển con trỏ tới cuối dòng và chèn văn bản vào

	+ o- bắt đầu 1 dòng mới ngay dưới dòng hiện tại

	+ O- bắt đầu 1 dòng mới ngay trên dòng hiện tại

<a name="3"></a>
### 3. Chỉnh sửa nội dung kí tự với vi:

- Chuỗi kí tự có thể được thay đổi hoặc thay thế bởi 1 kí tự, một dòng, 1 câu hoặc 1 từ

	+ cw- thay đổi 1 từ đơn tại vị trí con trỏ hiện tại

	+ c$- thay đổi dòng hiện tại

	+ r- thay thế kí tự dưới con trỏ

	+ R- thay thế chuỗi văn bản trên cùng 1 dòng cho tới kih bấm `ESC`

- Các lệnh sao chép và dán:

	+ yw để sao chép một từ. Ví dụ: 2yw sẽ sao chép 2 từ tính từ vị trí con trỏ hiện tại

	+ yy để sao chép 1 dòng. Ví dụ: 2yy sao chép 2 dòng tính từ vị trí con trỏ hiện tại

	+ p- dán 1 chuỗi kí tự sang bên phải con trỏ

	+ P-dán 1 chuỗi kí tự sang bên trái con trỏ

<a name="4"></a>
### 4. Xóa bỏ nội dung kí tự trong vi:

<a name="5"></a>
### 5. Tìm kiếm chuỗi kí tự trong vi:

- Tìm kiếm tiến thực hiện tìm kiếm từ vị trí con trỏ hiện tại cho tới cuối văn bản chuỗi mà người dùng quan tâm

- Cú pháp: /search_string.

- Ví dụ: /install

- Tìm kiếm lùi tiến hành tìm kiếm chuỗi người dùng quan tâm từ vị trí con trỏ hiện tại tới đầu văn bản

- Cú pháp: ?search_string

- Chữ n sẽ tìm đến mẫu tự thỏa mãn điều kiện ở phía trước, **shift+N** sẽ tìm đến mẫu thỏa mãn điều kiện ở phía sau

- Cú pháp tìm kiếm và thay thế mẫu tự tìm thấy như sau:

	**:s/search-string/replacement_string/**

- Có thể thiết lập được 60 tùy chọn khác nhau để hiệu chỉnh quá trình làm việc của vi

- Các tùy chọn thường dùng bao gồm: đánh số dòng, tab stops, bộ nhớ đệm lịch sử lệnh

- Các tùy chọn có thể được thiết lập qua file ~/.exrc cho từng người dùng hoặc /etc/exrc cho mọi người dùng

- Tùy chọn có thể được thiết lập trong vi thông qua việc sử dụng lệnh set trong chế độ lệnh

- Dùng lệnh set để xem các tùy chọn đang được áp dụng cho phiên làm hiện tại của vi

<a name="6"></a>
### 6. Thiết lập các tùy chọn:

- Có thể thiết lập 60 tùy chọn khác nhau để hiệu chỉnh quá trình làm việc của vi

- Các tùy chọn thường bao gồm: đánh số dòng, tab stops, bộ nhớ đệm lịch sử đệm

- Các tùy chọn có thể được thiết lập qua file ~/.exrc cho từng người dùng hoặc /etc/exrc cho mọi người dùng

- Có tùy chọn có thể được thiết lập trong vi thông qua việc sử dụng lệnh set trong mọi chế độ lệnh

- Có thể dùng lệnh set để xem các tùy chọn đang được áp dụng cho mọi phiên làm hiện tại của vi

- Sử dụng set để bật tắt các tùy chọn

	+ **:set number** - bật chế độ hiển thị số thứ tự dòng trong file hiện tại

	+ **:set nonumber** - tắt chế độ hiển thị số thứ tự dòng trong file hiện tại

	+ **:set all** - để xem mọi tùy chọn có thể thiết lập

<a name="7"></a>
### 7. Lưu file và thoát khỏi vi:

- Để thoát khỏi vi và ghi lại các thao tác đã thực hiện với file có 1 số cách để thực hiện trong chế độ lệnh

- Trong trường hợp không chỉnh sửa gì thoát khỏi file: `:q`

- Trường hợp đã chỉnh sửa và muốn thoát không lưu lại: `:q!`

- Với việc ghi lại kết quả trong vi - có thể ghi lại và thoát hoặc ghi lại và tiếp tục chỉnh sửa

	+ Để ghi lại và tiếp tục làm việc **:w**

	+ Để ghi lại và thoát khỏi vi **:wq**

	+ Để ghi lại bằng mọi giá **:wq!**

- Có 2 cách khác để lưu lại và thoát: `:x` và `<SHIFT>+ZZ`

<a name="8"></a>
### Tài liệu tham khảo:

> [1] Chỉnh sửa văn bản với VI (7.1).FLV. https://www.youtube.com/watch?v=CHiivOuCssM&list=PLF09AC5E5EAC05E52&index=25
>
> [2] Chỉnh sửa văn bản với VI (7.2 end).FLV. https://www.youtube.com/watch?v=50ftvHXZ0oQ&list=PLF09AC5E5EAC05E52&index=26
