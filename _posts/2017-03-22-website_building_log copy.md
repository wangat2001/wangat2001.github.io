---
layout: post
title:  "blog搭建问题锦集"
date:   2017-03-22 20:51:01 +0800
categories: jekyll blog
---

1. ruby

   a.源码安装：https://www.ruby-lang.org/en/downloads/
     $ tar -xvzf ruby-2.2.3.tgz    
     $ cd ruby-2.2.3
     $ ./configure
     $ make
     $ sudo make install
   
   b.自动安装
     $ sudo yum install ruby    # CentOS, Fedora, 或 RHEL 系统
     $ sudo apt-get install ruby-full # Debian 或 Ubuntu 系统
     $ brew install ruby 苹果系统

2.gem

   a.download rubyGem https://rubygems.org/pages/download
   b.$ ruby setup.rb

3.bundler

   a.$ gem install bundler

4.bundle install nokogiri-1.6.8.1 --path vendor/bundle

5.config

   _.config.yml
       url:  https://sunping0612.github.io

6.local server
   
   $ bundle exec jekyll serve

7.build

   $ JEKYLL_ENV=production bundle exec jekyll build

8.update github pages
   
   a.master -- 源码
   b.ph-pages -- 保存构建后的文件，Setting > Options > GitHub Pages > Source ---> ph-pages

   $ cd _site
   $ git add .
   $ git commit -m "Build"
   $ git push origin gh-pages


### 我的环境
- 操作系统：linux mint 18
- 静态网站生成器：jekyll 3.4.2
- Ruby: 2.3
- website platform: github pages

```
 bundle exec jekyll serve
```

### Throubleshooting
1. 执行bundle install failed，提示
>run command boundle install error relate 'nokigiri':....

解决之道：
```shell
sudo apt-get install libxslt-dev libxml2-dev zlib1g-dev
sudo apt-get install ruby ruby-all-dev
bundle install
```

