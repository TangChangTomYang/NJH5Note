
在HTML5之前呢,HTML标签只能处理两种数据, 文本数据和图片数据,在HTML5之后呢可以处理video audio 数据了.


####HTML5中主要新增的标签
##video 标签

- **什么是video标签?
    - 作用:
        - 播放视频
    - 格式:
    ```
     <video src="">   </video>
    ```
    - video  标签的属性 
        - src: 用于告诉video标签需要播放的视频地址
        - autoplay: 用于告诉浏览器是否需要自动播放视频
        - controls: 用于告诉播放器 是否显示控制条
        - poster: 用于视屏没有播放前显示占位图片
        - loop: 一般用于做广告视频, 视频循环播放
        - preload: 用于预加载视频,但是注意preload 和 autoplay属性相冲,如果设置了autoplay属性,那么preload属性会失效
        - muted: 静音属性
        - width:  宽度和高度的属性和img 的属性是一样的效果,会等比缩放
        - height:


```
<body>

        <!--<video src="../imgs/sb1.webm" autoplay="autoplay" controls="controls" poster="../imgs/button.png">  </video> -->

        <video src="../imgs/sb1.webm"  controls="controls" poster="../imgs/button.png">   </video>

    </body>
```    


##二、video 标签的第二种格式 (解决浏览器视频格式兼容问题)

- 由于视频数据非常的重要，所以5大浏览器厂商都不愿意支持别人的视频格式，所以导致了没有一种视频格式是所有浏览器都支持的，这时候w3C为了解决这个问题，所以推出了第二个标签的格式。

- video 标签的第二种格式存在的意义就是为了解决浏览器适配的问题，video 元素支持三种视频格式
，我们可以把这三种格式通过 source 标签指定给video标签，那么当浏览器播放视频时
就会从其中来查找一种

- 虽然下面写了3种格式,兼容各个厂商的浏览器,但是 前提 条件是 浏览器要支持 HTML5 的Video ,因为video 是html5 的标签



```
  <video>

            <source src="../imgs/sb1.mp4"  type="video/mp4"> </video>   // 这个source就是为了解决浏览器适配，第一个source 不能解析就使用下面一个，直到找完
            <source src="../imgs/sb1.webm"  type="video/webm"> </video>
            <source src="../imgs/sb1.ogg"  type="video/ogg"> </video>

 
        </video>
```



