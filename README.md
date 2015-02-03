# Landscape plus

[![Join the chat at https://gitter.im/xiangming/landscape-plus](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/xiangming/landscape-plus?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

针对中国大陆地区对hexo官方主题landscape进行优化。

## 所有新特性

+ 根据国情，**去掉Google的库**，改用cloudflare的cdn，打开页面不再卡住了。=> [参与国内cdn的讨论](https://github.com/xiangming/landscape-plus/issues/3)
+ 增加了 **语言包** 。（支持英文、中文简体和中文繁体。）
+ 代码高亮，**采用Monokai**，熟悉SublimeText的朋友一定不陌生。
+ 增加了 **友情链接** widget。（已默认开启，修改方法看下面的[常见问题](#常见问题)。）
+ 不使用header里面的大图，节省带宽，页面加载更快。（大图文件还在，恢复方法看下面的[常见问题](#常见问题)。）
+ 修改了原主题的 **配色** 和部分markdown样式（blockquote/code...）
+ 集成 **多说评论模块** 。（开启方法看下面的[常见问题](#常见问题)。）
+ 集成 **百度分享模块** 。（已默认开启，详情看下面的[常见问题](#常见问题)。）
+ 增加对 **IE8** 的支持。
+ 集成 **mathjax**，即latex数学公式的支持。（感谢 @Svtter 的[pull request](https://github.com/xiangming/landscape-plus/pull/35)）

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

## <a name='演示'>演示</a>

你可以点击[这里](http://jasonxiang.com/landscape-plus/)，查看演示。

## <a name='安装'>安装</a>

``` bash
$ git clone https://github.com/xiangming/landscape-plus.git themes/landscape-plus
```
**Landscape plus 需要 Hexo 2.7 及以上版本.**

## <a name='启用'>启用</a>

修改主题的设置文件`_config.yml`，把`theme`的值设置为`landscape-plus`

## <a name='更新'>更新</a>

``` bash
cd themes/landscape-plus
git pull
```

## <a name='配置'>配置</a>

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
  主题作者: http://xiguabaobao.com
  热前端: http://reqianduan.com

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
+ `baidushare` - 是否开启百度分享

## <a name='常见问题'>常见问题</a>

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

**问**：如何使用RSS分享功能？
> 请参考这条[issue](https://github.com/xiangming/landscape-plus/issues/31)进行配置。

## <a name='更新日志'>更新日志</a>

### v1.0.4
+ 增加返回顶部功能
+ 修改渲染方式，现在默认page布局下仅渲染 .md 文件格式，其他格式一律只做复制。（方便添加静态页面，原本需要在每个文件开头添加 **layout: false**）
+ 添加**mathjax**的模块开关,不需要的可以自己关闭。

特别感谢来自 @myqianlan 的[pull request](https://github.com/xiangming/landscape-plus/pull/39) 和 @bearpaw 的[pull request](https://github.com/xiangming/landscape-plus/pull/53)。

### v1.0.3
+ 增加对 **IE8** 的支持
+ 集成 **mathjax** ，即latex数学公式的支持。（感谢 @Svtter 的[pull request](https://github.com/xiangming/landscape-plus/pull/35)）

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

## <a name='网站列表'>网站列表</a>

- **[hexo-theme-landscape-plus]** - The demo site of Landscape-plus theme.
- **[bawn]** - iOS开发博客
- **[假唐]** - 个人博客
- **[tangyumeng]** - tangyumeng's blog
- **[novsec]** - novsec's blog
- **[joysboy]** - 小峰网络遨游记
- **[沉默紀]** - Silenceage
- **[游走的艺术]** - Artwalk's Blog
- **[Mark's Blog]** - Life and Technology
- **[一盏灯，一部随身听，一本书。。。。。。]** - This is 洛桑扎巴's personal blog
- **[YumeMichi's Blog]** - 随心、随想
- **[小新技术随想]** - 技术，生活，梦想
- **[N神的研究所]** - 我正在考虑在这里写点啥...
- **[Mcl's Space]** -MCL 的空间
- **[Hello,world]** - 红红的个人博客
- **[SkyCoder‘s Blog]** - SkyCoder‘s Blog
- **[Yilong's Blog]** - Keep It simple,small...
- **[漠北空城]** - 做好自己
- **[Just for Free]** - 自由为王, 一生只为自由的活着
- **[Rang]** - Rang
- **[Beeder's Blog]** - Beeder's Blog
- **[peng8.net]** - peng8.net 技术博客.

[Rang]: http://wurang.net/
[Beeder's Blog]: http://beeder.me/
[peng8.net]:http://www.peng8.net/
[hexo-theme-landscape-plus]: http://jasonxiang.com/landscape-plus/
[bawn]: http://bawn.github.io/    
[假唐]: http://jiatang.me
[tangyumeng]: http://www.tangyumeng.com
[novsec]: http://www.novsec.com/
[joysboy]: http://xfeng.me/
[沉默紀]: http://silenceage.com/
[游走的艺术]: http://artwalk.github.io/
[Mark's Blog]: http://codermango.com/
[一盏灯，一部随身听，一本书。。。。。。]: http://lszb811.com/
[YumeMichi's Blog]: https://dsy.im
[小新技术随想]: http://litengfei.com
[N神的研究所]: http://nshen.net
[Mcl's Space]: http://mclspace.com
[Hello,world]: http://lihongn.tk
[SkyCoder‘s Blog]: http://twocucao.github.io/
[Yilong's Blog]: http://laiyilong.github.io/
[漠北空城]: http://yuechang.github.io/
[Just for Free]: http://cifer.me

如果你的网站正在使用**landscape-plus**主题，欢迎将网址添加到[wiki的网站列表](https://github.com/xiangming/landscape-plus/wiki)，我会不定期进行整理。
