---
title: Codevember Number Four
date: '2016-11-05'
category: craft-code
tags:
- codevember
- audio-vis
- simple-html-css
- audio-api
status: published
---

We're in it for the long haul - so we're still using the same technique. Stick with me - come next week, I'll be looking at some different, new shiny things and the week after the same. Over the next month we shall learn some great audio vis techniques together. These ones aren't bad btw - they may just not be 'wow' juuuussstt yet 🙃

This is my inspiration for today’s pen: Bridget Riley's Quiver 3.

<figure>
  <img src="/media/bridgetQuiver.jpg" />
  <figcaption>Bridget Riley : Quiver 3</figcaption>
</figure>

I really like this one, although it took a few tricks to get the triangles looking and positioned right. And I even didn't replicate the curved edges particularly. Later on in this series I'm going to explore different techniques and hopefully find better ways of creating shapes like these (SVGs anyone?).

READMORE

The only big difference here is I’m jumping up the frequencies by 4 steps at a time, as there’s only 40 elements.

Also, I'm only showing elements (or setting an opacity more than zero) when the frequency velocity hits over 50.

<pre><code class="language-javascript">if (freqVol > 50) {
  allRepeatedEls[i].style.opacity = freqVol/150;
} else {
  allRepeatedEls[i].style.opacity = 0;
}
</code></pre>

Tweaked for [Witness the Fitness by Roots Manuva](https://www.youtube.com/watch?v=zN226CmaNcI)
