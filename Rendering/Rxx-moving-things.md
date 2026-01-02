# Moving Things

## Info
In computer graphics, positions are defined using three values along the x, y, and z axes.

In TiXL’s coordinate system, x points to the right, y points upward, and z points toward the camera.

You can use the thumb, index finger, and middle finger of your right hand to remember their orientation.

## Info
Other software may use different coordinate systems.

For example, some CAD applications use x and y as the ground plane.

With TiXL’s default camera, the position (0, 0, 0) is centered on the screen, so an object that is 2 units tall touches both the top and bottom edges of the view.

## Info
We can use [AnimValue] and [Vector3] to build a simple animation.

Both operators will be covered in more detail later.

## CallToAction
Adjust the values to recreate the reference example.


# Transform

## Info
Instead of changing an object’s position directly, you can keep it unchanged and define an offset that determines how it is drawn.

This offset is called a transformation and can include position, rotation, and scale.

## CallToAction
Recreate the animation by combining the given operators.

All parameters are already set correctly. Only the operator order needs to be fixed.


# Combining Transforms

## Info
When multiple transformations are applied, they are combined into a single transformation.

You do not need to understand the underlying math for now, but the topic of matrices is available later if you are curious.

## Info
You can think of each transformation step like a step in a dance routine.

After each step, you stand at a new position and face a new direction.

This is often referred to as the local coordinate system.

## CallToAction
Build a small example by connecting [AnimVec3] to [Transform] to create a simple eye animation.

No parameter changes are required.


# Stacking Transforms

## Info
You can combine an animated transform with another transform to offset it further, for example by moving it to the left.


# Instancing

## Info
In this step, a transform is not only used to define where something is drawn.

The same object is drawn multiple times at different positions.

## Info
This is called instancing.

It allows all copies to be defined and adjusted together.

## Info
Instancing is a powerful concept, and TiXL provides multiple ways to work with it.

## CallToAction
Replicate the example.


# Transform Order

## Info
When drawing multiple instances using [Transform] operators, each branch can be thought of as a sequence of events.

Examples include “move right,” “rotate,” “scale,” and finally “draw.”

Each operator is applied in the current local coordinate system.

## Info
The order matters.

If the world is mirrored first, a rotation to the left may appear as a rotation to the right.

Always follow the chain step by step.

## Info
There are many operators related to movement, depending on what is being moved, such as images, particles, or geometry.

The teal command-style [Transform] operators are special because they are combined into a single instruction and are effectively free.

Other movement operators are covered in their respective chapters.

## Info
The [Group] operator also provides built-in transform parameters.

This is useful for moving or rotating multiple objects together.

## CallToAction
Recreate the challenge using the given operators.


# Simpler Transformations

## Info
Sometimes it is clearer to use separate operators for rotation, scaling, or offset.

The connection order is still important.

Rotating first and then moving produces a different result than moving first and then rotating.

## CallToAction
Combine the operators in the correct order without changing any parameters.

Tip: you can drag a horizontal slice of an operator stack to reorder it.


# Spreading

## Info
Sometimes it is useful to arrange multiple instances in space.

The [Spread] operator can help with this.

## CallToAction
Recreate the challenge using the given operators.


# Repeating

## Info
The [RepeatTransform] operator draws its input multiple times.

This can be useful, but it can become slow when used excessively.

Efficient ways to render hundreds or millions of instances are covered later.

## CallToAction
Recreate the challenge using the given operators.


# Locator

## Info
Sometimes it is useful to know the final world-space position after a sequence of transformations.

The [Locator] operator is connected like a drawable object.

Instead of rendering geometry, it stores the current position.

## Info
The second output provides this position.

To access it, open the additional output indicated by the small triangle in the bottom-right corner and drag out the position output.

## Info
The [Text] operator only supports x and y positioning.

A separate [Transform] operator is therefore required.

## CallToAction
Recreate the challenge using the given operators.
