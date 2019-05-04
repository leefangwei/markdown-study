
# Basic grammar 基本语法 {#title1}

link <https://www.cnblogs.com/shawWey/p/8931697.html>

Markdown
:   轻量级文本标记语言，可以转换成html，pdf等格式  //  开头一个`:` + `Tab` 或 四个空格

---

+ > title 标题

# h1

## h2

### h3

#### h4

##### h5

###### h6

+ > font 字体

例子**加粗**
例子*斜体*
例子~~删除线~~
例子 `强调`

+ > separator 分割线

三个或者三个以上的 - 或者 * 都可以。

---

+ >quote 引用

> quote1
quote1

>quote2
>>quote2

+ > link 链接

[百度一下](http://www.baidu.com "百度一下")

[百度2][link1]

[link1]: http://www.baidu.com/   "百度二下"

+ > picture 图片

![图片1](./img/01.png '我是一个图片')

![图片2][img1]

[img1]:./img/01.png '我是一个图片'

[![图片1](./img/01.png '百度一下')](http://www.baidu.com "百度一下")

+ > list 列表

无序

+ one
+ two

序列

1. one
2. two

+ > 任务列表 checkbox

+ [ ] item1
+ [x] item2

+ > 定义列表语法

项目１
:   定义 A
:   定义 B

+ > table 表格

|    a    |       b       |      c     |
|:-------:|:------------- | ----------:|
|   居中  |     左对齐     |   右对齐   |
|=========|===============|============|

:|

a  | b | c  
:-:|:- |-:
居中|左对齐|右对齐
============|=================|=============

+ > 脚注

Markdown[^1]

[^1]: Markdown是一种纯文本标记语言        // 在文章最后面显示脚注

+ > 描点

注：只有标题支持锚点， 跳转目录方括号后 保持空格

[标题描点](#title1)

+ > inline making 行内标记

 标记之外`< div>
    < div></div>
    < div></div>
    < div></div>
< /div>`标记之外

+ > code block 代码块

```html
<div>
    <p>this is a line</p>
</div>
```

```C#
var a=1;
var b=2;
if(a>0){
    return(a+b);
}
```

```javascript
var a=1;
var b=2;
if(a>0){
    return(a+b);
}
```

```java
var a=1;
var b=2;
if(a>0){
    return(a+b);
}
```

```python
a=1
b=2
if(a>0):
    return(a+b)
```

+ > 公式

注：1个$左对齐，2个居中

$$ x \href{why-equal.html}{=} y^2 + 1 $$
$ x = {-b \pm \sqrt{b^2-4ac} \over 2a}. $