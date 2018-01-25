# &lt;input&gt;

input标签平时使用的频率非常高，但是对于其他属性并不是很了解，以为是那么回事，到用的时候就发现不是那么回事。

### type

不用说，这个属性肯定要用到。

高频`type`属性值

* **text **——默认。定义一个单行的文本字段（默认宽度为 20 个字符）。
* **button**—— 定义可点击的按钮（通常与 JavaScript 一起使用来启动脚本）。
* **checkbox**——定义复选框。
* **password** ——定义密码字段（字段中的字符会被遮蔽）。
* **radio** ——定义单选按钮。
* **submit **——定义提交按钮。
* **file** ——定义文件选择字段和 "浏览..." 按钮，供文件上传，可以配合accept属性使用。
* email ——定义用于 e-mail 地址的字段。

HTML5新定义

* colorNew定义拾色器。

```html
选择你喜欢的颜色: <input type="color" name="favcolor"><br>
```

value值为颜色的6位十六进制表示法的值

* date ——定义 date 控件（包括年、月、日，不包括时间）,就相当于一个时间插件，功能很强大。
* datetime ——定义 date 和 time 控件（包括年、月、日、时、分、秒、几分之一秒，基于 UTC 时区）。
* datetime-local ——定义 date 和 time 控件（包括年、月、日、时、分、秒、几分之一秒，不带时区）。

```
生日: <input type="date" name="bday">
```

![](/assets/type1.png)  
hidden定义隐藏输入字段。  
image定义图像作为提交按钮。  
monthNew定义 month 和 year 控件（不带时区）。  
numberNew定义用于输入数字的字段。  
  
rangeNew定义用于精确值不重要的输入数字的控件（比如 slider 控件）。  
reset定义重置按钮（重置所有的表单值为默认值）。  
searchNew定义用于输入搜索字符串的文本字段。  
  
telNew定义用于输入电话号码的字段。  
timeNew定义用于输入时间的控件（不带时区）。  
urlNew定义用于输入 URL 的字段。  
weekNew定义 week 和 year 控件（不带时区）。


