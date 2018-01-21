---
title: Codevember Number Eight
date: '2016-11-10'
category: craft-code
tags:
- codevember
- audio-vis
- new-css-thangs
- audio-api
status: published
---

### Part Two: Random Cool New Features

So this next section I did ponder for a while. I could take you straight on to a much better way of creating visuals within the DOM, but before I do that I want to introduce some new features we have in simple CSS that can really help our visuals later down the track. Our inspiration for this set is a little tumblr called [Archery: Into the Continuum](http://intothecontinuum.tumblr.com/). Here I want to take inspiration from some of these random gifs, not exactly replicate them.

So first up, this gif:

<figure>
  <img src="http://67.media.tumblr.com/e829a18961367c45baf1c2dcbcea47a0/tumblr_mr6p8hVjSQ1qfjvexo2_r1_500.gif" />
</figure>

### Custom Properties

_Or_ JavaScript all up in your CSS

And the much talked about CSS Custom properties. ✨💥💜 We can really use these to our advantage when doing audio vis work as we can reference them directly in our JavaScript and basically update our CSS in realtime.

READMORE

Custom properties are declared at the start of your CSS with a `:root` block and can be references throughout your CSS, much like (but not entirely) pre-processor variables. So instead of declaring properties that make sense as far as styling goes, I’m going to be changing them within my JavaScript, so it makes sense to name them something a little more explicit.

For this we’ll create a `—level` property, and just grab one of the items of the `frequencyData` array and pipe it in. This is where the magic happens:

<pre><code class="language-css">:root {
  --level: 1;
}</code></pre>

<pre><code class="language-javascript">document.documentElement.style.setProperty('--level', frequencyData[10]/255);
</code></pre>
  

This —level property will now update _*within our  css*_. Oh. My. Gawd. I know right… 😱

Magic!

So if we use it on the opacity for instance:

<pre><code class="language-css">i {
  opacity: var(--level);
}</code></pre>

Boom! Opacity of `i` updated! In real time, in our CSS.

I know - all the wows!

<p data-height="300" data-theme-id="1345" data-slug-hash="yVeoJo" data-default-tab="html,result" data-user="Rumyra" data-embed-version="2" data-pen-title="yVeoJo" class="codepen">See the Pen <a href="https://codepen.io/Rumyra/pen/yVeoJo/">yVeoJo</a> by Rumyra (<a href="http://codepen.io/Rumyra">@Rumyra</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>