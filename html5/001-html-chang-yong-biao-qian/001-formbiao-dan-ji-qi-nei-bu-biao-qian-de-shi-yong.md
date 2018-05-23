####form表单
- 什么是表单?
- 表单是专门用来收集用户信息的
- 什么是表单元素?
- 什么是元素?
- 在html中 标签\标记\元素都是指html中的 标签.如: `<a>` a标签\a标记a元素
- 表单元素其实也是html中的标签,只不过这些标签比较特殊,在浏览器中所有的表单都有特殊的外观和默认的功能.
- 表单的格式:
```
<form>
    <表单元素>
</form>
```
<br>

####常见的表单元素
####input 标签
- **input 标签输入框**
    ```
    <!--明文输入框-->
    账号:
    <input type="text"><br>
    <!--密文输入框-->
    密码:
    <input type="password"><br>

    ```
- **input 标签输入框 添加默认的值**
    ```
    <!--给输入框设置默认值-->
    账号:
    <input type="text" value="yanrui">
    密码:
    <input type="password" value="123">
    ```
- **input 标签输入框 单选框**

    ```
    性别:
    <input type="radio">男
    <input type="radio">女
    <input type="radio">其它
    ```
    ![](/assets/屏幕快照 2018-05-10 下午4.44.41.png)
    - **注意:**
            - 单选框 ,为什么单选框的type是radio呢? 因为最早的收音机的按钮只能按一个
            - 默认情况下单选框不会互斥,要想单选框互斥,那么必须给要互斥的每个单选框设置一个name属性,且name 属性必须一样,name属性的值可以随便写
            - 默认情况下单选框是没有选中的,要想单选框默认选中某个框子,那么必须给input标签加一个checkec 属性,即 checked = "checked"
            - 在我们HTML开发中,如果属性的值和属性的名字一样,那么可以省略属性的值,但是在Xhtml 中要求必须写,因此我们在企业开发中是不推荐省略的
&emsp;![](/assets/Snip20180510_1.png)

- **input 标签输入框 复选框**

    ```
    // 默认选中
    <input type="checkbox" checked="checked"><br>
    <input type="checkbox" checked="checked"><br>
    <input type="checkbox"><br>
    ```
- **input 标签输入框 按钮**
    - **普通按钮**
    注意: 点击普通按钮
    ```
    <input type="button" value="我是按钮">
    ```
    - **图片按钮**
    注意: 用户点击图片按钮后html页面会自动条状到 form 表单action 属性指定的网页(有点像查看具体图片的功能)

    ```
    <input type="image" src="imgs.jpg" alt="图片不存在">
    ```
    - **重置按钮**
        - **作用:** 重置按钮是用来清空(恢复\复原)和重置按钮在同一个form里面的其他input标签的值得
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
       - **注意**:重置按钮必须要写在form表单内才有效果,重置按钮有默认的名字"重置",想修改为其他名字,使用value属性修改
       <br>
    ![](/assets/屏幕快照 2018-05-10 下午5.16.33.png)
    - **提交按钮**
        - **作用:** 将表单中的数据内容提交到具体的服务器
        ```
        <form action="https://baidu.com"> 
            账号:
            <input type="text" name="usrName"><br> 
            密码:
            <input type="password" name="pwd"><br>
            <input type="submit">
        </form>
        ```
        - **注意点:**
            - 必须要在提交按钮的form表单里面**添加 action属性,指明提交的服务器地址**
            - 必须要在提交的form表单的对应的input标签中**添加name属性,指定对应input标签的字段名称 **
            ![](/assets/屏幕快照 2018-05-10 下午5.30.08.png)
               ![](/assets/Snip20180510_3.png)      
              
    - **隐藏域**
        - **作用:** 配合提交按钮将一些数据默默地悄悄咪咪的提交到服务器,真正的明白什么是隐藏域,要等学完Ajax才会明白.
        - **注意:** 隐藏域必须配合提交按钮才能工作,隐藏域是不显示的一个input标签
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
         

##Label 标签

####label标签文字和输入框(input标签)绑定操作
- 默认情况下文字和输入框是没有关联关系的,也就是说,点击文字输入框不会聚焦,如果想点击文字时让对应的输入框聚焦,那么就需要让文字和输入框进行绑定
- 想要输入框和文字绑定在一起,那么就可以使用label标签
- **绑定的格式(方式1):**
    - 将需要和输入框绑定的文字使用label标签包裹起来
    - 给输入框添加id属性
    - 在label标签中通过for属性和输入框中的id进行绑定即可

    ```
    <form action="https://baidu.com">
        <label for="usr">账号:</label> <input type="text"      id="usr"><br>
        <label for="pwd">密码:</label> <input type="password"  id="pwd"><br>
    </form>
    ```
    ![](/assets/Snip20180511_3.png)
- **绑定的格式(方式2):**
    - 直接使用label标签将文字和input标签包裹
    ```
     <label> 
        账号: <input type="text"  > 
    </label><br>
    
    <label> 
        密码: <input type="password"  >
    </label><br>
    ```
    - 方式2的缺点,只能绑定label包裹的部分,要绑定其他地方的标签就不可以了,方式1通过 for= id可以绑定任意的标签,是官方推荐的方法.

##datalist 标签 (仅作为了解)

####给输入框input标签绑定datalist标签

- datalits标签的作用?
    - 给输入框绑定带选项,如下图:
    ![](/assets/Snip20180511_4.png)
- 使用步骤:
    - 创建一个input标签
    - 创建一个datalist标签
    - 给datalist标签增加一个id属性
    - 给input标签添加一个list属性,list属性的值就是datalist的id的值
    ```
    <form> 
        <label>
            选择汽车的类型: <input type="text"     list="cars"  >
        </label><br>

        <datalist id="cars">
            <option>奔驰</option>
            <option>宝马</option>
            <option>奥迪</option>
            <option>马自达</option>
            <option>现代</option>
    </datalist>
    
    </form>
```
- 注意:
    - 所有主流浏览器都支持 <datalist> 标签，除了 Internet Explorer 和 Safari。 
 <br>   
 <br>
 <br>
 
##input 标签 HTML5新增标签 (仅作了解)

- **input标签 邮箱类型**

```
<form>

    <!--email类型输入标签
    可以自动校验输入的内容是否符合邮箱的格式-->
    邮箱:<input type="email">
    <input type="submit"><br>

</form>
```

- **input标签 域名类**

```
<form>

    <!--域名类型输入标签
   可以自动校验输入的内容是否符合URL的格式-->
    网址:<input type="url">
    <input type="submit"><br>
</form>
```

- **input标签 数字类型**

```
<form>

    <!--数字类型输入标签
   可以自动校验输入的内容是否是数字-->
    电话:<input type="number">
    <input type="submit"><br>
</form>
```
- input标签 颜色类型

```
<form>

    颜色:<input type="color">
    <input type="submit"><br>
</form>
```
- **input标签 日期类型**

```
<form>

    日期:<input type="date">
    <input type="submit"><br>
</form>

```

####select选择标签
- **作用:**
    - 用于定义下拉列表
- **格式1单组模式**

    ``` 
    <select >

        <option>列表数据</option> 
        
    </select>
    ```
- **格式2分组模式**

```
<form >

    <select >
        <optgroup label="北京">
            <option selected="selected">朝阳区</option>
            <option>昌平区</option>
            <option>通州区</option>
        </optgroup>

        <optgroup label="广州">
            <option>天河区</option>
            <option>越秀区</option>
            <option>黄埔区</option>
        </optgroup>

    </select>
</form>

```


- **注意点:**
    - 下拉列表不能设置输入内容,但是可以直接在列表中选择内容
    - 可以给选择标签设置默认值,给option标签添加selected 属性
    - 可以通过optgroup标签包裹 option标签来给下拉数据分组,optgroup中增加label属性来添加分组名称
    
    ![](/assets/屏幕快照 2018-05-11 上午11.37.08.png)![](/assets/屏幕快照 2018-05-11 上午11.47.50.png)
    
##textarea 标签

- **作用:** 定义一个多行的输入框
- **格式:**

```
<form action="http://baidu.com">
    <textarea name="name" cols="30" rows="10">
        默认文字
    </textarea>
    <input type="submit">
</form>
```
    
- **注意点:**
    - 默认情况下输入框可以无限换行.
    - 默认情况下输入框有自己的宽度和高度
    - 可以通过clos和rows来指定输入框的宽度和高度,但是虽然指定了列数和行数但是还是可以无限往下书写.
    - 默认情况下,是可以手动设置输入框的大小的
    
    
    
##表单标签的综合练习
代码:

```
<!--表单标签完整练习-->
        <form action="https://baidu.com">

            <!--添加表单标签的边框-->
            <fieldset>
                <!--设置表单标签的标题-->
                <legend>注册页面</legend>

                <!--添加表单具体内容-->


                <p>账号: <input type="text" name="account"></p>
                <p>密码: <input type="password" name="pwd"></p>


                <!--单选框-->
                <p>性别: <input type="radio" name="sex" value="male" checked="checked">男
                        <input type="radio" name="sex" value="female" >女
                        <input type="radio" name="sex" value="scret" >保密

                </p>

                <!--复选框-->
                <p>性别: <input type="checkbox" name="love" value="basketball" checked="checked">篮球
                    <input type="checkbox" name="love" value="football" >足球
                    <input type="checkbox" name="love" value="read" >阅读

                </p>

                <p>个人简介: <textarea name="des"cols="30" rows="10"></textarea></p>

                <p>生日: <input type="date" name="birthday"> </p>

                <p>邮箱: <input type="email " name="email"> </p>

                <p>手机: <input type="number" name="phoneNum"></p>


                <input type="submit" value="注册"> &emsp; &emsp; &emsp; <input type="reset" value="清空">

            </fieldset>

        </form>
```

![](/assets/Snip20180511_6.png)
[查看代码](https://github.com/TangChangTomYang/HTML5Code.git)



    
    
    
    




















               




