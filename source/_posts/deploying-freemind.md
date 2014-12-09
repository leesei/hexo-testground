layout: page
title: Deploying Freemind
date: 2014-12-02 12:20:27
tags:
- hexo
- tutorial
- freemind
toc: true
---

[Freemind](http://hahack.tk/hexo-theme-freemind/) by wzpan. Freemind's [source branch](https://github.com/wzpan/hexo-theme-freemind/tree/source).

<!-- more -->

## Install

```bash
git clone https://github.com/wzpan/hexo-theme-freemind.git themes/freemind
# or use submodule on your current repo
git submodule add https://github.com/wzpan/hexo-theme-freemind.git themes/freemind

npm install hexo-tag-bootstrap --save
```

Change `theme` in `_config.yml` as `freemind`.

## Modify Freemind config

Change  `slogan`, `links` in `themes/freemind/_config.yml`

## Setup default pages

```bash
cd source
mkdir categories; echo -e "title: Categories\nlayout: categories\ncomments: false\n---" > categories/index.html
mkdir tags; echo -e "title: Tags\nlayout: tags\ncomments: false\n---" > tags/index.html
mkdir about; echo -e "title: About\nlayout: about\ncomments: false\n---" > about/index.md
```
