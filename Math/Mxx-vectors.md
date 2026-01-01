# Hello Vectors!

## Info

In the previous topics we have been talking about float and integer values.

In this topic we will combine them into “vectors”. You can imagine a vector as a group of values representing different components. Depending on the context these can be coordinates like x, y, z. Color channels like r, g, b or sizes like width and height.

In tixl they can have a size of two, three and four components and consist of floating or integer values.

## Info
Let’s start by building some vectors!

In this example we will use the [Vector3] to combine a noise and animValue to control the position of a text with a Vector.

## CallToAction

Can you figure our the correct parameters?


# Breaking stuff

## Info

You can use the [Vec3Components] operator to access the individual components of a vector.

In this example we want to position the [Text] operator to the [perlinNoise3] position.

## CallToAction
Try to solve the puzzle

# How long is yours?

## Info

We can use the [Length] operator to compute the “magnitude” of a vector. This can be quite useful.

In this example, we want to draw circle with the correct size so that it touches our random point.

Notice how we can use the handy [Vec2ToVec3] operator to add a value so we can connect it to the sphere’s position.

## CallToAction
Try to solve this puzzle.

# Scaling Vectors

## Info
It can be very useful to scale the magnitude of a vector.

Here we’re extending our last example so that the random position oscillates between small and large values.

## CallToAction

Try to solve this puzzle.

# Totally normal

## Info

The opposite of calculating a vectors length is to convert it into a direction with the length of 1. 

This operation is called Normalization and is very common in computer graphics.

## Info

Let’s look that this interesting example: after normalizing a random vector its radius becomes one.

When we use it to draw a point trail it becomes a sphere!

## CallToAction

Try to solve this puzzle.

# Orientation class

## Info

In this example we use the random position to position and orient a point on the surface of a sphere.

## CallToAction
Can you figure out how to do it?

# Rotation

## Info
Sometimes we want to "construct" positions.

In this can we take a vector and rotate it around a random axis with quite interesting results.

## CallToAction
Can you figure out how to do it?

# Quat-what?

## Info

Speaking of rotations. Sooner or later you will hear the term “quaternion” with various undertones of mathematical mastery, ignorance or pure angst. 

But you don't have to understand how they work to use them, though.

## Info

They are a vector with 4 components x, y, z, and w and very useful to define and blend rotations.

Internally tixl uses quaternions all over the place. But they are rarely used in parameters, because most people will not be able to read or even enter a rotation in this format.

## Info

Most rotation parameters in TiXL use Euler angles that come with their only bag of problems. 

In the few cases where we actually need a "precise" rotation, TiXL will ask for an axis and a rotation angle around it.

So the only really confusing thing about quaternions in TiXL will be that it assumes Vector4 to be colors!

## Info

Here is a rare example for a use-case: blending between two rotations.

## CallToAction

Try to solve this puzzle.
