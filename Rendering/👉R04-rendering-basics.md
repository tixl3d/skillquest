# From 3D to 2D

## Info
The final output of most things you build in TiXL are images.

These are sometimes called textures or image buffers.

You can explore the SkillQuest topics on working with images to learn about other ways to generate and use them.

## Info
The [RenderTarget] operator is used to render 3D geometry into an image.

It is one of the most important operators in TiXL and is used in many projects.

It can be helpful to understand how the RenderTarget works internally.

## Info
You can think of the RenderTarget as a blank canvas.

All geometry connected to it (from the left or above) is prepared to be drawn onto this canvas.

## Info
At the beginning of each frame, the RenderTarget is cleared with a solid color.

After that, any draw operator (the teal command operators) can render onto it.

## Info
In this example, clearing is disabled.

## CallToAction
Reproduce the challenge.


# Z-Buffer

## Info
In computer graphics, an algorithm called the Z-buffer is used to ensure that distant objects are not drawn in front of objects that are closer to the camera.

The [RenderTarget] operator automatically provides a depth buffer for this purpose.

Each draw operator has parameters that control how it interacts with depth.

## Info
Operators are still drawn in the order they are connected.

Depth testing determines whether a fragment is visible.

## Info
In this playful example, the orange torus should appear in front.

## CallToAction
Solve the challenge.


# Multisampling (MSAA)

## Info
RenderTarget uses multisample anti-aliasing (MSAA) to smooth jagged edges.

This instructs the graphics hardware to render edges at a higher effective resolution.

MSAA is enabled by default.

## Info
Higher quality comes at a performance cost.

In most projects this is not an issue, but scenes with dozens or hundreds of RenderTargets can be affected.

In some cases, a sharper look may even be preferred.

## Info
This challenge compares different MSAA modes.

Notice that MSAA affects mesh edges, but not images or raymarched geometry.

## CallToAction
Find the correct settings to replicate the example.
