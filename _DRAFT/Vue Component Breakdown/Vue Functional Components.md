---
tags: ["#draft", "#vue"]
---
- metadata
	- #draft/updated [[2020-12-02]]

One of the things that I like about Vue is the templating syntax,  it adds just enough sugar ontop of Vue to make the experience of writing markup for components really simple - without getting in your way too often.

One of the other things I like about Vue, is that it knows how to get out of the way and give you back control when you need to.

> Vue recommends using templates to build your HTML in the vast majority of cases. There are situations however, where you really need the full programmatic power of JavaScript. That’s where you can use the render function, a closer-to-the-compiler alternative to templates. [^basics]

For example, one of the limitations of [[Vue Single File Components|Single File Components]]  is that you need to have a single root element.

# Single Root Example
![[Z-Single Root Example#^9dfb9a]]

# Multi Root Example
![[Z-Multi Root Example#^fa5108]]




[^basics]: [Render Functions & JSX](https://vuejs.org/v2/guide/render-function.html)
