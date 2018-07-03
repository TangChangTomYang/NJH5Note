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


