## ONLINE JOURNAL

This Journal is a way to document my research directions and practical attempts in **Digm5010 Foundations of Digital Media** course, delivered by ***Graham Wakefield*** at York University, Digital Media department. This online resource will not only serve as a place to gather, trace and archive ideas, store written academic articles and lists of literature. This Journal will directly support and help to establish the main research questions for my PhD research.


> **Week#1**

*Objectives*:
Familiarise ourselves with history of Machines and Cellular Automata. Practice JavaScript code using different libraries: Canvas,vectors and matrices. Post results in this journal. Maeda approach: Given a point in space over a finite rectangular area, create a parametric drawing that illustrates **repetition**, **variety**, or **rhythm**.

Example 1

<div class="codepen" data-height="590" data-theme-id="light" data-default-tab="js,result" data-user="Ka-Vi" data-slug-hash="OJNwBRw" data-prefill='{"title":"digm5010_week1_canvas-rain","tags":[],"scripts":[],"stylesheets":[]}'>
  <pre data-lang="html">&lt;style type="text/css">
  canvas {
    border: 0.5px solid grey;
  } &lt;/style>
&lt;canvas id="screen" width="500" height="500">&lt;/canvas>
</pre>
  <pre data-lang="css">body {
  margin: 0px;
}</pre>
  <pre data-lang="js">// This code is based on Graham's @grrrwaaa class example Yellowtails
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
      for (let i = 1; i &lt; mark.length; i++) {
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

//note to myself: try and add different colour variations, so that each canvas layer differs from previous one. Also, try to add sound component</pre></div>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script><br/>


> **Week#2**

*Objectives*:
Continue work with Javascript and mutate more sketches, and/or create an *interesting* (define "interesting") random programs using codepen.io. Start with Literature Review assignment (Step 1).

> **Week#3**

**Theme: Complexity**

Keywords: *interactions*, *feedback loops*, *constant change*, *complex relationships*, *dangers of disruption caused by interconnectedness*.  

The bottom line and wake up call is this:
**The pandemic results from the same causes as the climate crisis.**



Main questions to investigate:  

1) How can we live in this globalised multiconnected world while still maintaining balance with nature and preserve our environment<br/>
2) What practices can we develop to foster caring and gentle interconnectedness, embracing differences and welcoming change; that is our new reality this world experiencing right now<br/>
3) How can we converse in the same language while speaking in different tongues, cherishing unique perspectives and cultural differences. How can we open to diversity without homogenising, suppressing and erasing minority<br/>
4) How can we bridge experiences learned in the past with potential future narratives and make the best possible solution for today and tomorrow<br/>

Solutions and possible approaches:  

* long term visions
* use interconnectivity to our advantage
* listen to marginalised and suppressed voices and learn how to forge better and more robust, and meaningful relationships with nature and between each other
* see emergence as global phenomena (pandemic, evolution, embedded response mechanisms)

`What would art look like if it would be created taking these aspects as the main guidelines and inspiration?`
---

List of papers and publications.

**Complexity / Emergence**

`“…acknowledgment of the role of chance and indeterminacy in shaping the living world around us. .. notion that the natural world is a compromise between               opposing tendencies toward order and disorder.” (Ulanowicz, p.8)`

* [Burroughs, William S., and Brion Gysin. The third mind. Viking Books, 1978.](http://lab404.com/lang/burroughs_gysin_third_mind.pdf)
* [Johnson, Steven. Emergence: The connected lives of ants, brains, cities, and software. Simon and Schuster, 2002.](https://books.google.ca/books?hl=en&lr=&id=qAtgKyaLH4MC&oi=fnd&pg=PA9&dq=Johnson,+Steven.+Emergence:+The+Connected+Lives+of+Ants,+Brains,+Cities,+and+Software.&ots=-Y1vhQkXWJ&sig=sL9Kug9qZ1NvqKJfhslIUjGlJwg&redir_esc=y#v=onepage&q=Johnson%2C%20Steven.%20Emergence%3A%20The%20Connected%20Lives%20of%20Ants%2C%20Brains%2C%20Cities%2C%20and%20Software.&f=false)
* Langton, Marcia, and Nikos Papastergiadis. "Complex Entanglements: Art, Globalisation, and Cultural Difference." London, Sydney, and Chicago: Rivers Oram Press, 2003.
* [Mitchell, Melanie. Complexity: A guided tour. Oxford University Press, 2009.](https://books.google.ca/books?hl=en&lr=&id=j-PQCwAAQBAJ&oi=fnd&pg=PR7&dq=Complexity+Melanie+Mitchell&ots=bNkkgx2tMP&sig=iWZi170ZDnnLTQ4o0U-tj9hmtpw&redir_esc=y#v=onepage&q=Complexity%20Melanie%20Mitchell&f=false)
* [Sommerer, Christa, and Laurent Mignonneau. "Modeling the emergence of complexity: Complex systems, the origin of life and interactive on-line art." Leonardo 35.2 (2002): 161-169.](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.23.1177&rep=rep1&type=pdf)
* [Ulanowicz, Robert E. Ecology, the ascendent perspective. Columbia University Press, 1997.](https://books.google.ca/books?hl=en&lr=&id=jSKDw_zAMJUC&oi=fnd&pg=PR11&dq=Ulanowicz,+Robert+E.+Ecology:+The+Ascendant+Perspective,+Columbia+University+Press,+1997.&ots=pEyOK573Sy&sig=vWnIrXmQnrv-zxtL2wvweZV6gtw&redir_esc=y#v=onepage&q=Ulanowicz%2C%20Robert%20E.%20Ecology%3A%20The%20Ascendant%20Perspective%2C%20Columbia%20University%20Press%2C%201997.&f=false)
* Volkart Schmidt, Yvonne. "Technologies of the Ecological after the Antropocene." Article in the book Virtualities and Realities, Pasa Smite, Raitis Smits (eds.). Riga: RIXC, 2019. 
* [Whitelaw, Mitchell. Metacreation: art and artificial life. Mit Press, 2006.](https://books.google.ca/books?hl=en&lr=&id=8o8CX6sPTKwC&oi=fnd&pg=PA39&dq=Whitelaw,+Mitchell.+Metacreation:+Arts+and+Artificial+Life.+MIT+Press,+2006.&ots=kgRhMK-sCN&sig=wsGhFzYndaa_FRfHrFnC5N2T_vs&redir_esc=y#v=onepage&q&f=false)

**Patterns - computer generated, ornamental fork art, physiological phenomena**

Pattern/Ornament: ways to abstract the nature and natural phenomena?
Embodied, shared phenomena : Purkinje cell and tree in nature (similar shape) 
`"The phosphenes seem like universal shapes or what the German psychologist Heinrich Kluver in his research on mescaline labelled "form constants"; elementary feautures of the nervous system that we may be hardwired to perceive. lattices, circles, crossed-out squares, undulating lines, curly cues, zigzags, fork-like shapes, matrices of points, and rows of dots." (Salter 2015, p.207)`

* [Floreano, Dario, and Claudio Mattiussi. Bio-inspired artificial intelligence: theories, methods, and technologies. MIT press, 2008.](https://books.google.ca/books?hl=en&lr=&id=1S03AgAAQBAJ&oi=fnd&pg=PR7&dq=bio+inspired+artificial&ots=h1IwCD4v87&sig=FWbbk2_yhuKyUtjGfsbV5-6P6BE&redir_esc=y#v=onepage&q=bio%20inspired%20artificial&f=false)
* [Grzegorz Kępisty, “Generative art: reaction-diffusion and Chladni figures.” 2020. PDF from Research Gate](https://www.researchgate.net/publication/344327257_Generative_art_reaction-diffusion_and_Chladni_figures)
* Dzērvītis, Aleksandra. Latvju Raksti [Lativian Design. Latvian Federation in Canada, 1973.
* [Prusinkiewicz, Przemyslaw, and Aristid Lindenmayer. The algorithmic beauty of plants. Springer Science & Business Media, 2012](http://algorithmicbotany.org/papers/abop/abop.pdf)
* [Salter, Chris, and Andrew Pickering. Alien agency: Experimental encounters with art in the making. MIT Press, 2015.](https://books.google.ca/books?hl=en&lr=&id=gTYhBwAAQBAJ&oi=fnd&pg=PR7&dq=Salter+Chris,+Alien+Agency.+MIT+press,+2015.&ots=hoXkSwVlrs&sig=f3DpbfPmRMJxQohsdOn_bvD_PaU&redir_esc=y#v=onepage&q=Salter%20Chris%2C%20Alien%20Agency.%20MIT%20press%2C%202015.&f=false)
* [Vuillemot, Romain, and Samuel Huron. "Gl i tch e s as a generative design process." 2017 IEEE VIS Arts Program (VISAP). IEEE, 2017.](https://visap.uic.edu/2016/materials/07_visap-0174-paper_Vuillemot.pdf)

**Human-Computer-World, one-another-together, sketching new languages**

* [Ascott, Roy. Telematic embrace: Visionary theories of art, technology, and consciousness. Univ of California Press, 2007.](https://books.google.ca/books?hl=en&lr=&id=zN85LrAoDwUC&oi=fnd&pg=PR9&dq=Ascott,+Roy.+Telematic+Embrace.+Visionary+theories+of+art,+technology,+and+consciousness.&ots=ljD66PsuIw&sig=psIHbZW7qEJ0lahRup_hbqblens&redir_esc=y#v=onepage&q=Ascott%2C%20Roy.%20Telematic%20Embrace.%20Visionary%20theories%20of%20art%2C%20technology%2C%20and%20consciousness.&f=false)
* [Licklider, Joseph CR. "Man-computer symbiosis." IRE transactions on human factors in electronics 1 (1960): 4-11.](http://worrydream.com/refs/Licklider%20-%20Man-Computer%20Symbiosis.pdf)
* Maeda, John. How to Speak Machine: Laws of Design for a Digital Age. Penguin UK, 2019.
* Packer, Randall, and Ken Jordan, eds. Multimedia: From Wagner to Virtual Reality. W.W.Norton&Company, 2002.
* [Salter, Chris. Entangled: technology and the transformation of performance. MIT Press, 2010.](https://books.google.ca/books?hl=en&lr=&id=ZBJbIP0fMr0C&oi=fnd&pg=PR7&dq=salter+entangled&ots=GFseMkTr6Z&sig=PQR4euMsHMzExHXX-JmFm2RVuPc&redir_esc=y#v=onepage&q=salter%20entangled&f=false)
* [Sommerer, Christa, Laurent Mignonneau, and Florian Weil. "The Art of human to Plant Interaction." The Green Thread: Dialogues with the Vegetal World (2015): 233.](https://books.google.ca/books?hl=en&lr=&id=ELpRCwAAQBAJ&oi=fnd&pg=PA233&dq=talk+to+me+exploring+human-plant+communication&ots=1QWmdsJWGL&sig=1l-tJnOOUUrevSmb6fv3yCka844&redir_esc=y#v=onepage&q&f=false)
* Vortex. Visual Aural Textual. One Language. Robert Appleton interview by Majid Abassi. AGI, 2011.
<br/>

<div class="codepen" data-height="428" data-theme-id="light" data-default-tab="result" data-user="Ka-Vi" data-slug-hash="mdPojzw" data-prefill='{"title":"CA_Melting_Ice","tags":[],"scripts":["https://alicelab.world/digm5950/al2019.js"],"stylesheets":[]}'>
  <pre data-lang="js">//Iteration mutated from a class example
//2020 DATT4950/DIGM5950_GameOfLife

// global declarations here

//creates a 20 x 20 grid of cells
let dim = 500;
let field = new field2D(dim);

//create another field so that we can store future values. By creating two fields (current=past && future, we achieve something that is called 'double buffer')
let field2 = new field2D(dim);

field.set(1, 0, 0);

function initialise_field(c, r) {
  //return random() &lt; 0.5 ? 1 : 0;
  return c > 1 && r &lt; 5 ? 1 : 0;
}

function update_field(c, r) {
  let C = field.get(c, r);

  //define each of the 8 neighbours in all directions
  let E = field.get(c + 1, r);
  let W = field.get(c - 1, r);
  let S = field.get(c, r + 1);
  let N = field.get(c, r - 1);
  //let SE = field.get(c + 1, r + 1);
  //let SW = field.get(c - 1, r + 1);
  let NE = field.get(c + 1, r - 1);
  let NW = field.get(c - 1, r - 1);

  //GOL is outer totalistic, which means I need to add all neighbours together
  //that will return the value of total neighbours alive
  let total = E + W + S + N + NE + NW;
  //SE + SW;

  //set up rules:
  if (C == 1) {
    //we are alive
    //if the neighbour total is less than 1, then new state 0
    if (total &lt; 3) {
      return 0;
    } else if (total &lt; 2) {
      return 0;
    } else {
      return 1;
    }
  } else {
    //we are dead
    //if neighbour is exactly 1, we are dead
    return total == 1 ? 1 : 0;
  }
}

// called at start, and whenever Enter key is pressed:
function reset() {
  // (re)initialization here
  field.set(initialise_field);
}

// called before rendering each frame
// dt is the time in seconds since the last update()
// (the global variable `now` gives the time since start in seconds)
// updates can be 'paused' using the spacebar
function update(dt) {
  // simulation code here
  field2.set(update_field);

  // let temp = field;
  // field = field2;
  // field2 = temp;

  //same above swapping operation can be expressed as such:
  [field,field2] = [field2,field];
}

// called to render graphics
// ctx is  an HTML5 canvas 2D rendering context
// Escape key will toggle fullscreen
function draw(ctx) {
  // rendering code here
  //field.draw();
  field.draw();
  
}

// called when any mouse (or touch) events happen
// kind is the event type (down, up, move, etc.)
// pt is a normalized mouse coordinate
// id refers to any button pressed/released
function mouse(kind, pt, id) {}

// called when any key events happen
// kind is the event type (down, up, etc.)
// key is the key (or keycode) pressed/released
function key(kind, key) {}
</pre></div>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>
<br/>
Melting Ice, CA by Kavi. 2020
