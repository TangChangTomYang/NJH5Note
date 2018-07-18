####2D转换模块

- 1 **正常**

- 2 **旋转**

- 3 **平移**

- 4 **缩放**

- 5 **综合的**

```
/*旋转45度*/
transform: rotate(45deg);
/*x方向平移10, y方向平移20*/
transform: translate(10px, 20px);
/*x方向1.5倍, y方向0.5倍, 如果x y 方向上的缩放一样可以简写,比如: scale(0.5) */
transform: scale(1.5,0.5);
            
/*旋转 平移 缩放一起写*/
transform: rotate(45deg)  translate(10px,20px) scale(1.5,1.5);
            
```