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