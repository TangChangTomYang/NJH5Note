##Label 标签

####label标签文字和输入框(input标签)绑定操作
- 默认情况下文字和输入框是没有关联关系的,也就是说,点击文字输入框不会聚焦,如果想点击文字时让对应的输入框聚焦,那么就需要让文字和输入框进行绑定
- 想要输入框和文字绑定在一起,那么就可以使用label标签
- 绑定的格式(方式1):
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
- 绑定的格式(方式2):
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
    
















