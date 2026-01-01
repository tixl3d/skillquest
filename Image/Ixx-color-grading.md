# "Color Grading"

## Info

Professional designers call the proceeds of adjusting and tweaking colors "grading". It often also deals with removing color tints or artifacts.

Again professional asks for precision. So we will need another tool for measuring.

## InfoFor(WaveForm)
This time it's called with the misleading name [WaveForm] and it will take some getting used to. But believe me: you will quickly understand why every professional app uses it.

Take a look at this example. At the bottom we can see the waveform overlay. It's similar to ImageLevels, but it not only shows a single curve for a slice through the image: it shows curves for all slices overlaid.

So you can quickly read all columns of the image and get an overview.

## Info

In this case we can see that the challenge somehow adjusted the saturation of parts of our image, because on the left side, all curved fall together into a single gray line.

## CallToAction
Try to reproduce the image.

# Getting better Grades

## Info

[ColorGrade] is a very powerful operator to adjusts colors. And once again it's closely related to core tools of many professional color grading apps. So you will be able to apply the knowledge of the topic directly to other software.

## Info

Its core is the 3 parameters gain, Gamma and lift. To get a feeling for how they work let's look at an example. The linear gray grader goes from pure black to pure white.

## Info

If the gain, gamma and lift parameters are pure gray they are neutral without an effect. As always you can click the parameter names to reset to default.

## InfoFor(ColorGrade.Gain)

Now use your right mouse button to drag the color thumbnail of **gain** up and down. Do you see the effect?

It affects the lightest colors.

## InfoFor(ColorGrade.Lift)

Try the same with **lift**. And it affects the dark colors.

## InfoFor(ColorGrade.Gamma)
Now try the **gamma** color. It adjusts the overall brightness, without affecting the lights and darks.

## Info

Tip: you can also drag the color thumb with the left button to adjust the Alpha channel and thus increase or decrease each effect.

## CallToAction
Recreate the challenge at the bottom.

# Conforming colors

## Info

In this level we will remove a color cast. Our example image looks too blue.

In the wave form we can see how the blue curve is higher than the reds and greens.

Our operator of choice for these kinds of tasks is the color grade. In this example it's already added. Select it.

## Info

Now click the color thumbnail of the gain parameter to open the color picker. 

We will talk about the other parameters later.

With pure gray the parameters have no effect. But if you start dragging the small handle in the color circle out of the gray center you will see an effect.

To get rid of the color cast we want to move slightly away from that to is complementary color. In this case yellow.

## Info

Tip: Holding shift key gives finer control.

## Info
TiXL's color picker is tweaked for this kind of operations because it shows more desaturated colors and keeps the highly saturated colors on the edges.

## CallToAction
Now try to find the right color by balancing the curves of the wave form.

# Going Hollywood

## Info
Many action movies like "Matrix" have a very distinct color grade -- sometimes called "teal/orange", "complementary" and sometimes just called "Hollywood look".

## Info
The idea behind this is to make bright orange skin tons pop in front of a dark bluish/greenish background. Separating these complementary colors adds a color contrast without losing image details.

## CallToAction(ColorGrade)

Let's create this look. Insert the [ColorGrade] operator and adjust the lift and gain parameters.
