####设置背景图片


- 1 **如何设置背景图片?**<br><br>**在CSS中有一个叫做 background-image:url() 的属性, 就是专门用于设置背景色的属性**<br><br>
**注意:**<br>
(1) 图片的地址必须放在url 中,图片的地址可以是本地的地址也可以是网络的地址<br>(2) 如果图片的大小 小于标签的大小,那么会自动水平垂直平铺.<br> 
(3)出现了网页,后会在发送请求回去网络图片.

```
  background-image: url(images/picture.jpg);
  background-image: url(http://img3.imgtn.bdimg.com/it/u=3958361117,863751032&fm=27&gp=0.jpg);
```

<br>
___
- 2 **设置背景图片是否平铺,如何平铺?**<br> <br> 
**在CSS 中设置 background-repeat 属性即可设置背景的平铺方式** <br><br>
**应用场景:**<br>
**解决网络下载一张很大的图片(小图片平铺成一张大图片)提升用户体验**

  ```
  background-repeat: no-repeat; // 不平铺
  background-repeat: repeat-x;  // 水平平铺
  background-repeat: repeat-y;  // 竖直平铺
  background-repeat: repeat;    // 平铺 默认就是这个
  ```
  ![](/assets/Snip20180703_5.png)


<br>
___
- 3 **背景定位图片**<br>
**在CSS 中,有一个叫做 background-position 的属性, 是专门用于设背景图片位置的,此属性 有2个参数 x 方向参数 和 Y方向参数** 如下:<br><br>
**(1)方位取值**

  ```
  水平方位: left center right
  垂直方位: top center bottom;

  background-position: left bottom;
  ```
**(2) 具体像素取值(距离左上角偏移)**

  ```
  background-position: 50px 60px;  // 表示x 方向距离左边50px,表示y 方向距离上边60px

  ```

<br>
___

- 4 **背景属性的缩写方式:**<br><br> 
**格式:**<br>
```
background 背景颜色 背景图片 平铺方式 关联方式  定位方式
```
**通过这种方式可以同时给背景设置多个属性,比如:**

  ```
  width: 500px;
  height: 500px;
  background: red;
  background-image: url(abc.jpg);
  background-repeat: no-repeat;
  background-position: top left;

  可以简写为
  background:red url(abc.jpg) no-repeat top left
  ```
  **注意点:**<br>
  **background 属性中的任何一个属性都可以省略,即可以这样写:<br><br> 
  background:red <br>
  或者<br> 
  background:url(abc.jpg)<br>
  或者<br> 
  background: no-repeat<br>
  或者<br> 
  background: top left<br> ... ...
**


<br>
___
- 5 **设置背景图片的关联方式** <br><br>
(1) **什么是背景图片的关联方式?**<br><br> 
默认情况下背景图片是随着屏幕滚动条的滚动而滚动的,如果我们不想背景图片随着滚动条滚动的话就需要设置背景关联<br><br>
**如何设置背景图片的关联?**  <br><br>
在CSS 中有个 background-attachment 属性就是用来设置背景图的关联的,默认取值是scroll, 如果想设置不随屏幕滚动就设置 fixed;

  ```
  background-attachment: fixed;
  ```
  





