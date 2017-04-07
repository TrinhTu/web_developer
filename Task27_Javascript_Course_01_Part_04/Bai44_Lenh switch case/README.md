## BÀI 44: LỆNH SWITCH CASE TRONG JAVASCRIPT

> Tài liệu: Lệnh Switch case trong Javascript
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 07/04/2017

### Mục lục: 

- [1. Lệnh switch case trong Javascript](#1)

- [2. Ví dụ lệnh switch case trong javascript](#2)

	+ [2.1 Trường hợp không có default](#2.1)

	+ [2.2 Trường hợp không có break](#2.2)

	+ [2.3 Trường hợp gom nhóm case](#2.3)

- [Tài liệu tham khảo](#3)

***

<a name="1"></a>
### 1. Lệnh switch case trong Javascript:

- Lệnh **switch case** dùng để rẽ nhánh chương trình, ứng với mỗi nhánh sẽ có 1 điều kiện cụ thể và điều kiện đó ở dạng so sánh bằng.

**Cú pháp**:

```javascript
switch (variable)
{
    case value_1 : {
        // do some thing
        break;
    }
    case value_2 : {
        // do some thing
        break;
    }
    default : {
        // do something
    }
}
```

- Nếu trong **cases** không có `case` nào phù hợp thì nó sẽ chạy lệnh ở `default`, nếu có case nào phù hợp rồi thì lệnh `break` sẽ thoát khỏi lệnh `switch`, còn nếu không thêm lệnh `break` thì sẽ tiếp tục kiểm tra ở `case` tiếp theo.

- Quy trình chạy như sau:

	+ Nếu tham số `variable` có giá trị là `value_1` thì những đoạn code nằm bên trong sẽ được thực hiện, còn ngược lại thì nó sẽ nhảy xuống case tiếp theo.

	+ Lúc này nếu `variable` có giá trị là `value_2` thì những đoạn code dòng 2 sẽ được thực hiện, ngược lại nó sẽ kiểm tra tiếp xem còn `case` nào không

	+ Nếu không còn `case` nào nữa thì nó sẽ kiểm tra có lệnh default không, nếu có lệnh default thì nó sẽ chạy đoạn code trong lệnh default rồi thoát khỏi `switch case`.

**Ví dụ:** Viết chương trình cho người dùng nhập vào 1 số, kiểm tra số đó chẵn hay lẻ. 

Kết hợp lệnh prompt() để lấy thông tin từ người dùng, kết hợp lệnh 	`switch case` để hiển thị kết quả, sử dụng hàm `parseInt()` để chuyển dữ liệu người dùng nhập sang Number.

```javascript
var number = parseInt(prompt("Nhập số cần kiểm tra"));
 
var mod = (number % 2);
 
switch (mod)
{
    case 0 : {
        document.write(number + " là số chẵn");
        break;
    }
    case 1: {
        document.write(number + " là số lẽ");
        break;
    
    default : {
        document.write("Ký tự bạn nhập không phải số");
    }
}
```
<a name="2"><
### 2. Ví dụ lệnh switch case trong Javascript:

Đề: Viết chương trình cho người dùng nhập vào 1 màu để kiểm tra màu đó có phải màu đỏ hay màu vàng hay không, nếu không phải thì thông báo cho người dùng biết nhập sai màu.

Các cách giải quyết yêu cầu bài.

<a name="2.1"><
#### 2.1 Trường hợp không có default:

- Trường hợp này nếu nhập 1 màu khác màu đỏ và vàng thì sẽ không hiển thị thông báo.

**Ví dụ**:

```javascript
var color = prompt("Nhập màu cần kiểm tra");
 
switch (color){
    case 'red' : 
        document.write("Bạn nhập màu đỏ, đúng rồi đó");
        break;
    case 'yellow' : 
        document.write("Bạn nhập màu vàng, đúng rồi đó");
        break;    
}
```

<a name="2.2"></a>
#### 2.2 Trường hợp không có break:

- Trường hợp này nếu nhập vào màu đỏ thì chương trình sẽ in ra cả lệnh ở case màu vàng phía dưới, bởi trong case màu đỏ không sử dụng lệnh break để thoát khỏi lệnh switch nên nó sẽ chạy thẳng xuống case phía dưới mà không kiểm tra điều kiện.

**Ví dụ:**

```javascript
var color = prompt("Nhập màu cần kiểm tra");
 
switch (color){
    case 'red' : 
        document.write("Bạn nhập màu đỏ, đúng rồi đó");
    case 'yellow' : 
        document.write("Bạn nhập màu vàng, đúng rồi đó");
        break;  
    default :
        document.write("Màu bạn nhập không có trong hệ thống");
}
```

<a name="2.3"></a>
#### 2.3 Trường hợp gom nhóm case:

- Nếu người dùng nhập vào màu đỏ, vàng và xanh thì đều có thông báo nhập đúng --> gom 3 trường hợp đó thành 1 

```javascript
var color = prompt("Nhập màu cần kiểm tra");
 
switch (color){
    case 'red' : 
    case 'yellow' : 
    case 'blue' : 
        document.write("Bạn nhập màu " + color + ", đúng rồi đó");
        break; 
    default :
        document.write("Màu bạn nhập không có trong hệ thống");
}
```
<a name="3"></a>
### Tài liệu tham khảo:

> [1] Lệnh switch case trong javascript. https://freetuts.net/lenh-switch-case-trong-javascript-402.html