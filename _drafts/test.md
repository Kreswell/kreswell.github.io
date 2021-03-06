---
layout: post
title: Test Post
subtitle: Test page in "post" layout.
image: /img/bubble-chamber-bebc.jpg
bigimg: [/img/Fermilab_Spring.jpg, /img/blue_ridge.jpg, /img/Atractor_Poisson_Saturne.jpg]
gh-repo: Kreswell/kreswell.github.io
gh-badge: [star, fork, follow]
tags: [test, more different test]
---

This is a test page to see if I understand how to create a new post, and to test out several of the different options and tools. I'm including pretty much every header tag I know of.

## Basic Markdown

Basic markdown features, such as **bold**, *italic*, tables, lists, etc. are 

## Images
Here's a picture of my dog.

![Sammy in a chair](/img/Sammy_in_a_chair.jpg "Sammy")

Here's the same picture at a fixed, smaller size.

<img src="/img/Sammy_in_a_chair.jpg" width="250">

And here's the XKCD from today, as a test of including an image from an external source.

![XKCD 2081](https://imgs.xkcd.com/comics/middle_latitudes.png)

## Embedded Content
It looks like I can embed content with an iframe, but getting auto-sizing and other iframe features to work is tricky. I think I need to better understand where the page gets styling info from.

Here's a video from Vi Hart about Fibonacci numbers and golden spirals.

<iframe width:560 height:315 src="https://www.youtube.com/embed/ahXIMUkSXX0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Here's a Google document. It should be viewable, but not editable, on the page.

<iframe width:560 height:720 src="https://docs.google.com/document/d/e/2PACX-1vQ_WmJlvgpjr0CSlIdDvIUgHlc7ZKBVz55essX_6J-ZDuFlNxfBTYbEgfuj1y0nHI987n6spnuQy3yP/pub?embedded=true"></iframe>

## Javascript

Buttons can be embedded in the usual html format.

<button type="button" onclick="myfunc()">Click to show the date.</button>
<p id='date'></p>
<script >
  function myfunc()
  {
    document.getElementById('date').innerHTML = Date();
  }
</script>

## Equations

This is one of the big things I want to get working. I want a fast, easy way to format equations, ideally with the full $\LaTeX$ mathtools functionality, and inline $\LaTeX$ formatting, or something nearly equivalent.

{: .box-note}
**Edit:** I've added MathJax, so now equations render correctly. See [this post](/2018-12-12-MathJaxTest).

<p>It looks like Github flavored markdown doesn't recognize $\LaTeX$, but maybe if I explicitly put it inside an html paragraph block, it will. This paragraph is in one.</p>

This paragraph is not in an html block, but the following equation is.

<p>$$
  \sum_{n=0}^{\infty}\frac{1}{2^n} = 2
$$</p>

And this is the same one with slightly different line breaks around the escape characters.

<p>$$ \sum_{n=0}^{\infty}\frac{1}{2^n} = 2 $$</p>

## Tags

The "test" tag already existed in the example pages that I forked this repository from. I've deleted all of the example posts except for ["Test Markdown"](2015-02-28-test-markdown). I've also added a new tag called "more different test". Let's see if it automagically updates the [tags.html](tags.html) file. 

