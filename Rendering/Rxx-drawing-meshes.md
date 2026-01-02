# Drawing Meshes

## Info
In TiXL, geometry made from polygons is called a mesh.

Internally, a mesh is a collection of triangles. Each triangle is defined by three corners, called vertices.

## Info
There are many operators to create and modify meshes.

In this topic, the focus is on different ways to draw meshes.


## Info
Most operators that draw meshes start with the word “Draw”.

They use the teal command color, which indicates that they render geometry.

## CallToAction
Start simple.

Draw a [Cube] and a [Torus] mesh.


# Unlit Drawing

## Info
[DrawMesh] applies default material and lighting automatically.

How to change materials and lighting is covered in later topics.

## Info
Sometimes you do not want any shading at all.

For example, when drawing an image directly onto a surface, shading can be distracting.

In earlier topics, [Layer2D] was used for this purpose.

An even simpler option for meshes is [DrawMeshUnlit].

## Info
Like all draw operators, it includes a Color parameter that is multiplied with the result.

## Tip
You do not need to adjust any parameters for this example.

## CallToAction
Connect the operators and recreate the challenge.


# Solid Color Image

## Info
Earlier, [RenderTarget] was introduced as a canvas that is cleared before drawing.

## Info
Sometimes a project needs a simple image that contains only a single color.

## Info
In this example, the [RenderTarget] is set to a size of one pixel.

MSAA and the depth buffer are disabled to reduce overhead.

This setup is intentionally minimal and optimized.

## CallToAction
Recreate the example.


# Transparent Textures

## Info
Transparency makes rendering more complex.

Once transparency is involved, the depth buffer can no longer reliably sort geometry.

As a result, distant surfaces may appear in front of closer ones.

## Info
In this challenge, a transparent Ryoji pattern is applied to a cube.

The goal is to see both the outside and the inside faces.

## Info
To achieve this, two things are required.

First, back-face culling must be disabled so faces pointing away from the camera are still rendered.

## Info
Second, the alpha cut-off parameter may need adjustment.

It defines a threshold at which transparent pixels are treated as holes and discarded.

## CallToAction
Adjust the draw settings and complete the example.


# Hatching Style

## Info
There are additional operators for drawing meshes with specialized shaders.

Instancing and field shaders are covered later.

## Info
This example uses a shader that produces a hatching-style look.

It is a good example of how drawing operators can define visual style directly.

## CallToAction
Recreate the example.
