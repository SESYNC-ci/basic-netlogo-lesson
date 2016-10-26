---
---

Let's start with a basic tour of the NetLogo environment.

Start NetLogo.

The window you see is called the NetLogo integrated development environment (IDE).

It has seveal parts:

| IDE Component | Description                                                       |
|---------------+-------------------------------------------------------------------|
| Interface     | Control, run, and visualize model (current tab)                   |
| Info          | Description of model purpose, function, and features (middle tab) |
| Code          | Model syntax (last tab)                                           |
| View          | Monitor, i.e. the 'World', used for real-time model visualization |

===

Open an existing model from the NetLogo model library to explore.

Choose "Models Library" from the File menu.
Open the "Biology" folder.
Click on the model called "Wolf Sheep Predation".
Press the "open" button.

===

The Interface tab will fill up with lots of buttons, switches, sliders and monitors. These interface elements allow you to interact with the model. Buttons are blue; they set up, start, and stop the model. Sliders and switches are green; they alter model settings. Monitors and plots are beige; they display data.

The '+ Add' button along the top toolbar allows one to add additional features to the interface.

When you first open the model, the Monitor is empty.

To initialize the model with its default setting, press the 'setup' button.

===

There are two different types of buttons: 'once' and 'forever'.

Buttons without arrows, like the 'setup' button, perform a task once and then pop back up when the task is completed.

Buttons with arrows, like the 'go' button, will run until the user manually stops the task by clicking the same button again.

Many models also have a once button called "go once" or "step once" which is like "go" except that it advances the model by one tick (time step) instead of over and over. Using a once button like this lets you watch the progress of the model more closely.

You can also stop a model with the 'Halt' item on the Tools menu, but you should only do this if the model is stuck for some reason. Using 'Halt' may interrupt the model in the middle of an action, which coudl create an error.

===

Click on the 'Info' tab to switch screens.

Here you will find useful 'meta' information about the model.

| Section          | Description                                                                                      |
|------------------+--------------------------------------------------------------------------------------------------|
| What is it?      | Model purpose and topic.                                                                         |
| How it works     | An overview of the functioning of the model, core behaviors, and model features.                 |
| How to use it    | Describes the buttons, sliders, and parameters.                                                  |
| Things to notice | What you see in plots and display when running model, as well as questions the model can answer. |
| Things to try    | Experiments you can try.                                                                         |
| Extend the model | Future enhancements or interesting modifications.                                                |

There may also be additional sections, such as: NetLogo Features, Related Models, Credits, and How to Cite.

===

Click on the 'Code' tab to switch screens.

Code Tab:
Extensions, Global variables
Attributes of agents (turtles), patches (environment agents)
Button procedures
Other procedures

Defining Agents and the Environment in NetLogo:
- Agents are called turtles (can be mobile)
- The environment consists of patches (not mobile)

===

Return to the 'Interface' by clicking the tab.

A note about the speed slider before we get going.

The speed slider allows you to control the speed of a model, that is, the speed at which turtles move, patches change color, and so on.

When you move the slider to the left the model slows down so there are longer pauses between each tick (time step). That makes it easier to see what is happening. You might even slow the model down so far as to see exactly what a single turtle is doing.

When you move the speed slider to the right the model speeds up. NetLogo will start skipping frames, that is, it won't update the view at the end of every tick, only some ticks. Updating takes time, so fewer view updates means the model progresses faster.

Note that if you push the speed slider well to the right, the view may update so infrequently that the model appears to have slowed down. It hasn't, as you can see by watching the tick counter race ahead. Only the frequency of view updates has lessened.

===

Let's see it in action. If you haven't done so already, press the 'setup' button to initialize the model with current settings.

Press 'go'.

What model dynamics do you see? How many 'ticks' did it take?

===

What settings could we change to get a stable outcome?

Change to the 'Info' tab to learn what each of the sliders and switches represent.

Note that in order to re-run the model with new settings, you must click the 'setup' button first before hitting 'go' again.

Give it a try. Green sticky notes when you get both sheep and wolf populations to persist.

===

## Gathering Information: Plots and Monitors

**Plots**

The plot in Wolf Sheep Predation contains three lines: sheep, wolves, and grass / 4. (The grass count is divided by four so it doesn't make the plot too tall.) The lines show what's happening in the model over time. The plot legend shows what each line indicates. In this case, it's the population counts.

When a plot gets close to becoming filled up, the horizontal axis is compressed and all of the data from before gets squeezed into a smaller space. In this way, more room is made for the plot to grow.

If you want to save the data from a plot to view or analyze it in another application, use the "Export Plot" item on the File menu. It saves the plot data in a format that can by read back by spreadsheet and database programs such as Excel. You can also export a plot by right-clicking it and choosing "Export..." from the popup menu.

===

**Monitors**

Monitors are another means of displaying information from a model. Monitors in Wolf Sheep Predation model track the total population of sheep, wolves, and grass. (Remember, the amount of grass is divided by four to keep the plot from getting too tall.)

The numbers displayed in the monitors change as the model runs, whereas the plots show you data from the whole course of the model run.

These are particularly useful if you have a quantitative indicator of model dynamics that you would like to track in real time.

===

## Controlling the View

Like any other simulation software, visualization is computationally costly. You can supress model output in the View by toggling the view updates control.

Press 'go'. Note the speed of simulation.
Uncheck the 'View Updates' box. What happened?

Turning off updates and moving the speed slider all the way to the right will greatly improve simulation time if you just want to produce model results to analyze later.

===

# Controlling the View, cont'd.

The size of the view is determined by five separate settings: min-pxcor, max-pxcor, min-pycor, max-pycor, and patch size. Let's take a look at what happens when we change the size of the view in the "Wolf Sheep Predation" model.

There are more model settings than there's room for in the toolbar. The "Settings..." button lets you get to the rest of the settings.
By modifying the max-pxcor or max-pycor settings, you can change the extent of the model view. With all else the same, this also increases the number of patches. Note that the grass monitor changes values when you increase the model extent.

Modify the patch size, however, does not change the number of patches.

===

Model Library - a tremendous resource for code ideas!
The library contains four sections: Sample Models, Curricular Models, Code Examples, and HubNet Activities.

**Sample Models**

The Sample Models section is organized by subject area and currently contains more than 200 models. We are continuously working on adding new models to it, so come visit this section at a later date to view the new additions to the library.
Some of the folders in Sample Models have folders inside them labeled "(unverified)". These models are complete and functional, but are still in the process of being reviewed for content, accuracy, and quality of code.

**Curricular Models**

These are models designed to be used in schools in the context of curricula developed by the CCL at Northwestern University. Some of these are models are also listed under Sample Models; others are unique to this section. See the Info tabs of the models for more information on the curricula they go with.

**Code Examples**

These are simple demonstrations of particular features of NetLogo. They'll be useful to you later when you're extending existing models or building new ones. For example, if you wanted to add a histogram to your model, you'd look at "Histogram Example" to find out how.

**HubNet Activities**

This section contains participatory simulations for use with groups. For more information about HubNet, see the HubNet Guide.
