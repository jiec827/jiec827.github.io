---
layout: post
title: 基于GitHub+Jekyll的网站文件结构
categories: [demo, tech_notes]
tags: [demo, Jekyll]
fullview: False
shortinfo: 简介Jekyll的文件结构
---

### Template **dbyll** is on GitHub
**dbyll** is minimalist, stylish theme for jekyll. Supports gravatar, account links (github, twitter, e-mail, pinterest, résume file) and a bio.  

**dbyll** is brought to you by **[dbtek](http://ismaildemirbilek.com)**. Open sourced under [MIT](http://opensource.org/licenses/MIT) license.

<a class="btn btn-default" href="https://github.com/dbtek/dbyll">Grab your copy now!</a>

### Jekyll文件结构
[Jekyll](http://jekyll.bootcss.com/) 的核心是一个文本转换引擎。它的核心是把你零散的文件、文本组合起来，形成一个个网页，最终呈现在浏览器上展现出来。一个最基础的 Jekyll 博客，会拥有下面的目录结构：

    .
    ├── _config.yml
    ├── _drafts
    |   ├── begin-with-the-crazy-ideas.textile
    |   └── on-simplicity-in-technology.markdown
    ├── _includes
    |   ├── footer.html
    |   └── header.html
    ├── _layouts
    |   ├── default.html
    |   └── post.html
    ├── _posts
    │   └── 2013-08-07-welcome-to-jekyll.markdown
    ├── _site
    └── index.html

我们把自己需要的文件放到博客目录下，通过 jekyll build，该目录就会被复制到_site里面。明白了目录结构之后，我们在通过 git 提交博客到服务器的时候，就可以通过.gitignore来过滤掉_site目录，而在服务器端再执行命令生成。

### 配置文件

{% highlight yaml %}
  title: dbyll
  author:  
    name: yourname  
    email: youremail
    github: asd123
    linkedin: asd123
    weibo: asd123
    jianshu: asd123
    pinterest: asd123
    bio: Your stylish,  minimalist theme!  
    email_md5: md5ofemail  

    rss_path: feed.xml
    categories_path: categories.html
    tags_path: tags.html
    resue_path: resume.md

  # set it as url of an image
  # sidebar_background_image: assets/sky.png

{% endhighlight %}
