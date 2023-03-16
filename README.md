# [Tetris Latam Site](https://tetrislatam.netlify.app)

Add files to `content/` and commit them to add posts.

They will deploy to the site shortly.


## Creating Chapters:

To create a **chapter** (a higher level category on the sidebar), create a folder with the title as the name of your category. Then, add a file `_index.md` in that folder, with the following text at the top:

### Chapter Example
```
+++
title = "Title of Chapter"
chapter = true
pre = "<b>1. </b>"
weight = 5
+++

Blah blah blah this is an article in markdown
```

## Creating Sub-articles

To create sub articles, create a markdown file and add the following text to the top. 

### Sub-article Example
```
+++
title = "Title of Article"
pre = "<b>1. </b>"
weight = 3
+++

Blah blah blah this is an article in markdown
```

## Explanation of Front-matter properties:

**title** 

The title of the article.  Appears as the title in the tab.

**chapter**

Set this to true if this is the `_index.md` file of a chapter folder.

**pre**

The prefix that appears on the sidebar. This is html, so you can use tags like `<b>` (bold) to style them. 

e.g. a pre of `<b>1. </b>` produces:
![image](https://user-images.githubusercontent.com/70501945/225487197-20fa23d0-3b2a-4aaa-ad01-db5f77a56ac3.png)


**weight**

This property determines the order of the articles. If an article has no weight defined, it will just go to the bottom. Otherwise, they'll be ordered (within their chapter, if it's a subarticle) in order of ascending weight.

More detailed information on page creation can be found in the docs for the [Hugo Learn Theme](https://learn.netlify.app/en/cont/pages/)
