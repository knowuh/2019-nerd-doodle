
# Doodling with the Canvas API
<div class="left">
  [@knowuh](https://twitter.com/knowuh/)<br/>
  knowuh@gmail.com <br/>
  http://paessel.com/
</div>


<slide>

# What is this talk?

<vertical>
<img src="images/spiro-graph-box.jpg"/>

<vertical>
<img src="images/spiro-graph-art.jpg"/>

<vertical>
# What is this talk?
  * An introduction to creative coding.
  * Highlight real from a class *Sketching with Code*.
  * This talk is for newbies.
  * This talk is for cranky old-timers.

<vertical>
## What is this talk?
* Some visual tricks.
* Some art history.
* Some Javascript.
* An intro to [canvas 2d api](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)
* We use naked Javascript.

<vertical>
## Why sketch with code?
  * To teach and learn programming.
  * To discover things and have fun.
  * For happy accidents.
  * It's good for your brain*.

</br></br>
*not a doctor*

<vertical>
## Why Canvas
  * Javascript is everywhere.
  * More immediate than SVG or WebGL.
  * No Frameworks, no building, single page.


<slide>
"I like to think of play not as an activity, but as an attitude, a way of engaging with the world"
<br/>–  *Mitchel Resnick*  (@mres)

<slide>

## Who am I?
  * A student and teacher of visual art and design.
  * Someone who has been programmg a long time.
  * I want you to make things.

<vertical>
<img src="images/umass-1975.png"/>

<vertical>
<img src="images/dec-writer-2.jpg"/>

<slide>

# Visual hacks
  * Sketch.
  * Use arbitrary constraints.
  * Learn about gestalt principles.
  * Some quick tips.

<vertical>
## Sketching
* Start on paper.
* Create many examples quickly.
* They are disposable.
* Good sketches generate questions.
* Process not product.

<br/><br/>

<span class="fragment">**Sketch**.</span>
<span class="fragment">**All**.</span>
<span class="fragment">**The**.</span>
<span class="fragment">**Time**.</span>

Note:
* Artschool 101
* Not precious.
* Can be code …
<vertical>

## Constraints
By holding some things constant, we focus on the possibilities of the remaining parameters.
* Music
* [Haiku](https://en.wikipedia.org/wiki/Haiku)
* [Dogme films](https://en.m.wikipedia.org/wiki/Dogme_95)
* Only paint in 2" squares.
* Only use 400 pixels.
* Only use black and white.

<vertical>
## Gestlat principles of design
  <div class="left">
    The Gestalt Principles are a set of laws arising from 1920s' psychology, describing how humans typically see objects by grouping similar elements, recognizing patterns and simplifying complex images. Designers use these to engage users via powerful -yet natural- "tricks" of perspective and best practice design standards.
  <div class="left">

<vertical>

## Gestlat principles of design
* Gestalt principles are real. They are grounded in the *mechanics* of human perception.
* Art, design, and [Optical illusions](https://en.wikipedia.org/wiki/Optical_illusion) exploit artifacts of human perception.

<vertical>
## Some gestalt princples are …

* Closure: Our brain fills in gaps.
* Proximity: We group closer-together elements.
* Continuation: We follow lines.
* Similarity: We look for differences and commonality of shape.

<vertical>
<img src="images/proximity.jpg"/>
<vertical>
<img src="images/closure.jpg"/>
<vertical>
## Book about gestalt theory:
* ["Primer of Visual Literacy"](https://www.amazon.com/Primer-Visual-Literacy-Donis-Dondis/dp/0262540290) by Donis A. Dondis.

<slide>
# Artist cheat codes:
  * Currate.
  * Crop.
  * Contrast.
  * Accidents.
  * Fake it.
  * Steal and  **give credit**.
  <br/><br/>
<div>
  <span class="fragment">Make it **Big**.</span>
  <span class="fragment">Make it **red**.</span>
  <span class="fragment">Or make **many** of them.</span>
</div>

Note:
* Take 1000 photographs, and choose one.
* Crop: Your initial framing will be wrong. Direct attention. Cut out noise.
* Constrast: What is the focus, what will stand out?
* Accidents: investigate, celebrate, incorporate your accidents.
* Fake it: Its art. Its all fake. Their is no purity, its all for show.

<slide>
# Programming hacks
* Reduce friction.
* Wishful programming.
* Get *something* on the screen ASAP.
* Generalize.
* HSLA color.
* Google MDN.

<vertical>
## Wishful programming
```

  drawSquare(10, 10, 100)
  drawSquare(120, 10, 100)
  drawSquare(240, 10, 100)

  function drawSquare (x, y, size) {
    // Not sure what to do yet!
    console.log('drawing a square:', x, y, size)
  }


```


<slide>
# Finding Inspiration
From the earliest computer artists.

<vertical>
<div class="artist">
  <div> Michael Noll – Engineer<div>
  <img src="images/noll/noll-1.png"/>
</div>

<vertical>
<div class="artist">
  <div> Michael Noll – Engineer<div>
  <img src="images/noll/noll-2.png"/>
</div>

<vertical>
<div class="artist">
  <div> Michael Noll – Engineer<div>
  <img src="images/noll/noll-3.png"/>
</div>

<vertical>
<div class="artist">
  <div>Frieder Nake – Mathemetician<div>
  <img src="images/nake/nake-1.png"/>
</div>

<vertical>
<div class="artist">
  <div>Frieder Nake – Mathemetician<div>
  <img src="images/nake/nake-2.png"/>
</div>

<vertical>
<div class="artist">
  <div>Frieder Nake – Mathemetician<div>
  <img src="images/nake/nake-3.png"/>
</div>


<vertical>
<div class="artist">
  <div>Georg Nees – Mathematics & Philosophy<div>
  <img src="images/nees/nees.png"/>
</div>

<vertical>
<div class="artist">
  <div>Vera Molnar – Artist & Designer<div>
  <img src="images/mulnar/vera-mulnar-1.png"/>
</div>

<vertical>
<div class="artist">
  <div>Vera Molnar – Artist & Designer<div>
  <img src="images/mulnar/vera-mulnar-2.png"/>
</div>

<vertical>
<div class="artist">
  <div>Vera Molnar – Artist & Designer<div>
  <img src="images/mulnar/vera-mulnar-3.png"/>
</div>


<slide>
<img src="images/mulnar/vera-mulnar-1.png"/>

<!-- <div class="artist">
  <div>Vera Molnar – Artist & Designer<div>
  <img src="images/mulnar/vera-mulnar-1.png"/>
</div> -->

<slide>
  <img src="images/canvas-axis.jpg"/>


<slide>
## VM-01: Squares on a canvas
```
<html>
  <head> … </head>
  <body> … <canvas width="500" height="500"></canvas> </body>
  <script>
    // Where to draw:
    var canvas = document.querySelector('canvas');
    var context = canvas.getContext('2d');

    // Draw a square:
    context.strokeStyle = "black";
    context.beginPath();
    context.moveTo(10,10);
    context.lineTo(100,10);
    context.lineTo(100,100);
    context.lineTo(10,100);
    context.lineTo(10,10);
    context.stroke();

    // cheater way:  
    context.strokeRect(10, 10, 100, 100);

  </script>
</html>
```
<slide>
## VM-02: Reuse.
```javascript
    // Draw a square at xy:
    function drawSquare (xLoc, yLoc, size) {
      context.beginPath();
      context.moveTo(xLoc       ,  yLoc       );
      context.lineTo(xLoc + size,  yLoc       );
      context.lineTo(xLoc + size,  yLoc + size);
      context.lineTo(xLoc       ,  yLoc + size);
      context.closePath();
      context.stroke();
    }

    // draw 4 sqaures
    var squareSize = 100;
    drawSquare(10, 10, squareSize);
    drawSquare(120, 10, squareSize);
    drawSquare(230, 10, squareSize);
    drawSquare(340, 10, squareSize);
```

<slide>
## VM-03: Multiple Squares

<slide>
## VM-04: How many / how large?

<slide>
## 04b: Intermission: Context & Transforms.

## VM-05: Make it big.
## VM-06: Futher Iteration.
## VM-07: Imperfections and randomnesss
## VM-08: Parameters and Variations
## VM-09: HSLA Colors
## VM-11: Radial
## VM-12: Animation
# Collecting code for reuse
# [Other examples time permitting]
# Artists and Educators
# Technical Resources


## META:
10 main topics.  No more than 4 minutes per topic (average).
19 slides.  ~2 minutes per slide.

### Unsorted Notes

[Apple II](https://www.scullinsteel.com/apple2/)

[vera molnar](https://en.wikipedia.org/wiki/Vera_Moln%C3%A1r
She is considered a pioneer of computer art.

Vera Molnar – Artist & Designer
Michael Noll – Engineer
Frieder Nake – Mathemetician
Georg Nees – Mathematics & Philosophy



Sol LeWitt, wall drawing, in May 2012 during the Wall Drawings from 1968 to 2007 Sol LeWitt retrospective exhibition at the Centre Pompidou-Metz, Metz, France.
In 1968, LeWitt began to conceive sets of guidelines or simple diagrams for his two-dimensional works drawn directly on the wall. According to the principle of his work, LeWitt's wall drawings are usually executed by people other than the artist himself. Even after his death, people are still making these drawings.[19] He would therefore eventually use teams of assistants to create such works. Writing about making wall drawings, LeWitt himself observed in 1971 that "each person draws a line differently and each person understands words differently"
http://solvingsol.com/solutions/
