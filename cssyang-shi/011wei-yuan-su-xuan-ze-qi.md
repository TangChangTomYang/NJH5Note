
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
<br>
**伪元素选择器的使用场景1:--用于清除浮动**
具体代码如下:

    ```
    *{
        margin: 0px;
        padding: 0px;
    }

    .box1{
        background: red;
    }

    .box2{
        background: yellow;
    }

        .box1 p{
            float: left;
            width: 100px;
            background: purple;
        }
        .box2 p{
            float: left;
            width: 100px;
            background: blue;
        }

        /*通过伪元素选择器在指定标签的内容后添加一个标签*/
        .box1::after{
            content: "";
            clear: both; /*注意,如果是用作 隔离墙的功能,这个clear 属性一定要加上*/
            display: block; /* 隔离墙一定要设置 添加标签为块级元素*/
            height: 0px;
            // 这个隐藏属性,根据情况选择要不要设置
            visibility: hidden;
        }

    <div class="box1">
        <p>我是段落1</p>
        <p>我是段落1</p>
        <p>我是段落1</p>
    </div>
    <div class="box2">
        <p>我是段落2</p>
        <p>我是段落2</p>
        <p>我是段落2</p>
    </div>
    
    ```
    (伪元素选择器)清除浮动前:
    ![](/assets/Snip20180712_8.png)
    (伪元素选择器)清除浮动后:
    ![](/assets/Snip20180712_10.png)
    **注意点:**
    





