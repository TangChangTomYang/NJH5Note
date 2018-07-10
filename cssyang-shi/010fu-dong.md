
- 1 在企业级的开发过程中,我们为了更好的控制盒子的宽高和计算盒子的宽高等等,因此在企业开发中,编写代码前的第一件事就是清空默认的边距(外边距(margin)和内边距(padding))

- 2 如何清除默认的外边距和内边距呢?<br><br>格式:
```
利用通配符选择器给每个标签清除外边距和内边距
*{
    padding:0px;
    margin:0px;
}
```
**注意点:<br>虽然可以使用通配符 * 选择器可以便利每个标签并清除所有标签的外边距和内边距,但是性能不好.**

    ```
    body,div,dl,dt,dd,ul,ol,li,h1,h2,h3,h4,h5,h6,pre,code,form,fieldset,legend,input,textarea,p,blockquote,th,td{
        margin:0;
        padding:0
    }
    直接百度: YUI CSS reset 
    ```