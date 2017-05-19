## Natas

> Category: Level2-Level3
>
> Point:
>
> URL: http://overthewire.org/wargames/natas/

### Write-up

- **URL**: http://natas3.natas.labs.overthewire.org/

- **Description**: 

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task31_CTF_OverTheWire_Natas/image/3.png"/></p>

- **Solution**:

	+ View-source, tại đây có dòng thông báo: `No more information leaks!! Not even Google will find it this time` 

	+ Có thể thông tin đã được tập tin `robots.txt` chặn, link đến http://natas3.natas.labs.overthewire.org/robots.txt

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task31_CTF_OverTheWire_Natas/image/5.png"/></p>

- Truy cập tới http://natas3.natas.labs.overthewire.org/s3cr3t/ tìm được tập tin users.txt trong đó chứa **natas4:Z9tkRkWmpt9Qr7XrR5jWRkgOU901swEZ**