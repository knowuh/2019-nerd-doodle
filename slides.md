
# Doodling with the Canvas API
@knowuh
knowuh@gmail.com http://paessel.com/

<slide>

# What is this talk?
  * A light introduction to the practice of creative coding.
  * The cliff notes for a class "Sketching with Code"
  * This talk is for newbies.
  * This talk is for cranky old-timers.


<vertical>
## What is this talk?
* I will give you cheat codes!
* We find out about [canvas 2d api](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)
* We will learn some art history.
* We use plain-old Javascript.

<vertical>
## Why should I?
  * To try programming.
  * To engage in visual explorations.
  * It's good for your brain*.

</br></br>
*I am not a doctor*


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
  * I studied visual art and design.
  * I have been programming for 35+ years.
  * I want you to make things.

<slide>

# Visual hacks
  * Doodle and sketch.
  * Use arbitrary constraints.
  * Learn about gestalt principles.
  * Some quick tips.

<vertical>
## Sketch for ideas
* Use a pencil.
* Its not precious.
* Notice what interests you.
* Ask questions.

<br/><br/>

<span class="fragment">**Sketch**.</span>
<span class="fragment">**All**.</span>
<span class="fragment">**The**.</span>
<span class="fragment">**Time**.</span>


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
## Some gestalt princples are..

* Closure: Our brain fills in gaps.
* Common Fate: We group elements that move the same direction.
* Common Region: We group elements in the same perceived enclosure.
* Proximity: We group closer-together elements.
* Continuation: We follow lines.
* Similarity: We look for differences and commonality of shape.

<vertical>
## Book about gestalt theory:
* ["Primer of Visual Literacy"](https://www.amazon.com/Primer-Visual-Literacy-Donis-Dondis/dp/0262540290) by Donis A. Dondis.

<slide>
# Cheat codes:
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
* Get *something* on the screen ASAP.
* Reduce friction.
* Wishful programming.
* Generalize.
* Clean up.
* HSLA color.
* Google MDN.

<vertical>
## Wishful programming
```
  var drawSquare = function (x, y, size) {
    // Not sure what to do yet!
    console.log('drawing a square:', x, y, size)
  }

  var drawTheSquares = function () {
    drawSquare(10, 10, 100)
    drawSquare(120, 10, 100)
    drawSquare(240, 10, 100)
  }

  drawTheSquares()
```

<vertical>
## Generalize
```
  var squareSize = 100
  var borderSize = 10

  var drawSquare = function (column, row) {
    var x = column * (squareSize + borderSize);
    var y = row * (squareSize + borderSize);
    drawSquareAtXY(x, y);
  }

  var drawTheSquares = function () {
    drawSquare(0, 0)
    drawSquare(1, 1)
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
<div class="artist">
  <div>Vera Molnar – Artist & Designer<div>
  <img src="images/mulnar/vera-mulnar-1.png"/>
</div>


<slide>
## VM1: Draw a some squares on a canvas
```
<html>
  <head>
    <title>Vera Molnar 01</title>
    <style>
      // ...
    </style>
  </head>
  <body>
    Vera Molnar 01
    <canvas width="500" height="500"></canvas>
  </body>
  <script>
    // Get some place to draw:
    var canvas = document.querySelector('canvas');
    var context = canvas.getContext('2d');

    // draw one square:
    context.strokeStyle = "black";
    context.beginPath();
    context.moveTo(10,10);
    context.lineTo(100,10);
    context.lineTo(100,100);
    context.lineTo(10,100);
    context.lineTo(10,10);
    context.stroke();

  </script>
</html>
```
<slide>
## VM2: Clean it, make it reusable.
## VM3: Multiple Squares & placement
## VM4: How many / how large?
## VM5: Nested structures [-]
## VM6: Imperfections and randomnesss
## VM7: Parameters and Variations
## VM8: Transformational Yoga
## VM9: Make it yours
# Animation
# Collecting code for resuse
# [Other examples time permitting]
# Artists and Educators
# Technical Resources


META:
10 main topics.  No more than 4 minutes per topic (average).
19 slides.  ~2 minutes per slide.

### Unsorted Notes

[vera molnar](https://en.wikipedia.org/wiki/Vera_Moln%C3%A1r
She is considered a pioneer of computer art.

Vera Molnar – Artist & Designer
Michael Noll – Engineer
Frieder Nake – Mathemetician
Georg Nees – Mathematics & Philosophy



Sol LeWitt, wall drawing, in May 2012 during the Wall Drawings from 1968 to 2007 Sol LeWitt retrospective exhibition at the Centre Pompidou-Metz, Metz, France.
In 1968, LeWitt began to conceive sets of guidelines or simple diagrams for his two-dimensional works drawn directly on the wall. According to the principle of his work, LeWitt's wall drawings are usually executed by people other than the artist himself. Even after his death, people are still making these drawings.[19] He would therefore eventually use teams of assistants to create such works. Writing about making wall drawings, LeWitt himself observed in 1971 that "each person draws a line differently and each person understands words differently"
http://solvingsol.com/solutions/
