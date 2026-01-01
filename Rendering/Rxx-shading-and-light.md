# Shading with light

## Info

So far we have been using the default stdio light for all examples.

This setup contains of a 360 degree texture HDRI map.

Lets begin by turning of the light and set what happens.

## CallToAction(SetEnvironment)

The [SetEnvironment] operator comes with multiple presets.

We can use the "black" preset to turn off the IBL lighting.

## CallToAction(PointLight)

Now we can add a [PointLight] and move it around in our scene using a 3d perlin noise.

We can use the same position to draw a [Sphere] to indicate the position of our light.

## CallToAction

Try to recreate the example.

# Custom environments

## Info

we can pass a texture into the [SetEnvironment]. It takes either a CubeMap or an HDR environment.

## Info

Let's create a custom environment by cycling a [LinearGradient].

## CallToAction

We already set up all the parameters in this example. But you still have to connect the operators to recreate the example.

# ???

## INfo

If you want to see the HDR map in teh background have to make sure that the camera is et correctly after [SetEnvironment], so that the camera is applied to both, the scene and the background image.

## CallToAction

Fix the operator order in this example.


# Foggy

A nice shading trick is to add a [SetFog] operator to colorize or darken objects in the background.

## Info

In this example the far view distance adds a lot of visual noise.

## CallToAction

Can you find the right distance to match the reference?

