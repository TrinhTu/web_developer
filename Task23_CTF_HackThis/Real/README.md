## HackThis: Real

> **Category:** Crypt
>
> **Points:** 
>
> **URL:** http://www.hackthis.co.uk/levels/real
## Write-up

### Level 1:

- **URL**: https://www.hackthis.co.uk/levels/real/1

- **Desciption**:

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Real/image/1.png"/></p>

- **Solution:**

	+ Click vào **email**

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Real/image/1.1.png"/></p>

Vào thư mục `Trash(1)` ta tìm được Password= `imagod`

Kế tiếp vào thư mục `input` sẽ hiển thị đường dẫn đăng nhập, tại đây ta nhập mật khẩu vừa tìm được và submit.

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Real/image/1.2.png"/></p>

### Level 2:

- **URL**: https://www.hackthis.co.uk/levels/real/2

- **Desciption**:

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Real/image/2.png"/></p>

- **Solution:**

Sau khi tiến hành login, tìm được thông tin sau:

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Real/image/2.1.png"/></p>

Điểm cần lưu ý ở đây: `URL= "members/" + username + " " + password + ".htm";`

Thêm vào URL `/members` thì URL sẽ thành như sau: https://www.hackthis.co.uk/levels/extras/real/2/members/

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Real/image/2.2.png"/></p>

Sau khi thử lần lượt các kết quả tìm được `username= librarian` và `pass= sweetlittlebooks`