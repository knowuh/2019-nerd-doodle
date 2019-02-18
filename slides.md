

# Why should I do this?
  * To try programming.
  * To engage in visual explorations.
  * Its good for you (*)
“I like to think of play not as an activity, but as an attitude, a way of engaging with the world" – @MRES

# Who is talking
  * I studied visual art and design.
  * I have been programming for 35+ years.
  * I love inspiring people to make and share for making sake.

# Visual hacks
  * Sketch a lot.
    * Looking at things.
    * Notice what interests you.
    * Play with pencil and paper.
    * MANY sketches.
  * Constraints.
    These are an important creative fuel.
    By holding some things constant, we focus on the possibilities of the remaining parameters.
    Music, poetry, all have various established formal constraints.
    * Examples:
      * [Haiku](https://en.wikipedia.org/wiki/Haiku)
      * [Dogme films](https://en.m.wikipedia.org/wiki/Dogme_95)
      * Only sketch in 2" squares.
      * Only use 250,000px
      * Only use black and white.
  * Learn about gestlat principles and human perception.
    * The Gestalt Principles are a set of laws arising from 1920s’ psychology, describing how humans typically see objects by grouping similar elements, recognizing patterns and simplifying complex images. Designers use these to engage users via powerful -yet natural- “tricks” of perspective and best practice design standards.
    * Gestalt principles as design concepts grounded in the mechanics of human perception.
    * Art, design, and [Optical illusions](https://en.wikipedia.org/wiki/Optical_illusion) typically exploit these same mechanism.
    * Some specific examples of gestalt princples are:
      * Closure: We automatically fill in gaps
      * Common Fate: We group elements that move the same direction.
      * Common Region: We group elements in the same perceived enclosure.
      * Prägnanz: We percieve simpler objects first, or in favor of complex ones.
      * Proximity: We group closer-together elements.
      * Continuation: We follow lines.
      * Similarity: We look for differences and commonality of shape.
    * Recommended book: ["Primer of Visual Literacy"](https://www.amazon.com/Primer-Visual-Literacy-Donis-Dondis/dp/0262540290) by Donis A. Dondis.
  * Quick visual art hacks that *always* work:
    * Currate: Take 1000 photographs, and choose one.
    * Crop: Your initial framing will be wrong.
    * Less is more: pay attention whitespace and visual complexity.
    * Legibility: mind contrast.
    * Make it *big*, make it *red* , or make *lots of them*.
    * Cheat. This is art. Its all fake. Break. The. Rules.
    * Steal. Get inspired by others, but GIVE CREDIT.

# Programming hacks
# Finding Inspiration
# Example: Vera Molnar
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
    var canvas = document.querySelector('canvas');
    var context = canvas.getContext('2d');
    context.strokeStyle = "black";
    context.beginPath();
    context.moveTo(10,10);
    context.lineTo(100,10);
    context.lineTo(100,100);
    context.lineTo(10,100);
    context.lineTo(10,10);
    context.stroke();
    context.beginPath();
    context.moveTo(110,10);
    context.lineTo(200,10);
    context.lineTo(200,100);
    context.lineTo(110,100);
    context.lineTo(110,10);
    context.stroke();
  </script>
</html>
```
## VM2: Clean it up, do some magic.
## VM3: Multiple Squares & placement
## VM4: How many / how large?
## VM5: Nested structures [-]
## VM6: Imperfections and randomness
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
