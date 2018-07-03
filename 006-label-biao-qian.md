##Label 标签
- 默认情况下文字和输入框是没有关联关系的,也就是说,点击文字输入框不会聚焦,如果想点击文字时让对应的输入框聚焦,那么就需要让文字和输入框进行绑定
- 想要输入框和文字绑定在一起,那么就可以使用label标签
- 绑定的格式:
    - 将需要和输入框绑定的文字使用label标签包裹起来
    - 给输入框添加id属性
    - 在label标签中通过for属性和输入框中的id进行绑定即可

    ```
    <form action="https://baidu.com">
        <label for="usr">账号:</label> <input type="text"      id="usr"><br>
        <label for="pwd">密码:</label> <input type="password"  id="pwd"><br>
    </form>
    ```
    
---
##marquee 标签(跑马灯标签)?

marquee 标签不是W3C 推荐的标签,在W3C 官方文档中也无法查询到这个标签,但是各大浏览器对这个标签的支持非常好.

![](/assets/Snip20180606_8.png)
格式:
```
<html>

    <head>
        <meta charset="utf-8">
        <title>audio 标签</title>

        <style>
            marquee{
                width:  120px;
                height: 120px;
                background: #999999;;                
            }
        </style>
    </head>

    <body>

    <marquee>随便写点东西</marquee>
    <marquee direction="right">随便写点东西</marquee>
    <marquee direction="down">随便写点东西</marquee>
    <marquee direction="up">随便写点东西</marquee>
       <!--scrollamount 属性使用来设置速度的-->
       <!--loop 属性设置速度,默认-1 无限滚动-->
       <marquee scrollamount="100" loop="1">随便写点东西</marquee>
        <!--behavior 设置滚动的模式 =slide 滚到边就听, =alternate 滚到边就反弹 -->
       <marquee behavior="slide">随便写点东西</marquee>
    <marquee behavior="alternate">随便写点东西</marquee>
    </body>

</html>
```    


##HTML 中被废弃的标签
- 1、为什么HTML中有一部分标签会被废弃呢？<br>因为当前的HTML标签中的标签只有一个作用,就是用来添加语义,而早期的HTML标签中有一部分标签是没有语义的,有一部分标签是用来修改样式的,所以这部分标签就被淘汰了,如:
```<br>、<hr>、<font>、
<b>  (bold 缩写)加粗文本,没有任何语义
<u>  (underline)给文本加下滑下,没有任何语义
<i>  (italic) 将文本倾斜,没有任何语义
<s>  (strikethrough) 给文本添加删除线,没有语义
```
在企业开发中,尽量不要使用这些被废弃的标签,上面这几个标签被废弃了,HTML5 新增的几个标签用来代替原来的标签

```
   <!--strong的语义是重要性强的文字-->
    <strong> 代替 原来的 b 标签</strong>
    <!--insert的缩写,定义插入文字的语义-->
    <ins>代替原来的u标签</ins>
    <!--emphasized的缩写,定义强调的文字-->
    <em>代替原来的i标签</em>
    <!--Delete的缩写,定义被删除的文字-->
    <del>代替原来的s标签</del>

```

---

##字符实体
- 在HTML中对空格、回车、tab 不敏感，会把多个空格、回车、tab当做一个空格来处理

- 在HTML中有的字符是被HTML保留的,有的HTML字符在HTML中是有特殊含义的,是不能再浏览器中直接被显示出来的,那么这些东西想要被显示出来就必须通过字符实体.

`&nbsp;` 就是一个字符实体,一个`&nbsp;`就代表一个空格.
`&lt;` (lt 是 less than 的缩写)是一个字符实体.表示的是 <
`&gt;` (gt 是 greate than 的缩写)是一个字符实体.表示的是 >
`&copy` 是版权符号的实体 &copy;
 











 
