####设置背景图片


- 1 **如何设置背景图片?**<br><br>**在CSS中有一个叫做 background-image:url() 的属性, 就是专门用于设置背景色的属性**<br><br>**注意:**<br>(1) 图片的地址必须放在url 中,图片的地址可以是本地的地址也可以是网络的地址<br>(2) 如果图片的大小 小于标签的大小,那么会自动水平垂直平铺.<br> (3)出现了网页,后会在发送请求回去网络图片.

```
  background-image: url(images/picture.jpg);
  background-image: url(http://img3.imgtn.bdimg.com/it/u=3958361117,863751032&fm=27&gp=0.jpg);
```


- 2 **设置背景图片是否平铺,如何平铺?**<br> <br> **在CSS 中设置 background-repeat 属性即可设置背景的平铺方式** <br><br>**应用场景:**<br>**解决网络下载一张很大的图片(小图片平铺成一张大图片)提升用户体验**

```
background-repeat: no-repeat; // 不平铺
background-repeat: repeat-x;  // 水平平铺
background-repeat: repeat-y;  // 竖直平铺
background-repeat: repeat;    // 平铺 默认就是这个
```
![](/assets/Snip20180703_5.png)



- 3 **背景定位图片**



