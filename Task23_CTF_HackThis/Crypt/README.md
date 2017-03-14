## HackThis: Crypt

> **Category:** Crypt
>
> **Points:** 
>
> **URL:** http://www.hackthis.co.uk/levels/crypt
## Write-up

### Level 1:

- **URL**: https://www.hackthis.co.uk/levels/crypt/1

- **Desciption**:

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Crypt/image/1.png"/></p>

- **Solution:**

Đoạn văn trên đã được mã hóa theo kiểu dịch ngược. Sử dụng hàm:

```javascript
function reverse(s){
    return s.split("").reverse().join("");
}
```

- Áp dụng cho bài trên:

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Crypt/image/1.1.png"/></p>

`pass= woocrypt`

### Level 2:

- **URL**: https://www.hackthis.co.uk/levels/crypt/2

- **Desciption**:

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Crypt/image/2.png"/></p>
- **Solution:**

Trong đoạn văn trên, trước dấu 2 chấm ta có thể đoán đó là chữ `pass`, tra bảng mã ASCII ta tìm ra quy tắc sau: `teww` --> `pass` lùi 5

Sử dụng Tool sau: http://rumkin.com/tools/cipher/caesar.php để tìm ra đáp án

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Crypt/image/2.1.png"/></p>

Vậy `pass=shiftthatletter`

### Level 2:

- **URL**: https://www.hackthis.co.uk/levels/crypt/3

- **Desciption**:

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Crypt/image/3.png"/></p>
- **Solution:**

Xem các gợi ý thấy được đoạn văn bản trên được mã hóa theo kiểu Morse:

Sử dụng Tool: http://rumkin.com/tools/cipher/morse.php để tìm ra kết quả:

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task23_CTF_HackThis/Crypt/image/3.1.png"/></p>

Vậy `pass=thankyousir`