# Landscape plus

针对中国大陆地区对hexo官方主题landscape进行优化。

## 所有新特性

+ 根据国情，**去掉Google的库**，改用cloudflare的cdn，打开页面不再卡住了。=> [参与国内cdn的讨论](https://github.com/xiangming/landscape-plus/issues/3)
+ 增加了 **语言包**，所以英语不好的同学，我懂你的。
+ 代码高亮，**采用Monokai**，熟悉SublimeText的朋友一定不陌生。
+ 增加了 **友情链接** widget。（已默认开启，修改方法看下面的[常见问题](#常见问题)。）
+ 不使用header里面的大图，节省带宽，页面加载更快。（大图文件还在，恢复方法看下面的[常见问题](#常见问题)。）
+ 修改了原主题的 **配色** 和部分markdown样式（blockquote/code...）
+ 集成 **多说评论模块** 。（开启方法看下面的[常见问题](#常见问题)。）
+ 集成 **百度分享模块** 。（已默认开启，详情看下面的[常见问题](#常见问题)。）

主题还在调整中，欢迎[open issue](https://github.com/xiangming/landscape-plus/issues/new)来提建议，参与讨论。

## 文档目录

+ [演示](#演示)
+ [安装](#安装)
+ [启用](#启用)
+ [更新](#更新)
+ [配置](#配置)
+ [常见问题](#常见问题)
+ [更新日志](#更新日志)
+ [网站列表](#网站列表)

## 演示

你可以点击[这里](http://reqianduan.com/)，查看演示。

## 安装

``` bash
$ git clone https://github.com/xiangming/landscape-plus.git themes/landscape-plus
```
**Landscape plus 需要 Hexo 2.7 及以上版本.**

## 启用

修改主题的设置文件`_config.yml`，把`theme`的值设置为`landscape-plus`

## 更新

``` bash
cd themes/landscape-plus
git pull
```

## 配置

```yml
# Header
menu:
  Home: /
  Archives: /archives
rss: /atom.xml

# Content
excerpt_link: Read More
fancybox: false

# Sidebar
sidebar: right
widgets:
- category
- tag
- tagcloud
- archive
- recent_posts
- links

# Links
links:
  主题作者: http://themes.xiguabaobao.com
  iOS开发博客: http://bawn.github.io/
  tangyumeng's blog: http://tangyumeng.com/
  novsec's blog: http://www.novsec.com/
  小峰网络遨游记: http://xfeng.me/
  沉默紀: http://silenceage.com/

# Miscellaneous
google_analytics:
favicon: /favicon.png
twitter:
google_plus:
fb_admins: 
fb_app_id:

# Duoshuo
duoshuo_shortname: 

# Baidu share
baidushare: true
```

+ `links` - 友情链接
+ `duoshuo_shortname` - 多说评论id
+ `baidushare` - 是否开始百度分享

## 常见问题

**问**：Demo看起来很赞，我要**怎么使用landscape+主题？**
> 按照上方的步骤进行`安装`、`启用`、`更新`。

**问**：怎么提建议？
> 主题还在调整中，欢迎[open issue](https://github.com/xiangming/landscape-plus/issues/new)来提建议，参与讨论。

**问**：怎么添加友情链接？
> 修改`themes/landscape-plus/_config.yml`中的`links`。

**问**：我喜欢原主题顶部的大图，如何恢复？
> `themes/landscape-plus/source/css/_partial/header.styl`，取消第33行的注释。

**问**：我是中国人，但是我喜欢英语？
> 配置你的hexo源文件的`_config.yml`，去掉`language: zh-CN`。

**问**：Landscape plus主题的字体配色太闪眼睛了，我怎么换回原主题的样式？
> 请参考这条[issue](https://github.com/xiangming/landscape-plus/issues/13)进行配置。

**问**：如何开启多说评论模块？
> 修改`themes/landscape-plus\_config.yml`，填写你的多说id即可。（主题会自动启用多说评论，忽略hexo默认的disqus。）

**问**：如何开启百度分享模块？
> 修改`themes/landscape-plus\_config.yml`，将`baidushare`设置为`true`即可。（已默认开启）

## 更新日志

### v1.0.2
+ 修改: 优化Generate速度，refs #13

### v1.0.1
+ 新增: 百度分享模块

### v1.0.0
+ 修改：根据国情，去掉Google的库，改用cloudflare的cdn
+ 新增：语言包
+ 修改：代码高亮配色修改为`Monokai`
+ 新增：友情链接
+ 修改：隐藏顶部大图
+ 修改：主题配色和部分markdown样式
+ 新增：多说评论模块

## 网站列表

- **[reqianduan]** - The demo site of Landscape+.
- **[bawn]** - iOS开发博客
- **[tangyumeng]** - tangyumeng's blog
- **[novsec]** - novsec's blog
- **[joysboy]** - 小峰网络遨游记
- **[沉默紀]** - Silenceage
- **[游走的艺术]** - Artwalk's Blog

[reqianduan]: http://reqianduan.com/
[bawn]: http://bawn.github.io/    
[tangyumeng]: http://www.tangyumeng.com
[novsec]: http://www.novsec.com/
[joysboy]: http://xfeng.me/
[沉默紀]: http://silenceage.com/
[游走的艺术]: http://artwalk.github.io/

如果你的网站正在使用**landscape-plus**主题，欢迎将网址添加到[wiki的网站列表](https://github.com/xiangming/landscape-plus/wiki)，我会不定期进行整理。
