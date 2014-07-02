title: 'IE8不支持:last-child伪类的解决方案'
tags:[IE8, CSS3, 伪类]
---

## 背景
所有主流浏览器均支持 :last-child 选择器，除了 IE8 及更早的版本。（了解详情：http://www.w3school.com.cn/cssref/selector_last-child.asp）
`:first-child`是CSS2的伪类，得到IE7+浏览器的支持；（了解详情：http://www.w3school.com.cn/cssref/selector_first-child.asp）
`:last-child`是CSS3的伪类，仅支持IE9+浏览器。

## 方案
- 因为IE8支持:first-child伪类，可以通过调整顺序，如:将最后一个元素移到第一位置；
- 可以在页面加载完后，使用javascript代码操作最后一个元素；
- 使用IE才支持的expression；（IE8 不再支持expression，了解详情：http://blogs.msdn.com/b/ie/archive/2008/10/16/ending-expressions.aspx）
