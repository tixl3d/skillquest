# Switching Scenes

## Info
For complex projects or setups, it can be necessary to switch between different materials, objects, cameras, or entire scenes.

All of these are command operators and share the same connection type.

This allows a single operator to switch between them.

## Info
You can think of this operator like a fork in a track.

You can choose either the left or the right path.

The [Switch] operator works the same way, but because it supports multiple inputs, it can switch between many branches.

## Info
The active branch is controlled by the Index parameter.

Like all index parameters in TiXL, it starts counting at 0 and wraps around if the value exceeds the number of connected inputs.

## CallToAction
This is a simple example.

Reconnect the operators to match the reference.


# Multiple Switches

## Info
This example is more complex because a [Switch] is also used to control the [Material].

## Info
Notice how inactive parts of the graph fade out.

These branches are dormant and do not need to be updated.


# Special Index Values

## Info
The [Switch] operator supports two special index values.

If the index is set to -1, none of the connected branches are active.

This effectively disables all connected scenes and can be useful to temporarily turn parts of a project off.

## Info
If the index is set to -2, all connected branches are active at the same time.

## CallToAction
Recreate the example.


# Execute Nothing

## Info
Another way to disable all connected inputs is to use the [Execute] operator.

By turning off its IsEnabled parameter, nothing downstream will be executed.

## CallToAction
Recreate the example.


# Pick vs. Switch

## Info
There are other operators that switch between values such as images, numbers, or meshes.

These operators are called [Pick...] instead of [Switch].

## Info
This distinction is intentional.

Command operators are the only operator type in TiXL that can become undefined or inactive.

Most other operators keep their last valid value.

For example, a [LinearGradient] remains a valid texture in memory even if it is no longer updated or used.

## CallToAction
Enough theory.

Pick some images and reproduce the example.
