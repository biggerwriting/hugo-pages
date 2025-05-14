+++
date = '2025-05-13T12:49:34+08:00'
draft = true
title = 'Writing Content in Markdown'
tags = ['hugo', 'markdown']
+++

Markdown的基础用法
=================


## Paragraphs 
用两个换行符来分隔段落。

一个换行符。
还是一伙。

## 块元素

#just a tag
\# not a heading
Also a # tag

- list
+ list1
* list2

1) apple
2) banana
3) cherry


------------


> quote
aaa
bbb


## direct-emojis
You can use the emoji cheat sheet from https://www.unicode.org/emoji/charts/emoji-list.html for a list of supported emojis.

I :heart: emojis!

A link to [Emojis](#direct-emojis)


## Definition lists
Alex
: Hippy Web Developer
: Technophile

Bob
: Classic SysAdmin
: Conservative

Gabby
: Cool Content Master
: Cautious

## Code block
```javascript
 var x= 10;
 x++;
 console.log(x);
```
 
With highlighting:
```javascript {linenos=true,hl_lines=[2,"4-6"],linenostart=199}
 while (!success) {
  tryAgain();
  attempt++;
  if (Dead) {
    break;
  }
 }
```
