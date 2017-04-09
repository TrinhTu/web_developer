
## Bài 2: Cú pháp và cách viết CSS

> Tài liệu: Cú pháp và cách viết CSS
>
> Người thực hiện: Lê Tú Trinh
>
> Cập nhập lần cuối: 14/11/2016

### Mục lục:

[1. Cú pháp CSS](#1)

[2. Nơi viết CSS](#2)

### Nội dung:

<a name="1"></a>
#### 1. Cú pháp CSS:

Cú pháp viết CSS như sau, ví dụ:

```
	h1 {
	background: blue;
	color: pink;
	}
```

Trong đó:

- `h1` là đối tượng HTML được áp dụng CSS

- `background`, `color` là các thuộc tính bên trong dùng để tạo style trong các đối tượng trên

<a name="2"></a>
#### 2. Nơi viết CSS:

ó 3 cách viết CSS đó là:

- **Inline** : viết trực tiếp trên thẻ thông qua thuộc tính `style`

- **external**: viết riêng 1 thẻ khác với phần đuôi .css sau đó thêm vào bằng thẻ link

- **internal**: viết tại file HTML hiện tại, nằm trong thẻ link

Ví dụ về **Inline**:

```
<div style="background: pink; color: green"> Task10_CSS_Course_02</div>
```
Ví dụ về **external**: Viết CSS trong cặp thẻ `<style>`

```
<style type="text/css">
	div {
		background: pink;
		color: green;
	}
</style>
<div>Task10_CSS_Course_02</div>
```

Ví dụ về **external**:

Tạo 1 file mới lưu lại với đuôi `.css` sau đó viết CSS vào trong file này rồi dùng thẻ link thêm file này vào trong tài liệu HTML.

- Tạo file mới và viết CSS vào như sau:

```
div{
	background: pink;
	color: green; 
}
``` 
- Lưu lại và chèn file này vào trong tài liệu HTML bằng thẻ link như sau:

```
<link href="style.css" rel="stylesheet"/>
<div>Task10_CSS_Course_01</div>
```
Trong đó thẻ `href` là đường dẫn tới file muốn add vào, còn `rel=stylesheet` cho trình duyệt biết được đây là file CSS.

Đối với 3 kiểu trên ta đều thu được kết quả như sau:

![anh](http://i.imgur.com/NOTvEO7.png)

Trong 3 cách trên ta nên sử dụng **external** để có thể tách biệt 2 tài liệu ra, dễ dàng kiểm soát và sửa chữa đối với những lab phức tạp hơn.


