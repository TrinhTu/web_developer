## Bài 27: Lệnh break-continue trong Javascript

> Tài liệu: LỆNH `break-continue` TRONG JAVASCRIPT
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 06/03/2017

## Mục lục:

[1. Lệnh break trong Javascript](#1)

[2. Lệnh continue trong Javascript](#2)

[Tài liệu tham khảo](#3)

***

<a name="1"></a>
### 1. Lệnh Break trong Javascript:

Lệnh break có tác dụng là dừng vòng lặp thoát khỏi vòng lặp mặc dù nội dung của vòng lặp vẫn đang đúng, không quan tâm đến điều kiện lặp. Lệnh break sử dụng cho mọi vòng lặp như: for, while, và do while,...

**Ví dụ 1**: 

```javascript
for (var i = 1; i <= 10; i++)
{
	document.write(i+ "-");
	if (i==5){
		document.write("Vòng lặp bị dừng");
		break;
	}
}
```

<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task25_Javascript_Course_01_Part_03/Bai27_Lenh_break_continue/image/1.png"/></p>

**Ví dụ 2:**Vòng lặp while bị nhảy ra khỏi vòng lặp khi biến `i` chia hết cho 9

```javascript
var i = 1;
while (i <= 1000)
{
	document.write(i + "-");
	if (i % 9 == 0) {
		document.write("Vòng lặp bị dừng");
		break;
	}
	i++;
}
```
<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task25_Javascript_Course_01_Part_03/Bai27_Lenh_break_continue/image/2.png"/></p>

<a name="2"></a>
### 2. Lệnh continue trong Javascript:

Lệnh này dùng để bỏ qua 1 bước lặp nào đó, tức là lúc gặp lệnh continue thì tất cả đoạn code bên dưới sẽ không được thực hiện, nó sẽ chuyển sang 1 vòng lặp mới.

**Ví dụ 1:** Vòng lặp for bỏ qua đoạn code in ra giá trị 5

```javascript
for (var i = 1; i <= 10; i ++)
{
	if (i == 5) {
		continue;
	}
	document.write(i + "-");
}
```
<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task25_Javascript_Course_01_Part_03/Bai27_Lenh_break_continue/image/3.png"/></p>

**Ví dụ 2:** Vòng lặp while bỏ qua bước lặp nếu `i`chia hết cho 9

```javascript
var i = 1;
 
while (i <= 100)
{
    if (i % 9 == 0) {
        i++;
        continue;
    }
 
    document.write(i + " - ");
    i++;
}
```
<p align="center"><img src="https://github.com/TrinhTu/web_developer/blob/master/Task25_Javascript_Course_01_Part_03/Bai27_Lenh_break_continue/image/4.png"/></p>

### Tài liệu tham khảo:

> [1] Lệnh break-continue trong javascript.http://freetuts.net/lenh-break-continue-trong-javascript-382.html