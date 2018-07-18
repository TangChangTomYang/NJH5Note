####a 标签的伪类选择器

- 1、 **通过我们的观察,发现a标签有一定的状态 **
    - 默认状态,从未访问过
    - 被访问过的状态
    - 鼠标长按的状态
    - 鼠标悬停在a标签上的状态
    
    
 <br><br>   
- 2、**什么是a标签的伪类选择器?**<br>
(1)、 a标签的伪类选择器是用来修改a标签不同状态的样式的.



<br><br>   
- 3、**a标签伪类选择器的格式**

    ```
    // 修改从未访问过状态下的样式
    a:link{
    color: red;
    }
    // 修改被访问过状态下的样式
    a:visited{
        color: blue;
    }
    // 修改长按状态下的样式
    a:active{
        color: pink;
    }
    // 修改鼠标悬浮状态下的样式
    a:hover{
       color: orange;
    }
    ```
    
- 4、***a 标签伪类选择器注意点:**<br>
(1)、a 标签的伪类选择器可以单独出现,也可以一起出现<br>
(2)、a 标签的伪类选择器如果一起出现,那么必须要严格的遵守编写顺序,否则可能导致效果失效, 顺序: 爱恨原则 love hate (即 link --> visited --> hover --> active)<br>
(3)、如果默认状态的样式和被访问的演示一样,那么可以简写

    ```
    简写
    a{
        color:red;
    }
    相当于 下面2句
    a:link{
        color:red;
    }
    a:visited{
        color:red;
    }
    后面的顺序不变
    ```
(4)、在编写a标签的伪类选择器时,要将伪类选择器的代码写在 a 标签选择器之后
```
a{
    属性名:属性值;    
}
// 伪类选择器要写在 a 之后
a:伪类选择器{
    属性名:属性值;  
}
```
(5)、在企业开发中和a标签盒子相关的属性都写在 a 标签选择器中(比如: 显示模式/宽度高度等),只有和状态变化相关的才写在伪类选择器中.
(6)、 在企业开发中和a标签文字 背景相关的都写在伪类选择器中.

  
  
  
 ####过度模块 transition
 
 - :hover 伪类选择器除了可以用在 a 标签前上,还是可以用在其他任何标签上
 
 - 过度动画3要素
     - 1、必须要有属性发生变化
     - 2、必须告诉系统那个属性需要执行过渡效果
     - 3、必须告诉系统过度效果持续时长
     ```
     div{
            width: 200px;
            height: 50px;
            background: red;

            /*设置要过度动画的属性*/
            transition-property: width;
            /*设置过度动画的时长*/
            transition-duration:2s;
            // 以下2个可选
            // 动画延时执行
            transition-delay: 2s;
            // 动画执行方式
            transition-timing-function: linear; /*ease ease-in ease-out ease-in-out*/

    }
    /*设置过度动画的触法 事件 和 动画执行范围*/
    div:hover{
        width: 500px;
    }
    ```
    
- **transition 过度连写**<br>
**格式**
```
过度属性 过度时长 过度样式 延时
transition: property duration timing-function delay
```
**连写注意点:**<br>
(1) 多个需要动画的属性之间使用逗号分割,不能单独写,后面会层叠掉前面的

    ```
    // 正确写法, 过度效果之间用逗号 , 分割
    transition:width 2s linear 0s, background-color 5s linear 0s;

    //错误写法
    transition:width 2s linear 0s;
    transition:background-color 5s linear 0s; // 这一行会把上一行的过度层叠掉
    ```
    (2) 如果有很多属性需要动画可以使用 all 替代: 
    ```
    // 就是说我所有变化的属性都需要动画,动画时长为2秒
    transition:all 2s;
    ```
    (3) 只要满足3要素(动画的属性 动画的时长 变化的属性值)就会有动画效果


     
 
 




