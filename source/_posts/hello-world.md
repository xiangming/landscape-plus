title: Hello World
---
Welcome to [Hexo](http://hexo.io/)! This is your very first post. Check [documentation](http://hexo.io/docs/) for more info. If you get any problems when using Hexo, you can find the answer in [trobuleshooting](http://hexo.io/docs/troubleshooting.html) or you can ask me on [GitHub](https://github.com/tommy351/hexo/issues).

## Quick Start

### google-code-prettify

``` html
<html>
<head>
    <meta charset="utf-8">
    <title>google-code-prettify demo</title>
    <link rel="stylesheet" href="prettify.css">
</head>
<body>
    
    <pre>
        <!-- html/css/js -->
        html/css/js
    </pre>

    <script src="jquery-1.9.1.min.js"></script>
    <script src="prettify.js"></script>
    <script src="run-prettify.js"></script>
</body>
</html>
```

``` javascript
// Search
  var $searchWrap = $('#search-form-wrap'),
    isSearchAnim = false,
    searchAnimDuration = 200;

  var startSearchAnim = function(){
    isSearchAnim = true;
  };

  var stopSearchAnim = function(callback){
    setTimeout(function(){
      isSearchAnim = false;
      callback && callback();
    }, searchAnimDuration);
  };
```

### Create a new post

``` bash
$ hexo new "My New Post"
```

More info: [Writing](http://hexo.io/docs/writing.html)

### Run server

``` bash
$ hexo server
```

More info: [Server](http://hexo.io/docs/server.html)

### Generate static files

``` bash
$ hexo generate
```

More info: [Generating](http://hexo.io/docs/generating.html)

### Deploy to remote sites

``` bash
$ hexo deploy
```

More info: [Deployment](http://hexo.io/docs/deployment.html)