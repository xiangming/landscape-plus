title: hexo上手笔记
tags: [笔记, hexo]
---

## 准备工作
+ nodejs环境
+ git环境

---

## 安装

### 全局安装hexo

```bash
npm install -g hexo
```

### 创建项目

```bash
hexo init project_name
```

上面会自动创建目录`project_name`，如果你已经手动创建了目录`project_name`，也可以进入目录后，省略目录名来初始化项目：

```bash
cd project_name
hexo init
```

### 安装依赖

推荐修改hexo默认的`package.json`，增加`RSS`和`sitemap`的依赖。
当然，如果你用不上`RSS`和`sitemap`，也可以不添加。
无论你是否添加，都执行下面的命令，来安装依赖。

```bash
npm install
```

上面会根据`package.json`安装依赖包，这是`nodejs`的命令。

### 本地运行
将会自动启用一个端口`4000`的nodejs服务器（端口可在`_config.yml`中配置）

```bash
hexo generate
hexo server
```

generate命令生成静态文件，server命令启动本地服务器。

### 部署到Github Pages
先配置项目根目录的`_config.yml`，主要是文件最后面的deploy部分。

```yaml
# Deployment
## Docs: http://hexo.io/docs/deployment.html
deploy:
  type: github
  repository: https://github.com/xiangming/hexo.git
  branch: gh-pages
  message: 
```

默认使用`master`分支，但是我使用了`gh-pages`分支。当我第一次提交的时候，hexo会自动帮我创建这个分支。
建议使用两个分支，一个用于管理源文件，一个用于博客。

```bash
hexo generate
hexo deploy
```

### 创建文章/页面/草稿

```bash
hexo new post "文章标题"
hexo new page "页面名称"
hexo new draft "草稿标题"
```

你可以不写双引号，但是推荐写上，尤其是带空格的中文标题。
默认new是创建post，所以新建文章时，你可以省略post。
draft和post几乎一样，只是不会被自动发布，在你将它从**source/_drafts**移到**source/_posts**之前，没人看得到它。

到这里基本就完成了，下面的内容，一般读者可以不看。  

---

## hexo命令
### 简写

```bash
hexo n == hexo new
hexo g == hexo generate
hexo s == hexo server
hexo d == hexo deploy
```

### 组合

```bash
hexo g -d
```

以上命令，会自动先执行`generate`然后执行`deploy`。

---

## widget
除了theme默认已提供的widget外，你还可以自定义自己的widget，在`hexo\themes\landscape\layout\_widget\`下，新建自己的ejs文件，如`myWidget.ejs`，然后在配置文件`hexo\themes\landscape\_config.yml`中配置。(根据文件名匹配)

```js
widgets:
  - myWidget
```

---

## Q/A
Q：官方发布了新版本，我要如何更新自己的hexo版本？
A：在任意目录执行`npm update -g hexo`
Q：更新了文件，网站却没变化？
A：删除`.deploy`文件夹和`db.json`，再重新执行`generate`。
Q：github项目repo能不能绑定自己的域名？
A：可以。`reqianduan.com`就是一个项目repo。