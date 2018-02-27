---
layout: post.html
title: "This blog's mini pattern library"
date:   2018-02-13
category: craft-code
tags:
- styleguide
- pattern library
- blog
summary: "A mini pattern library for this blog, to help with content and styling"
---

## Main Header

### Sub Header

##### Small caps

<p class="body__text">This is a regular text size paragraph. Skate ipsum dolor sit amet, judo air boned out Christ air ollie impossible locals. Salad grind masonite indy grab bearings cess slide slappy. Dudesblood smith grind axle hang ten rail slide coper downhill. Tail boneless slide Omar Hassan coping chicken wing axle set.</p>

<p class="article__text">This is a reading paragraph. Hang up rocket air hand rail Kevin Harris kick-nose dude grab. Powerslide opposite footed alley oop air nose-bump Kien Lieu Saran Wrap hip. No comply Neal Hendrix front foot impossible rocket air 1080 downhill hanger stoked.</p>

<p class="article__text">Another reading paragraph, with link, bold/strong, italic/em etc... Pop <a href="#">shove-it powerslide nosegrind drop in gnar</a> bucket. Hand rail <strong>impossible hard flip</strong> skater Jeremy Klein Kevin Harris. Shoveit <em>crailtap grind</em> pressure flip nosegrind. Andrew Reynolds hurricane sketchy layback full-cab bearings. Pump nose camel back alley oop chicken wing.</p>

##### Feature image

{{> picture class="media__feature" alt="Description of image here" highRes="/media/almenac.jpg" url="/media/almenac.jpg" caption="Oh my god it's evil!" }}

##### Regular image

{{> picture alt="Description of image here" highRes="/media/almenac.jpg" url="/media/almenac.jpg" caption="Oh my god it's evil!" }}

##### Tweets

{{> tweet id='963924756373430274' }}

##### Code

<pre><code class="language-javascript">// set up audio context
var audioContext = (window.AudioContext || window.webkitAudioContext);
// create audio class
if (audioContext) {
  // Web Audio API is available.
  var audioAPI = new audioContext();
  } else {
  // Web Audio API is not available. Ask the user to use a supported browser.
  alert("Oh nos! It appears your browser does not support the Web Audio API, please upgrade or use a different browser");
}

// variables
var analyserNode,
  frequencyData = new Uint8Array(256);
const screen = document.querySelector('#screen'),
  allRepeatedEls = document.querySelectorAll('#screen section'),
  totalEls = allRepeatedEls.length;
</code></pre>

##### Blockquotes

>You're decision might be 'Should I use SASS' well the answer to that one is yes but…


##### Lists

- This is a learning experience for me too, so things may stay quite basic. The code will probably _be_ basic, however this does mean it won’t be too complicated for entry level coders.
- I’ll be analysing audio from the microphone, which means I’ll be using the [Media Streams API](https://developer.mozilla.org/en-US/docs/Web/API/Media_Streams_API), which only works over https, you’ll need to view the pens over https://codepen.io
- Things work best in Canary so I’ve noticed, please don’t expect pens to work cross browser. The main end game for me is to integrate them into my VJ software, which I run in a sandboxed environment (my machine, my choice of browser) sux I know!
- I’ll be cross posting all these articles to both my [Codepen Blog](https://codepen.io/Rumyra/posts/published/) and [my personal blog](http://rumyrashead.com/).
- There's a high chance I won't make every single day, but I will try 🙃

1. Raspberry
2. Rambutan
3. Redcurrant
4. Salak
5. Satsuma
6. Soursop
7. Star fruit

