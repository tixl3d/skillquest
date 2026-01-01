# ??

## Info

In TiXL we call geometry made from polygons a "mesh". Internally a mesh is a set of triangles that are defined by connection 3 corners (i.e. "vertices").

There are many operators to create or modify meshes. We ill cover many of them in the upcoming topics. In this topic we will focus on different methods to draw meshes.


## Info

Most of the relevant ops are start with the word "Draw" and have the teal command color.

## CallToAction

Let's start simple and draw a [Cube] and [Torus] mesh.


# ???

## Info

DrawMesh already adds some default material and lighting. We will explain how to change this in the upcoming topics.

Sometimes you din't need to even want shading.

For instance to draw an image directory onto a screen we have seen the [Layer2d] operator earlier. But an even simpler method is [DrawMeshUnlit].

## Info

As with all Draw-operators it comes with a Color parameter that gets multiplied.

Try to connect these ops to recrate the challenge.

Tip: You don't need to adjust any parameters.


# Simple solid image

## Info

In an earlier topic we talked about [RenderTarget] as a canvas that gets cleared before using it.

Sometimes you might need a simple image that only contains a single color. 

## Info

Note that the parameters of the [RenderTarget] are adjust to a tine size of 1 pixel and that we disabled MSAA and depth buffer to make it even faster. it's totally O.C.D. but hey faster is better if it doesn't make a visual difference.

# Transparent textures

As you might have learned by now: transparency makes everything more complicated, because we can no longer rely on the Depth-Buffer to sort the geometry.

And without depth buffer, distance objects could be draw on top of of nearby stuff, with some quite irritating results.

## Info

In this challenge we want to use a transparent Ryoji pattern to cover a cube. We also have to adjust the draw parameters so that we can see the insides.

To do this we have to do two things:

## Info

First we need to disable culling so the inside face -- that are facing away from the camera will actually be rendered.

## Info

Second we might need to adjust the alpha cut off parameter. This controls a threshold for which transparent pixels are considered as "holes" and will be "discarded".

## CallToAction

Try to complete the example.


# Hatching something out

## Info

There are a bunch of other operators to draw meshes. We will cover instance and field shaders later. But here is an interesting example that uses a special shader to draw a simple hatching style.


