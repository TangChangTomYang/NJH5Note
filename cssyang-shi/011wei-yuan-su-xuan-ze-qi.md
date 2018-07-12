
- 1 **什么是伪元素选择器?**<br>**可以给指定标签 的内容前面 添加一个子元素或者给指定标签的内容后面添加一个子元素** <br><br> **格式:**

    ```
    标签名称::before{
    属性名称:值;
    }

    标签名称::after{
        属性名称:值;
    }    
    ```
    比如:
    ```
     div{
        background: red;
        width: 200px;
        height: 200px;
        }
        // 在div内容前面增加一个子标签
        div::before{
            display: block;
            content: '前面';
            width: 50px;
            height: 50px;
            background: pink;

        }
        // 在div内容后面增加一个子标签
        div::after{
            content: '后面';
            width: 50px;
            height: 50px;
            background: pink;
            display: block;
        }
        
         <div> wo shi wen zi</div>
        ```
    效果图      
![](/assets/Snip20180712_6.png)