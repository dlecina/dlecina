---
layout: post
title: Prism Demo
date: '2014-04-27 22:01:34'
tags:
- ghost-tag
- staypuft
---

This is what code normally looks like with Ghost:

```
/* ==========================================================================
   0. Normalize.css v2.1.3 | MIT License | git.io/normalize | (minified)
   ========================================================================== */

html {
   font-family: sans-serif;
   -ms-text-size-adjust: 100%;
   -webkit-text-size-adjust: 100%;
}
body { margin: 0; }
a { background: transparent; }
a:focus { outline: thin dotted; }
a:active, a:hover { outline: 0; }
h1 { font-size: 2em; margin: 0.67em 0; }
abbr[title] { border-bottom: 1px dotted; }
b, strong { font-weight: bold; }
dfn { font-style: italic; }
```

Now, with [Prism](https://github.com/LeaVerou/prism):

```css
/* ==========================================================================
   0. Normalize.css v2.1.3 | MIT License | git.io/normalize | (minified)
   ========================================================================== */

html {
   font-family: sans-serif;
   -ms-text-size-adjust: 100%;
   -webkit-text-size-adjust: 100%;
}
body { margin: 0; }
a { background: transparent; }
a:focus { outline: thin dotted; }
a:active, a:hover { outline: 0; }
h1 { font-size: 2em; margin: 0.67em 0; }
abbr[title] { border-bottom: 1px dotted; }
b, strong { font-weight: bold; }
dfn { font-style: italic; }
```

###Usage

The syntax for using Prism is almost the same as normal code blocks, except you have to indicate the language like so:
```
```css
```
Please note that you will not be able to see the Prism style in the Ghost Admin/Editor. In other words, **any code blocks you see while creating or editing a post will look like normal Ghost code blocks**. This is because the Ghost Editor does not have the Prism CSS and Javascript files attached to it. However, **when you actually publish the post, they will look like Prism code blocks** (as long as you used the Prism syntax).

###Languages
Prism has an ever growing library of languages it supports, including major languages such as C, Java, Python, HTML, CSS and Javascript, as well as lesser-known languages such as Smalltalk and LOLCODE.

While previous versions of the theme simply included all available languages in one relatively huge Prism.js file, the current version of the theme is configured to dynamically load any languages that were actually used in a page, rather than always loading all of them and encumbering the theme, or selecting just the few I expect to use and screwing everyone else.

You may check the supported languages by looking at the contents of the `assets/js/prism-components` [folder](https://github.com/dlecina/StayPuft/tree/master/assets/js/prism-components).

###Plugins
This theme includes a variety of plugins that provide Prism with a number of useful features. Kudos to [pwntester](https://github.com/pwntester) for providing initial Markdown support for some of these.

####[Line Numbers](http://prismjs.com/plugins/line-numbers/)
With this plugin, you may include line numbers in your code blocks, like so:

```
```python|line-numbers
```

```python|line-numbers
import os

os.system('ls')
print "test"
for a in range(1,2):
    print a
```

You may also want to indicate a starting line number:

```
```python|line-numbers|data-start="2"
```

```python|line-numbers|data-start="2"
import os

os.system('ls')
print "test"
for a in range(1,2):
    print a
```

####[Line Highlight](http://prismjs.com/plugins/line-highlight/)
With Line Highlight, you can specify lines that you want to draw attention to:

```
```python|data-line="1-3,5"
```

```python|data-line="1-3,5"
import os

os.system('ls')
print "test"
for a in range(1,2):
    print a
```

Or even:

```
```python|line-numbers|data-line="1-3,5"
```

```python|line-numbers|data-line="1-3,5"
import os

os.system('ls')
print "test"
for a in range(1,2):
    print a
```

####[File Highlight](http://prismjs.com/plugins/file-highlight/)
With File Highlight, you can fetch external files and highlight them:

```
```js|data-src="https://davidlecina.com/blog/assets/js/prism/prism-preprocessor.js"
```

```js|data-src="https://davidlecina.com/blog/assets/js/prism/prism-preprocessor.js"
```

####Other plugins

[Autoloader](http://prismjs.com/plugins/autoloader/) is responsible for the previously mentioned "on-demand" language support. [Autolinker](http://prismjs.com/plugins/autolinker/) is also included.