---
layout: archive
title:  "插入svg动图"
modified: 2018-06-19T20:00:00-21:00
categories: 
  - SVG制作
tags:
  - svg
---
  
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