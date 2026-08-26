# Transforming Meshes

## Info
This chapter focuses on generating geometry.

As mentioned earlier, each mesh consists of two buffers stored on the GPU.

One buffer contains a list of vertices (corner points), and the second contains a list of triangles defined by references to three of these vertices.

## Info
You may remember the [Transform] operator and how it can be stacked to build increasingly complex transformations.

The [TransformMesh] operator looks similar, has the same parameters, and produces the same visual result.

However, it works very differently.

Each [TransformMesh] creates a **new mesh**.

## Info
Try to guess how many mesh buffers are used in this example.

Keep a number in mind before continuing.

## Info
It is three.

The first buffer contains the original cube.

The second buffer contains a rotated copy.

The third buffer is a new, larger mesh that combines both.

This final buffer is what gets drawn.

## CallToAction
Recreate the example.


# Combining Meshes

## Info
Continuing from the previous example, you might wonder why TiXL uses this approach.

It may sound less efficient at first, and in some cases it is.

## Info
However, this is a deliberate trade-off that is faster in most real-world scenarios.

Graphics cards struggle with drawing many small objects, where “small” means very few polygons.

It is much faster to draw a single object with millions of faces than to draw a thousand cubes with twelve faces each.

## Info
Each draw operation comes with overhead.

These operations are called draw calls.

If you exceed a few thousand draw calls per frame, performance will drop significantly, regardless of how powerful the GPU is.

## Info
There are many techniques to render complex scenes with few draw calls.

Combining many small meshes into a single larger mesh is one of them.

## CallToAction
Build the example.

Some operators already have their parameters set correctly.


# A Temple

## Info
Starting from small building blocks, very complex geometry can be created by repeating and combining them step by step.

## Info
Meshes are not just instructions but buffers that store computed results.

TiXL only recreates and updates these buffers when one of their parameters changes.

## Info
This behavior is called caching.

When operators in the graph fade slightly, they are cached.

The more of your graph is cached, the faster TiXL can render the scene.

## Info
In this example, [RadialRepeatMesh] and [GridRepeatMesh] are used to construct a small building.

## CallToAction
Figure out how to repeat the beveled cubes to form columns and walls.


# Merged Vertices

## Info
For best performance, TiXL reuses vertices whenever possible.

Vertices that occupy the same position are shared between faces.

## Info
In this plane, a [Scatter] effect is applied.

It does not behave as expected because vertices between adjacent faces are shared.

Since the vertices are the same, gaps cannot form between faces.

## Info
To fix this, the [SplitVertices] operator can be used.

## CallToAction
Recreate the example.


# UVs

## Info
Applying an image to a mesh is called texturing.

To define how the image maps onto the mesh, each vertex stores image coordinates in its U and V attributes.

## Info
Most generated or imported meshes already contain a UV set, even if it is not actively used.

In some cases, it is useful to modify these coordinates.

## Info
In this example, a new UV coordinate system is projected onto a [Torus] mesh.

## CallToAction
Reproduce the example.
