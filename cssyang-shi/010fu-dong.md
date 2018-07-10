

####一 编写代码请,清空系统默认的外边距 和 内边距

- 1 在企业级的开发过程中,我们为了更好的控制盒子的宽高和计算盒子的宽高等等,因此在企业开发中,编写代码前的第一件事就是清空默认的边距(外边距(margin)和内边距(padding))

- 2 如何清除默认的外边距和内边距呢?<br><br>格式:
```
利用通配符选择器给每个标签清除外边距和内边距
*{
    padding:0px;
    margin:0px;
}
```
**注意点:<br>虽然可以使用通配符 * 选择器可以便利每个标签并清除所有标签的外边距和内边距,但是性能不好.建议使用下面的CSS 样式 替换**

    ```
    body,div,dl,dt,dd,ul,ol,li,h1,h2,h3,h4,h5,h6,pre,code,form,fieldset,legend,input,textarea,p,blockquote,th,td{
        margin:0;
        padding:0
    }
    直接百度: YUI CSS reset 
    网址: https://yuilibrary.com/yui/docs/cssreset/
    ```
    
    
    
    
    
    
---
####二 行高 和 字号


- 1 **什么是行高?<br> 在CSS 中 所有的行都有自己的行高<br><br>注意点:<br>(1) 行高和盒子的高不是同一个高度,行高是指一行内容的高度, 盒子的高度是内容的高度**













