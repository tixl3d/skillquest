# Rendering

## Info
TiXL uses physically based rendering (PBR) for lighting and materials.

This model defines material properties such as roughness and metallic, and combines direct lighting with image-based lighting (IBL).

This chapter introduces the essential concepts needed to work with materials.

## Info
By default, TiXL uses a predefined studio lighting setup.

The default material is too rough to clearly show reflections, so a new [Material] operator is added to adjust this.

## CallToAction
Add a [Material] operator and adjust its roughness to match the reference.


# Is It Shiny?

## Info
The Metallic parameter defines whether a surface behaves like a metal or a non-metal.

Non-metallic materials such as plastic or stone show their color through diffuse lighting.

Light enters the surface and exits tinted by the material color.

## Info
Metallic materials show their color primarily through reflections.

They do not use diffuse lighting in the same way.

## Info
In theory, the Metallic parameter should be either 0 or 1.

TiXL does not enforce this rule, allowing intermediate values.

## CallToAction
Study the reference example and observe the difference.

Recreate it.


# Material Textures

## Info
So far, only color parameters of [SetMaterial] have been used.

Each of these parameters also provides a texture input that allows images to be connected.

## CallToAction
Recreate the color example using texture inputs.


# Multi-Channel Textures

## Info
The roughnessMetallicOcclusion texture parameter is special.

It expects a channel-packed texture where each property is stored in a different color channel.

## Info
The [Combine3Channels] operator can be used to construct such textures.

## CallToAction
Recreate the example.


# Alpha

## Info
The base color of a material is called the albedo.

The term comes from Latin and refers to lightness, similar to diffuse color.

It represents the material color without shading or shadows.

## Info
The alpha channel of the albedo defines material opacity.

In this example, an alpha gradient is animated across the surface.

## CallToAction
Reproduce the animation.


# Emitting Light

## Info
Materials can emit light using the emission color and emission texture parameters.

The texture and color values are multiplied.

The default emission color is black, so emission textures remain invisible until the color brightness is increased.

## Info
HDR emission values greater than 1 work particularly well when combined with a [Bloom] post-processing effect.

## Info
In this example, the highlight color of [RyojiPattern] is brightened to create a glow effect.

## CallToAction
Recreate the example.


# Normal Mapping

## Info
Raymarched SDFs will be covered in detail later.

Since they use the same material and lighting system, they can be used here to demonstrate normal mapping.

## Info
Normal maps store surface curvature information in their color channels.

They are commonly used to add fine surface detail without increasing geometry complexity.

## Info
Normal map formats vary.

The [NormalMap] operator converts a grayscale height map into a normal map.

## Info
In this example, a [FractalNoise] operator is animated to drive the normal map.

The noise must be seamless to avoid visible artifacts where the pattern wraps.

## CallToAction
Recreate the example.
