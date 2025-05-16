---
layout: ../../layouts/MarkdownPostLayout.astro
title: "Code Blocks in Markdown"
pubDate: 2022-07-01
description: "How to use code blocks in an Astro Markdown file"
author: "David Strube"
image:
  url: "https://docs.astro.build/assets/rose.webp"
  alt: "The Astro logo on a dark background with a pink glow."
tags: ["astro", "markdown", "programming"]
---

An important step in becoming a developer is writing about what you're learning. I'm super excited about Astro, but I was concerned about whether or not it could display code blocks with Javascript, if Astro is designed to eliminate as much Javascript as possible.

## Solution

Triple ticks to the rescue:

```js
console.log("Hello World!");
```

This is a really simple way to start discussing the code concepts I've been learning.

Here's a simple example from the Secrets of the Javascript Ninja 2nd Edition. Note that the assert function is created by the author and the definition is not listed here

```js
function Ninja() {
  this.skulk = function () {
    return this;
  };
}

var ninja1 = new Ninja();
var ninja2 = new Ninja();

assert(ninja1.skulk === ninja1, "The 1st ninja is skulking");
assert(ninja2.skulk === ninja2, "The 2nd ninja is skulking");
```

The context of this example is to show how a function can be assigned to an object instance. Here, the Ninja function can be invocted as a constructor using the "new" keyword. When it does, it creates a new object, passes that into the function as the the "this" parameter as the function context, the new object has the function "skulk" attached as a method, and then the object is returned from the constructor.

When "ninja1.skulk()" is called, it returns the context of the method, which in this case is the object created: either ninja1, or ninja2.
