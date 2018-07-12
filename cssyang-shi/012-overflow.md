- 1 **overflow:hidden; 的作用?**<br><br>(1)**可以将超出范围的内容裁掉**

 ```
  .abc{
   width: 200px;
   height: 200px;
   background: green;
   overflow: hidden;
}
 ```
 清除前(即 overflow: visible;)
 ![](/assets/Snip20180712_11.png)
 清除后(即 overflow: hidden;)<br>![](/assets/Snip20180712_12.png)
 <br>(2) **清除浮动** 给盒子1设置overflow:hidden; 即可

  ```
   *{
    margin: 0px;
    padding: 0px;
    }
    .box1{
    background: red;
    // 使用overflow 清除浮动
     overflow: hidden;
     // 兼容overflow 在IE6 中的兼容问题
     *zoom:1; 
     
     }
    .box2{
     background: yellow;
    }
    .box1 
    p{   
     float: left;
     width: 100px;
     background: purple;
    }
    .box2 p{
    float: left;
    width: 100px;
    background: blue;
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
    清除浮动前
    ![](/assets/Snip20180712_14.png)
    清除浮动后
    ![](/assets/Snip20180712_13.png)
    
    **注意点:**<br>(1) 因为overflow 是 CSS3之后推出来的,在IE6 中不支持,需要在overflow 中添加  *zoom:1; 

