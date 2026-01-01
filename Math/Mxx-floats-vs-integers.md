# Integers vs Floats

## Info
For computers values are not all the same. They come in different formats.
In tixl we use 3 different types:
Floating point values are used for almost everything. From times, to radius or the strength of effects — most of these parameters are defined as floating point values.
The precision and format might be different for various parameters but internally they are all the same.

Integer values are different. The can only be changed in increments of one. They are used for all counts and indices and many modes.

To convert between these different types you can use FloatToInt and IntToFloat operators.

It would be convenient to do this conversion automatically and maybe this feature will come in a future version of tixl but for now you will need those operators.

## InfoFor(FloatToInt)
Note that the FloatToInt operator will not round. Everything behind the period will be zeroed out. Period.

## CallToAction
Let’s start with a bunch of small examples:

We want to use the time (remember in floating point) to drive which text we are swing.

Try to complete this example.

# Angle steps

## Info
In this example we want to change the rotation of our cube by increments of precisely 15 degrees.
This sounds like we could use the FloatToInt operator for this.

## CallToAction
Try to complete the example.

# Angle steps revised
I have to admit that the previous example was pretty constructed.
Rounding a floating point value is such a common task that tixl provides many operators for this.

The [floor] operator is identical to converting a float to an integer and back. It just zeros out the values after the period.

## CallToAction

Let’s try the last example again.

# Rounding

## InfoFor(Ceiling)
Sometimes it’s useful to round to the next upper whole number. 
The [Ceiling] operator does just that.

Try to solve the Example.

# Yet another Round(ing)

## CallToAction
And sometimes it can be useful to round to a fraction or a larger number.

Let’s try our earlier example again. 

Can you figure out  this example?

# Precision

## Info
Excellent — we are making great progress.

One final warning about floating point values: they might not be what you think they are! Internally the computer has to cramp these into 32 bits that don’t really love floating non-integer numbers. A lot of really smart people eventually came up with a standard compromise:
Small values (closer to zero) have a higher precision than very large values. The larger the value, the courser becomes the resolution and steps become larger and larger.

## CallToAction
As a example how bad this can become, check out this:

Can you figure out how many zeros you have to add to the factors to reproduce the example?

