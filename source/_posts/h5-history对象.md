---
title: h5 history对象
date: 2017-01-07 16:26:17
tags: 'history'
---

 在HTML5之前，浏览器的历史记录是不能被操作的，开发者只能调用history对象的几种方法来实现简单的跳转，比如back、Go、forward等等。然而，历史总是会被新生事物代替的，Html5来了，这一切都将会得到改变，下面将重点解析下html5中的history新增的东西。

1. history.pushState(data,title,url),这个方法会在浏览器历史记录的堆栈顶部添加一条新记录，而且这个新记录会重置当前的url（但页面不会刷新），该方法的三个参数中，第一个感觉是作为辨识用的，并没有什么乱用啊，第二个参数说是会改变页面的title，但是也没有作用啊（我用的是google），重点感觉还是第三个参数，这个是改变的url，而且这个url是可选的，不写则为当前页面地址；
2. history.replaceState(data,title,url),这个方法是跟上面方法的用法基本相同，不同的是它并没有往历史记录中增加记录，而是直接替换了当前的url，页面也是没跳转；
3.history.state,用户存取以上方法中的data，所以上面说了，data是用户标识的，不同浏览器的读写权限不一样；
4.popstate事件，这个事件是window的事件，用法如下：

``` js

window.addEventListener("popstate",function(e){   
        console.log(e.state);  
    },false);

```


