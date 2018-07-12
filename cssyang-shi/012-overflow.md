- 1 **overflow:hidden; 的作用?**<br><br>(1) 可以将超出范围的内容裁掉

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
