针对大陆地区对landscape主题进行优化，主题还在调整中，欢迎`open issue`来提建议，参与讨论。

## 与Landscape不同的地方

- 根据国情，**去掉Google的库**，改用cloudflare的cdn，打开页面不再卡住了。
- 增加了 **语言包**，所以英语不好的同学，我懂你的。
- 代码高亮，**采用Monokai**，熟悉SublimeText的朋友一定不陌生。
- 主题默认包含feed和sitemap，不需要你手动安装了。
- 增加了 **友情链接** widget，已默认开启，可在landscape-plus/_config.yml中自行配置。
- 不使用header里面的大图，节省带宽，页面加载更快。（大图文件还在，你可以很方便的恢复它。）

## 演示

你可以点击[这里](http://reqianduan.com/)，查看演示。

## 安装主题

``` bash
$ git clone https://github.com/xiangming/landscape-plus.git themes/landscape-plus
```

## 启用主题

修改主题的设置文件`_config.yml`，把`theme`的值设置为`landscape-plus`

## 更新主题

``` bash
cd themes/landscape-plus
git pull
```

## Q/A
- **Q**：为什么之前不创建，现在又单独创建了新repo?
- **A**：之前landscape+主题和demo放在一个repo，有的朋友不知道如何使用，所以现在单独创建一个。
- **Q**：Demo看起来很赞，我要**怎么使用landscape+主题？**
- **A**：按照上方的步骤进行安装/启用/更新。
- **Q**：怎么提建议？
- **A**：主题还在调整中，欢迎`open issue`来提建议，参与讨论。
- **Q**：怎么添加友情链接？
- **A**：可在themes/landscape-plus/_config.yml中自行配置。
- **Q**：我喜欢原主题顶部的大图，如何恢复？
- **A**：themes/landscape-plus/source/css/_partial/header.styl，取消第33行的注释。
- **Q**：我是中国人，但是我喜欢英语？
- **A**：这个其实和theme无关，配置你的hexo源文件的_config.yml，删掉`language: zh-CN`。

## TODO
1. 使用多说替代disqus？
2. 使用国内社交网络，代替Facebook，twitter等？
3. 去掉边栏，改为单栏？

下面是hexo官方主题landscape的README.md，供参考。

---

# Landscape

A brand new default theme for [Hexo].

- [Preview](http://hexo.io/hexo-theme-landscape/)

## Installation

### Install

``` bash
$ git clone https://github.com/tommy351/hexo-theme-landscape.git themes/landscape
```

**Landscape requires Hexo 2.4 and above.**

### Enable

Modify `theme` setting in `_config.yml` to `landscape`.

### Update

``` bash
cd themes/landscape
git pull
```

## Configuration

``` yml
# Header
menu:
  Home: /
  Archives: /archives
rss: /atom.xml

# Content
excerpt_link: Read More
fancybox: true

# Sidebar
sidebar: right
widgets:
- category
- tag
- tagcloud
- archives
- recent_posts

# Miscellaneous
google_analytics:
favicon: /favicon.png
twitter:
google_plus:
```

- **menu** - Navigation menu
- **rss** - RSS link
- **excerpt_link** - "Read More" link at the bottom of excerpted articles. `false` to hide the link.
- **fancybox** - Enable [Fancybox]
- **sidebar** - Sidebar style. You can choose `left`, `right`, `bottom` or `false`.
- **widgets** - Widgets displaying in sidebar
- **google_analytics** - Google Analytics ID
- **favicon** - Favicon path
- **twitter** - Twiiter ID
- **google_plus** - Google+ ID

## Features

### Fancybox

Landscape uses [Fancybox] to showcase your photos. You can use Markdown syntax or fancybox tag plugin to add your photos.

```
![img caption](img url)

{% fancybox img_url [img_thumbnail] [img_caption] %}
```

### Sidebar

You can put your sidebar in left side, right side or bottom of your site by editing `sidebar` setting.

Landscape provides 5 built-in widgets:

- category
- tag
- tagcloud
- archives
- recent_posts

All of them are enabled by default. You can edit them in `widget` setting.

## Development

### Requirements

- [Grunt] 0.4+
- Hexo 2.4+

### Grunt tasks

- **default** - Download [Fancybox] and [Font Awesome].
- **fontawesome** - Only download [Font Awesome].
- **fancybox** - Only download [Fancybox].
- **clean** - Clean temporarily files and downloaded files.

[Hexo]: http://zespia.tw/hexo/
[Fancybox]: http://fancyapps.com/fancybox/
[Font Awesome]: http://fontawesome.io/
[Grunt]: http://gruntjs.com/
