##Bài 20: ĐỐI TƯỢNG THIS TRONG JAVASCRIPT

>Tài liệu: Đối tượng this trong javascript
>
>Người thực hiện: Lê Tú Trinh
>
>Cập nhập lần cuối: 04/12/2016

### Mục lục:

[1. This trong javascript](#1)

###Nội dung:

<a name="1"></a>
####1. This trong javascript:

Đối tượng `This` chính là đối tượng hiện tại đang được sử dụng hoặc đang truy cập tới.

Ví dụ: Truyền đối tượng this trong HTML:

```javascript
<script language="javascript">
    function show_type(obj)
    {
        alert(obj.type);
    }
</script>
<input type="button" onclick="show_type(this)" value="Check" />
```

![1](https://github.com/TrinhTu/web_developer/blob/master/Task15_Javascript_Course_01_Part_02/Bai_20_This/1.png)

