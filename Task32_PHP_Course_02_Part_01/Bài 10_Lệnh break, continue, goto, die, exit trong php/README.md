## BÀI 10: LỆNH BREAK, CONTINUE, GOTO, DIE, EXIT TRONG PHP

> Tài liệu: Lệnh break, continue, goto, die, exit trong php
> 
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 25/05/2017

### Mục lục:

[1. Câu lệnh break](#1)

[2. Câu lệnh continue](#2)

[3. Câu lệnh goto](#3)

[4. Lệnh die và exit](#4)

[Tài liệu tham khảo](#5)

***

<a name="1"></a>
### 1. Câu lệnh break:

- Lệnh break thường được dùng để thoát khỏi vòng lặp dù vòng lặp vẫn chưa kết thúc.

- Ví dụ:

```
for ($i = 1; $i <= 100; $i++)
{
    echo $i . ' ';
    if ($i == 20)
    {
        break;
    }
}
```

- Trong ví dụ này thì vòng lặp được lặp từ 1 cho tới 100, nhưng nó không chạy hết 100 lần vì chạy tới lần thứ 20 thì câu lệnh kiểm tra if đúng nên lệnh break bên trong câu lệnh if được thực hiện -> dừng vòng lặp

<a name="2"></a>
### 2. Câu lệnh continue:

- Lệnh này sẽ bỏ qua những đoạn code bên dưới nó và chuyển sang vòng lặp kế tiếp (không thoát khỏi vòng lặp như lệnh break)

```
for ($i = 1; $i <= 10; $i++)
{
    if ($i == 5)
    {
        continue;
    }
    echo $i . ' '; 	// kết quả in ra thiếu số 5
}
```

<a name="3"></a>
### 3. Câu lệnh goto:

- Dùng để nhảy đến 1 dòng code nào đó

```javascript
$a = 12;
$b = 13;
$c = $a + $b;
  
echo $a;
  
goto label_end;
  
echo $b; 	// dòng này không được thực hiện
  
label_end;
```

<a name="4"></a>
### 4. Lệnh die và exit:

- Với lệnh break và continue chỉ ảnh hưởng trong vòng lặp thì lệnh die và exit ảnh hưởng đến cả chương trình, chương trình sẽ được dừng ngay lập tức và những dòng code bên dưới die vad exit sẽ không được thực hiện.

```javascript
echo '123';
  
die(); // hoặc exit();
echo '456';		// không được thực hiện
```

<a name="5"></a>
### Tài liệu tham khảo:

> [1] Lệnh break, continue, goto, die, exit trong php. https://freetuts.net/lenh-break-continue-goto-die-exit-trong-php-10.html