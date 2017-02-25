## HackThis: Main

> **Category:** Main
>
> **Points:** 10
>
> **URL:** http://www.hackthis.co.uk/levels/main

## Write-up

### Level 1:

- View source:

[1]

- Ta tìm được username: **in** và password: **out** --> easy

### Level 2:

- View source:

[2]

- Ta tìm được username: **resu** và password: **ssap** --> easy

### Level 3:

- View source:

[3]

- Ta thấy value user= **heaven** và value password= **hell** --> easy

### Level 4:
- View source:

[4]

- Ta thấy giá trị cần tìm đã bị ẩn tại đường dẫn `../../extras/ssap.xml` ta add đường dẫn này vào URL hiện tại và có được đường dẫn sau: https://www.hackthis.co.uk/levels/main/extras/ssap.xml Kết quả hiển thị như sau:

[4.1]

- Vậy username = 999 và password = 111

### Level 5:

- View source:

[5]

- Ta tìm được password = 9286jas

### Level 6:

- Yêu cầu login Ronald nhưng trong list tùy chọn lại không có tên đó để lựa chọn. View source:

[6]

- Vậy yêu cầu phải edit lại source code sao cho có Ronald để login.

### Level 7:

- View source rỗng --> không có thông tin cần tìm, vậy nên hiển thị gợi ý (Show hint)

[7.1]

- Ta biết được thông tin cần tìm được cất trong tập tin `txt` và không hiển thị sẵn trong mã nguồn và cũng không thể tìm thấy bằng công cụ tìm kiếm. Để ngăn chặn công cụ tìm kiếm vào 1 tập tin nào đó trong website có thể thiết lập bằng tập tin `robots.txt`. Vậy nên vào đường dẫn: https://www.hackthis.co.uk/robots.txt ta có:

[7]

- File robots.txt đang chặn file: https://www.hackthis.co.uk/levels/extras/userpass.txt vậy ta có được thông tin cần tìm:

	+ username: 48w3756

	+ password: u3qh458

### Level 8:

- View source:

[8-1]

- Tương tự ta thấy giá trị cần tìm được để trong 1 đường dẫn khác: https://www.hackthis.co.uk/levels/extras/secret.txt. Ta có kết quả như sau:

[8]

- Mặc khác gợi ý cho ta biết rằng mật khẩu đã được chuyển đổi sang hệ nhị phân và cần được chuyển lại sang cơ số 16 và phải được viết in hoa nên ta tìm được kết quả như sau:

	+ username: B00B

	+ password: FEED

### Level 9:

- Dựa vào gợi ý và view source cho biết có thể đăng nhập theo 1 cách khác để tìm mật khẩu thay thế: https://www.hackthis.co.uk/levels/main/9?forgot

[9-1]

- Tại đây giá trị cần điền là email thay vì username và password. 

[9]

- Giá trị của email mà họ cung cấp là: `admin@hackthis.co.uk`. Nhưng theo gợi ý để lấy lại mật khẩu thì cần nhập email của người dùng, vậy cần edit lại source code và thay đổi giá trị email ban đầu thành email nào khác bất kì.

### Level 10

- Xem source 

###