##一、字体属性
<br>
####(一)、字体属性(样式、粗细、字号、字体名称) 
- 1、**规定文字样式的属性,font-style**<br>格式:

``` 
// 正常样式,默认就是这种 ,快捷键 fsn
  font-style: normal;  
// 倾斜样式, 快捷键 fs 
  font-style: italic;   
```



- 2、**规定文字粗细的属性,font-weight**<br>格式:

  ```
  // 有2种取值,数字(100~900)和单词
  // 快捷键 fwb
  font-weight:bold;

  ```
  
  
  
- 3、**规定文字大小的属性,font-size**<br>格式:
```
// 快捷键: fz30
font-size:30px;
```
**注意:**<br> 通过font-size设置字体,数值后面必须要加px




- 4、**规定文字字体的属性,font-family**<br>格式:
```
// 快捷键,ff
font-family:"楷体";
```
**注意:**<br>(1)、如果取值是中文，需要双引号或者单引号括起来.<br>(2)、设置的字体必须是用户电脑里面已经安装的字体。


 

<br>

####(二)、字体名称属性补充
- 1、**如果设置的字体不存在,系统会默认采用宋体显示,如果设置的字体不存在,而我们又不想用默认的字体显示怎么办?**
```
font-family="可能不存在字体","备选字体1", "备选字体2",...;
```

- 2、**如果想给中文和英文分别单独设置字体怎么办?**<br>**注意:**<br>(1)、但凡是中文字体，里面都包含了英文。<br>(2)、但凡是英文字体，里面都没有包含中文.<br>(3)、也就是说中文字体可以处理英文,英文字体不能处理中文,<br><br>**解决方案:**
```
// 先设置英文的字体, 在设置中文的字体(即先设置部分有的字体,在设置全部有的字体)
font-family:"英文字体","中文字体";
```
<br>**补充:**<br>在企业开发中最常用的字体有一下几个.<br>(1)、**中文：**宋体(SimSun)、黑体(SimHei)、微软雅黑(Microsoft YaHei)。<br>(2)、**英文:** "Time New Roman”、”Arial“<br>还有一点,并不是名称是英文的都是英文,中文也有英文名字.

 
<br>

####(三)、一次性设置 样式、粗细、大小、字体名称属性

```
font-style: italic;
font-weight:bold;
font-size:30px;
font-familay:"宋体";
```
可以简写成下面这样:<br>**格式:**
`font: style weight size family;`<br>具体如下:
```
font:italic bold 30px "宋体";
// 注意:属性之间使用空格分割
```
**注意:**<br>(1)、在这种缩写格式中有的属性可以省略，（style 属性可以省略、weight 属性可以省略）有的不能省略.<br>
(2)、在这种缩写格式中style 和 weight 的位置可以交换,size 和 family 的位置必须在style 和 weight 之后且size必须在family 前 .
<br>(3)、在这种属性中有的属性值不能省略（size 和 family 不能省略）否则其他的属性也不能生效



***
***
<br><br><br>

##二、文本装饰属性

- 1、**文本装饰属性,text-decoration**<br>**格式:**
```
text-decoration:underline;
```
**取值:** 
<br>underline: 下划线
<br> line-through: 中划线
<br>overline:上划线
<br>**none:什么都没有,默认就是这个属性(作用老大了,比如去除a标签的下划线)**

<br>
- 2、**文本水平对齐属性,text-align**<br>**格式**:
```
text-aligh:left;
```
**取值:** 
<br>left 左对齐 
<br>right 右对齐 
<br>right 右对齐


- 3、**文本缩进的属性,text-indent**<br>**格式:**
```
text-indent:2em;
或者
text-indent:10px;
```
**取值**<br>
2em,其中em表示一个文字的宽度,当然也可以使用像素,eg:10px



***
***
<br><br>
##三、字体颜色属性

- 1、**字体颜色的属性，color**<br>**格式**
```
color:red;
color:rgb(255,0,0);
color:rgba(255,0,0,1);  //注意 alpha 的取值是 0~1 
color:#FF0000;
color:#F00;
```






 













