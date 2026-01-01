# Transforming meshes

## Info

Let's talk about generating geometroy.

As mentioned earlier, each mesh is two buffers stored on your GPU. One for a list of corners (vertices) and a second one for a list of triangles defined by references to 3 of these vertices.

## Info

You might remember the [Transform] operator and how it can be stacked to build more and more complete transformations.

The [TransformMesh] operator looks the same and has the same parameters and even leads to the same visual results.

But don't be fooled! Because it's working completely different:

Every [TransformMesh] creates a NEW mesh.

## Info

Try to guess how many mesh buffers are used in this example. Have number in mind before pressing continue...

## Info
It's 3. Most people didn't see that coming: 

The first the actual cube.

The second is a rotated copy.

The 3rd is a new larger buffer, that includes both.

This final buffer is then drawn.

## CallToAction

Try to recreate the example.

# Combining meshes

## Info

Picking up from the last example you might be wondering while TIXL uses this method? It sounds slightly less efficient, and you are totally right. But...

## Info

... it's a compromise that will be faster in most cases. The graphics card has a very hard time individually drawing many small objects (small as in very few polygons).

It's much faster to draw a single object with millions of faces that 1000 cubes with 12 faces.

## Info

Draw something -- anything really -- comes with a lot of overhead. These draw operators are called "draw calls". And if you have more than a couple of thousand draw calls per frame, your animation will no longer run smooth. No matter how fast your graphics card is.

## Info

There are many methods to cleverly draw complex stuff with few calls.

Combining many small meshes into a single larger geometry is one of them.

## CallToAction

Let's try to build this example. 
Some of the operators already have the correct parameters.

# A temple

## Info

Starting from small building blocks you can create very complex geometry by repeating and combining it into more and more complex objects.

## Info

Because meshes are not only instructions but also buffers that contain the results of these instructions TiiXL will only create and update them if any of their parameters got changes.

## Info

This is called "caching" When operators on the graph fade out slight, you know they are cached. That's a great thing: Them more of your graph is cached, the faster TiXL can render it.

## Info

Let's take this example. We use a [RadialRepeatMesh] and [GridRepeatMesh] to create a small building.

## CallToAction

Can you figure out how to repeat the bevelled cubes to create its columns and walls?


# Merged vertices

## Info

We want to generate and render objects as fast as possible. For that TiXL resuses vertices (I.e. Corner points) if possible.

## Info

In this plane we want o apply a [Scatter] effect. But somehow it doesn't work as expected because the vertices between the faces are literally the sam.e So there can't be gaps between them.

## Info

To fix that we can use the [SplitVertices] operator.

## CallToAction

Try to replicated the example.

# UVs

## Info

We call the combinates of a mesh with an image "texturing". 

To define where each part of the image should go, each vertex stores the image position in the U and V attributes.

## Info

Most objects you load or generate already come with such a "UV-set", even if you're not using it.

But sometimes it's useful to change these coordinates.

## Info

In this example we are project a new coordinate system onto our [Torus] Mesh.

## CallToAction

Try to reproduce the example.