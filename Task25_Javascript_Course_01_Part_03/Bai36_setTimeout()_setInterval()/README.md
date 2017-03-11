## Bài 36: setTimeout() và setInterval() trong Javascript

> Tài liệu: setTimeout() và setInterval() trong Javascript
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 11/03/2017

## Mục lục:

- [1. Hàm setTimeout() trong Javascript](#1)

	- [1.1 Hàm clearTimeout() trong Javascript](#1.1)

- [2. Hàm setInterval() trong Javascript](#2)

	- [2.1 Hàm clearInterval() trong Javascript](#2.1)

- [Tài liệu tham khảo](#3)

***

<a name="1"></a>
### 1. Hàm setTimeout() trong Javascript:

Hàm `setTimeout()` dùng để thiết lập một khoảng thời gian nào đó sẽ thực hiện vụ nào đó và chỉ thực hiện đúng 1 lần.

**Cú pháp:** `setTimeout(function, time)`

**Trong đó:**

- `function`: là nội dung cần thực hiện, đây là 1 hàm

- `time` là khoảng thời gian bao nhiêu (tính bằng mili giây) thì function đó sẽ thực hiện.

**Ví dụ:** thiết lập thời gian sau 3 giây sẽ xuất hiện câu chào:

```javascript
setTimeout(function(){
    alert("Chào mừng bạn đến với freetuts.net");
}, 3000);
```

Ngoài ra còn có thể viết như sau:

```javascript
var do_alert = function(){
    alert("Chào các bạn");
};
setTimeout(do_alert, 3000);
```

<a name="1.1"></a>
#### 1.1 Hàm clearTimeout() trong Javascript:

Để hủy bỏ 1 chương trình nào đó đã được thiết lập trước đó sử dụng hàm `clearTimeout()`. Tham số truyền vào hàm `clearTimeout()` là đối tượng `setTimeout()` nên phải đặt hàm `setTimeout()` vào 1 biến cụ thể.

```javascript
//hành động
var action = setTimeout(function(){
	//something
}, 3000);
///hủy hành động
clearTimeout(action);
```

**Ví dụ:**

```javascript
<script language="javascript">
    var do_alert = setTimeout(function(){
    	alert("Chào các bạn");
    }, 3000);
          
    function clearAlert()
    {
        clearTimeout(do_alert);
    }
</script>
<input type="button" onclick="clearAlert()" value="Clear" />
```

<a name="2"></a>
### 2. Hàm setInterval() trong Javascript:

Hàm `setInterval()` có cú pháp và chức năng giống với hàm `setTimeout()` tuy nhiên với hàm `setInterval()` thì số lần thực hiện là mãi mãi.

**Ví dụ:** Cứ sau 3 giây sẽ xuất hiện câu chào 1 lần

```javascript
setInterval(function(){
	alert("Chào các bạn");
}, 3000);
```

<a name="2.1"></a>
#### 2.1 Hàm clearInterval() trong Javascript:

Tương tự như hàm `clearTimeout()` thì hàm `clearInterval()` sẽ xóa đi nhiệm vụ đã được thiết lập trong hàm `setInterval()`,và phải đặt hàm vào trong 1 biến.

**Ví dụ:** Sử dụng hàm `setInterval()` để xuất ra câu chào và chỉ xuất hiện 1 lần.

```javascript
var interval_obj = setInterval(function(){
	alert("Chào các bạn");
	clearInterval(interval_obj);
}, 3000);
```

Trong ví dụ trên thì câu chào chỉ xuất hiện 1 lần và ngay lập tức sẽ xóa. 

<a nam="3"></a>
### Tài liệu tham khảo:

> [1] setTimeout và setinterval trong Javascript. http://freetuts.net/settimeout-va-setinterval-trong-javascript-391.html