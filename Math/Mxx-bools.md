# Are you a bit? Yes. Yes. No.

## Info
Booleans or “bools” are also numbers. Just very small ones: Boolean values can be zero (false) or one (true). A Boolean number represents a single bit. 

In tixl Boolean values have an important role because they are used be parameters that enable things (I.e. everything with a checkbox) and by trigger events. We will discuss triggers in the next topic.

## CallToAction

In this example we define a Boolean with the bool operator. 
You can toggle it directly in the graph. To move the operator you can use the drag handle on the left edge.

# Blinking

## Info
In this first example we use the AnimBool operator to generate a Boolean value that “blinks” true for a single frame at the beginning of a bar.

## CallToAction

Try to recreate the example.

# Bool... what?

## Info

You might be wondering about the name? Why don’t we call it booleans not bits?
This name comes from a Mathematician that invented a system to describe logical expression by combining these true and false values.

One of these expressions is called “and”. Its result is true only if both inputs are true.

## CallToAction
These expressions can be extremely powerful to define procedural animations.

In this example we combine phases of short flashes with phases silences.

Can you solve the puzzle?

# This is a test...

## CallToAction
In this example we test if a noise value is between -0.1 and 0.1.

Can you figure out how?

# Let's have it All!

## Info
When you are building more and more complex projects you might end up [and] all over the place.
You might notice that chaining multiple and operators is kind of cumbersome.

Pro tip: unless you want animate one of the and parameters (eg to only enable an effect for sometime) you can always use the [all] operator instead of [and].

This uses a multi input and returns only true, if all of the connected inputs are true.

Like in this example.

## CallToAction

# Or and Any

## Info
The relaxed siblings of the [And] and [All] operators are called [Or] and [Any].

They return true if any of the inputs are true.

In this example we use multiple sequence anim operators to simulate a drum pattern. 

## CallToAction

Let’s make it for all “parts” of the rhythm.


# Not

## CallToAction(Not)

Sometimes you need to invert an Boolean. You can use the [Not] operator for this.

Try to solve this example.