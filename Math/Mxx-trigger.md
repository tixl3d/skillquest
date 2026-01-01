# Trigger events

## Info
In the beginning of the last chapter I mentioned “trigger events”. 

Internally trigger parameters are just ordinary Boolean values:they are either true or false. So nothing prevents you from connecting a Boolean to a trigger input.

In tixl triggers or events are just a convention to call booleans results that are only true for a single frame or parameters that only have an effect if they switch from false to true.

For example many of the anim operators have an additional WasHit output that returns true when a new cycle starts.

## CallToAction

In this example we are constantly incrementing a value, and thus counting frames.

Solve the example so that we reset the counter at the beginning of each bar.

# Maximum Random

## Info

In this example we are constantly creating random numbers and keep the value if it exceeds the last one.

To do this we can use the [keep] operator.

## CallToAction

Try to solve the puzzle.

# Maximum Random II

## CallToAction

Let’s build upon the last example and reset our highest value on the beginning of each bar.

# Random jump detector

## CallToAction

In this example we round a noise value. Then we count every time the rounded value jumps to the next step.

Can you solve this puzzle?