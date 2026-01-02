# LinearGradient: Width and Scale Mode  &DAcIMk5

## Info &rzDaYoP
Gradients are a core building block in TiXL. They are used in many operators and effects.

This is the [LinearGradient]. It draws a gradient along a line.

## InfoFor(LinearGradient)  &d6igVMf
Notice that the gradient does not cover the full width of the image.

This is because the default scale mode is AlignToHeight. When the output aspect ratio changes, TiXL adjusts the left and right edges.

Aligning to the height helps avoid unexpected layout changes and keeps the result consistent across aspect ratios.

## CallToAction(LinearGradient)  &7Yf3Hf4
Adjust the parameters so the gradient covers the full width.


# LinearGradient: Rotate  &3cRCNE3

## InfoFor(LinearGradient)  &OainiGL
This gradient is already connected to the solution, but its rotation does not match.

## InfoFor(LinearGradient.Rotation)  &ApqwWb7
Select the gradient. Use the rotate icons on the right side of the parameter to rotate by 45 degrees.

Hold Ctrl or Alt for finer control.

## CallToAction(LinearGradient)  &qWuItpM
Rotate the gradient until it matches the goal.


# LinearGradient: Offset  &kO80BTF

## Info &VFjPENM
Use Offset to shift the gradient along its axis.

An offset of one equals the current width of the gradient.

## CallToAction(LinearGradient)  &cgWtcv4
Move the gradient so it only appears at the bottom of the screen without changing its color ramp.


# LinearGradient: Repeat and PingPong  &KlTdfKs

## Info &bW0QWvq
Repeating a gradient can create strong patterns with very little setup.

## Info &ZEyTKIn
Enabling PingPong mirrors the gradient in the middle.

## CallToAction(LinearGradient.PingPong)  &K5H7ZpS
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

- The gradient is linear, with sharp ends.
- It does not cover the full width of the image.
- It starts at pure black and ends at pure white.

# LinearGradient: Interpolation  &5fStiK9

## InfoFor(LinearGradient.Gradient)  &JFdYr92
To get a smoother result for this challenge, change the gradient interpolation type from "linear".

Select [LinearGradient], then right-click the color gradient in the parameter window to open its context menu and change the interpolation type.

## CallToAction(LinearGradient.Gradient)  &vOLBTKR
Adjust the interpolation and any needed parameters until the output matches the goal.

## Tip(LinearGradient.Width)  &xcLhuQw
Most SkillQuest challenges use simple values like 1/2 or 1/10.

You can also use the Infinity Slider. It appears when dragging numeric values and often marks the target value with a small dot.


# LinearGradient: Cleanup Tools  &853NzUH

## Info &gRq1o3Q
Sometimes gradients need cleanup.

The color gradient context menu includes tools to reverse a gradient and evenly distribute its color steps.

## CallToAction &dLOYqg3
Recreate the goal without dragging or changing any color steps.


# I02h_InterpolationMadness  &Swdnv6K

## Info &uuxxbpd
Some interpolation modes like Spline and OKLab might have unexpected results.

## Info &PCgDxCp
In this example the Spline Interpolation leads to color clamping of the red channel.

## CallToAction(LinearGradient)  &MtL7FK7
Select the [LinearGradient] operator.



Then adjust the position of the middle gradient step to resolve the clamping.



# LinearGradient: Flip with Negative Width  &rrELaAb

## Info &clTZUUT
You can flip a gradient without touching any color steps by using a negative Width value.

## CallToAction &D8jGAPa
Solve the challenge without changing any of the gradient's color steps.


# LinearGradient: Chain Overlay  &lOEH4i0

## Info &03ayyLl
Like most image operators, [LinearGradient] can be chained to overlay an existing image.

With Normal blend mode, the original image is fully covered.

Use opacity in the gradient's color steps to let the image show through.

## CallToAction(LinearGradient.Gradient)  &2odqBT8
Select a gradient step to open the Color picker. 

Then use the opacity slider at the bottom. 

Adjust the opacity of the gradient's color steps to complete the challenge.



# LinearGradient: Blend Modes  &172Ez6o

## Info &qRwkavS
Many image operators include a Blend Mode parameter.

Exploring blend modes can lead to strong stylistic effects.

## CallToAction &ohAbRx0
Recreate the image without changing any color steps.


# LinearGradient: Invert Blend Mode  &475Bd88

## Info &lbopEGz
Chaining operators with the Difference blend mode can lead to complex results.

White inverts the original color. Black leaves it unchanged.

## CallToAction &k4PVMaj
Use the Difference blend mode to to solve the puzzle.

# LinearGradient: GainAndBias  &KaCBZji

## Info &500vVwQ
Many operators include a GainAndBias parameter.

It is a powerful tool for fine-tuning effects in TiXL.

## InfoFor(LinearGradient.GainAndBias)  &5W0W2OA
Everything is already connected. 

Select the LinearGradient operator and focus only on GainAndBias.

Next to the parameter is a small graph showing a straight diagonal line.

## InfoFor(LinearGradient.GainAndBias)  &dOm07wC
Drag the graph vertically to shift the bias toward the left or right side of the gradient.

## CallToAction(LinearGradient.GainAndBias)  &S34q2rB
Drag the graph horizontally to adjust contrast: lower on the left, higher on the right.

## CallToAction(LinearGradient.GainAndBias)  &CrsMzLM
Combine both directions and find the setting that matches the goal.


# RadialGradient: Dot  &8joV7XO

## Info &9eRmvkV
[RadialGradient] is similar to [LinearGradient], but it is based on distance from a center point.

## Info &NqSIZbM
Width and Offset shape the result.

A width of one aligns to the image height, which helps keep the result circular across aspect ratios.

## CallToAction &yYOjGaI
Adjust Width and Offset to create the circle.



# RadialGradient: Vignette  &xz2g7my

## Info &jFM5ipG
A transparent radial overlay is useful for a vignette that dims the corners.

## CallToAction &EWUggdw
Adjust width and blend mode to recreate the goal.



# RadialGradient: Polar Direction  &fh5ZCjF

## Info &34JEHEq
The radial gradient can also work in a polar, circular direction.

## CallToAction &ykjSboS
Recreate the goal.


# RadialGradient: Invert Pattern  &GADHWGQ

## Info &l8njeUQ
The Different blend mode can also combine multiple [RadialGradient] operators into patterns.

## CallToAction &HBBbuUs
Connect and adjust the parameters of the two gradients to recreate the pattern.




