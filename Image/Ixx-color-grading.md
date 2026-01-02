# Color Grading

## Info
In professional design, adjusting and refining colors is called “grading”.

It often involves shaping the overall look, but also removing unwanted color tints or visual artifacts.

Precise work requires precise measurement.

## InfoFor(WaveForm)
The tool for this is called [WaveForm].

The name can be misleading at first, but it is widely used in professional software.

It works similarly to ImageLevels, but instead of showing a single slice, it overlays slices from the entire image.

This allows you to read brightness and color distribution across all columns at once.

## Info
In this example, the curves on the left side merge into a single gray line.

This shows that parts of the image have reduced saturation, because all color channels share the same value.

## CallToAction
Try to reproduce the image.


# ColorGrade: Gain, Gamma, Lift

## Info
[ColorGrade] is a powerful operator for adjusting colors.

Its parameters are closely related to tools used in professional color grading software.

## Info
The core parameters are Gain, Gamma, and Lift.

The reference gradient goes from pure black to pure white.

## Info
If Gain, Gamma, and Lift are pure gray, they are neutral and have no effect.

You can click parameter names to reset them to their defaults.

## InfoFor(ColorGrade.Gain)
Adjust Gain by dragging its color thumbnail with the right mouse button.

It primarily affects the brightest parts of the image.

## InfoFor(ColorGrade.Lift)
Adjust Lift in the same way.

It primarily affects the darkest parts of the image.

## InfoFor(ColorGrade.Gamma)
Adjust Gamma to change overall brightness without pushing only highlights or shadows.

## Tip
Dragging the color thumbnail with the left mouse button adjusts the alpha channel.

This scales the strength of the effect.

## CallToAction
Recreate the challenge at the bottom.


# Removing a Color Cast

## Info
In this level, the image has a visible blue color cast.

In the waveform, the blue curve sits higher than the red and green curves.

## Info
[ColorGrade] is the appropriate tool for this task.

It is already present in the graph. Select it.

## Info
Open the color picker for the Gain parameter.

Pure gray has no effect.

Moving away from gray introduces a color shift.

To counter a blue cast, move slightly toward the complementary color: yellow.

## Tip
Hold the Shift key for finer control.

## Info
TiXL’s color picker is tuned for grading work.

It emphasizes usable, desaturated colors and keeps highly saturated colors near the edges.

## CallToAction
Balance the waveform curves to remove the color cast.


# Teal and Orange

## Info
Many action movies use a distinct “teal and orange” color grade.

Warm highlights contrast with cool shadows, creating separation without losing detail.

## CallToAction(ColorGrade)
Insert a [ColorGrade] operator and adjust Lift and Gain to create the look.
