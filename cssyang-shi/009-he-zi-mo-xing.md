####一 边框属性 border



- 1 **设置标签的边框**<br><br>(1)**连写:(同时设置4条边的边框)**
```
border: 边框的宽度  边框的样式  边框的颜色
border: 10px solid blue;
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
 
 
 
 
 ####二 内边距 Padding
 
 - 1 **什么是内边距(Padding)? <br> 内边距(padding)就是边框(border)和内容(content)之间的距离**<br> <br> **注意:<br> 给标签设置内边距(padding)后,标签占有的宽度和高度会发生变化**
 
 ![](/assets/Snip20180709_1.png)
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

 
 
 

 


