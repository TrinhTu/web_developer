## BÀI 08: VÒNG LẶP WHILE VÀ DO WHILE TRONG PHP

> Tài liệu: Vòng lặp while và do while trong php
> 
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 24/05/2017

### Mục lục:

[1. Cấu trúc vòng lặp while](#1)

[2. Cấu trúc vòng lặp do while](#2)

[3. Một bài toán có thể giải ở cả 3 vòng lặp không](#3)

[4. Vòng lặp while, do while lồng nhau](#4)

[5. Vòng lặp while, do while trong việc truy xuất mảng](#5)

[Tài liệu tham khảo](#6)

***

<a name="1"></a>
### 1. Cấu trúc vòng lặp while:

- Cú pháp:

```
while ($condition){
	// dòng lệnh
}
```

- $condition: là điều kiện dừng vòng lặp, nếu $condition có giá trị false thì vòng lặp dừng, ngược lặp vòng lặp sẽ tiếp tục lặp. Vòng lặp while sẽ lặp vô hạn nếu biểu thức điều kiện truyền vào luôn đúng

- Ví dụ: liệt kê các số từ 1 tới 10

```javascript
for ($i = 1 ; $i <= 10 ; $i++){
	echo $i. '-';  //xuất ra màn hình biến $i và kí tự `-`
}
```

```javascript
$i = 1; // Biến dùng để lặp
while ($i <= 10){ // Nếu $i <= 10 thì mới lặp
    echo $i . ' - '; // Xuất ra màn hình biens $i và kí tự `-`
    $i++; // Tăng biến $i lên 1
}
```

<a name="2"></a>
### 2. Cấu trúc vòng lặp do while:

- Đối với vòng lặp while sẽ kiểm tra điều kiện trước khi lặp còn vòng lawoj do while thì sẽ thực hiện câu lệnh trước rồi mới kiểm tra điều kiện, nếu điều kiện đúng thì sẽ thực hiện tiếp vòng lặp kế tiếp, nếu điều kiện sai sẽ dừng vòng lặp. Vòng lặp do while luôn luôn thực hiện ít nhất 1 lần lặp.

- Cú pháp

```
do {
	//dòng lệnh
} while ($condition);
```


- Ví dụ:

```javascript
$i = 1;
do{
    echo $i;
    $i++;
}while ($i <= 10);
```

<a name="3"></a>
### 3. Một số bài toán có thể giải ở cả 3 vòng lặp không

- Tùy theo từng bài. Ví dụ: In ra màn hình các số từ 100 -> 200

- Dùng vòng lặp for:

```javascript
for($i = 100 ; $i <= 200; $i++){
	echo $i. '-';
}
```

- Dùng vòng lặp while:

```javascript
$i = 100;
while($i <=200){
	echo $i. '-';
	$i++;  //tăng $i lên 1
}
```

- Vòng lặp do while

```javascript
$1 = 100;
do{
	echo $i. '-';
	$i++;
} while($i <= 200);
```

<a name="4"></a>
### 4. Vòng lặp while, do while lồng nhau:

- Cũng giống như vòng lặp for và mệnh đề if, vòng lặp while và do while có thể lồng nhau.

- Ví dụ:

```javascript
$i = 1;
while ($i < 10)
{
    $j = $i;
    while ($j < 10)
    {
        echo $j;
        $j++;
    }
    echo '
';
    $i++;
}
```

<a name="5"></a>
### 5. Vòng lặp while, do while trong việc truy xuất mảng:

- Tương tự vòng lặp for, vòng lặp while và do while có thể dùng để truy xuất các phần tử trong mảng chỉ mục.

- Ví dụ:

```javascript
// Cho Danh Sách Năm
$nam = array(
    1990,
    1991,
    1992,
    1993,
    1994,
    1995
);
  
// Xuất theo cách thông thường
echo $nam[0];
echo $nam[1];
echo $nam[2];
echo $nam[3];
echo $nam[4];
echo $nam[5];
  
// Dùng while
$i = 0;
while ($i <= 5){
    echo $nam[$i];
    $i++; // Tăng biến $i
}
  
// Dùng do .. while
$i = 0;
do {
    echo $nam[$i];
    $i++;
}while ($i <=5);
```

<a name="6"></a>
### Tài liệu tham khảo:

> [1] Vòng lặp while và do while trong php. https://freetuts.net/vong-lap-while-va-do-while-trong-php-8.html