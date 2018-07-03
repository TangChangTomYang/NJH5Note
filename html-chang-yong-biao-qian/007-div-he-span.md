####一、什么是div?

- **div 的作用:**<br> **一般用于配合CSS 完成网页的布局**,网页一般分为3个部分,如下图: 

![](/assets/Snip20180703_1.png)

```
 .head{
    width: 980px;
    height: 100px;
    background: red;
    margin: auto;
}

.content{
    width: 980px;
    height: 500px;
    background: green;
    margin: auto;
}

.footer{
    width: 980px;
    height: 100px;
    background: orange;
    margin: auto;
}

<div class="head"></div>
<div class="content"></div>
<div class="footer"></div>

```
<br> <br>

####二、什么是span?

- **一般用于配合CSS 完成网页中一些局部的信息,如下:**

![](/assets/Snip20180703_3.png)

```
p{
    color: blue;
}

span{
    color: red;
}

<p>努力到 <span>无能为力</span> ,拼搏 <span>到感动自己</span> </p>
```


<br> <br>
####三、div  和 span 有什么区别?

- 1、**div 会单独占一行,而span 不会单独占一行**
- 2、**div 是一个容器级别的标签,span 是一个文本级别的标签** 这是最重要的


<br> <br>
####四、容器级的标签和文本级的标签的主要区别?

- 1、**容器级别的标签可以嵌套 其它所有的标签**
- 2、**文本级的标签只能嵌套 文字 超链接 图片**

<br>**容器级别的标签主要有:**<br> **div h ul ol dl li ...** <br> **span p buis strong em ins del **


**注意:**<br>**那些标签是文本级别的,那些我标签是容器级别的,我们不用刻意去记忆,在企业开发中一般嵌套都是嵌套在div中,或者按照组标签来嵌套**

