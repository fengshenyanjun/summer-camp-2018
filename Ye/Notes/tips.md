## html Notes

+ 预文本**<pre> **

  普通段落标签，文字的空格、换行符会被自动忽略；

  预文本内可以保留空格、换行符。

## CSS Notes

+ position布局：

  ##### 属性

  1. static（默认）   忽略top、bottom、left、right声明
  2. relative               相对于**static**起始位置偏移
  3. absolute             相对**父元素**左上角为原点进行偏移
  4. fixed                    相对**浏览器窗口**左上固定

+ float布局：

  1. 浮动靠左（float：left）
  2. 浮动靠右（float：right）

+ flex布局：

  .box{

  ​	display: flex;

  }

  + 设置flex布局后，子元素 *flex item* 的float、clear、vertical-align将失效

  ##### 属性

  1. ***flex-direction***：row、row-reverse、column、column-reverse

     ![flex-direction](http://www.runoob.com/wp-content/uploads/2015/07/0cbe5f8268121114e87d0546e53cda6e.png)

  2. ***flex-wrap***： nowrap、wrap、wrap-reverse

     （1.  nowrap

     ![nowrap](http://www.runoob.com/wp-content/uploads/2015/07/9da1f23965756568b4c6ea7124db7b9a.png "nowrap")

     （2.  wrap

     ![wrap](http://www.runoob.com/wp-content/uploads/2015/07/3c6b3c8b8fe5e26bca6fb57538cf72d9.jpg)

     （3.  wrap-reverse

     ![wrapreverse](http://www.runoob.com/wp-content/uploads/2015/07/fb4cf2bab8b6b744b64f6d7a99cd577c.jpg)

  3. ***justify-content***：flex-start、flex-end、center、space-between、space-around

     ![justify-content](http://www.runoob.com/wp-content/uploads/2015/07/c55dfe8e3422458b50e985552ef13ba5.png)

  4. ***align-items***：

     ![align-items](http://www.runoob.com/wp-content/uploads/2015/07/2b0c39c7e7a80d5a784c8c2ca63cde17.png)

  5. ***align-content*** ：

     ![align-content](http://www.runoob.com/wp-content/uploads/2015/07/f10918ccb8a13247c9d47715a2bd2c33.png)

