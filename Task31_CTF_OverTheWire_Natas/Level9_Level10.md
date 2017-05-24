## Natas

> Category: Level9-Level10
>
> Point:
>
> URL: http://overthewire.org/wargames/natas/

### Write-up

- **URL**: http://natas10.natas.labs.overthewire.org/

- **Description**: 

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task31_CTF_OverTheWire_Natas/image/20.png"/></p>

- **Solution**:

	+ Trong source code ta có:

```javascript
<?
$key = "";

if(array_key_exists("needle", $_REQUEST)) {
    $key = $_REQUEST["needle"];
}

if($key != "") {
    if(preg_match('/[;|&]/',$key)) {
        print "Input contains an illegal character!";
    } else {
        passthru("grep -i $key dictionary.txt");
    }
}
?>
```

- Đã có 1 số kí tự đã bị filter vì lí do bảo mật, vậy nên không thể tìm mật khẩu theo level9. Sẽ có thông báo như sau: `Input contains an illeqal character!`. Các kí tự `; & ` đã bị filter.

- Trong biểu thức chính quy, dấu chấm `.` thay cho 1 kí tự kết hợp với dấu sao -> `.*` thay thế cho bất kì chuỗi kí tự nào.

`.* /etc/natas_webpass/natas11`

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task31_CTF_OverTheWire_Natas/image/21.png"/></p>