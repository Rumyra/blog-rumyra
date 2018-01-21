---
title: A Little Thing About Blends
date: '2016-10-20'
category: craft-code
tags:
- css
- blend-modes
status: published
---

I learnt a little thing whilst playing around with [CSS blend modes](https://developer.mozilla.org/en-US/docs/Web/CSS/mix-blend-mode) this morning which I thought I should share.

I was just making a little visual:

<figure class="media-feature">
  <img src="/media/visualPlain.jpg" />
  <figcaption>Visual without blend modes</figcaption>
</figure>

And I thought, wouldn't it be lovely to have some CSS blend modes to add some 🤗 

So I wrote a little Sass @each to try them out. Firstly here's the HTML of one _flower_, of which I have nine.

<pre><code class="language-html">&lt;section>
  &lt;div>&lt;i>&lt;/i>&lt;/div>
  &lt;div>&lt;i>&lt;/i>&lt;/div>
  &lt;div>&lt;i>&lt;/i>&lt;/div>
  &lt;div>&lt;i>&lt;/i>&lt;/div>
  &lt;div>&lt;i>&lt;/i>&lt;/div>
  &lt;div>&lt;i>&lt;/i>&lt;/div>
  &lt;div>&lt;i>&lt;/i>&lt;/div>
  &lt;div>&lt;i>&lt;/i>&lt;/div>
  &lt;div>&lt;i>&lt;/i>&lt;/div>
  &lt;div>&lt;i>&lt;/i>&lt;/div>
  &lt;div>&lt;i>&lt;/i>&lt;/div>
  &lt;div>&lt;i>&lt;/i>&lt;/div>
&lt;/section>  
</code></pre>


A bit gumphy, but rotating and sizing and well yeh... Then the @each

<pre><code class="language-css">@each $num, $blendMode in 
  ( 1:overlay, 2:darken, 3:color-dodge, 4:color-burn, 5:hard-light, 6:difference, 7:hue, 8:saturation, 9:luminosity ) {
  #ohFour #screen section:nth-of-type(#{$num}) i {
    mix-blend-mode: $blendMode;
  }
}
</code></pre>
  

There are more modes than this, but I've only got 9 sections and we can subsitute.

Spot the obvious mistake. By putting the blend mode onto the `i` element, we see no difference. As per the spec:

>The mix-blend-mode CSS property describes how an element's content should blend with the content of the element's direct parent and the element's background.

So let's back up and put it on the `section`. Phew, there we go that's better.

<figure class="media-feature">
  <img src="/media/visualFirstBlend.jpg" />
  <figcaption>Visual with first blend modes</figcaption>
</figure>

<hr />  

## Slow rendering and FPS Monitor

Now we could have put the blend mode on the `div` elements. However the performance changes dramtically.

What with the audio analysis, amount of DOM elements and animation *with* these blend modes is pretty trying in Chrome. I'm getting about 5fps when on the `div`. Whereas on the `section` I run at about 15fps. Not amazing, but I wonder who would notice in a club.

If you want to check out the FPS monitor in Chrome Dev Tools, just open them, click on the menu at the top right (three vertical dots), choose _'More tools'_ -> _'Rendering settings'_ and check _'FPS Meter'_.

## Different Blend Modes

Yeh I know you see it too. We've lost the little _flowers_ in the centre. Some blend modes don't like being blended against black. Let's change that @each up a bit!

<figure class="media-feature">
  <img src="/media/visualSecBlend.jpg" />
  <figcaption>Visual with second blend modes</figcaption>
</figure>

I'm gonna be having some fun with CSS Blend Modes! Chroma key on video anyone?


