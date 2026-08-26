# Boolean Values

## Info
Booleans, or “bools”, are numbers with only two possible values.

They can be zero (false) or one (true). A boolean represents a single bit.

## Info
In TiXL, booleans are important because they are used by parameters that enable or disable things, such as checkboxes.

They are also used to drive trigger-like behavior. Triggers are covered in the next topic.

## CallToAction
Define a boolean value using the [Bool] operator.

You can toggle it directly in the graph. To move the operator without toggling it, use the drag handle on the left edge.


# Animated Boolean

## Info
In this example, the [AnimBool] operator generates a boolean value that turns true for a single frame at the beginning of a bar.

This kind of signal is useful for events and rhythmic logic.

## CallToAction
Recreate the example.


# Boolean Logic: And

## Info
The term “boolean” comes from a mathematician who developed a system to describe logic using true and false values.

One of the basic operations is “and”.

The result is true only when both inputs are true.

## CallToAction
Combine phases of short flashes with phases of silence using boolean logic.

Solve the puzzle.


# Boolean Logic: Range Test

## CallToAction
Test whether a noise value is between -0.1 and 0.1.

Figure out how to solve the puzzle.


# Boolean Logic: All

## Info
As projects grow, chaining many [And] operators can become cumbersome.

## Info
Unless you need to animate individual inputs, you can use the [All] operator instead.

It accepts multiple inputs and returns true only if all connected inputs are true.

## CallToAction
Replace the chain of [And] operators with [All] and recreate the example.


# Boolean Logic: Or and Any

## Info
The more relaxed siblings of [And] and [All] are [Or] and [Any].

They return true if at least one input is true.

## Info
In this example, several sequence animation operators are combined to simulate a rhythm pattern.

## CallToAction
Extend the logic so it works for all parts of the rhythm.


# Boolean Logic: Not

## CallToAction(Not)
Sometimes you need the opposite boolean value.

Use the [Not] operator to invert the signal and solve the example.
