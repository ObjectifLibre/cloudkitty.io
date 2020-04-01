---
layout: post
title: Sustain Markdown cheatsheet
tags: [CheatSheet, HowTo]
thumbnail: /assets/markdown-cheatsheet/thumbnail.jpg
---

> This is a Markdown Cheatsheet Demo for **Sustain**, this Jekyll theme. Please check the raw content of this file for the markdown usage.

## Typography Elements in One

Let's start with a informative paragraph. **This text is bolded.** But not this one! _How about italic text?_  Ok, let's **_combine_** them together. In case you have code to highlight, `ProceedLikeThis()`. By the way, [here's a link to this template](https://github.com/jekyller/sustain) or [https://github.com/jekyller/sustain](https://github.com/jekyller/sustain).

<div class="divider"></div>

## Headings H1 to H6

# H1 Heading

## H2 Heading

### H3 Heading

#### H4 Heading

##### H5 Heading

###### H6 Heading

<div class="divider"></div>

## Footnote

Let's say you have text that you want to refer with a footnote, you can do that too! This is an example for the footnote number one [^1]. You can even add more footnotes, with link! [^2]

<div class="divider"></div>

## Blockquote

> If you decide to design your own language, there are thousands of sort of amateur language designer pitfalls. -- Guido van Rossum

**NOTE:** This theme does NOT support nested blockquotes.

<div class="divider"></div>

## List Items

1. First order list item
2. Second item

* Unordered list can use asterisks
- Or minuses
+ Or pluses

<div class="divider"></div>

## Code Blocks

{% highlight javascript %}
var s = "JavaScript syntax highlighting";
alert(s);
{% endhighlight %}

{% highlight python %}
import sys
s = "Python syntax highlighting"
print(s)
def run_some_function():
    "Docs..."
    return
{% endhighlight %}

{% highlight css %}
/* css synthax highlighting */
#container {
    float: left;
    margin: 0 -240px 0 0;
    width: 100%;
}
{% endhighlight %}

```
No language indicated, so no syntax highlighting.
But let's throw in a <b>tag</b>.
```

<div class="divider"></div>

## Table

### Table 1: With Alignment

| Tables        | Are                    | Cool  |
| ------------- |:----------------------:| -----:|
| col 1 is      | left-aligned (default) |    $1 |
| col 2 is      |        centered        |   $12 |
| col 3 is      |     right-aligned      | $1600 |

### Table 2: With Typography Elements

Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3

<div class="divider"></div>

## Horizontal Line

The HTML `<hr>` element is for creating a "thematic break" between paragraph-level elements. In markdown, you can create a `<hr>` with any of the following:

* `___`: three consecutive underscores
* `---`: three consecutive dashes
* `***`: three consecutive asterisks

renders to:

___

---

***

<div class="divider"></div>

## Media

### YouTube Embedded Iframe

<iframe width="560" height="315" src="https://www.youtube.com/embed/XOrfVzbbKTo" frameborder="0" allowfullscreen></iframe>

### Image

![CloudKitty](assets/markdown-cheatsheet/cloudkitty-openstack-community.png)

[^1]: Footnote number one.

[^2]: A footnote you can link to - [click here!](https://github.com/openstack/cloudkitty)
