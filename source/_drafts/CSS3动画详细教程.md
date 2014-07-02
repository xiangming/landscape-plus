title: CSS3动画详细教程
tags:[CSS3,动画,教程]
---

## 准备

下面是一个登陆表单的代码，供参考：

```html
<div class="form-module">
    <div class="header">
        <h1>Create new store</h1>
    </div>
    <form id="signup-form" action="/signup" method="post" data-validate="" novalidate="novalidate">
        <input type="hidden" name="name" value="">

        <div class="email-field field-container">
            <label for="email-field">Enter your email address</label>
            <input required="" autofocus="" type="email" name="email" id="email-field" placeholder="Your Email" value=""></div>
        <div class="password-field field-container">
            <label for="password-field">Set a password</label>
            <input required="" type="password" minlength="6" name="password" id="password-field" placeholder="New Password" value=""></div>
        <div class="cta-wrap">
            <button type="submit" class="cta-btn">Start your store</button>
        </div>
    </form>
</div>
```

```css
未添加
```

>为了方便演示，我使用了最新版的Firefox浏览器，而没有使用兼容性写法，在文章末尾我会给出完整兼容性代码。

## 第一步 - 默认的ease效果

```css
.form-module {
    animation: form-fly-up 0.35s ease;
}
@keyframes form-fly-up {
    0% { transform: translateY(500px); }
    100% { transform: translateY(0); }
}
```

这是默认的ease动画效果，很简单，你可以使用它，但是效果不太好，动作比较僵硬。

## 第二步 - 反弹效果

```css
.form-module {
    animation: form-fly-up 0.45s ease;
}
@keyframes form-fly-up {
    0% { transform: translateY(500px); }
    50% { transform: translateY(-50px);}
    100% { transform: translateY(0); }
}
```

我在第一步的基础上增加了一个向下移动的动作，这样看起来有反弹的效果。你可以反复调整距离和时间，也可以增加新的动作，来达到一个比较理想的效果。


## 第三步 - 反弹减弱效果

## 第四步 - 跟进和重叠效果

## 第五步 - 挤压和拉伸效果

这是最终的版本，它看起来很炫，但也许并不是你想要的。我只是介绍方法，你可以根据自己的想法，去获得更适合你的效果。

这只是设计师用来实现动画效果的一种方式，很高兴看到web技术使这一方向成为可能，相信web动画会有更多的发展。

## 完整兼容性代码

```
插入代码
```

为什么这样写，请参考[CSS3动画详细笔记](#)。