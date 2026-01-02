# Where the Path Begins  &HVoGwBo

## Info &esJrfth
These early levels introduce the basics of working with TiXL's node graph.

## Info(ImageQuiz)  &HkJaGm6
Each level shows the target image at the bottom.

Recreate it using the available operators and connect them to the [Quiz] operator.

## Tip &SNlmZeY
If stuck, expand the Solution to see how it was built.

## CallToAction(RoundedRect)  &mszyfJn
Start by learning how to connect operators.

Drag a connection from [RoundedRect] to [ImageQuiz].


# Stacking Operators  &py8vfdI

## Info &G70qVyl
TiXL can snap operators into horizontal or vertical stacks.

This reduces clutter and makes graphs easier to read.

## CallToAction(RoundedRect)  &UjKuxop
When operators get close, they snap and connect automatically.

Try dragging [RoundedRect] toward [Blob].

## CallToAction(RoundedRect)  &GmYDs1r
Dragging a non-selected operator moves the entire stack.

Long-press to separate a single operator.

## Info &8ye7X9m
Shake an operator to remove its connections.

## Info &Oole6GS
Use Ctrl+Z to undo movements or disconnects.

## Tip(Raster)  &iGh0wop
Operators can also snap into vertical stacks.

## CallToAction(RoundedRect)  &5qzgdcg
To finish the level, stack [RoundedRect], [Blob], and [Raster] onto [ImageQuiz].


# Unstacking an Operator  &oqMRuV8

## CallToAction(Blob)  &5ywJl3n
Sometimes an operator needs to leave a stack.

Remove the [Blob] by long-pressing and dragging it out.


# Controlling a Parameter  &8R86EjU

## CallToAction(RoundedRect)  &hLeRt0s
When an operator is selected, its parameters appear in the Parameter Window.

Select the [RoundedRect].

## CallToAction(RoundedRect.Scale)  &7zmQq5L
The Scale parameter is highlighted because it was changed.

Click the parameter name \"Scale\" to reset it.

## Info &m6rVqOd
Static values are fine, but animation is often more useful.

The Rotate parameter is a good candidate.

## Info(Time)  &2wuPR9p
The [Time] operator is perfect for animation.

But dragging it next to [RoundedRect] does not snap.

That is because [Time] outputs a number, while [RoundedRect] expects an image by default.


## CallToAction(Time)  &QpAMfeX
Drag a connection from the [Time] output.

The blinking dot on [RoundedRect] shows parameters, like Rotate, that accept numeric input.

## CallToAction(RoundedRect)  &ckYNrte
Drop the connection on [RoundedRect] and choose Rotate from the popup.

## CallToAction &HHcPfRz
Snap to the connected input to keep the graph tidy.


# Increasing Animation Speed  &T7WeT4E

## InfoFor(RoundedRect.Rotate)  &4810LcS
The [RoundedRect] is rotating, but very slowly.

TiXL uses degrees, so a full rotation takes 360 seconds at this speed.

## CallToAction(Multiply)  &Sicxwam
Insert a [Multiply] operator between [Time] and [RoundedRect] to speed things up.
