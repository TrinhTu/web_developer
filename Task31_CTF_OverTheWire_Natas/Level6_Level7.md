## Natas

> Category: Level6-Level7
>
> Point:
>
> URL: http://overthewire.org/wargames/natas/

### Write-up

- **URL**: http://natas7.natas.labs.overthewire.org/

- **Description**: 

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task31_CTF_OverTheWire_Natas/image/14.png"/></p>

- **Solution**:

	+ Kiểm trả thông tin trong source code tìm được `<!-- hint: password for webuser natas8 is in /etc/natas_webpass/natas8 -->`

	+ Dựa vào đặc điểm của url: `index.php?page=home`, `index.php?page=about`

	+ Thay thế thông tin phía sau dấu `=` bằng đường dẫn `/etc/natas_webpass/natas8`

	+ Kết quả hiển thị password là: **DBfUBfqQG69KvJvJ1iAbMoIpwSNQ9bWe**

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task31_CTF_OverTheWire_Natas/image/15.png"/></p>