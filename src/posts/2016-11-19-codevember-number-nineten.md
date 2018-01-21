---
title: Codevember Number Nine And Ten
date: '2016-11-19'
category: craft-code
tags:
- codevember
- audio-vis
- new-css-thangs
- audio-api
status: published
---

Phew, there was a break wasn't there! Apparently it's hard to keep up when you're on the road. So I thought there's probably only one thing to do and that's try and do *two* codevembers for the next few days to make up for it.

Let's see how that goes 🤓

### AudioVis #9

NB This one comes with a warning. The way I coded this is highly UNRECOMMENDED. Not only was it a total ball ache, it doesn’t perform well and there are work arounds. It took what felt like days and the result is not amazing. If you’re wondering, I would probably use canvas for an audio vis of this nature in future. Hashtag learning, amiright?

So today I’m going to expand a little on yesterday and take influence from [this crazy gif](http://intothecontinuum.tumblr.com/post/119241330868/maihudson-mathematica-codesn-t-sinn3)

But in my version, I want a shape for each of the low frequencies, the mid frequencies and the high frequencies, that change depending on the level we get back from the analysis.

READMORE

I'm setting a load more custom properties than the previous [codevember](https://codepen.io/Rumyra/pen/yVeoJo), so I'm looping over them in the JS. Things I learnt include:

- We actually don’t need to set those properties in the root block at the top of our CSS if we’re setting them within our JavaScript. They’re set there, so they get passed into the CSS regardless... nuice!
- Maths in CSS is hard, even with nice things like a `calc` function and shiny extras preprocessors like Sass give us. JavaScript is much better as maths, so I found keeping number crunching there is a lot better. Just pass the value you want in the CSS into the custom property.

<p data-height="300" data-theme-id="1345" data-slug-hash="NbdXaE" data-default-tab="html,result" data-user="Rumyra" data-embed-version="2" data-pen-title="Codevember AudioVis #9" class="codepen">See the Pen <a href="https://codepen.io/Rumyra/pen/NbdXaE/">Codevember AudioVis #9</a> by Rumyra (<a href="http://codepen.io/Rumyra">@Rumyra</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

This one was a great learning experience and great experiment, even if the final result wasn't ideally what I was after at the start. I would keep using custom properties to do things like filter effects and glitch's for final VJing rather than modifying multiple DOM elements with them in the future.

### AudioVis #10: Blend Modes 😎

Inspiration:

<figure>
  <img src="http://66.media.tumblr.com/cc6b92fc94e847f5358890da3ed2c5c5/tumblr_nobi29xtOO1sn5m9vo4_1280.gif" />
</figure>

I've actually written about using blend modes for [this audio vis before](http://rumyrashead.com/a-little-thing-about-blends.html). The make up of the visual itself isn't too different code wise to previous ones. I have some DOM elements, I am positioing them, I am animating them, the only extra feature I am encorporating is blend modes on the elements to see what effect that has.

It looks super nice, but with all the DOM elements I have with this one performance isn't so great. I can up it by making sure I add the `will-change` property in the CSS to any elements that have any other properties that are to change.

However I think we should probably move into a better, more performant way of creating and manipulating DOM els for audio vis, don't you?

<p data-height="300" data-theme-id="1345" data-slug-hash="BQprdW" data-default-tab="html,result" data-user="Rumyra" data-embed-version="2" data-pen-title="Codevember AudioVis #10" class="codepen">See the Pen <a href="https://codepen.io/Rumyra/pen/BQprdW/">Codevember AudioVis #10</a> by Rumyra (<a href="http://codepen.io/Rumyra">@Rumyra</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

