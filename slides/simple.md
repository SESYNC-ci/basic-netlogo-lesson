---
---

## Making a simple model

The Command Center is found in the Interface tab. It allows you to enter commands or directions to a model. Commands are instructions you can give to NetLogo's agents: turtles, patches, links, and the observer.

Start by creating a new model file:

> `File > New`

===

## Model Objective

We are going ask some patches to turn green, create a set of agents, and have them move around. We will ask the patches to count how many agents are on them.

===

## Commands

Into the Command Center input (at the `observer>` prompt), type the following:

~~~
count patches
~~~
{:.input}

~~~
observer: 1089
~~~
{:.output}

Why do we get that answer?

===

~~~
ask n-of 20 patches [set pcolor green]
count patches with [pcolor = green]
~~~
{:.input}

~~~
observer: 20
~~~
{:.output}

===

Create some agents

~~~
create-turtles 10 [set size 3]
~~~
{:.input}

===

Make them move

~~~
ask turtles [rt random 360 fd 10]
~~~
{:.input}

What are `rt` and `fd`? 

If you need help, type a command at the `observer>` prompt and hit F1.

===

What did we just tell our agents to do? Here is what each command in the 'move-turtles' procedure does:

- `ask turtles [ ... ]` says that each turtle should run the commands in the brackets. 
- `rt random 360` is another command that uses a reporter.
  -  each turtle picks a random whole number between 0 and 359. (random doesn't include the number you give it as a possible result.)
  -  each turtle turns right (or `rt` for short) this number of degrees 
- `fd 10` makes the turtle move forward ten steps.

===

## Change agent appearances

~~~
ask n-of random 10 turtles [set color red set shape "circle"]
ask n-of 10 turtles [set color red set shape “circle”]
~~~
{:.input}

===

To see shape options:

~~~
show shapes
~~~
{:.input}

~~~
observer: ["default" "airplane" "arrow" "box" "bug" "butterfly" "car" "circle" "circle 2" "cow" "cylinder" "dot" "face happy" "face neutral" "face sad" "fish" "flag" "flower" "house" "leaf" "line" "line half" "pentagon" "person" "plant" "sheep" "square" "square 2" "star" "target" "tree" "triangle" "triangle 2" "truck" "turtle" "wheel" "wolf" "x"]
~~~
{:.output}

===

Maybe something more uplifting ...

~~~
ask n-of random 10 turtles [set color yellow set shape "face happy"]
~~~
{:.input}

===

## Interlude: Colors in NetLogo

Notice that we used 'pcolor' to change the color of patches, and 'color' to change the color of turtles. 
Each of these is an entity-specific attribute.

In NetLogo, colors have a numeric value. In all of the exercises we have been using the name of the color. This is because NetLogo recognizes 16 different color names. This does not mean that NetLogo only recognizes 16 colors. There are many shades in between these colors that can be used too. Here's a chart that shows the whole NetLogo color space:

![]({% include asset.html path="images/netlogo-colors.jpg" %})

===

And if you don't have the chart ...

You can send commands to specific entities by changing the object of the command line. Choose "turtles" from the popup menu in the Command Center (or use the tab key).

For example, when you type:

~~~
set color red
~~~
{:.input}

this does the same thing as if you had typed:

~~~
set color 15
~~~
{:.input}

===

If you want an intermediate shade, but don't know the number, adding or subtracting a number from a name will work too. 

And you can get a lighter or darker version of the same color by using a number that is a little larger or a little smaller, as follows.

Choose "patches" from the popup menu in the Command Center (or use the tab key). 

~~~
set pcolor red - 2 
~~~
{:.input}

(The spacing around the "-" is important.) 

By subtracting from red, you make it darker. 

~~~
set pcolor red + 2 
~~~
{:.input}

By adding to red, you make it lighter. 

===

## Back to the model

Count your turtles

~~~
count turtles
~~~
{:.input}

~~~
observer> show count turtles
observer: 10
~~~
{:.output}

Notice that NetLogo accepts this even though it is shorthand. The full command is printed in the Command Center window. You can recall through past commands with the 'up' arrow.

===

Count by agent attribute:

~~~
count turtles with [color = yellow]
~~~
{:.input}

~~~
0
~~~
{:.output}

===

Make agents move

~~~
ask n-of 20 patches [set pcolor green]
ask turtles [move to one-of patches with [pcolor = green]]
~~~
{:.input}

===

Why didn't this work?

The Netlogo dictionary can help: `File > Help`

Look at turtle commands that are similar. We just need to add a dash in between "move" and "to".

~~~
ask turtles [move-to one-of patches with [pcolor = green]]
~~~
{:.input}

===

## Extracting information

~~~
ask patches with [pcolor = green][show count turtles-here]
ask turtles with [color = red][die]
count turtles
clear-all
~~~
{:.input}

~~~
(patch 13 -2): 1
(patch -13 13): 1
(patch 3 -7): 2
(patch 1 -4): 1
(patch -7 0): 1
(patch 2 -14): 1
(patch 7 -1): 0
(patch 8 4): 0
(patch -3 -11): 0
(patch -15 5): 0
(patch -1 3): 0
(patch 0 -14): 0
(patch -14 -1): 0
(patch -5 -15): 2
(patch 3 -15): 0
(patch 15 -14): 0
(patch -7 8): 0
(patch -7 15): 0
(patch 13 -4): 0
(patch -5 10): 1
observer> show count turtles
observer: 10
~~~
{:.output}

===

## More online

Thus far, we have been working with complete sets of entities (e.g., all turtles), but you may want to refer to specific agents or sub-groups.

For instructions on how to access, manipulate, and monitor specific entities, see [Tutorial #2]{:target="_blank"} in the NetLogo User Manual.

[Tutorial #2]: https://ccl.northwestern.edu/netlogo/docs/tutorial2.html
