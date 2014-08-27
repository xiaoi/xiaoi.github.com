---
layout: post
title: "the nil error"
date: 2014-08-27 15:05:57 +0800
comments: true
categories: 
- rake
- nil
---
今天更新文章内容的时候，在执行到rake generate时，报以下错：

Generating... 
     Build Warning: Layout 'nil' requested in blog/categories/octopress/atom.xml does not exist.
     Build Warning: Layout 'nil' requested in blog/categories/git/atom.xml does not exist.
     Build Warning: Layout 'nil' requested in blog/categories/octopress/atom.xml does not exist.
     Build Warning: Layout 'nil' requested in blog/categories/git/atom.xml does not exist.


问了谷哥哥，还是stackflow上的回答靠谱：


As detailed here since version 2.2 Jekyll has an issue with the layout validation, so you will manually have to change nil to null in 2 files:

source/atom.xml
source/_includes/custom/category_feed.xml
This will sort out Jekyll and it will stop hicking up :)

说白了就是要把这两个文件里的nil修改为null，然后再执行:

rake generate
rake deploy

总算不报错了

传送门：http://stackoverflow.com/questions/25159075/integrating-bourbon-to-default-octopress-theme

