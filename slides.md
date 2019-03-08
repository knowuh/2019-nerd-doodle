
# Doodling with the Canvas API
<div class="left">
  [@knowuh](https://twitter.com/knowuh/)<br/>
  knowuh@gmail.com <br/>
  http://paessel.com/
</div>


<slide>

# What is this talk?

<slide>
<img src="images/spiro-graph-box.jpg"/>

<slide>
<img src="images/spiro-graph-art.jpg"/>

<slide>
# What is this talk?
  * An introduction to creative coding
  * Highlights from *Sketching with Code* course
  * For newbies
  * For cranky old-timers

<slide>
## What happens next?
* An intro to [canvas 2d api](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)
* Using minimal Javascript
* Live mistakes
* Visual tricks
* Art history
* Resources

<slide>
<img src="images/doodle2.png"/>

<slide>
<img src="images/doodle1.png"/>


<slide>
## Why sketch with code?
  * Educational
  * Happy accidents
  * Good for the brain*

</br>
<p class="tiny">* I am not a doctor</p>

<slide>
"I like to think of play not as an activity, but as an attitude, a way of engaging with the world"
<br/>–  *Mitchel Resnick*  (@mres)


<slide>

## Who am I?
  * Developer
  * Student and teacher of visual art
  * Longtime programmer
  * Cheerleader

<slide>
<img src="images/umass-1975.png"/>

<slide>
<img src="images/dec-writer-2.jpg"/>

<slide>
<img src="images/duchamp.png"/>

<slide>
# Early Computer artists.

<vertical>
<div class="artist">
  <div> Michael Noll – Engineer<div>
  <img src="images/noll/noll-2.png"/>
</div>

<vertical>
<div class="artist">
  <div>Frieder Nake – Mathemetician<div>
  <img src="images/nake/nake-1.png"/>
</div>


<vertical>
<div class="artist">
  <div>George Nees – Math & Philosophy<div>
  <img src="images/nees/nees.png"/>
</div>

<vertical>
<div class="artist">
  <div>Vera Molnar – Artist<div>
  <img src="images/mulnar/vera-mulnar-1.png"/>
</div>

<vertical>
<div class="artist">
  <div>Vera Molnar – Artist<div>
  <img src="images/mulnar/vera-mulnar-2.png"/>
</div>

<vertical>
<div class="artist">
  <div>Vera Molnar – Artist<div>
  <img src="images/mulnar/vera-mulnar-3.png"/>
</div>

<slide>
#### VLW / ACG
<img src="images/maeda-mug.png"/>

<slide>
<img src="images/maeda-sketch.png"/>
<slide>
# Teaching Programming
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
## Our Goal
<img src="images/mulnar/vera-mulnar-1.png"/>
<p class="tiny">Point of departure: ~1970</p>

<slide>
## canvas
  <img src="images/canvas-axis.jpg"/>
  <p class="tiny">context</p>
<slide>

## One-page sketch template
```html
  <html>
    <head> … </head>
    <body>
      <canvas width="500" height="500"></canvas>
    </body>
    <script>

      // what we are doing is all in between these script tags
      var canvas = document.querySelector('canvas');
      var context = canvas.getContext('2d');

    </script>
  </html>
```

<slide>
## Square on a canvas
<a href="/example/vm-01" target="sample">demo</a>

```javascript
    // Easy way to draw a rectantangle:  
    context.strokeRect(10, 10, 100, 100);

    // The hard way
    context.strokeStyle = "black";
    context.beginPath();
    context.moveTo(10,10);
    context.lineTo(100,10);
    context.lineTo(100,100);
    context.lineTo(10,100);
    context.lineTo(10,10);
    context.stroke();
```
<vertical>
## 01
<img src="images/1.png"/>

<slide>
## Multiple Squares
<a href="/example/vm-02" target="sample">demo</a>

```javascript
    // Draw a square at x,y of size:
    function drawSquare (xLoc, yLoc, size) {
      context.beginPath();
      context.moveTo(xLoc       ,  yLoc       );
      context.lineTo(xLoc + size,  yLoc       );
      context.lineTo(xLoc + size,  yLoc + size);
      context.lineTo(xLoc       ,  yLoc + size);
      context.closePath();
      context.stroke();
    }

    // draw some squares
    var squareSize = 100;
    drawSquare(10, 10, squareSize);
    drawSquare(120, 10, squareSize);
```
<vertical>
## 02
<img src="images/2.png"/>

<slide>
## Squares on a Grid

<a href="/example/vm-03" target="sample">demo</a>

```javascript
    var squareSize = 140;
    var padding = 10;

    // Draw a square at grid-y grid-y:
    function drawSquare(gridX, gridY) {
      var startX = gridX * (squareSize + padding) + padding;
      var startY = gridY * (squareSize + padding) + padding;
      context.beginPath();
      context.moveTo(startX,               startY);
      context.lineTo(startX + squareSize,  startY);
      context.lineTo(startX + squareSize,  startY + squareSize) ;
      context.lineTo(startX,               startY + squareSize) ;
      context.closePath();
      context.stroke();
    }

    drawSquare(0, 0);
    drawSquare(1, 0);
    drawSquare(2, 1);
    drawSquare(0, 2);
```
<vertical>
## 03
<img src="images/3.png"/>


<slide>
## Loop it
<a href="/example/vm-04" target="sample">demo</a>

```javascript
   // hella squares:
    var x, y;
    var numWide = 4;
    var numTall = 4;
    for(x=0; x < numWide; x++) {
      for(y=0; y < numTall; y++) {
        drawSquare(x,y);
      }
    }
```
<vertical>
## 04
#### *--record scratch--*
<img src="images/4.png"/>

<slide>
## Context & Transforms

<slide>
### Remember this?
<img src="images/canvas-axis.jpg"/>

<slide>
## We can change it with:
* `context.fillStyle=`
* `context.tranlate(…)`
* `context.rotate(…)`
* `context.scale(…)`
* `context.transform(…)`
* `context.restore` 

<vertical>
<img src="images/transforms.jpg"/>

<slide>
## Make it big
<a href="/example/vm-05" target="sample">demo</a>

```javascript
    // Variables:
    var marginScale = 0.9;
    var numColumns = 3;

    function setgridSize() {
      if (canvas.width > canvas.height) {
        gridSize = canvas.height / numColumns;
      }
      else {
        gridSize = canvas.width / numColumns;
      }
    }

    function adjustMargins () {
      var size = gridSize * numColumns;
      var extraSpaceX = canvas.width - size;
      var extraSpaceY = canvas.height - size;
      context.translate(extraSpaceX/2, extraSpaceY/2);
      setgridSize()
    }

    function resize() {
      var {width: w, height: h}  = canvas.getBoundingClientRect();
      canvas.width = w;
      canvas.height = h;
      setgridSize();
      draw();
    }

    window.addEventListener("resize", resize);
```
<vertical>
##### 05
<img src="images/5.png"/>

<slide>
## Moar loops
<a href="/example/vm-06" target="sample">demo</a>
```javascript
    function veraSquare() {
      var i = 0;
      var numSquares = 10;
      var stepSize = 1 / numSquares;
      // sale from  0 to 1 in numSquares steps
      for (i = 0; i <= 1; i += stepSize) {
        context.save();
        context.scale(i, i);
        drawSquare();
        context.restore();
      }
    }

    // Align a drawing function into a grid
    function drawInGrid (gridX, gridY, drawingFunction) {
      var halfGrid = gridSize / 2;
      context.save();
      context.translate(gridX * gridSize + halfGrid, gridY * gridSize + halfGrid);
      context.scale(marginScale, marginScale);
      drawingFunction();
      context.restore();
    }

    // draw all the squares
    function draw () {
      setgridSize();
      adjustMargins();
      context.save();
      var x, y;
      for(x=0; x < numColumns; x++) {
        for(y=0; y < numColumns; y++) {
          drawInGrid(x, y, veraSquare);
        }
      }
      context.restore();
    }
    ```
<vertical>
##### 06
<img src="images/6.png"/>

<slide>
### Imperfectionz & randomnez
<a href="/example/vm-07" target="sample">demo</a>

```javascript
  function randomNudge(gridFraction) {
    var randAmount = gridSize * gridFraction;
    return randAmount - Math.random() * (randAmount/2)
  }

  function drawSquare () {
    var halfGrid = gridSize / 2;
    var wiggleFraction = 0.3;

    var startX = - halfGrid + randomNudge(wiggleFraction) ;
    var startY = - halfGrid + randomNudge(wiggleFraction) ;
    var endX = halfGrid + randomNudge(wiggleFraction) ;
    var endY = halfGrid + randomNudge(wiggleFraction) ;

    context.beginPath();

    context.moveTo(startX, startY);
    context.lineTo(endX,   startY);
    context.lineTo(endX,   endY);
    context.lineTo(startX, endY) ;

    context.closePath();
    context.stroke();
  }
```

<slide>
## VM-08: Parameters and Variations

<slide>
## VM-09: HSLA Colors

<slide>
## VM-11: Radial

<slide>
## VM-12: Animation



<slide>
# Accelerated Art School
  * Sketch.
  * Use arbitrary constraints.
  * Learn about gestalt principles.
  * Some quick tips.

<vertical>
## Sketching:
* On paper.
* Many examples quickly.
* Disposable.
* Generate questions.
* Process not product.

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
* eg: only paint 2" squares
* eg: only 400 pixels
* eg: only black and white

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

<vertical>
## Quick Tips:
  * Currate & crop
  * Contrasting elements
  * Accidents
  * Steal and  **give credit**
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
## Resources: low-friction tools

* [surge](https://surge.sh/) - instantly publish a website
* [code pen](https://codepen.io/) - scratch-pad for websites
* [live  server](https://www.npmjs.com/package/live-server) - quick feedback
* [Vistual Studio Code](https://code.visualstudio.com/) -- nice editor.
* [shader toy](https://www.shadertoy.com/) -- not for beginners

<vertical>
## Resources: inspiration and teachers:

* [Daniel Schiffman's Coding Train](https://www.youtube.com/user/shiffman) - [@shiffman](https://twitter.com/shiffman)
* [@invonvergent](https://twitter.com/inconvergent) [instructions](https://inconvergent.net/#writing)
* [@mxsage](https://twitter.com/mxsage) [instructions](https://www.sagejenson.com/physarum)
* [solving sol](http://solvingsol.com/solutions/) -- Sol Lewitt

<vertical>
## Resources: documentaiton & frameworks

* [MDN Canvas API docs](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D)
* [D3](https://d3js.org/) - SVG & Javascruot visualization toolkit
* [Processing](https://processing.org/) - granpappy of creative coding envs
* [Open Frameworks](https://openframeworks.cc/) -- C++ creative coding
* [ThreeJS](https://threejs.org/) - wrapper for canvas 3D API.

