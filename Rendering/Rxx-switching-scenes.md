# Switching scenes

## Info

For complex projects or setups it can be necessary to switch between different materials, objects, cameras or scenes.

All of the above are command operators that share the same connection type.

That means we can use a single operator to switch between them.

## Info

Imagine this operator like a fork on a track. You can either pick the left or the right side.

The switch operator works similar, but because it's using a multi input it can switch between as many tracks as you want.

## Info

The active branch is controlled by the Index parameter. As with all other index parameters in TiXL it starts counting with 0 and will roll over if it exceeds the count of connected inputs.

## CallToAction

Here is a simple example. 

Try to reconnect to match the example.

# Multiple switches

## Info

This example is slightly more complex, because we also use a [Switch] to control the [Material].

## Info

Do you notice how the inactive parts of the graph are fading out?

They are dormant and don't need to be updated.

# ??

## Info

The [Switch] operator has two magic index values!

If you set the index to -1 none of the connected scenes will be active -- and everything is "disabled". That can be useful to temporarily disable one or more branches of your project.

## Info

Inf you set the index to -2 ALL connections will be active.

## CallToAction

Try to recreate this example.

# Execute nothing!

Another method to disable all connected inputs is to use [Execute] and turn off its IsEnabled parameter.

Simple but effective.

## CallToAction

Try to recreate the example


# Pick vs. Switch

## Info

There are many other different operators switch between other types likes Images, Values, Meshes, etc. But confusingly these operators are called [Pick...].

## Info

This inconsistency is by design: Command is the only type in TiXL that can "undefined" or "inactive". All other operators (with very few exceptions) keep their last updated value.

A [LinearGradient] will remain a valid texture in memory, even if it is no longer updated or used.

## CallToAction

Enough theory. Let's pick some images!

Try to reproduce the example.
