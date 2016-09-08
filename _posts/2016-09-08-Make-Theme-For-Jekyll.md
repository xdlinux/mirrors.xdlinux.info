---
layout: post
title:  为 Jekyll 制作一个 theme
date:   2016-09-08 12:40
categories: jekyll theme
description: Jekyll 在装好的时候自带一个主题 minima ，可是非常神奇的是，这个主题没有主题文件，难道是集成在 Jekyll 里，这样的话让我们很难自己制作主题吖。
---

`Jekyll` 在装好的时候自带一个主题 `minima` ，可是非常神奇的是，这个主题没有主题文件，难道是集成在 `Jekyll` 里，这样的话让我们很难自己制作主题吖。

博客模板，有的什么都帮你做好，自动化生成，自动部署，一开始用的时候感觉很友好，但是用久了就发现它不能够定制化就不好了，而有的博客模板什么都是自己可见的，自己写的，一开始可能觉得不友好，但是用习惯了就学会自己写了，然后就不再用博客模板。

好吧，想办法把自己的模板套上去。

再来试一下语法高亮

```
def show
  @widget = Widget(params[:id])
  respond_to do |format|
    format.html # show.html.erb
    format.json { render json: @widget }
  end
end
```

