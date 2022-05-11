---
layout: post
title: "QT样式表设置背景色 background-color无效的原因"
date: 2021-07-15 15:39:39
categories: [Qt]
article: true
published: true
comments: false
copyright: false
original: false
reprintAuthor: "qq_31073871"
reprintUrl: "https://blog.csdn.net/qq_31073871/article/details/79965015"
permalink: /:title/
---

例如我们给一个按钮设置背景色为红色：
```css
QPushButton
{ 
    background-color: red; 
}
```

结果发现，按钮的背景色并没有被设置为红色！

问题的原因，QT的帮助文档里讲了，比较难找，打开帮助文档，依次展开->style sheet->Qt Style Sheets Reference，找到表格中的QPushButton，如下图所示
![](https://abaoa.cn//assets/post/2021-07-15-15-39-39/1.png)

大体意思就是，要想使背景色生效，必须要设置一下某个border属性，border-color、border-width等等任何一个跟border相关的属性都行。因为pushbutton的原生边界把背景色给覆盖住了。