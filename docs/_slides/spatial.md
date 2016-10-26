---
---


## Explore spatial neighborhoods

The following commands would be useful for modeling mobility, segregation/aggregation, growth, and foraging

~~~
create-turtles 1
ask turtles [ask neighbors [set pcolor green]]
~~~
{: .input}

The default neighborhood is a Moore neighborhood of 8 adjacent patches

===

## Explore spatial neighborhoods

As opposed to a Von Neumann neighborhood of 4 neighbors in cardinal directions:

~~~
ask turtles [ask neighbors4 [set pcolor yellow]]
~~~
{: .input}

===

## Agent movement

~~~
ask turtles [move-to one-of neighbors4]
~~~
{: .input}

Repeat. See what happens when remove 4.

===

Move agent and change patch attribute

~~~
ask turtles [move-to one-of neighbors ask patch-here [set pcolor red]]
~~~
{: .input}

Repeat. See what happens when add to neighbors 4.

How many red patches?

~~~
count patches with [pcolor = red]
~~~
{: .input}
