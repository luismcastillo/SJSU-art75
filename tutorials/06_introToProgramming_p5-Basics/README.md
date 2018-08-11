
# Intro to Programming with p5.js



 ◇─◇──◇────◇────◇────◇────◇────◇─◇─◇
<br />

#### On this page:

1. Resources
2. Getting Started
3. Basics
4. Structure of p5.js
5. Color: fill, stroke, transparency
6. Variables
7. Conditionals - if statements
8. Loops - while and for loops
9. Displaying images in p5
10. Exercise: Super Mario Clouds

**NOTE: This is not intended as a stand-alone tutorial. It is supplemental material for following along in class. For those of you who missed class, do follow along with the understanding that not everything is spelled out. Running the code and making changes to it is highly recommended.**

---
<br>



## ▼△▼△▼ Resources

ALWAYS refer to the p5 documentation online at p5js.org

* ***[p5 reference docs](https://p5js.org/reference/)***
* ***[p5 examples](https://p5js.org/examples/)***

<br>


Videos: Dan Schiffman's Coding Train YouTube channel is GREAT
* [Foundations of Programming in JavaScript: p5 Tutorial](https://www.youtube.com/playlist?list=PLRqwX-V7Uu6Zy51Q-x9tMWIv9cueOFTFA)

<br>

Books:

* [*Getting Started with p5.js*](https://p5js.org/books/)
* [*Learning Processing*](http://learningprocessing.com/)
  - This is Dan Schiffman's book on Processing (predecessor to p5 - in Java not Javascript)


<br>


## ▼△▼△▼ Getting Started

Download and unzip the [p5-blankExample folder](assets/p5-blankExample.zip) from GitHub, or on the class google drive.

Copy it into your GitHub page local repository (the folder on your computer linked to the GitHub repo). You can also create a new repo if you want to keep your p5 sketches separate.  

Open it in Atom. Start a server by with the package we installed: Packages > atom-live-server > start server.

This will launch a browser page — if you add '/p5-blankExample' (or whatever you name the folder) to the end of the URL, it will display the contents of that directory: your p5 sketch live.

<br>

**IF YOU ARE HAVING TROUBLE WITH ATOM-LIVE-SERVER, YOU WILL NEED TO CREATE A LOCAL SERVER USING PYTHON OR NODE**

To do this, follow [this tutorial](https://github.com/processing/p5.js/wiki/Local-server).

If on a mac, you can use the program 'terminal' to make these installations using the command line. If a windows user, you will have to [install git bash](https://gitforwindows.org/) to get access to the command line prompt.  


<br>

![HTML links](assets/introP5_00.png)
<br>
Note: Your HTML file needs to link to the p5 libraries AND your p5 sketch.js file, just as it linked to your CSS file.
<br>
<br>

## ▼△▼△▼ Basics


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
Note the indentation: keeping all your lines properly indented will make your code more readable. To auto format using the atom-beautify plugin we installed, use the shortcut 'shift cmmd t'.

<br>

#### Case sensitive

Javascript is case-sensitive — hello is different than Hello.

The convention is to use camelCase - squish words together and capitalize first letter of every new word.

Start variable, function and method names with lowercase letters, class and object names with a capitalized letter, and constants as all caps
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


<br>* Shortcut to comment out a line or block of code is 'cmmd /'

<br>


#### Note on debugging

The console is your friend! Use it often to check that your code is working, or to try to figure out why it is not.

    console.log("text string")
    console.log(variableName)

<br>
<br>


## ▼△▼△▼ Structure of p5.js

    // declare variables at top

    function setup() {
      // runs once
    }

    // computer skips to draw

    function draw() {
      // step 1
      // step 2
      // (loops over and over)
    }

    // write functions here

<br>

#### Drawing in p5

See [object primitives example](https://p5js.org/examples/form-shape-primitives.html) in p5 docs

Note: The x, y graph coordinates start at the top left of your canvas.


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
      // no need to loop
    }

The default mode for the ellipse is to have the x, y coordinates mark the center, while rectangles by default are in corner mode.

You can change this with the functions: <br>
ellipseMode(CORNER); <br>
rectMode(CENTER);

<br>

    function setup() {
      createCanvas(500, 500);
      background(150);
    }

    function draw() {
      // loops because the shape is updated with
      // changing mouse position
      ellipse(mouseX, mouseY, 80, 80);
      rect(mouseX - 50, mouseY - 50, 80, 80)
    }

See what happens if you move the background(150); function into the draw loop.

You can achieve the same effect with clear(); at the top of your draw loop.

<br>

## ▼△▼△▼ Color: fill, stroke, and transparency

#### Finding RGB values

Digital Color Meter - native utility in Mac OSX

[Colorzilla](http://www.colorzilla.com/) is a browser extension for Chrome and Firefox that will give you the Hexcode and RGB value for any color on the page


<br>

    function setup() {
    	createCanvas(500, 500);
    	// background is very light grey
    	background(230);
    }

    function draw() {

    	// create bright green ellipse with white stroke
    	// fill is bright green
    	fill(0, 255, 0);
    	// stroke is white
    	stroke(255, 255, 255);
    	strokeWeight(1); // reset to default
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

## ▼△▼△▼ Variables

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
    	let hello = 'hello';
    }

<br>

Note: Strings are defined within single '' or "" double quotes, and are text as-is.

Without the quotes, console.log will log the *variable* named hello.

Strings can be added together. Try adding this to your code:

    let p = "pets";
    let n = "Nala";
    console.log("My dog " + n + " loves " + p);
<br>


## ▼△▼△▼ Conditionals - If statements


#### BOOLEAN EXPRESSION

Booleans are expressions that evaluate to true or false.

* 120 equals 120 -> true
* 120 equals 121 -> false
* 120 - 10 equals 110 -> true!


<br>

#### Anatomy of an if statement

    if (something is true) {
      // run this code
    } else {
      // do this
    }


<br>

#### Interaction:

Here is an if statement that checks to see if the mouse is pressed:

    function setup() {
    	createCanvas(500, 500);
    	background(200);
    }

    function draw() {
    	if (mouseIsPressed) {
    		fill(10, 100, 200);
    		ellipse(mouseX, mouseY, 80, 80);
    	} else {
    		fill(255, 100, 50);
    		rectMode(CENTER);
    		rect(mouseX, mouseY, 80, 80);
    	}
    }

<br>

#### Breakpoints

If statements can be chained together with 'else if'

<br>

It looks like this:

    if (something is true) {
      // run this code
    } else if (this is true) {
      // run this code
    } else {
      // do this
    }

<br>

    function setup() {
        createCanvas(500, 500);
        background(200);
        strokeWeight(10);
    }

    function draw() {
      if (mouseX > 400) {
        fill(255, 100, 50);
      } else if (mouseX > 300) {
        fill(200, 100, 100);
        } else if (mouseX > 200) {
            fill(150, 100, 150);
        } else if (mouseX > 100) {
            fill(100, 100, 200);
      } else {
        fill(50, 100, 250);
      }
        // A triangle!
      	triangle(50, 400, 150, 400, 100, 480);
        // A quad!
        quad(30, 100, 300, 450, 350, 150, 200, 50);
        // A text!
    		textSize(16);
        text("CHANGE COLOR WITH BREAKPOINTS", width/2 - 50, 475);
    }

<br>

#### Logical operators:

<br>

    >	greater than

    <	less than

    >=	greater than or equal to

    <=	less than or equal to

    ==	equal

    ===	equal value and equal type

    !=	not equal

    !==	not equal value or not equal type

    &&  both are true

    ||  one or the other are true

<br>

Note when you are CHECKING to see if something is true you use two equals signs. When you are assigning a variable you would use just one.

True or false also applies to whether or not variables exist. A variable that is not defined equates to false, one that is defined is true.


    // one equals sign for defining variables
    let p = 5;
    let q;

    function setup() {
      if (p) {
        console.log("p exists and is " + p);
      }

      // two equals signs for checking if something is true
      if (p == 5) {
        console.log("yup, p is definitely 5")
      }

      if (q) {
        console.log("q exists")
      }

      if (!q) {
        console.log("q does not exists and is " + q)
      }
    }
<br>

**Or statements use pipes ||** <br>
This code would get triggered when the mouse was greater than 400 OR less than 100.


    if (mouseX > 400 || mouseX < 100) {
      fill(255, 100, 50);
    } else {
      fill(50, 100, 250);
    }

<br>

**And statements use two 'ands' &&** <br>
This code gets triggered when the mouse is in the top right corner. Notice you don't need an else statement at the end — JavaScript will default to doing nothing.
<br>

    function setup() {
    	createCanvas(500, 500);
    }

    function draw() {
    	background(200);
    	noStroke();
      if (mouseX > 400 && mouseY > 400) {
        ellipse(100, 100, 100, 100);
        text("that's the spot", 63, 100);
      }
    }

<br>



## ▼△▼△▼ loops

Notes on operators shorthand

x = x + 4;
is same as:
x += 4;

x = x + 1;
is same as:
x++;

x = x - 1
is same as;
x--;
<br>
<br>

#### while loop

Will loop as long as condition is true! Just make sure there is an exit condition or it will loop for ever.

    let x = 0;

    function setup() {
      createCanvas(500, 500);

    }

    function draw() {
      background(100);
      while (x < width) {
        fill(129, 206, 15);
        rect(x, 100, 10, 10);
        x += 20;
        // line above is same as x = x + 20
      }
    }

<br>

#### for loop

loops a given number of times

      for (let i = 0; i < 10; i++) {
      // code will run 10 times here
      // the variable i increases by 1 each time
      console.log(i)
      }

For loop example: describe what this code will create:
<br>


    function setup() {
      createCanvas(720, 400);
    }

    function draw() {
      background(127);
      noStroke();
      for (var i = 0; i < height; i += 20) {
        fill(129, 206, 15);
        rect(0, i, width, 10);
        fill(255);
        rect(i, 0, 10, height);
      }
    }


## ▼△▼△▼ Display images

[p5 reference for image()](https://p5js.org/reference/#/p5/image)

[p5 example on loading images](https://p5js.org/examples/image-load-and-display-image.html)

    let img;

    function preload() {
      // you will need to change this to the file path to your image
      img = loadImage('filePath/image.png');
    }

    function setup() {
      createCanvas(500, 500);
      background(200);

      // Top-left corner of the img is at (0, 0)
      // Width and height are the img's original width and height
      image(img, 0, 0);

      // If you want to scale the image to 100 x 100 pixels
      // image(img, 0, 0, 100, 100);

      // If you want to scale image by 50%
      // image(img, 10, 10, img.width/2, img.height/2);
    }

Note img.width in references the variable name 'img'.

If your image was named something else it would be:

somethingElse.width/2

## ▼△▼△▼ Displaying GIFs

To display GIFs, you have to install a [separate p5 library](https://github.com/antiboredom/p5.gif.js/tree/master) that supports GIFs. To install, copy the library into your libraries folder and make sure it is linked to in your index.html.

***Note:*** *This library works in Chrome, but might not work in other browsers. If you are going to have many animated sprites, you might want to use the [p5.play library](../10-p5Play-sprites) (though it is little more work to set up).*

## ▼△▼△▼ Super Mario clouds

Make an image move from one side of screen to the other. You will need to store the image in a variable, then make its location move in the draw loop. Use an **if statement** to check to see if it has reached the end of the screen.

You can use the Super Mario Clouds pngs in the assets folder of this tutorial, or any other image you choose. Save the image inside your p5 sketch folder and make sure it is loading from the correct file path.

If you want, try running your sketch over the full screen, perhaps over some html on your webpage! The zip for a full screen sketch is in the assets folder: [p5-blankExample_fullScreen.zip](assets/p5-blankExample_fullScreen.zip)
