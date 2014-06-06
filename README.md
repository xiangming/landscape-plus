## 修改的地方
- 根据国情，**去掉Google的库**，改用cloudflare的cdn，速度更好。
- 增加了 **语言包**，所以英语不好的同学，我懂你的。
- 代码高亮，**采用Monokai**，熟悉SublimeText的朋友一定不陌生。
- 主题默认包含feed和sitemap，不要你自己去安装。
- 增加了 **友情链接** widget，可在主题的_config.yml中自行配置。
- 去掉header里面的大图，节省带宽，页面加载更快。（大图还在，你可以很方便的恢复它。）

## Demo
你可以点击[这里](http://reqianduan.com/)，看看速度。

## 说明
主题还在调整中，欢迎open issue来提意见，参与讨论。

几个讨论点：

1. 使用 **多说** 替代 **disqus**？

2. 使用国内社交网络，代替Facebook，twitter等？

下面是原主题landscape的README.md，后面会作修改，是否翻译，暂不确定。

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
