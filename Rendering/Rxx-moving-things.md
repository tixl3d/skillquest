# Moving things

## Info

In computer graphics positions are defined as 3 values on the axis x, y, z.

In TiXL's coordinate system X is pointing right, y up and z- towards the camera.

You can use your thumb, pointing and middle finger of your right hand to remember their orientation.

## Info

Other software prefer different coordinate systems (e.g. xy forming the floor plan of CAD applications for architects).

With TiXL's default camera, 0,0,0 is in the middle of the screen so that a object that is 2 units high precisely touches the upper and bottom borders of the screen.

## Info

We can use the [AnimValue] and [Vector3] to build a small animation.

We will cover both operator in detail later.

## CallToAction

Adjust the values to recreate the reference example.

# Transform

## Info

Instead of setting the position of an object we can leave its position unchanged and instead define an offset to where it should be drawn.

This offset is called "Transformation", and can include position, rotation and scale.

## CallToAction

Let's try to recreate the animation by combining these operators.

All parameter in this examples are already set correctly. You only have to connect the ops in the correct order.


# Combining transforms

## Info

If you apply one transformation only another they will be joined to create a new transform.

You don't need to know or even understand math behind this. But if you're curious, you can visit the topic on "Matrices" later.

## Info

You can imagine each of the these transformation steps like the steps in a dance routing. After each step you stand at a new position, looking towards a new position. We can call this the "local coordinate system".

## CallToAction

Let's build an small example. Connect the [AnimVec3] to the [Transform] operator to create a simple eye animation.

You don't have to adjust any parameters. You connect the operators.

# Stacking transforms

## Info

Now ewe can combine this animated transform with another transform to move it towards the left.

# Instancing

## Info

In this step we are doing something special, because we are not only using a Transform to define something should be drawn.

We're going to draw the same thing at two different positions!

Computer geeks call this "instancing". Ant it's great because you can define and adjust all copies at once.

## Info

Instance is a very powerful concept and TiXL has many different methods to use it.

## CallTAction

Try to replicate the example.

# Transform order

## Info

When drawing multiple instances with [Transform] operators, you can imagine each branch like a story with a serious of events like "move right", "turn left", "make everything smaller", "now draw!".

Each step is an operator being applied at the current local coordinate system.

Each step sounds simple and logical.

But if you mirror the world first, rotating left ends up as a rotation right! So always walk the path step by step.

## Info

There are many operators related to moving things around. We can group them by what they're moving. Live images, Particles. Geometry etc.

Although they work very similar, the "teal command" [Transform] operator are different, because they will be combined into a single instruction and are basically for free.

We'll be cover the other types in their respective chapters. For now let's look at some move commands.

## Info

The [Group] operator comes with build in transform parameters, which is useful to group and move a bunch of things in a single step.

## CallToAction

Try to recreate this challenge using the given operators.

# Simpler transformations

## Info

Sometimes you only need to rotate, scale or offset because it makes it easier to read the graph.

Keep in mind that the order in which they are connected is important. Rotating first than moving results onto a different position than first moving and then rotating.

## CallToAction

Try to combine these operators in the right order without changing any of the parameters.

Typ: You can select drag a horizontal slice of the operator stack to rearrange the order.

# Spreading

## Info

Sometimes it's useful to arrange the connected operators. The [Spread] operator can help with this.

## CallToAction

Try to recreate this challenge using the given operators.


# Repeating

## Info

The [RepeatTransform] renders the connected input multiple times. This can be useful for some tasks. But keep in mind that this can become very slow quickly.

We will cover hot o replicate hundreds or even millions of objects in the topic on instancing.


## CallToAction

Try to recreate this challenge using the given operators.


# 

## Info

Finally it is sometimes useful to know at which position a serious of transformations end up.

The [Locator] operator needs to be connected like it is something that is drawn.

But instead of rendering something it keeps tis current position in world space.

## Info

You can use its second output to get this position.

Creating a connection from it needs some practice though: Do you see the small triangle at the bottom right corner?

That's the "additional output" indicator. Open it with your left mouse button and drag out the position output.

Sadly the [Text] operator only has xy position. So we have to use a separate [Transform] operator.

## CallToAction

Try to recreate this challenge using the given operators.
