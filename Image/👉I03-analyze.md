# Analyzing Images

## Info
As projects grow, trial and error is often no longer enough.

Sometimes an image looks wrong.
Sometimes an effect behaves in an unexpected way.

In these cases you need information. Understanding that information is the key to fixing the problem.

## Info
One of the most useful tools for this is [ImageLevels].

It samples a line through the image and maps the brightness of all color channels onto a graph.

## Info
In this example, the curves sometimes merge into a single line.

This happens where the image becomes grayscale, because all color channels have the same value.

## CallToAction
Adjust the gradient settings to reproduce the example.


# Color Resolution

## Info
In this example, visible color steps appear in the secret image.

The color resolution of the input looks crushed, turning smooth gradients into hard edges.

## CallToAction
Get rid of the edges.


# Out of Range

## Info
Something is wrong with this image.

Bright values are clipped, creating a visible edge where colors reach pure white.

This may not be obvious at first glance, but with [ImageLevels] the edge becomes clear immediately.

## CallToAction
Use [ToneMap] to reduce the maximum brightness.


# Invalid Colors

## Info
These colors are outside the valid range.

Negative color values can cause unpredictable results when blending or rendering an image.

## Info
The alpha channel should always stay between 0 and 1.

Most image operators clamp alpha automatically, but relying on that can hide problems.

## Info
A simple fix is to add [RemapColors].

It samples colors from a gradient in the valid 0–1 range and clamps values outside that range.

## CallToAction
Fix the example.


# Color Banding

## Info
Most displays use 8-bit color.

That means 256 steps per channel, which is sometimes not enough for smooth gradients.

## Info
In this example, you can see visible banding.

The image itself is smooth. TiXL uses 16-bit color here, so the data has much higher precision than the display.

The artifacts come from the display, not from the image.

## CallToAction
Use [ImageLevels] to narrow the curve range and confirm that the image data is smooth.

## CallToAction
Reduce visible banding by inserting a [Grain] operator.


# Blur Quality

## Info
This example uses a classic [Blur], but the edges still look rough.

Increasing the sample count is not always the best solution.

## CallToAction
Improve edge smoothness without changing the blur sample count.
