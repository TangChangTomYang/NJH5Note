####一 边框属性 border



- 1 **设置标签的边框**<br><br>(1)**连写:(同时设置4条边的边框)**
```
border: 边框的宽度  边框的样式  边框的颜色
border: 10px solid blue;// 快捷键 bd+
```
(2)**连写:(单独设置一条边的边框)**
```
border-top:  边框的宽度  边框的样式  边框的颜色
border-bottom:  边框的宽度  边框的样式  边框的颜色
border-left:  边框的宽度  边框的样式  边框的颜色
border-right:  边框的宽度  边框的样式  边框的颜色
border-right: 10px solid blue;
```
**快捷键:**
```
bd+
border: 1px solid #  // 粗细 样式 颜色
```
**连写注意点:**<br>** (1)只有样式不能省略**

 ```
  border: 1px solid black  // 粗细 样式 颜色

 等价
 border: 1px solid    // 粗细 样式 
 等价
 border: solid    // 粗细  

 错误写法
 border: 1px  black  // 粗细   颜色

 ```
 
 ---

 <br>
 
 ####二 内边距 Padding
- 1 **什么是内边距(Padding)? <br> 内边距(padding)就是边框(border)和内容(content)之间的距离**<br> <br> 
 **注意:<br>(1) 给标签设置内边距(padding)后,标签占有的宽度和高度会发生变化.<br>(2) 设置padding后 内边距的背景色和标签背景色一样<br> (3) 设置padding后,内边距的背景图设标签的 一样**<br><br>
 ** 总结:
 设置padding 后标签占用的宽高会发生变化,标签的宽高范围内的背景色和背景图不和原来标签一样. 经过测试,其实border 属性也是一样的(当 透明色时)**<br>
 ![](/assets/Snip20180709_1.png)<br>
 **格式:<br>(1) 非连写:**
 ```
 padding-top:5px;
 padding-left:15px;
 padding-bottom:20px;
 padding-right:10px;
 ```
 **(2)连写:**
 ```
 padding: 上 右 下 左;
 比如:
 padding : 10px 20px 30px 40px;
 ```
 **连写的注意点:<br>(1) 省略左边,那么左右是一样的,即:**
 
   ```
   padding: 10px 20px 30px;
   等价于
   padding: 10px 20px 30px 20px;
   ```
 **(2)省略下边 和 左边,那么上下一样,左右一样,即:**
 
   ```
   padding: 10px 20px ;
   等价于
   padding: 10px 20px 10px 20px;
   ```
 **(3)省略 右 下 左,那么4边一样,即:**
 ```
 padding: 10px;
 等价于
 padding: 10px 10px 10px 10px;
 ```



---

<br>
####三 外边距(margin)

- 1 **什么是外边距(margin)?<br> 标签与标签之间的距离就是外边距(margin)**<br><br>
**注意:**<br>
**行内标签之间由于换行符会有一个间距,这个不是外边距 是空格**
![](/assets/Snip20180718_10.png)
**格式:<br> (1) 非连写**
```
margin-top:5px;
margin-left:15px;
margin-bottom:20px;
margin-right:10px;
```
**(2)连写**
```
margin: 上 右 下 左;
比如:
margin : 10px 20px 30px 40px;
```
**注意:**<br>
(1) 外边距(Margin )和内边距(padding)写法和注意点,省略写法也是一样的<br>
(2) **外边距(占用部分)是不会有标签的背景色和背景图的,这是和内边距(padding) 的最主要的区别**


---

<br>
####四 外边距合并现象

- 1 在默认情况下,标签的水平方向上 外边距是会叠加的,但是在垂直方向上,外边距是不会叠加的,谁的外边距大就听谁的(小的外边距被忽略),我们称外边距在垂直方向上的这种不叠加现象叫做,**---外边距合并显现. **
![](/assets/Snip20180709_2.png)

- 2 **什么时候会发生外边距合并现象呢?**<br>
 在垂直方向上有2个相邻的外边距就会发生外边距合并现象,比如:
 ```
 .top{
    margin-bottom:30px;
  }
  
  .bottom{
    margin-top:50px;
  }
  这种情况下,就会出现外边距(margin) 合并现象,谁的大听谁的
  ```
 




---

<br>
####五 CSS 盒子模型



**结论:<br> (1) 在HTML 中所有的标签都可以设置 宽度高度(width height)\ 内边距(padding)\ 边框(border)\ 外边距(margin).**

- **什么是宽度 高度? <br> 指定标签中可以存放内容的区域,就是用宽度和高度来描述**<br>
 ![](/assets/Snip20180709_3.png)

---

<br>
####六 盒子宽度和高度

- 1 **内容的宽度和高度<br>通过width 和 height 给标签设置的宽度和高度,就是标签内容的宽度和高度**
![](/assets/Snip20180709_5.png)

- 2 **元素的宽度和高度<br> 元素的宽的和高度就是指的是元素可以看见的范围,具体可以这样来计算: <br>元素宽度= (border-left) + (padding-left) + (width) + (padding-right) + (border-right) <br> 元素高度= (border-top) + (padding-top) + (height) + (padding-bottom) + (border-bottom)**
![](/assets/Snip20180709_4.png)


- 3 **元素空间的宽度和高度<br>元素空间宽度= (margin-left) + (border-left) + (padding-left) + (width) + (padding-right) + (border-right) + (margin-right) <br> 元素空间高度= (margin-top) + (border-top) + (padding-top) + (height) + (padding-bottom) + (border-bottom) + (margin-bottom)**<br>
![](/assets/Snip20180709_6.png)

---

<br>
#### 七 盒子 box-sizing 属性

- 1 **在 CSS3 中新增了一个 "box-sizing" 属性,这个属性可以保证我们给盒子新增 padding 和 border 之后,盒子元素的宽度 和  元素高度 不变化.(盒子内容的宽高会自动变化)**<br><br>
**注意:**
**仅仅是设置 `padding` 和 `border` 后不变, 设置 `margin` 后会变,如下图:![](/assets/Snip20180709_15.png)**

- 2 ** box-sizing 属性是如何保证 增加 padding 和 border 后,盒子元素的宽高不变的呢?** <br> 
**其实在增加 `padding` 和 `border` 之后想要保证盒子元素的宽高不变,就必须从元素内容的宽高减去增加的宽度和高度**


- 3 **border-sizing的2个取值:<br> (1) 取值 = content-box; 时 元素的宽高 = 边框宽(border) + 内边距(padding) + 内容宽度\高度(width) <br> (2) 取值 = border-box; 时, 元素宽高= 标签的宽度\高度, 元素内容宽高 = 标签的宽度 \ 高度 - 边框(border) - 内边距(padding)**
<br><br>**注意:<br>因为box-sizing 是CSS3新增的,有些浏览器是不支持的(IE6)**


---

<br>
####八 设置一个元素 在另一个元素中居中显示

- **方案1: 设置父标签padding** <br><br>
设置父标签的 padding, 把 子标签 挤到,看起来居中的位置.<br><br>这种方案,为什么可以呢?<br> 
因为设置一个标签的 padding  不会影响原来的背景色和背景图片的显示(这是主要原因 原理)<br><br>
注意点:<br> 
这种方法虽然是推荐的方法,但是要注意到修改了父标签的 padding 会改变父标签的元素尺寸,因此为了达到既又修改了子元素的位置又不影响父标签的布局 增加多少padding 就需要从父标签的 元素内容尺寸中相应的减去


- **方案2: 子标签margin<br>**

 ```
 step1: 
  给父标签设置一个border 属性 (保证父标签不会因为子标签设置了margin后 被一起顶下来)

  step2: 
 设置子标签的  margin-top 和 margin -left 属性
 ```
**注意点:**<br>
(1) 如果两个盒子是嵌套关系,那么设置了里面的一个盒子的 顶部的外边距, 那么外面一个盒子也会被顶下来<br>
(2) 如果外面的盒子不想被一起顶下来,那么可以给外面的标签设置一个边框属性(border)<br> 
![](/assets/Snip20180718_17.png)
(3) **在企业开发中,一般情况下需要控制嵌套关系盒子之间的距离,应该首先考虑 padding ,其次再考虑 margin,margin 一般是用于指定兄弟标签之间的距离,padding 一般是用来设定父子之间的关系的 **<br><br> 
**注意点2:**
(1) 在嵌套关系的盒子中,我们可以利用 margin:0px auto; 的方式来让子标签(子盒子)在父标签(父盒子中水平居中)
![](/assets/Snip20180710_1.png)
(2)**margin:0px auto;只能设置水平居中,没有 margin: auto auto 这样的写法,竖直方向是没有 auto 的概念的(竖直方向无效)**


 ---

<br>
####九 盒子的居中 和 内容的居中
 
 - 1 **text-align:center; 和 margin:0px auto 的区别?<br><br>作用:**<br>
 (1) text-align:center; 的作用很简单,就是用来设置某个标签内 **文字和图片的居中.**<br>
 ![](/assets/Snip20180710_2.png)
 <br>(2) margin:0px auto; 的作用其实也很简单,就是让一个**盒子(块级标签)在父控件(父标签中居中)**<br><br>
 **总结:**<br> 
 (1) text-align 是让盒子的内容居中<br>
 (2)margin:0px auto; 是让盒子居中<br><br>

 

 


