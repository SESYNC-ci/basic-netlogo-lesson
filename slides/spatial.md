---
---


## Spatial neighborhoods

The following commands would be useful for modeling mobility, segregation/aggregation, growth, and foraging

~~~
create-turtles 1
ask turtles [ask neighbors [set pcolor green]]
~~~
{:.input title="Console"}

The default neighborhood is a Moore neighborhood of 8 adjacent patches

===

The alternative Von Neumann neighborhood has 4 neighbors, one in each cardinal directions:

~~~
ask turtles [ask neighbors4 [set pcolor yellow]]
~~~
{:.input title="Console"}

===

## Agent movement

~~~
ask turtles [move-to one-of neighbors4]
~~~
{:.input title="Console"}

Repeat. See what happens when you remove the "4".

===

Move agent and change patch attribute

~~~
ask turtles [move-to one-of neighbors ask patch-here [set pcolor red]]
~~~
{:.input title="Console"}

Repeat. See what happens when add to neighbors 4.

How many red patches?

~~~
count patches with [pcolor = red]
~~~
{:.input title="Console"}

~~~
observer: 1
~~~
{:.output}
