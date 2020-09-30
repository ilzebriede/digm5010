## ONLINE JOURNAL

This Journal is a way to document my research directions and practical attempts in **Digm5010 Foundations of Digital Media** course, delivered by ***Graham Wakefield*** at York University, Digital Media department. This online resource will not only serve as a place to gather, trace and archive ideas, store written academic articles and lists of literature. This Journal will directly support and help to establish the main research questions for my PhD research.


> **Week#1**

*Objectives*:
Familiarise ourselves with history of Machines and Cellular Automata. Practice JavaScript code using different libraries: Canvas,vectors and matrices. Post results in this journal. Maeda approach: Given a point in space over a finite rectangular area, create a parametric drawing that illustrates **repetition**, **variety**, or **rhythm**.

Example 1

<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="js,result" data-user="Ka-Vi" data-slug-hash="OJNwBRw" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="digm5010_week1_canvas-rain">
  <span>See the Pen <a href="https://codepen.io/Ka-Vi/pen/OJNwBRw">
  digm5010_week1_canvas-rain</a> by ilzebriede (<a href="https://codepen.io/Ka-Vi">@Ka-Vi</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>
![Raining Canvas](https://raw.githubusercontent.com/ilzebriede/digm5010/gh-pages/images/Raining_canvas.png)

[Link to my codepen](https://codepen.io/Ka-Vi/pen/OJNwBRw)

```Javascript
// This code is based on Graham's @grrrwaaa class example Yellowtails
// https://codepen.io/grrrwaaa/pen/rNevzbL?editors=0010

const canvas = document.getElementById("screen");
const ctx = canvas.getContext("2d");
const width = canvas.width,
  height = canvas.height;

let mouse = {
  x: 0,
  y: 0,
  isDown: false
};

let marks = [];
let currentMark; // = undefined

function update() {
  for (let mark of marks) {
    for (let p of mark) {
      p.y += Math.random();
      p.x == Math.random();
    }
  }
}

function draw() {
  update();

  // clear background
  for (let mark of marks) {
    if (mark.length) {
      ctx.beginPath();
      ctx.moveTo(mark[0].x, mark[0].y);
      for (let i = 1; i < mark.length; i++) {
        ctx.lineTo(mark[i].x, mark[i].y);
      }
      ctx.stroke();
      ctx.lineWidth = 0.1;
    }
  }

  window.requestAnimationFrame(draw);
}

window.requestAnimationFrame(draw);

canvas.addEventListener("mousemove", function (event) {
  mouse.x = event.clientX;
  mouse.y = event.clientY;

  if (mouse.isDown && currentMark) {
    currentMark.push({ x: mouse.x, y: mouse.y });
  }
});

canvas.addEventListener("mousedown", function (event) {
  currentMark = [];
  marks.push(currentMark);
  mouse.isDown = true;
});
canvas.addEventListener("mouseup", function (event) {
  currentMark = null;
  mouse.isDown = false;
});
```

> **Week#2**

*Objectives*:
Continue work with Javascript and mutate more sketches, and/or create an *interesting* (define "interesting") random programs using codepen.io. Start with Literature Review assignment (Step 1).

> **Week#3**

**Theme: Complexity**

Keywords: *interactions*, *feedback loops*, *constant change*, *complex relationships*, *dangers of disruption caused by interconnectedness*.  

The bottom line and wake up call is this:
**The pandemic results from the same causes as the climate crisis.**



Main questions to investigate:  

1) How can we live in this globalised multiconnected world while still maintaining natural balance and preserve our environment.
2) What practices can we develop to foster caring and gentle interconnectedness, embracing differences and welcoming change; that is our new reality this world experiencing right now.
3) How can we converse in the same language while speaking in different tongues, cherishing unique perspectives and cultural differences. How can we open to diversity without homogenising and erasing minority.
4) How can we bridge experiences learned in the past with potential future narratives and make the best possible solution for today.


Solutions and possible approaches:  

* long term visions
* use interconnectivity to our advantage
* listen to marginalised and suppressed voices and learn how to forge better and more robust, and meaningful relationships
* see emergence as global phenomena (pandemic, evolution, embedded response mechanisms)

`What would art look like if it would be created taking these   aspects as the main guidelines and inspiration?`
---

List of papers and publications.

**Complexity / Emergence**

The source of disorganized complexity is the large number of parts in the system of interest, and the lack of correlation between elements in the system.
“…acknowledgment of the role of chance and indeterminacy in shaping the living world around us. .. notion that the natural world is a compromise between opposing tendencies toward order and disorder.” (Ulanowicz, p.8)



* Johnson, Steven. Emergence: The Connected Lives of Ants, Brains, Cities, and Software. Simon and Schuster, 2012.
* Papastergiadis, Nikos. Complex Entanglements: Art, Globalization and Cultural Difference, London. Rivers Oram,  2003
* Ulanowicz, Robert E. Ecology: The Ascendant Perspective, Columbia University Press, 1997.
* Volkart, Yvonne. Does Art Make a Difference? Technologies of the Ecological After the Antropocene. Article in the book Virtualities and Realities, Pasa Smite, Raitis Smits (eds.). Riga: RIXC, 2019. 
* Sommerer, Christa, and Laurent Mignonneau. “Modeling the Emergence of Complexity: Complex Systems, the Origin of Life and Interactive On-Line Art.” Leonardo32.2 (2002): 161-169
* Burroughs S. W., and Brion Gysin. The Third Mind. New York: The Viking Press, 1978.

**Patterns - computer generated, ornamental fork art, physiological phenomena**

Pattern/Ornament: ways to abstract the nature and natural phenomena?
Embodied, shared phenomena : Purkinje cell and tree in nature (similar shape) 
"The phosphenes seem like universal shapes or what the German psychologist Heinrich Kluver in his research on mescaline labelled "form constants"; elementary feautures of the nervous system that we may be hardwired to perceive. lattices, circles, crossed-out squares, undulating lines, curly cues, zigzags, fork-like shapes, matrices of points, and rows of dots." (Salter 2015, p.207)

* Grzegorz Kępisty, “Generative art: reaction-diffusion and Chladni figures.” 2020. PDF from Research Gate
* Salter Chris, Alien Agency. MIT press, 2015.
* Prusinkiewicz P., Aristid Lindernmayer. The Algorithmic Beauty of Plants. Electronic version available online. 2004. (http://algorithmicbotany.org/papers/abop/abop.pdf)

**Human-Computer, one-another, sketching new languages**

* Ascott, Roy. Telematic Embrace. Visionary theories of art, technology, and consciousness. University of California Press, 2003.
* Licklider, J. C. R. “Man-Computer Symbiosis.” IRE Transactions on Human Factors in Electronics,
volume HFE-1 (1960): 4-11
* Vortex. Visual Aural Textual. One Language. Robert Appleton interview by Majid Abassi. AGI, 2011





