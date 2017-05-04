---
title: css学习..
date: 2017-01-18 10:46:27
tags: css
---

调整placeholder样式

```html
 
::-webkit-input-placeholder { /* WebKit browsers */ 
color: #999; 
} 
:-moz-placeholder { /* Mozilla Firefox 4 to 18 */ 
color: #999; 
} 
::-moz-placeholder { /* Mozilla Firefox 19+ */ 
color: #999; 
} 
:-ms-input-placeholder { /* Internet Explorer 10+ */ 
color: #999; 
} 

```
启动 browserSync
```bash

browser-sync start --server --files "**/*.css, **/*.html"

```
input type="number"时出现小箭头，去除方法

```css
/*在chrome下：*/

input::-webkit-outer-spin-button,
input::-webkit-inner-spin-button{
    -webkit-appearance: none !important;
    margin: 0; 
}
/*Firefox下：*/

input[type="number"]{-moz-appearance:textfield;}

```
第二种方案：

将type="number"改为type="tel"，同样是数字键盘，但是没有箭头。

在移动端设置overflow:hidden为什么页面还能滚？要怎么禁止

```html

如果你是将overflow:hidden用在了body上那么不管用，因为移动端是基于touch事件。
你可以将你要隐藏滚动的内容加上一个包裹层div，然后给这个div设置高度为window.height()，并且overflow:hidden,就可以解决你的问题了;

还有一个就是body 加上position：fixed; 有坑！！！


```

