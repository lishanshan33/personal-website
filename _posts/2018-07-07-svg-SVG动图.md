---
layout: archive
title:  "svg动图"

categories: 
  - SVG制作
tags:
  - svg
---

### 插入svg动图

<svg viewbox="0 0 100 100">
  <path fill="#1EB287">
    <animate 
             attributeName="d" 
             dur="3000ms" 
             repeatCount="indefinite"
             values="M 0,0 
                     C 50,0 50,0 100,0
                     100,50 100,50 100,100
                     50,100 50,100 0,100
                     0,50 0,50 0,0
                     Z;

                     M 25,50 
                     C 37.5,25 37.5,25 50,0 
                     75,50 75,50 100,100
                     50,100 50,100 0,100
                     12.5,75 12.5,75 25,50
                     Z;"/>
  </path>
</svg>

### 新建scss文件

这个方法同样需要新建scss文件

![画图](https://gitee.com/lishanshan33/minimal-mistakes/raw/master/images/画图.PNG){: .align-center}

然后可以在这个网站中，画出自己想要做的svg图。

![源代码](https://gitee.com/lishanshan33/minimal-mistakes/raw/master/images/源代码.PNG){: .align-center}

然后在左上方的视图找到源代码，可以复制使用，然后再找新建的scss文件中打代码，根据自己的想要的svg动图要求。

> 参考 svg animation