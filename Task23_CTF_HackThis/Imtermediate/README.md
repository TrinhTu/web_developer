## HackThis: INTERMEDIATE

> **Category:** Intermediate
>
> **Points:** 
>
> **URL:** http://www.hackthis.co.uk/levels/intermediate

## Write-up

### Level 1:

- **URL**: https://www.hackthis.co.uk/levels/intermediate/1

- **Desciption**:

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Imtermediate/image/1.png"/></p>

- **Solution**:

	- Vì sử dụng phương thức GET thì dữ liệu sẽ hiển thị trên URL nên ta thêm trên URL nội dung như sau: `https://www.hackthis.co.uk/levels/intermediate/1?password=flubergump`

### Level 2: 

- **URL**: https://www.hackthis.co.uk/levels/intermediate/2

- **Desciption**:

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Imtermediate/image/2.png"/></p>

- **Solution**:

	+ Cài đặt Hackbar cho Firefox: https://addons.mozilla.org/En-us/firefox/addon/hackbar/

	+ Sử dụng công cụ đó gởi nội dung bằng phương thức POST:

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Imtermediate/image/2-1.png"/></p>

### Level 3:

- **URL**: https://www.hackthis.co.uk/levels/intermediate/3

- **Desciption**:

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Imtermediate/image/3.png"/></p>

- **Solution:**

	- Dùng Tampter Data ta thấy nội dung `restricted_login=false` thử thay đổi thành giá trị `true` ta được kết quả đúng.

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Imtermediate/image/3-1.png"/></p>

