# LinearGradient: Width and Scale Mode

## Info

Gradients are a core building block in TiXL. They are used in many operators and effects.

This is the [LinearGradient]. It draws a gradient along a line.

## InfoFor(LinearGradient)

Notice that the gradient does not cover the full width of the image.

This is because the default scale mode is AlignToHeight. When the output aspect ratio changes, TiXL adjusts the left and right edges.

Aligning to the height helps avoid unexpected layout changes and keeps the result consistent across aspect ratios.

## CallToAction(LinearGradient)

Adjust the parameters, so the gradient covers the full width.

## Conclusion

Nice. Now the gradient behaves predictably when the output size changes.

# LinearGradient: Rotate

## InfoFor(LinearGradient)

This gradient is already connected to the solution, but its rotation does not match.

## InfoFor(LinearGradient.Rotate)

Select the gradient. Use the rotate icons on the right side of the parameter to rotate by 45 degrees.

Hold Ctrl or Alt for finer control.

## CallToAction(LinearGradient.Rotate)

Rotate the gradient until it matches the goal.

# LinearGradient: Offset

## Info

Use Offset to shift the gradient along its axis.

An offset of one equals the current width of the gradient.

## CallToAction(LinearGradient)

Move the gradient so it only appears at the bottom of the screen without changing its color ramp.

# LinearGradient: Repeat and PingPong

## Info

Repeating a gradient can create strong patterns with very little setup.

## Info

Enabling PingPong mirrors the gradient in the middle.

## CallToAction

Use Repeat and PingPong to recreate the goal.


# Analyze: ImageLevels

## Info

Sometimes it is hard to see the actual numeric values behind an image.

## Info

To help with this, TiXL offers operators for analyzing images.

In this example, [ImageLevels] slices an image and visualizes the color values along an intersection line.

## CallToAction

Connect [LinearGradient] to [ImageLevels].

## Info

Now a few things become clear:

* The gradient is linear, with sharp ends.
* It does not cover the full width of the image.
* It starts at pure black and ends at pure white.

## Conclusion

ImageLevels makes it much easier to reason about what the gradient is really doing.

# LinearGradient: Interpolation

## InfoFor(LinearGradient.Gradient)

To get a smoother result for this challenge, change the gradient interpolation type from "linear".

Select [LinearGradient], then right-click the color gradient to open its context menu and change the interpolation type.

## CallToAction(LinearGradient.Gradient)

Adjust the interpolation and any needed parameters until the output matches the goal.

## Tip(LinearGradient.Width)

Most SkillQuest challenges use simple values like 1/2 or 1/10.

You can also use the Infinity Slider. It appears when dragging numeric values and often marks the target value with a small dot.

# LinearGradient: Cleanup Tools

## Info

Sometimes gradients need cleanup. The color gradient context menu includes tools to reverse a gradient and evenly distribute its color steps.

## CallToAction

Recreate the goal without dragging or changing any color steps.

## Tip

If stuck, pick the target gradient from the context menu or retry the challenge.

# LinearGradient: Flip with Negative Width

## Info

You can flip a gradient without touching any color steps by using a negative Width value.

## CallToAction

Solve the challenge without changing any of the gradient’s color steps.

# LinearGradient: Chain Overlay

## Info

Like most image operators, [LinearGradient] can be chained to overlay an existing image.

With Normal blend mode, the original image is fully covered. Use opacity in the gradient’s color steps to let the image show through.

## CallToAction

Adjust the opacity of the gradient’s color steps to complete the challenge.

# LinearGradient: Blend Modes

## Info

Many image operators include a Blend Mode parameter. Exploring blend modes can lead to strong stylistic effects.

## CallToAction

Recreate the image without changing any color steps.

# LinearGradient: Invert Blend Mode

## Info

Chaining operators with the Invert blend mode can lead to surprisingly complex results.

White inverts the original color. Black leaves it unchanged.

## CallToAction

Use Invert to solve the puzzle.

# LinearGradient: GainAndBias

## Info

Many operators include a GainAndBias parameter. It is a powerful tool for fine-tuning effects in TiXL.

A later topic will cover it in more detail. This level is a quick introduction.

## InfoFor(LinearGradient.GainAndBias)

Everything is already connected. Focus only on GainAndBias.

Next to the parameter is a small graph showing a straight diagonal line.

## CallToAction(LinearGradient.GainAndBias)

Drag the graph vertically to shift the bias toward the left or right side of the gradient.

## CallToAction(LinearGradient.GainAndBias)

Drag the graph horizontally to adjust contrast: lower on the left, higher on the right.

## CallToAction(LinearGradient.GainAndBias)

Combine both directions and find the setting that matches the goal.

# RadialGradient: Dot

## Info

[RadialGradient] is similar to [LinearGradient], but it is based on distance from a center point.

## Info

Width and Offset shape the result. A width of one aligns to the image height, which helps keep the result circular across aspect ratios.

## CallToAction

Adjust Width and Offset to create the circle.

# RadialGradient: Vignette

## Info

A transparent radial overlay is great for a vignette that dims the corners.

## CallToAction

Adjust width, stretch, and colors to recreate the goal.

# RadialGradient: Polar Direction

## Info

A fun option is to switch the radial gradient from its default direction to a polar, circular direction.

## CallToAction

Recreate the goal.

# RadialGradient: Invert Pattern

## Info

Invert blend mode can also combine multiple [RadialGradient] operators into interesting patterns.

## CallToAction(RadialGradient#2)

Adjust the parameters of the second gradient to recreate the pattern. 


# More contrast

## Info
Let's look at this final example.

We have seen the [RemapColors] operator before. It is super powerful. But did you know that it can be used to adjust brightness and contrast without adjusting the gradient?

The trick here is that we can "bias" the color before it is sampled from the gradient. 

## CallToAction
Todo adjust bias and gain to complete the challenge.