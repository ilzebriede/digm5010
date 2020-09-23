## ONLINE JOURNAL

This Journal is a way to document my research directions and practical attempts in **Digm5010 Foundations of Digital Media** course, delivered by ***Graham Wakefield*** at York University, Digital Media department. This online resource will not only serve as a place to gather, trace and archive ideas, store written academic articles and lists of literature. This Journal will directly support and help to establish the main research questions for my PhD research.


> **Week#1**

*Objectives*:
Familiarise ourselves with history of Machines and Cellular Automata. Practice JavaScript code using different libraries: Canvas,vectors and matrices. Post results in this journal. Maeda approach: Given a point in space over a finite rectangular area, create a parametric drawing that illustrates **repetition**, **variety**, or **rhythm**.

Example 1

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

##**Theme: Complexity**
######Keywords: *interactions*, *feedback loops*, *constant change*, *complex relationships*, *dangers of disruption caused by interconnectedness*.  

The bottom line and wake up call is this:
**The pandemic results from the same causes as the climate crisis.**



Main questions to investigate:  

1) How can we live in this globalised multiconnected world while still maintaining natural balance and preserve our environment.
2) What practices can we develop to foster caring and gentle interconnectedness, embracing differences and welcoming change; that is our new reality this world experiencing right now.
3) How can we converse in the same language while speaking in different tongues, cherishing unique perspectives and cultural differences. How can we open to diversity without homogenising and erasing minority.
4) How can we bridge experiences learned in the past with potential future narratives and make the best possible solution for today.


---
Solutions and possible approaches:
* long term visions
* use interconnectivity to our advantage
* listen to marginalised and suppressed voices and learn how to forge better and more robust, and meaningful relationships



__What would art look like if it would be created taking these   aspects as the main guidelines and inspiration?__  

[List of papers and publications]() pertaining to this topic.




