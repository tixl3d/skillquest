# Vectors

## Info
So far, float and integer values were used on their own.

Now they are combined into vectors.

A vector is a group of values that belong together.

## Info
Depending on context, vector components can represent:
- positions (x, y, z)
- colors (r, g, b)
- sizes (width, height)

In TiXL, vectors can have two, three, or four components and can use floating-point or integer values.

## Info
Let’s start by building some vectors.

## CallToAction
Use [Vector3] to combine a noise value and an animation value.

Use the result to control the position of a [Text] operator.

Find the correct parameters to match the goal.


# Accessing Vector Components

## Info
The [Vec3Components] operator allows access to the individual components of a vector.

## CallToAction
Position the [Text] operator using the output of [PerlinNoise3].


# Vector Length

## Info
The [Length] operator computes the magnitude of a vector.

This is often useful when distance-like behavior is needed.

## Info
In this example, draw a circle large enough to touch a random point.

The [Vec2ToVec3] operator can be used to add a missing component so connections work correctly.

## CallToAction
Solve the puzzle.


# Scaling Vectors

## Info
Scaling a vector changes its magnitude.

In this example, the random position oscillates between small and large values.

## CallToAction
Solve the puzzle.


# Normalization

## Info
Normalization converts a vector into a direction with a length of one.

This is a very common operation in computer graphics.

## Info
Here, normalizing random vectors causes all points to lie on the surface of a sphere.

## CallToAction
Solve the puzzle.


# Orientation

## Info
In this example, a random direction is used to position and orient a point on the surface of a sphere.

## CallToAction
Figure out how to solve the puzzle.


# Rotating a Vector

## Info
Sometimes positions are constructed intentionally.

In this case, a vector is rotated around a random axis to create structured motion.

## CallToAction
Solve the puzzle.


# Quaternions

## Info
Sooner or later, the term “quaternion” comes up when talking about rotations.

Understanding the math is not required to use them in TiXL.

## Info
A quaternion is a four-component rotation representation: x, y, z, and w.

It is useful for defining and blending rotations.

## Info
TiXL uses quaternions internally in many places.

Most parameters use simpler representations, such as Euler angles or axis–angle rotations.

## Info
One confusing detail is that Vector4 values are often interpreted as colors.

## Info
This example shows a rare case where quaternions are used directly: blending between two rotations.

## CallToAction
Solve the puzzle.
