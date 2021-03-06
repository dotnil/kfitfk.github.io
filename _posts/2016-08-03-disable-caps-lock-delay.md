---
layout: post
title: Disable Caps Lock Delay in Mac OS
category: programming
poster: https://img.alicdn.com/tps/TB1GpHRLXXXXXaJXpXXXXXXXXXX-1200-250.jpg
summary: Actually Apple calls it a feature. To prevent you from accidentally hitting the caps lock key when you mean to press A key, there's a delay on pressing caps lock key, meaning you have to press it longer to take effect. This feature is stupid to me. I never make such a mistake since I bought my first computer. Here's how to fix it.
---

最近写 SQL 稍微多一点，为了保持良好的习惯，需要把关键字都大写。然而 Mac 下面有个功能，为了方式按 A 键的时候误按到 caps lock 键，系统会在字母输入完成后立即按 caps lock 键添加一个延迟，导致按键不生效。It's not a bug; it's an undocumented feature! 然而我用了 15 年键盘从来没发生过这个事情，所以必须得禁用以提高效率。

本篇部分翻译自 [sleepycow 的一篇博文](http://sleepycow.org/2014/07/removing-the-caps-lock-delay-on-a-macbook/)。我坚信不要相信云存储，不要相信收藏夹链接有效性。当有需要记录一些东西的时候，一定要有本地备份。所以我要挪到自己的文章里。

首先，我们需要安装两个软件，分别是 [Seil](https://pqrs.org/osx/karabiner/seil.html.en) 和 [Karabiner](https://pqrs.org/osx/karabiner/)。

接着，禁用掉系统提供的 caps lock 键功能。打开系统偏好设置，并选择键盘一项，在右下角点击修饰键，把 Caps Lock 置为 No Action。

![Disable system caps lock key](https://img.alicdn.com/tps/TB1E4nLLXXXXXXoXFXXXXXXXXXX-1324-1056.png)

下面启动 Seil，勾上 Change the caps lock key 选项，并把 keycode 设置为 110。

![Seil settings](https://img.alicdn.com/tps/TB1p9fFLXXXXXXkXVXXXXXXXXXX-1324-396.png)

然后打开 Karabiner，在搜索框里输入 application key to capslock。展开 For PC Users 一栏，再展开 Change PC Application Key 一栏，勾选 Application Key to CapsLock。

![Karabiner settings](https://img.alicdn.com/tps/TB1JH2DLXXXXXaTXVXXXXXXXXXX-1586-912.png)

完成以上操作后，把这些软件都关掉就可以了。
