# An introduction to math  &otaAKv9

## Info(ValueQuiz)  &CzEdyEL

Math has a bad reputation. For many people, it felt pointless or confusing at school.

In TiXL, math is visual, playful, and actually useful. The following levels will teach everything needed, step by step.

## Info(Value)  &SdzTkb8

Math operators in TiXL are used to control parameters and animation.

There are different number types. We start with float values and explore others later.

## Info(Value)  &HCzQrbs

Connect this operator to the [ValueQuiz].

## Info(ValueQuiz)  &RjUQ59h

The [ValueQuiz] shows a target value and a graph at the bottom.

Find the correct value to solve the goal.

## Info(Value)  &o2Pj657

The most basic operator is [Value].

You can change its value in different ways:

1. Select the operator and use the Parameter Window.
2. Hold Ctrl and drag directly on the operator in the graph.

# Take that value!  &8R86EjU

## Info(RoundedRect)  &hLeRt0s

When an operator is selected, its parameters appear in the Parameter Window.

## Info(RoundedRect)  &7zmQq5L

Notice how the Scale parameter is highlighted.

This means it was changed from its default value.

Click the parameter name "Scale" to reset it.

## Info(RoundedRect)  &m6rVqOd

Static values are fine, but animation is better.

The Rotate parameter looks like a good candidate.

## Info(Time)  &2wuPR9p

The [Time] operator is perfect for animation.

But dragging it next to [RoundedRect] does not snap.

That is because [Time] outputs a number, while [RoundedRect] expects an image by default.

## Info(Time)  &QpAMfeX

Drag a connection from the [Time] output.

See the blinking dot on [RoundedRect]?

That means it has hidden parameters, like Rotate, that accept numeric input.

## Info(RoundedRect)  &ckYNrte

Drop the connection on [RoundedRect] and choose Rotate from the popup.

## Info  &HHcPfRz

Snap to the connected input to keep the graph tidy.

# I01c_Kalaidos  &mGUEmCV

## Info(MirrorRepeat)  &xJD23Dd

Repeating operators often leads to interesting results.

Here, a [LinearGradient] is repeated to form a kaleidoscope-like pattern.

## Info(LinearGradient)  &YgvV61e

Two parameters of the [LinearGradient] need adjustment.

Can you figure out which ones?

# Where the Path Begins  &HVoGwBo

## Info(RoundedRect)  &esJrfth

These early levels introduce the basics of working with TiXL's node graph.

## Info(ImageQuiz)  &HkJaGm6

Each level shows the target image at the bottom.

Recreate it using the available operators and connect them to the [Quiz] operator.

## Info(RoundedRect)  &SNlmZeY

Tip: If stuck, expand the Solution to see how it was built.

## Info(RoundedRect)  &mszyfJn

Start by learning how to connect operators.

Drag a connection from [RoundedRect] to [ImageQuiz].

# Riding the wave  &8l0343U

## Info(Sin)  &5J3IWfb

The [Sin] operator creates a smooth wave shape.

Yes, "Sine" would be the proper name.

## Info(Time)  &Mgi7wIR

To animate the wave, connect an animated value like [Time].

## Info(Time)  &Yp6fViA

Adjust the Speed Factor until it matches the goal.

# Get outta there!  &oqMRuV8

## Info(Blob)  &5ywJl3n

Sometimes an operator needs to leave a stack.

That bright orange [Blob] is a bit much.

Remove it by long-pressing and dragging it out of the stack.

# The Dark Sun  &iKP3QCU

## Info  &HllsRDn

This tour is still under construction.

# Saw!  &pFkvoXT

## Info(Modulo)  &dNRLyhV

If the [Sin] wave is too smooth, [Modulo] can help.

Modulo keeps a value looping. When it reaches a limit, it jumps back to the start.

This creates a sharp saw shape.

## Info(Time)  &AiNVGwU

Snap [Time] into [Modulo].

## Info(Modulo)  &ZpuWjcZ

Connect [Modulo] to the [ValueQuiz].

## Info(Modulo)  &fdCVHE7

Adjust the parameter to match the target.

# Swimming upwards...  &jEz14gc

## Info(RoundedRect)  &olR30GJ

The [RoundedRect] is already set up.

Leave its parameters unchanged.

## Info(MirrorRepeat)  &fxAa2u8

Focus on the [MirrorRepeat] operator.

It reflects images along an axis and is extremely flexible.

Only two parameters need adjustment to solve this challenge.

# Simple Chaos  &kr1bqNi

## Info  &4Q1Jigk

Even simple operators can create unexpected results when combined.

## Tip(Time)  &SxGS0XA

You may need to use the [Time] output more than once.

# So much time...  &AY4SKrL

## Info(Value:3)  &Tk717Br

Handling many numbers at once can be tricky.

Let TiXL do the heavy lifting.

## Info(Value:3)  &T4fIsVF

These [Value] operators were renamed using the Return key.

## Info(Value:3)  &DxYRgWF

Zoom into the graph to see live values.

## Info(Multiply)  &RoX0akt

Multiply all three values.

To connect additional inputs, drag outputs onto [Multiply] and watch for the blinking dot.

# Stack Attack  &py8vfdI

## Info(RoundedRect)  &G70qVyl

TiXL can snap operators into horizontal or vertical stacks.

This reduces clutter and makes graphs easier to read.

## Info(RoundedRect)  &UjKuxop

When operators get close, they snap and connect automatically.

Try dragging [RoundedRect] toward [Blob].

## Info(RoundedRect)  &GmYDs1r

Dragging a non-selected operator moves the entire stack.

Long-press to separate a single operator.

## Info(RoundedRect)  &8ye7X9m

Shake an operator to remove its connections.

## Info(RoundedRect)  &Oole6GS

Use Ctrl+Z to undo movements or disconnects.

## Info(Raster)  &iGh0wop

Tip: Operators can also snap into vertical stacks.

## Info(ImageQuiz)  &5qzgdcg

To finish the level, stack [RoundedRect], [Blob], and [Raster] onto [ImageQuiz].

# Speed it up!  &T7WeT4E

## Info(RoundedRect)  &4810LcS

The [RoundedRect] is rotating, but very slowly.

TiXL uses degrees. A full rotation takes 360 seconds at this speed.

## Info(Multiply)  &Sicxwam

Insert a [Multiply] operator between [Time] and [RoundedRect] to speed things up.
