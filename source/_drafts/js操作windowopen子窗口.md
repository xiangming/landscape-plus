title: js操作window.open子窗口
tags:[javascript,笔记]
---

## 注意点

虽然浏览器会自动添加补全`<head>`和`<body>`等标签，但是仍然要规范书写，以避免一些浏览器的解析异常（说你呢，IE8）。

**DOCTYPE** 要手动指定，像这样：

```js
newWindow.document.write('<!DOCTYPE html>');
```

## 参考代码

下面是项目中的代码块，供参考：

```js
function printEntry()
{
    var newWindow=window.open("Print","_blank");
    sprnstr="<!--startprint-->"; 
    eprnstr="<!--endprint-->"; 
    bdhtml=window.document.body.innerHTML; 
    headhtml=document.getElementsByTagName('head')[0].innerHTML;//refs #861
    prnhtml=bdhtml.substr(bdhtml.indexOf(sprnstr)+17); 
    prnhtml=prnhtml.substring(0,prnhtml.indexOf(eprnstr)); 
    var docStr = prnhtml; 

    newWindow.document.write('<!DOCTYPE html>');
    newWindow.document.write('<head>');
    newWindow.document.write('<link href="/assets/bootstrap/css/bootstrap.min.css" media="screen" rel="stylesheet" type="text/css">');
    newWindow.document.write('<link href="/css/admin/entry.view.css" media="screen" rel="stylesheet" type="text/css">');
    newWindow.document.write('</head>');
    newWindow.document.write('<body>');
    newWindow.document.write(docStr);
    newWindow.document.write('</body>');

    newWindow.document.close();
    newWindow.print();

    //newWindow.close();
}
```

## 相关内容

+ http://www.cnblogs.com/stswordman/archive/2006/06/02/415853.html