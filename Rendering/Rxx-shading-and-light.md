# Shading with Light

## Info
So far, the default studio lighting has been used in all examples.

This setup consists of a 360-degree HDRI texture used for image-based lighting.

## Info
To better understand how lighting affects shading, the light will first be turned off.

## CallToAction(SetEnvironment)
The [SetEnvironment] operator provides multiple presets.

Use the "black" preset to disable image-based lighting.


## CallToAction(PointLight)
Add a [PointLight] and move it through the scene using 3D Perlin noise.

Use the same position to draw a [Sphere] as a visual indicator for the light position.

## CallToAction
Recreate the example.


# Custom Environments

## Info
A texture can be connected to [SetEnvironment].

It accepts either a CubeMap or an HDR environment texture.

## Info
In this example, a custom environment is created by cycling a [LinearGradient].

## CallToAction
All parameters are already set.

Connect the operators to recreate the example.


# Camera and Environment Order

## Info
To see the HDR environment in the background, the camera must be placed after [SetEnvironment].

This ensures the camera affects both the scene geometry and the background image.

## CallToAction
Fix the operator order in this example.


# Foggy

## Info
A useful shading technique is to add a [SetFog] operator.

It can be used to darken or colorize objects based on distance.

## Info
In this example, the far view distance introduces too much visual noise.

## CallToAction
Find the correct distance to match the reference.
