# Analyzing images

## Info

On your journey into the world of procedural computer graphics you will reach teh point where trial and error is no longer good enough.

Maybe your contraption do not whatnot expect.

Or you see an effect that looks unexpected and you you want to understand where it comes from.

In these cases you need information and analyzing. 
Understanding that information is the best pathways to knowledge.

Let's look at some nice tools to analyst images.

The first one is ImageLevels we already encountered ii in the Topic on gradients.

Imagine slicing a line through an image and at each pint we map the brightness of all colors channels onto a graph.

In this case we can see how the curves sometimes merge where the image becomes grayscale.

## CallToAction

Adjust the gradient settings to reproduce the example.

# Color resolution

## Info

In this example we can see tha color steps in the secret image. 

It looks like the color resolution of our input image is crushed and forming visible edges.

## CallToAction

Get rid of the edges.

# Out of range

## Info

Something happened to this image.

Its brights are cut off which leading to an ugly visible edge where the colors reach pure white.

It might not be obvious at first glance but with [ImageLevels] it you see the edge immediately.

## CallToAction

Use [ToneMap] to adjust the max brightness.


# Does not compute

## Info

On noo. These colors are completely messed up! If colors are negative very strange things will happen if you try to blend or render this image!

The alpha channel should never exceed the range between 0 and 1.
Most Image operator will clamp that alpha channel to that range.

## Info

You can simply add a RemapColor operator to clamp.

It samples colors from a gradient in the valid range from 0 to 1. And all illegal colors exceeding that will be clamped.

## CallToAction

Fix that example.


# Color banding

# info most displays use 8 bit in color resolution. These 256 color steps are sometimes not enough for smooth gradients.

Can you see the ugly edges in this example?

## CallToAction

If you use the ImageLevels you can narrow the shown Curve Range.

It looks like the image is smooth. And yes, it uses 16bit so it has a much higher color resolution.

It's not the image that contains these artifacts, it's your display and it's a very common problem.

## CallToAction

A trick to get rid of the color banding is to add some noise.

Try to increase the smoothness by inserting a [Grain] operator.


# Blur Blur

## Finally let's look at this example.

We use a classic [Blur] operator, but the edges are not really smooth!

## CallToAction

Try to increase the smooth without adjusting the sample count.





