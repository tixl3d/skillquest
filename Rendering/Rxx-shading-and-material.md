# Rendering

## Info

TiXL uses physically based rendering (PBR) to define light and materials. This defines material properties (like "roughness" and "metallic") and direct and indirect image based lighting (IBL).

This topic will walk you through everything you need to know.

## Info

By default TiXL uses a predefined default studio setup.

The default material is too rhough to see it, but we can insert a new [Material] to change that.

## CallToAction

Add the [Material] and adjust its roughness to match the reference.


# Is it shiny?

## Info

The metal parameter defines wether a surface behaves like a metal or a non-metallic material. 

"Non-metals" like plastic or stone show their color through diffuse lighting: The light will enter the surface and then exit with some color. 

"Metals" show their color only in the reflection.

## Info

In theory ths parameter should be 0 or 1 (and nothing in between). But TiXL will not enforce this rule.

## CallToAction

Take a look at this reference example. Can you see the difference?

Try to rebuild it.

# ????

## Info

Until now we have been using the color parameters of [SetMaterial]. 

But each of them also comes with a Texture input that allows to connect an image.

## CallToAction

Try to recreate this color example.

# Multi channel textures

The texture-prameter for roughnessMetallicOcclusion is special. It requires a channel map that defines earch in tis red, green and blue channels.

## Info

We can use the [Combine3Channels] operator to define such complext materials.

## CallToAction

Try to recreate this example.

# Alpha

## Info

The basic color of a material is called "albedo". That's latin for "lightness" and similar to "diffuse" color. It's the base color of the material without shading or shadows.

Its alpha channel defines the opacoty of the material.

In this example we slide an alpha gradient across the material.

## CallToAction

Try to reproduce this animation.


# Emitting light

## Info

Sometimes you want to have light emmitting materials. You can achive this with the emission texture and color parameters.

Texture and color paramters are always multiplied. The default emissive color is black, so texture will not be visible until you increase the brightness of the emissive color.

## Info

Emissive HDR colors that are brighter than 1 look especially nice when applying a [Bloom] post processing effect.

## Info

In this example we increased the brightness of the [RyojiPatern]'s highlight color to create a glow effect.

## CallToAction

Try to recreate the example.

# Normal mapping

## Info

We will cover raymarching SDFs in a detail later. But since they use the same material and rendering algorithms we can use it in this example to discuss "normal maps".

These are textures that use their color channels to store how the surface is curved. This can be nice to add "bump" details to a procedural object.

## Info

Creating normal maps can be tricky because there are multiple diffrerent formats. We can use the [NormalMap] operator to convert a gratscale height map into a normal map.

## Info

In this example we animate a [FractalNoise] operator to drive the normal map. But we have to make it seamless to avoid artefact where the patterns repeats on the other side.

## CallToAction

Try to recreate this example.








