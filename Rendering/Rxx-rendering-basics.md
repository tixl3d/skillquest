# From 3D to 2D

## Info

The final output of most things you build in TiXL will be images.

We sometime s call them "Textures" or "Image buffers".

You can check out the Skill Quest Topics on working with images to learn more about other methods to generate and use images.


You use the [RenderTarget] operator to render 3d geometry into an image. It's one of TiXL's most important operators that you're going to need all the time.

Ig might be useful to get some background knowledge how the RenderTarget works.

Imagine the target to be a blank canvas that is prepared for all the geometry connected into it (I.e. connected left or above it).

## Info

In the beginning of every frame it will first be cleared with a solid color. Then any "Draw" operator (that would be the teal colored command ops) can draw onto that canvas.

## Info

In this example the clearing is disabled.

## CallToAction

Try to reproduce the challenge.


# Z-Buffer

## Info

In computer graphics we use an algorithm called Z-Buffer to sort geometry so that distance objects are not drawn in front of geometry that are closer to the camera.

The RenderTarget operator automatically adds a Depth Buffer for this. And every "draw" operator has parameters that control it or how to its.

Operators are always drawn in the order they are connected.


## Info

In this playful example the orange Torus wants to be in the front.

## CallToAction

Try to solve this challenge.


# Multi sampling (MSAA)

RenderTarget uses "Multi Sampling Anti Aliasing" (MSAA) to smoothen jagged edges. This tells the graphics card to render all edges with a higher resolution.

MSAA is enabled by default.

As with all things in life, quality comes with a cost. In most cases you don't need to worry but for projects with 10s or 100s or RenderTargets that can really make a difference.

Sometimes you might even prefer a sharper look.

This challenge compares the different modes.

Notice how MSAA only makes a different Mesh edges not for images and raymarched geometry.

## CallToAction

Try to find the correct settings to replicate the example.




