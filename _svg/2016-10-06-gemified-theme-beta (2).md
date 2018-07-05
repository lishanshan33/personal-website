---
layout: archive
title:  "svg的学习笔记"
modified: 2018-06-19T20:00:00-21:00
categories: 
  - SVG制作
tags:
  - svg
  
classes: wide
header:
  overlay_image: /images/home_page1.jpg
# caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
# cta_label: "More Info"
# cta_url: "https://unsplash.com"

---


svg允许在代码中使用矢量点来描述二维图像。 

## svg的基本信息

- SVG 指可伸缩矢量图形 (Scalable Vector Graphics)
- SVG 用来定义用于网络的基于矢量的图形
- SVG 使用 XML 格式定义图形
- SVG 图像在放大或改变尺寸的情况下其图形质量不会有所损失
- SVG 是万维网联盟的标准
- SVG 与诸如 DOM和 XSL 之类的W3C标准是一个整体

## SVG的根元素  
  
SVG的根元素有width、height和viewbox属性。
<svg width="198px" height="188px" viewBox="0 0 198 188" 这三个属性在SVG展示的时候都起到了十分重要的作用。  
宽度和高度属性对于创造一个视口十分有用。透过这个定义的视口，我们可以看到内部定义的SVG形状。和普通的Web页面一样，SVG的内容可能会比视口大，但是这不意味着多余的部分 就不存在，只是我们看不到而已。  
另一方面，视框（viewbox）则定义了SVG中所有形状都需要遵循的坐标系。 
你可以把视框值0 0 198 198视为对矩形左上角和右下角的描述。前两个值被称为min-x 和min-y，用于描述左上角的位置。而接下来的两个值被称作宽度和高度，可以描述右下角的位置。 
因此viewbox属性可以让你缩放图片。例如，你可以这么设置viewbox属性： 
<svg width="198px" height="188px" viewBox="0 0 99 94" 那么其中的形状为了填满SVG的宽度和高度，就会被放大。

## SVG的命名空间  

SVG会有一个由生成它的图形编辑程序定义的命名空间（xmlns是XML命名空间的缩写）。  
这些命名空间往往只是在生成SVG的程序中使用，所以在Web页面上展示SVG的时候它们并不是必需的。因此在优化流程中，为了减小SVG的大小，通常会把它们去掉。
  
## 元素g  

g元素能把其他元素捆绑在一起。例如，你要画一辆车的SVG，你会把用来构成车轮的形状 用g标签集合起来。   
在g标签中我们可以看到先前的命名空间。这会有助于图形编辑软件再次打开这个图像，但 是它对于这个图片在其他地方展示并没有影响。

## svg的优势 

svg它有以下优势：
- SVG 图像可通过文本编辑器来创建和修改
- SVG 图像可被搜索、索引、脚本化或压缩
- SVG 是可伸缩的
- SVG 图像可在任何的分辨率下被高质量地打印
- SVG 可在图像质量不下降的情况下被放大

## SVG的路径  

SVG路径和其他SVG形状有所区别，因为它们是由任意数量的连接点组成的（允许你自由创造你想要的形状）。  
这是SVG文件的价值所在。SVG的代码可以手写，也可以利用图像工具来生成。 

## 浏览器支持度

SVG现在的浏览器支持度也相当不错，Android 2.3以上和IE9以上都支持（见[caniuse.com](http://caniuse.com/ #search=svg)）。
