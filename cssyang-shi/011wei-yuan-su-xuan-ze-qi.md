
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
            // 指定添加的子元素的内容
            content: '后面';
            // 指定添加的子元素的宽度
            width: 50px;
            // 指定添加的子元素的高度
            height: 50px;
            // 指定添加的子元素的背景色
            background: pink;
            // 指定添加的子元素的 显示样式
            display: block;
            // 指定添加的子元素是显示还是不显示
            // visibility: hidden;
            
        }
        
         <div> wo shi wen zi</div>
        ```
    效果图      
![](/assets/Snip20180712_6.png)