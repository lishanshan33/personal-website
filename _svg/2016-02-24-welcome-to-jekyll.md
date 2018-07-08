---
layout: archive
title:  "插入svg动图"
modified: 2018-06-19T20:00:00-21:00
categories: 
  - SVG制作
tags:
  - svg
  
header:
 image: /images/home_page3.jpg
 
 sidebar:
  nav: "docs"
  
---

### 插入svg动图

<svg version="1.1" id="preloader" x="0px" y="0px" width="240px" height="120px" viewBox="0 0 240 120">

<style type="text/css" >
	<![CDATA[

		#plug,
		#socket { fill:#FDB515 }

		#loop-normal { fill: none; stroke: #FDB515; stroke-width: 12 }
		#loop-offset { display: none }

	]]>
</style>

<path id="loop-normal" class="st1" d="M120.5,60.5L146.48,87.02c14.64,14.64,38.39,14.65,53.03,0s14.64-38.39,0-53.03s-38.39-14.65-53.03,0L120.5,60.5
L94.52,87.02c-14.64,14.64-38.39,14.64-53.03,0c-14.64-14.64-14.64-38.39,0-53.03c14.65-14.64,38.39-14.65,53.03,0z">
	<animate attributeName="stroke-dasharray" attributeType="XML"
    	from="500, 50"  to="450 50"
    	begin="0s" dur="2s"
    	repeatCount="indefinite"/>
	<animate attributeName="stroke-dashoffset" attributeType="XML"
    	from="-40"  to="-540"
    	begin="0s" dur="2s"
    	repeatCount="indefinite"/>  
</path>
  
<path id="loop-offset" d="M146.48,87.02c14.64,14.64,38.39,14.65,53.03,0s14.64-38.39,0-53.03s-38.39-14.65-53.03,0L120.5,60.5
L94.52,87.02c-14.64,14.64-38.39,14.64-53.03,0c-14.64-14.64-14.64-38.39,0-53.03c14.65-14.64,38.39-14.65,53.03,0L120.5,60.5
L146.48,87.02z"/>
  
<path id="socket" d="M7.5,0c0,8.28-6.72,15-15,15l0-30C0.78-15,7.5-8.28,7.5,0z"/>  
  
<path id="plug" d="M0,9l15,0l0-5H0v-8.5l15,0l0-5H0V-15c-8.29,0-15,6.71-15,15c0,8.28,6.71,15,15,15V9z"/>
  
<animateMotion
	xlink:href="#plug"
  	dur="2s"
	rotate="auto"
	repeatCount="indefinite"
	calcMode="linear"
	keyTimes="0;1"    
	keySplines="0.42, 0, 0.58, 1">
	<mpath xlink:href="#loop-normal"/>
</animateMotion>
  
<animateMotion             
	xlink:href="#socket"
  	dur="2s"
	rotate="auto"
	repeatCount="indefinite"
	calcMode="linear"
	keyTimes="0;1"
	keySplines="0.42, 0, 0.58, 1">
	<mpath xlink:href="#loop-offset"/>
</animateMotion>  
</svg>

![svg](https://gitee.com/lishanshan33/minimal-mistakes/raw/master/images/svg.PNG){: .align-center}

首先要在minimal-mistakes文件里的_sass中新建一个scss命名为svg.scss；然后把svg动图的scss放进这个档中，而html就放在此markdown档中即可。

### 错误示范

![错误示范](https://gitee.com/lishanshan33/minimal-mistakes/raw/master/images/错误示范.PNG){: .align-center}

一开始我没有新建一个scss文件，而是选择在_animations.scss文件中的代码后面空一行后新增svg动图的scss代码，然后push之后发现网站发生了改变，就连背景色也都改变。所以发现这个方法是行不通的，最后尝试了新建scss文件。

> 参考 svg animation