---
layout: post
title: "Blog building"
categories: misc
author: Yangyuanchen Liu
tag: [code, tool]
---

All the tools, techniques and method I used to built this blog will be recorded here.
<!--more-->

## Timeline

`July. 21, 2019`: Sharing Room was built and pushed to [lyyc199586.github.io](https://github.com/lyyc199586/lyyc199586.github.io)

`Aug. 14, 2019`: Theme was changed from minimal (offical theme of GitHub Page) to minima (default theme of Jekyll)


## Tools

### Markdown

Blog contents are in markdown format (.md)

### vscode

Codes are edited with my favorite editor: vscode 😜

## Methods

### Jekyll

I am using [Jekyll](https://jekyllrb.com/) and [GitHub Pages](https://help.github.com/en/articles/configuring-a-publishing-source-for-github-pages) to generate static pages. Jakll is convenient and easy to use. The present theme I am using is _minima_, the default theme of Jakll.

### LaTeX

The latex codes are not originally supported by GitHub Pages, so addtional tools and methods are needed. Here I used MathJex to make latex codes useable.

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

I am using [Disqus](https://disqus.com) to comment because it can be connected to Jakll easily (Notice that Disqus is blocked in China!).
