####form表单
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
&emsp;![](/assets/Snip20180510_1.png)

    - input 标签 复选框
    ```
    // 默认选中
    <input type="checkbox" checked="checked"><br>
    <input type="checkbox" checked="checked"><br>
    <input type="checkbox"><br>
    ```
    - input 标签 按钮
        - 普通按钮
    ```
    <input type="button" value="我是按钮">
    ```
        - 图片按钮
    ```
    <input type="image" src="imgs.jpg" alt="图片不存在">
    ```
        - 重值按钮
            - 作用: 重置按钮是用来清空(恢复\复原)和重置按钮在同一个form里面的其他input标签的值得
    ```
    <form >
        账号:
    <input type="text"><br>
        密码:
    <input type="password"><br>
    // 重置按钮
    <input type="reset">
    </form>
    ```
            - 注意:重置按钮必须要写在form表单内才有效果,重置按钮有默认的名字"重置",想修改为其他名字,使用value属性修改
    ![](/assets/屏幕快照 2018-05-10 下午5.16.33.png)
        - 提交按钮
            - 作用,将表单中的数据内容提交到具体的服务器
        ```
        <form action="https://baidu.com"> 
            账号:
            <input type="text" name="usrName"><br> 
            密码:
            <input type="password" name="pwd"><br>
            <input type="submit">
        </form>
        ```
            - 注意点:
               - 必须要在提交按钮的form表单里面添加 action属性,指明提交的服务器地址
               - 必须要在提交的form表单的对应的input标签中添加name属性,指定对应input标签的字段名称 
               ![](/assets/屏幕快照 2018-05-10 下午5.30.08.png)
               ![](/assets/Snip20180510_3.png)      
              
        - 隐藏域
         - 作用: 配合提交按钮将一些数据默默地悄悄咪咪的提交到服务器,真正的明白什么是隐藏域,要等学完Ajax才会明白.
         - 注意: 隐藏域必须配合提交按钮才能工作,隐藏域是不显示的一个input标签
         ```
         <form action="https://baidu.com">
        账号:
        <input type="text" name="usrName"><br>
        密码:
        <input type="password" name="pwd"><br>
        <input type="submit">
        <input type="hidden" name="address" value="成都">
</form>
         ```
         ![](/assets/Snip20180510_6.png)
               




