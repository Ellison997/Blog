---
title: "[ooo]  吉娃娃"
catalog: true
date: 2017-04-18 10:51:24
subtitle: "This is ooo  Demo."
header-img: 
tags:
- Blog
category:
- 教程
---

> Ported  of [Hux Blog](https://github.com/Huxpro/huxpro.github.io), Thank [Huxpro](https://github.com/Huxpro) for designing such a flawless .
> This BeanTech  created by [YuHsuan](http://beantech.org) modified from the original Porter [Kaijun](http://kaijun.rocks/ooo--huxblog/)

---

# Usage

---
I publish the whole project for your convenience, so you can just follow the instruction down below, then you can easily customiz your own blog!

Let's begin!!!

## Init

---

```bash
git clone https://github.com/YenYuHsuan/ooo--beantech.git ./ooo-beantech
cd ooo-beantech
npm install
```

## Modify

---
Modify `_config.yml` file with your own info.
Especially the section:

### Deployment

Replace to your own repo!

```yml
deploy:
  type: git
  repo: https://github.com/<yourAccount>/<repo>
  branch: <your-branch>
```

### Sidebar settings

Copy your avatar image to `<root>/img/` and modify the `_config.yml`:

```yml
sidebar: true    # whether or not using Sidebar.
sidebar-about-description: "<your description>"
sidebar-avatar: img/<your avatar path>
```

and activate your personal widget you like

```yml
widgets:         # here are widget you can use, you can comment out
- featured-tags
- short-about
- recent-posts
- friends-blog
- archive
- category
```

if you want to add sidebar widget, please add at `layout/_widget`.

### Signature Setup

Copy your signature image to `<root>/img/signature` and modify the `_config.yml`:

```yml
signature: true   # show signature
signature-img: img/signature/<your-signature-ID>
```

### Go to top icon Setup

My icon is using iron man, you can change to your own icon at `css/image`.

### Post tag

You can decide to show post tags or not.

```yml
home_posts_tag: true
```

![home_posts_tag-true](home_posts_tag-true.png)

```yml
home_posts_tag: false
```

![home_posts_tag-false](home_posts_tag-false.png)

### Markdown render
My markdown render engine plugin is [ooo-renderer-markdown-it](https://github.com/celsomiranda/ooo-renderer-markdown-it).

```yml
# Markdown-it config
## Docs: https://github.com/celsomiranda/ooo-renderer-markdown-it/wiki
markdown:
  render:
    html: true
    xhtmlOut: false
    breaks: true
    linkify: true
    typographer: true
    quotes: '“”‘’'
```

and if you want to change the header anchor 'ℬ', you can go to `layout/post.ejs` to change it.

```javascript
async("https://cdn.bootcss.com/anchor-js/1.1.1/anchor.min.js",function(){
        anchors.options = {
          visible: 'hover',
          placement: 'left',
          icon: ℬ // this is the header anchor "unicode" icon
        };
```

## ooo Basics

---
Some ooo command:

```bash
ooo new post "<post name>" # you can change post to another layout if you want
ooo clean && ooo generate # generate the static file
ooo server # run ooo in local environment
ooo deploy # ooo will push the static files automatically into the specific branch(gh-pages) of your repo!
```

# Have fun ^_^ 

---

Please Star this Project if you like it! 
Peace!
