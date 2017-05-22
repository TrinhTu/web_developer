## Natas

> Category: Level5-Level6
>
> Point:
>
> URL: http://overthewire.org/wargames/natas/

### Write-up

- **URL**: http://natas6.natas.labs.overthewire.org/

- **Description**: 

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task31_CTF_OverTheWire_Natas/image/11.png"/></p>

- **Solution**:

	+ Khi kiểm tra source code ta tìm được 1 link tới tập tin `index-source.html`. Truy cập vào url: http://natas6.natas.labs.overthewire.org/index-source.html tìm được 1 đoạn code có nội dung sau:

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task31_CTF_OverTheWire_Natas/image/12.png"/></p>

- Có nghĩa là khi truy cập vào đường dẫn `includes/secret.inc` thì sẽ tìm thấy nội dung `secret`. Thực hiện việc truy cập vào http://natas6.natas.labs.overthewire.org/includes/secret.inc, view source code và kết quả là: 

```
<?
$secret = "FOEIUWGHFEEUHOFUOIU";
?>
```

- Kết quả trả về:

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task31_CTF_OverTheWire_Natas/image/13.png"/></p>