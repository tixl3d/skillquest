# Trigger Events

## Info
Earlier, trigger events were mentioned.

Internally, trigger parameters are just boolean values: true or false.

## Info
What makes them special is how they are used.

In TiXL, triggers usually describe booleans that are true for a single frame, or parameters that only react when the value changes from false to true.

## Info
Many animation operators provide a [WasHit] output.

It becomes true whenever a new cycle starts and is a common trigger source.

## CallToAction
In this example, a value is constantly incremented, counting frames.

Reset the counter at the beginning of each bar.


# Maximum Random

## Info
Here, random values are generated continuously.

Using the [Keep] operator, the value is updated only when a new maximum is reached.

## CallToAction
Solve the puzzle.


# Maximum Random with Reset

## CallToAction
Build on the previous solution.

Reset the maximum value at the beginning of each bar.


# Detecting Random Steps

## CallToAction
Round a noise value into steps.

Count every time the rounded value jumps to the next step and solve the puzzle.
