# Landscape plus

[![Join the chat at https://gitter.im/xiangming/landscape-plus](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/xiangming/landscape-plus?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

针对中国大陆的hexo用户，优化hexo官方主题landscape。支持hexo 3.x 和 hexo 2.x。[**演示**](http://jasonxiang.com/landscape-plus/)

## 主题特色

+ **新增多语言支持**，支持英文(default)、中文简体(zh-CN)和中文繁体(zh-TW)。
+ **新增友情链接模块**，已默认开启，修改方法看下面的[FAQs](#faqs)。
+ **新增百度分享模块**，已默认开启。
+ **新增多说评论模块**，开启方法看下面的[FAQs](#faqs)，仍支持Disqus。
+ **新增mathjax模块**，即latex数学公式的支持，默认关闭。（感谢 @Svtter 的[pull request](https://github.com/xiangming/landscape-plus/pull/35)）
+ **新增IE8支持**
+ **新增返回顶部功能**
+ **新增Monokai代码高亮配色**，最流行、最优雅的代码高亮配色方案。
+ **移除Google库**，改用国内可以访问的CDN，加快页面显示速度。
+ **外观美化**，美化了部分外观样式。
+ **主题配置项优化**，你可以将主题配置项放在站点的`_config.yml`中，避免主题更新造成的冲突。

主题还在扩展中，欢迎各种**Pull Request**。

## 文档目录

+ [安装](#install)
+ [启用](#enable)
+ [配置](#config)
+ [更新](#update)
+ [FAQs](#faqs)
+ [更新日志](#logs)
+ [贡献者们](#contributors)
+ [网站列表](#sites)

## <a name='install'>安装</a>

从[**release页面**](https://github.com/xiangming/landscape-plus/releases)下载，然后解压到hexo的themes目录下。

或者直接拉取最新版：（可能会存在bug，不建议新手尝试）

```bash
# 在hexo根目录下执行
git clone https://github.com/xiangming/landscape-plus.git themes/landscape-plus
```

## <a name='enable'>启用</a>

修改hexo的配置文件`_config.yml`，把`theme`的值设置为`landscape-plus`
```yml
# Extensions
## Plugins: http://hexo.io/plugins/
## Themes: http://hexo.io/themes/
theme: landscape-plus
```

## <a name='config'>配置</a>

主题的默认配置文件`landscape-plus\_config.yml`：

```yml
# Header
menu:
  Home: /
  Archives: /archives
rss: /atom.xml

# Content
excerpt_link: Read More
fancybox: false
mathjax: false

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
  主题作者: http://arvinxiang.com
  热前端: http://reqianduan.com
  远程.work: http://yuancheng.work

# Miscellaneous
google_analytics:
favicon: /favicon.png
twitter:
google_plus:
fb_admins:
fb_app_id:

# Comment system
duoshuo_shortname: your_shortname
disqus_shortname: your_shortname

# Baidu share
baidushare: true
```

+ `mathjax` - 是否开启latex数学公式
+ `links` - 友情链接
+ `duoshuo_shortname` - 多说评论id
+ `baidushare` - 是否开启百度分享

**建议！** `mathjax`、`links`、`duoshuo_shortname`、`baidushare`配置项也支持放在站点的`_config.yml`中，并且我们建议你这样做。

## <a name='update'>更新</a>

```bash
cd themes/landscape-plus
git pull
```

**提示** 如果更新发生错误，你可以删除整个主题文件夹，然后重新执行[安装](#install)操作。

## <a name='faqs'>FAQs</a>

**问**：**怎么使用landscape plus主题？**
> 按照上方的步骤进行`安装`、`启用`。

**问**：如何开启多说评论模块？
> 在站点的`_config.yml`中，增加`duoshuo_shortname: xxx`配置项，xxx是你的多说id。

**问**：如何关闭百度分享模块？
> 删掉`themes/landscape-plus\_config.yml`中的`baidushare`配置项。

**问**：如何使用RSS分享功能？
> 请参考这条[issue](https://github.com/xiangming/landscape-plus/issues/31)进行配置。

**问**：怎么添加友情链接？
> 在站点的`_config.yml`中，增加`links:`配置项。

**问**：怎么切换语言版本？
> 在站点的配置文件`_config.yml`，修改`language:`配置项，zh-CN为中文简体，zh-TW为中文繁体，default为英文。

**问**：我喜欢原主题顶部的大图，如何恢复？
> `themes/landscape-plus/source/css/_partial/header.styl`，取消第33行的注释。

**问**：Landscape plus主题的字体配色太闪眼睛了，我怎么换回原主题的样式？
> 请参考这条[issue](https://github.com/xiangming/landscape-plus/issues/13)进行配置。

**问**：怎么提建议？
> 主题还在调整中，欢迎[open issue](https://github.com/xiangming/landscape-plus/issues/new)来提建议，参与讨论。

## <a name='logs'>更新日志</a>


### v1.0.6
+ 修复归档页面没有分页的BUG, refs #36, fix #78, #79, #85, #103, #106

### v1.0.5
+ 主题配置项优化, refs #17
+ 百度分享样式调整，refs #45, refs #61

### v1.0.4
+ 新增返回顶部功能
+ 修改渲染方式，现在默认page布局下仅渲染 .md 文件格式，其他格式一律只做复制。（方便添加静态页面，原本需要在每个文件开头添加 **layout: false**）
+ 添加**mathjax**的模块开关，不需要的可以自己关闭。

特别感谢来自 @myqianlan 的[pull request](https://github.com/xiangming/landscape-plus/pull/39) 和 @bearpaw 的[pull request](https://github.com/xiangming/landscape-plus/pull/53)。

### v1.0.3
+ 增加对 **IE8** 的支持
+ 集成 **mathjax** ，即latex数学公式的支持。（感谢 @Svtter 的[pull request](https://github.com/xiangming/landscape-plus/pull/35)）

### v1.0.2
+ 修改: 优化Generate速度，refs #13

### v1.0.1
+ 新增: 百度分享功能

### v1.0.0
+ 新增：语言包
+ 新增：友情链接
+ 新增：多说评论模块
+ 新增：代码高亮配色`Monokai`
+ 修改：使用国内可以访问的CDN，加快页面显示速度。

## <a name='contributors'>贡献者们</a>

+ [xiangming](https://github.com/xiangming)
+ [myqianlan](https://github.com/myqianlan)
+ [HADB](https://github.com/HADB)
+ [Svtter](https://github.com/Svtter)
+ [bearpaw](https://github.com/bearpaw)

主题还在扩展中，欢迎各种**Pull Request**。

## <a name='sites'>网站列表</a>

如果你的网站正在使用**landscape-plus**主题，你可以将网址添加到[wiki的网站列表](https://github.com/xiangming/landscape-plus/wiki)。
