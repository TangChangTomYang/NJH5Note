
####表单
- 什么是表单?
 - 表单是专门用来收集用户信息的
 
- 什么是表单元素?
 - 什么是元素?
   - 在html中 标签\标记\元素都是指html中地 标签.如: `<a>` a标签\a标记a元素
 - 表单元素其实也是html中的标签,只不过这些标签比较特殊,在浏览器中所有的表单都有特殊的外观和默认的功能. 

- 表单的格式:
```
<form>
 <表单元素>
</form>
```
- 常见的表单元素
 - input 标签
   ```
   <!--明文输入框-->
    账号:
    <input type="text"><br>
    <!--密文输入框-->
    密码:
    <input type="password"><br>

   ```
  - input 标签 添加默认的值
   
   ```
  <!--给输入框设置默认值--> 
  账号:
   <input type="text" value="yanrui"> 
  密码:
   <input type="password" value="123">
  ```
  - input 标签 单选框
  ```
  性别:
  <input type="radio">男 
  <input type="radio">女
  <input type="radio">其它
  ```
  ![](/assets/屏幕快照 2018-05-10 下午4.44.41.png)
 
  - 注意: 
   - 单选框 ,为什么单选框的type是radio呢? 因为最早的收音机的按钮只能按一个
   - 默认情况下单选框不会互斥,要想单选框互斥,那么必须给要互斥的每个单选框设置一个name属性,且name 属性必须一样,name属性的值可以随便写
   - 默认情况下单选框是没有选中的,要想单选框默认选中某个框子,那么必须给input标签加一个checkec 属性,即 checked = "checked"
   - 在我们HTML开发中,如果属性的值和属性的名字一样,那么可以省略属性的值,但是在Xhtml 中要求必须写,因此我们在企业开发中是不推荐省略的
![](/assets/Snip20180510_1.png)



 