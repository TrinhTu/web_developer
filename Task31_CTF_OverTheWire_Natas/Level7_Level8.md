## Natas

> Category: Level7-Level8
>
> Point:
>
> URL: http://overthewire.org/wargames/natas/

### Write-up

- **URL**: http://natas8.natas.labs.overthewire.org/

- **Description**: 

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task31_CTF_OverTheWire_Natas/image/11.png"/></p>

- **Solution**:

	+ Tương tự như ở level6, ở source code ta tìm được 1 đường dẫn tới tập tin `index-source.html`: http://natas8.natas.labs.overthewire.org/index-source.html

	+ Tại đây nội dung chính là đoạn code:

```javascript
<?

$encodedSecret = "3d3d516343746d4d6d6c315669563362";

function encodeSecret($secret) {
    return bin2hex(strrev(base64_encode($secret)));
}

if(array_key_exists("submit", $_POST)) {
    if(encodeSecret($_POST['secret']) == $encodedSecret) {
    print "Access granted. The password for natas9 is <censored>";
    } else {
    print "Wrong secret";
    }
}
?>
```

- Phân tích thì nếu `encodeSecret($_POST['secret']) == $encodedSecret`

- Mặc khác `$encodeSecret` đã được mã hóa bởi `bin2hex(strrev(base64_encode($secret)))`

- Đầu tiên chuỗi `3d3d516343746d4d6d6c315669563362` đã được mã hóa **base64_encode**, tiếp đó đem dịch ngược **strrev**, cuối cùng là mã hóa **bin2hex**, vậy để tìm ra giá trị cuối cùng của chuỗi ta tiến hành như sau:

	+ decode **bin2hex** là **hex2bin**, sử dụng http://www.onlinefunc.com/php/hex2bin để decode, ta tìm được chuỗi **==QcCtmMml1ViV3b**

	+ Tiếp theo dùng tool https://www.tools4noobs.com/online_php_functions/strrev/ tìm chuỗi reverse của chuỗi trên ta được 1 chuỗi mới **b3ViV1lmMmtCcQ==**

	+ Cuối cùng sử dụng https://www.tools4noobs.com/online_php_functions/base64_decode/ để decode base64 chuỗi vừa tìm được ta được kết quả cuối cùng: **oubWYf2kBq**

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task31_CTF_OverTheWire_Natas/image/16.png"/></p>

- Vậy password là **W0mMhUcRRnG8dcghE4qvk3JA9lGt8nDl**