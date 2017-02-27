## HackThis: Main

> **Category:** Main
>
> **Points:** 
>
> **URL:** http://www.hackthis.co.uk/levels/main

## Write-up

### Level 1:

- **URL**: https://www.hackthis.co.uk/levels/main/1

- **Desciption**:

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Main/image/1.1.png"/></p>

- **Solution:**

	+ View-source ta tìm được username: **in** và password: **out**

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Main/image/1.png"/></p>

### Level 2:

- **URL:** https://www.hackthis.co.uk/levels/main/2

- **Description:**

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Main/image/2.1.png"/></p>

- **Solution:** 

	+ View-source ta tìm được username: **resu** và password: **ssap**

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Main/image/1.png"/></p>

### Level 3:

- **URL:** https://www.hackthis.co.uk/levels/main/3

- **Description:**

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Main/image/3.1.png"/></p>

- **Solution:**

	+ View-source ta thấy value user= **heaven** và value password= **hell** 

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Main/image/3.png"/></p>

### Level 4:

- **URL:**https://www.hackthis.co.uk/levels/main/4

- **Description:**

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Main/image/4.1.png"/></p>

- **Solution:**

	+ view-source giá trị cần tìm đã bị ẩn tại đường dẫn `../../extras/ssap.xml` ta add đường dẫn này vào URL hiện tại và có được đường dẫn sau: https://www.hackthis.co.uk/levels/main/extras/ssap.xml Kết quả hiển thị như sau:


<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Main/image/4.png"/></p>


<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Main/image/4-1.png"/></p>

Vậy username = 999 và password = 111

### Level 5:

- **URL:** https://www.hackthis.co.uk/levels/main/

- **Description:** 

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Main/image/5.1.png"/></p>

- **Solution:** 

	+ View-source tìm được password = 9286jas

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Main/image/5.png"/></p>

### Level 6:

- **URL:** https://www.hackthis.co.uk/levels/main/6

- **Description:**

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Main/image/6.1.png"/></p>

- **Solution:** 

	+ Yêu cầu login Ronald nhưng trong list tùy chọn lại không có tên đó để lựa chọn. View source:

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Main/image/6.png"/></p>

Vậy yêu cầu phải edit lại source code sao cho có Ronald để login.

### Level 7:

- **URL:** https://www.hackthis.co.uk/levels/main/7

- **Description:**

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Main/image/7.1.png"/></p>

- **Solution:**

	+ View source rỗng --> không có thông tin cần tìm, vậy nên hiển thị gợi ý (Show hint)

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Main/image/7-1.png"/></p>

Ta biết được thông tin cần tìm được cất trong tập tin `txt` và không hiển thị sẵn trong mã nguồn và cũng không thể tìm thấy bằng công cụ tìm kiếm. Để ngăn chặn công cụ tìm kiếm vào 1 tập tin nào đó trong website có thể thiết lập bằng tập tin `robots.txt`. Vậy nên vào đường dẫn: https://www.hackthis.co.uk/robots.txt ta có:

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Main/image/7.png"/></p>

File robots.txt đang chặn file: https://www.hackthis.co.uk/levels/extras/userpass.txt vậy ta có được thông tin cần tìm:

	+ username: 48w3756

	+ password: u3qh458

### Level 8:

- **URL:** https://www.hackthis.co.uk/levels/main/8

- **Description:**

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Main/image/8.1.png"/></p>

- **Solution:** 

	+ View source

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Main/image/8-1.png"/></p>

Tương tự ta thấy giá trị cần tìm được để trong 1 đường dẫn khác: https://www.hackthis.co.uk/levels/extras/secret.txt. Ta có kết quả như sau:

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Main/image/8.png"/></p>

Mặc khác gợi ý cho ta biết rằng mật khẩu đã được chuyển đổi sang hệ nhị phân và cần được chuyển lại sang cơ số 16 và phải được viết in hoa nên ta tìm được kết quả như sau:

	+ username: B00B

	+ password: FEED

### Level 9:

- **URL:** https://www.hackthis.co.uk/levels/main/9

- **Description:**

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Main/image/9.1.png"/></p>

- **Solution:** 

	+ Dựa vào gợi ý và view source cho biết có thể đăng nhập theo 1 cách khác để tìm mật khẩu thay thế: https://www.hackthis.co.uk/levels/main/9?forgot

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Main/image/9-1.png"/></p>

Tại đây giá trị cần điền là email thay vì username và password. 

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Main/image/9.png"/></p>

Giá trị của email mà họ cung cấp là: `admin@hackthis.co.uk`. Nhưng theo gợi ý để lấy lại mật khẩu thì cần nhập email của người dùng, vậy cần edit lại source code và thay đổi giá trị email ban đầu thành email nào khác bất kì.

### Level 10

- **URL:** https://www.hackthis.co.uk/levels/main/10

- **Description:**

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Main/image/10.1.png"/></p>

- **Solution:**

	+ View source

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Main/image/9.png"/></p>

Ta thấy giá trị cần tìm được cất trong link: https://www.hackthis.co.uk/levels/extras/level10pass.txt. Ta có kết quả hiển thị như sau:

`69bfe1e6e44821df7f8a0927bd7e61ef208fdb25deaa4353450bc3fb904abd52:f1abe1b083d12d181ae136cfc75b8d18a8ecb43ac4e9d1a36d6a9c75b6016b61`

Đây là 1 dãy đã được mã hóa bằng MD5, sử dụng https://md5hashing.net/hash/sha256 để tìm ra kết quả.

### Tài liệu tham khảo:

