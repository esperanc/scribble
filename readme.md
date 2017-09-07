# Scribble

A very minimal 2D sketch using [three.js](https://threejs.org).

# What is this?

This is my attempt at writing a template that could be used to write three.js-based javascript programs using a coding style similar to that used when writing [p5.js / Processing](https://p5js.org)-based sketches. The idea is to set up global Three.js objects such as a `Scene`, a `Renderer`, a `Camera`, etc and automatically links mouse callbacks. This code is just a demo which lets you use your mouse to draw free-hand lines on the screen.

If you just want to use the scribble application, upload it to your web server and access index.html. For instance, here is a [live scribble page](https://rawgit.com/esperanc/scribble/master/index.html).

 A more interesting use, however, is to use this code as a template to write a 2D drawing application that does what you want. Notice that you still need to understand how Three.js works!

# Usage

The demo is divided into two sections: the first part contains some global variables and the definition of some functions, being  `init ()` the most important of them. This first part should need no modification if you only want a 2D application using the mouse. The second part is the drawing application itself, which you will want to customize. It consists of your definition of mouse callback functions, whose names are the same as the analogous functions in p5, i.e.,
 - `function mousePressed ()` --> called when a mouse button is pressed,
 - `function mouseReleased ()` --> called when a mouse button is released,
 - `function mouseDragged ()` --> called when the mouse is moved while a button is pressed,
 - `function mouseMoved ()` --> called when the mouse is moved regardless of whether a button is pressed or not.

There is also support for the `setup()` function that serves as a good spot to put you initialization code. This is automatically called by `init()` if defined. 

Finally, you must call `init ()` explicitly - usually in the last line of your code.