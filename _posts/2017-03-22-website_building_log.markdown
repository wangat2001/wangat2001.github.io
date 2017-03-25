---
layout: post
title:  "blog搭建问题锦集"
date:   2017-03-22 20:51:01 +0800
categories: jekyll blog
---
### 我的环境
- 操作系统：linux mint 18
- 静态网站生成器：jekyll 3.4.2
- Ruby: 2.3
- website platform: github pages


### Throubleshooting
1. 执行boundle install failed，提示
>run command boundle install error relate 'nokigiri':....

解决之道：
```shell
sudo apt-get install libxslt-dev libxml2-dev zlib1g-dev
sudo apt-get install ruby ruby-all-dev
bundle install
```

