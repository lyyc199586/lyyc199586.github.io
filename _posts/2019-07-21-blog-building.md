---
layout: post
title: "Blog building"
categories: misc
author: Yangyuanchen Liu
tag: [code, tool]
excerpt_separator: <!--more-->
---

All the tools, techniques and method I used to built this blog will be recorded here.
<!--more-->

## Timeline

`July. 21, 2019`: Sharing Room was built and pushed to [lyyc199586.github.io](https://github.com/lyyc199586/lyyc199586.github.io)

`Aug. 14, 2019`: Theme was changed from `minimal` (official theme of GitHub Page) to `minima` (default theme of Jekyll)

`Sept. 4, 2019`: Sidebar and table of content are added to post page.

## Editing

### Markdown

Blog contents are in markdown format (.md), most posts are written with Typora, an elegant and useful markdown editor. 

### vs-code

Codes are edited with my favorite editor: vs-code 😜

## Sources

### Jekyll

I am using [Jekyll](https://jekyllrb.com/) and [GitHub Pages](https://help.github.com/en/articles/configuring-a-publishing-source-for-github-pages) to generate static pages. Jekyll is convenient and easy to use. The present theme I am using is _minima_, the default theme of Jekyll.

### MathJax

The latex codes are not originally supported by GitHub Pages, so additional tools and methods are needed. Here I used MathJax to make latex codes useable.

1. from [layout page](https://github.com/pages-themes/THEME_NAME/blob/master/_layouts/default.html), change `THEME_NAME` to the theme you are using (for me it's `minima`), then add this page to your repo `_layout/default.html`.

2. add following code in `<head>` tag of `default.html` page

```html
    <script type="text/x-mathjax-config">
      MathJax.Hub.Config({
        TeX: {
            equationNumbers: { autoNumber: "all" },
            Macros: {bm: "\\boldsymbol"}
          }
        });
    </script>
    <script type="text/x-mathjax-config">
      MathJax.Hub.Config({
          tex2jax: {
            inlineMath: [ ['$','$'], ["\\(","\\)"] ],
            processEscapes: true
        }
      });
    </script>
    <script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript">
    </script>
```

Then latex formulas are supported, for example, $\LaTeX$ .

### Comment

I am using [Disqus](https://disqus.com) to comment because it can be connected to Jekyll easily (notice Disqus is blocked in China!).



### Sidebar

I am using a Sidebar from GitHub named  [Lanyon](https://github.com/poole/lanyon), see `./_includes/sidebar.html` and add style in `./_sass/minima/_layout.scss`



### Table of content

I am using a TOC from GitHub named [Jekyll-toc](https://github.com/allejo/jekyll-toc), see `./_includes/toc.html` and add `{% include toc.html html=content}`  in `sidebar.html`.