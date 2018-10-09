
# Intro to Programming with p5.js



 ◇─◇──◇────◇────◇────◇────◇────◇─◇─◇
<br />

#### On this page:

1. [Resources](#-resources)
* [Getting Started](#-getting-started)
* [Code Basics](#-code-basics)
* [Structure of p5](#-structure-of-p5)
* [Drawing Shapes](#-drawing-shapes)
* [Color](#-color)
* [Variables](#-variables)
* [In-class exercise 4](#-in-class-exercise-4)


**NOTE: This is not intended as a stand-alone tutorial. It is supplemental material for following along in class. For those of you who missed class, do follow along with the understanding that not everything is spelled out. Running the code and making changes to it is highly recommended.**

---
<br>



# ▼△▼△▼ Resources

![P5.JS](assets/p5js_logo.png)

ALWAYS refer to the p5 documentation online at p5js.org

* ***[p5 reference docs](https://p5js.org/reference/)***
* ***[p5 examples](https://p5js.org/examples/)***

<br>

![Coding train](assets/coding-train.jpeg) ![Coding train](assets/coding-train_1.jpeg)

**Videos:** Dan Schiffman's [Coding Train YouTube channel](https://www.youtube.com/channel/UCvjgXvBlbQiydffZU7m1_aw) is GREAT, and hilarious, and so GREAT.

⬇⬇⬇⬇⬇⬇⬇⬇⬇⬇⬇⬇⬇⬇⬇⬇⬇⬇⬇⬇⬇⬇⬇⬇⬇⬇⬇⬇⬇⬇⬇⬇⬇⬇⬇⬇⬇⬇⬇⬇
#### ***HIGHLY RECOMMEND the Coding Train playlist [Foundations of Programming in JavaScript: p5](https://www.youtube.com/playlist?list=PLRqwX-V7Uu6Zy51Q-x9tMWIv9cueOFTFA)***
⬆⬆⬆⬆⬆⬆⬆⬆⬆⬆⬆⬆⬆⬆⬆⬆⬆⬆⬆⬆⬆⬆⬆⬆⬆⬆⬆⬆⬆⬆⬆⬆⬆⬆⬆⬆⬆⬆⬆⬆

<br>

**Books:**

* [*Getting Started with p5.js*](https://p5js.org/books/)
* [*Learning Processing*](http://learningprocessing.com/)
  - This is Dan Schiffman's book on Processing (predecessor to p5 - in Java not Javascript)


<br>


# ▼△▼△▼ Getting Started

1. Download and unzip the [p5-blankExample folder](blankExamples/p5-blankExample.zip) from GitHub, in the *blankExamples folder* of this tutorial.

* Copy it into your GitHub page local repository (the folder on your computer linked to the GitHub repo). Rename the folder "in-class_exercise_1"

* Open it in Atom. Start a server by with the package we installed: Packages > atom-live-server > start server.

* This will launch a browser page — if you add '/in-class_exercise_1' (or whatever you name the folder) to the end of the URL, it will display the contents of that directory: your p5 sketch live.

* It will just look like a black box for now...

![blank p5 sketch](assets/introP5_00.png)



---> *IF YOU ARE HAVING TROUBLE WITH ATOM-LIVE-SERVER, YOU WILL NEED TO CREATE A LOCAL SERVER USING PYTHON OR NODE*

* To do this, follow [this tutorial](https://github.com/processing/p5.js/wiki/Local-server).

* If on a mac, you can use the program 'terminal' to make these installations using the command line. If a windows user, you will have to [install git bash](https://gitforwindows.org/) to get access to the command line prompt.  


<br>

#### Folder setup

You should have a folder that has the familiar index.html and main.css files, along with a libraries folder and sketch.js file...

* These libraries ARE p5.js ---> P5 is basically a bunch of code that runs on top of JavaScript. We link to it from our HTML <head> to access all the p5 magic.  
* sketch.js is the JavaScript file where you write your p5 sketch. We also link to this in the HTML <head>.

![HTML links](assets/introP5_01.png)

<br>

*Review:* Do you know how to navigate folders using code? What does "../" do?

<br>

# ▼△▼△▼ Code Basics


#### Code blocks

    {
      a block of code
    }

    {
      a block of code
      {
        a block of code inside a block
      }
    }

<br>
Note the indentation: keeping all your lines properly indented will make your code more readable. To auto format using the atom-beautify plugin we installed, use the shortcut 'shift cmmd b'.

<br>

#### Case sensitive

Javascript is case-sensitive — hello is different than Hello.

The convention is to use camelCase - squish words together and capitalize first letter of every new word.

Start variable, function and method names with lowercase letters. Class names with a capitalized letter,
(we'll get into what these mean later).

<br>


#### Comments

Single-line comments start with // and are terminated by the end of the line:

    // single-line comment

Multiline comments are delimited by /\* and \*/:

    /* This is
       a multiline
       comment.
    */


<br>* Shortcut to comment out a line or block of code is 'cmmd /' or 'ctrl /'

<br>


#### Note on debugging

* ***DEBUGGING IS THE ART OF ISOLATING POTENTIAL PROBLEMS***
* It can be very frustrating, but also so satisfying when you figure it out
* Having people to work with can really help if you get stuck.

<br>

---> ***USE THE CONSOLE***

The console is your debugger buddy! Use it often to check that your code is working, or to try to figure out why it is not.

<br>

    console.log("hello world! I am the console")

Try adding the code above to your p5 setup() function. Open up developer tools in your browser (right click > inspect), and see what appears in the console.



<br>

![dev tools](assets/introP5_03.png)

***NOTE on console.log:***  You can log strings (words in quotation marks), or *the value* of a variable by using its name, with no quotation marks.

    console.log("text string")
    console.log(variableName)


<br>
<br>

# ▼△▼△▼ Structure of p5

**setup( ) and draw( ) are two functions that are built into p5.**

* Code within the setup() function block runs JUST ONCE AT SETUP.

* Code within the draw() function block loops over and over.

* You can only have one setup() and draw() function in your sketch.

<br>

To see this in action, paste this into your sketch.js (erase what is there first).

    // declare variables at top

    function setup() {
      // runs once
      console.log("in setup function")
    }

    function draw() {
      // loops over and over
      console.log("in draw function")
    }

    // write functions here


See what happens in the console?
<br>




# ▼△▼△▼ Drawing Shapes

See [object primitives example](https://p5js.org/examples/form-shape-primitives.html) in p5 docs  ⤵

![object primitives screenshot](assets/introP5_04.png)

<br>
***Note:*** The x, y graph coordinates start at the top left of your canvas.

![graph coordinates](assets/introP5_05.png)

<br>

* To draw shapes to the screen, you call a function specific to that shape, and pass in a few parameters to set the x, y coordinates and size of the shape.

* Refer to the [p5 reference page for 2D primitives](https://p5js.org/reference/#group-Shape) to get all the details.

![ellipse example](assets/introP5_06.png)


* You can stack shapes on top of eachother. They are drawn in the order that the code is executed, from top to bottom.

* Note you can set the color of the background with the background( ) function.

* Try making changes to the code, can you make it look like the picture below?

      function setup() {
        createCanvas(500, 500);

        // set background color in grayscale:
        background(150);

        // draw ellipse
        ellipse(100, 100, 80, 80);

        // draw rectangle
        rect(100, 100, 80, 80)
      }

      function draw() {
        //
      }



![ellipse example](assets/introP5_07.png)

<br>

#### CORNER v. CENTER mode

* The default mode for the ellipse is the CENTER mode, where the x, y coordinates mark the center
* Rectangles by default are in corner mode, where x, y coordinates mark the top left.

You can change this with the functions:

    ellipseMode(CORNER);
    rectMode(CENTER);

<br>


#### Having shapes follow the mouse

Turns out you can use the position of your mouse as one of the x, y parameters for your shapes!

* Try replacing the x or y values with **mouseX** or **mouseY**

      ellipse(mouseX, mouseY, 80, 80);
      rect(mouseX - 50, mouseY - 50, 80, 80);

<br>
***!!! Wait!!!! Did nothing happen?***

* Move these shapes into the draw( ) function. Remember setup( ) only happens once. To get things to move, they will have to be in the draw( ) function so they are updated each frame.


![ellipse example](assets/introP5_08.png)

***!!! Are they leaving trails?***
* See what happens if you move the background(150) into the draw loop.

* You can achieve a similar effect by placing clear(); at the top of your draw loop. This will clear the whole canvas (background included) for each frame.

<br>

# ▼△▼△▼ Color

#### Setting color for fill and stroke

* By default, p5 uses RGB values to set colors.
* Colors are declared with the last fill( ) and stroke ( ) functions ABOVE the shape drawn.
* You can declare no stroke or no fill with the noStroke( ) and noFill( ) functions, they don't take any color values.
* If you only put ONE VALUE in the R,G,B field, it will default to grayscale. 0 is black, 255 is white.

What would this code look like?

      fill(0, 0, 255);
      ellipse(100, 100, 50);

      noStroke();
      fill(100);
      rect(0, 100, 100);

      stroke(255, 0, 0);
      strokeWeight(10);
      rect(200, 200, 20)

<br>
#### Finding RGB values

There are tools to sample colors and get their RGB values

* Digital Color Meter - native utility in Mac OSX

* [Colorzilla](http://www.colorzilla.com/) is a browser extension for Chrome and Firefox that will give you the Hexcode and RGB value for any color on the page

<br>
#### Transparency

Transparency can be defined by an optional ***fourth parameter***, which also ranges from 0 - 255.

    // this has about 50% transparency
    fill(255, 100, 50, 125);
    rect(100, 100, 80, 80);

<br>


#### Getting wild

    function setup() {
    	createCanvas(500, 500);
    	// background is very light grey
    	background(230);
    }

    function draw() {

    	// create bright green ellipse with white stroke
    	fill(0, 255, 0);
    	// stroke is white
    	stroke(255, 255, 255);
    	ellipse(100, 100, 80, 80);

    	// make transparent rectangle
    	// a color fill with a fourth argument will define transparency
    	// fill has about 50% transparency
    	fill(255, 100, 50, 125);
    	noStroke();
    	rect(100, 100, 80, 80);

    	// stroke weight will set thickness of line
    	stroke(100, 200, mouseY, mouseX);
    	strokeWeight(5);
    	line(100, 100, mouseX, mouseY);
    }

<br>

Try changing color values to a random number.

To create a random integer from 0 to 255: <br>
random(255);


To create random integer between 100 and 200: <br>
random(100, 200);

<br>

# ▼△▼△▼ Variables

#### Scope

Variables declared at the top of your code are in the global scope. Variables declared in the setup() or draw() functions are only accessible within those functions.

ES6, the latest version of JavaScript, uses 'let' to define variables at block-level scope (within bracket blocks). We will be using let, but in many tutorials you might see 'var'.

    var myVariable;
    let myBlockScopeVariable;
    const MYCONSTANT;

Constants are read-only, and are generally all-caps.

Unlike Java (if you are familiar with Processing or Arduino), you do not need to declare a variable type in JavaScript — so no need for 'int' or 'float' or 'bool'.

<br>



Load this code, run it, and open up the developer's tools console in your browser (shortcut cmmd option i). See what errors and console logs you get. Move code around and observe how that changes.  


    function setup() {
    	console.log(hello);
    	console.log('hello');
    }

    function draw() {
    	let hello = 'hey';
    }

<br>

Note: Strings are defined within single '' or "" double quotes, and are text as-is.

Without the quotes, console.log will log the *variable* named hello.

Strings can be added together. Try adding this to your code:

    let p = "pets";
    let n = "Nala";
    console.log("My dog " + n + " loves " + p);

<br>


# ▼△▼△▼ Variables In-class exercise 4

Draw a shape to your canvas and have it move across the screen.
