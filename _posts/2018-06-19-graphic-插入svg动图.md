---
layout: archive
title:  "插入svg动图"
modified: 2018-06-19T20:00:00-21:00
categories: 
  - 平面设计
tags:
  - 笔记
  
header:
 image: /images/home_page3.jpg
 
 sidebar:
  nav: "docs"
  
---

{% include base_path %}

{% include toc title="目录" %}

### svg动图

<svg viewbox="-15 -15 60 60">
  <path fill="#7F692F">
    <animate 
             attributeName="d" 
             dur="5000ms" 
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

### 步骤

![svg](https://gitee.com/lishanshan33/minimal-mistakes/raw/master/images/svg.PNG){: .align-center}

首先要在minimal-mistakes文件里的_sass中新建一个scss命名为svg.scss；然后把svg动图的scss放进这个档中，而html就放在此markdown档中即可。

### 错误示范

![错误示范](https://gitee.com/lishanshan33/minimal-mistakes/raw/master/images/错误示范.PNG){: .align-center}

一开始我没有新建一个scss文件，而是选择在_animations.scss文件中的代码后面空一行后新增svg动图的scss代码，然后push之后发现网站发生了改变，就连背景色也都被覆盖了，尝试了第二次还是这样的情况，则发现这个方法是行不通的，最后尝试了新建scss文件。

- 参考 svg animation