# Integers vs Floats

## Info
For computers, values are not all the same. They come in different formats.

In TiXL, three numeric types are commonly used.

Floating-point values are used for most parameters: time, radius, strength, positions, and animation inputs.  
While their precision or range may differ depending on the parameter, internally they all behave the same.

Integer values are different. They can only change in steps of one.  
They are used for counts, indices, and many mode or selection parameters.

## Info
To convert between these types, use the [FloatToInt] and [IntToFloat] operators.

Automatic conversion might be convenient, and may exist in the future, but for now these operators make the conversion explicit.


## InfoFor(FloatToInt)
The [FloatToInt] operator does **not** round.

Everything after the decimal point is removed. Period.


## CallToAction
Let’s start with a small example.

Use time (a floating-point value) to control which text is shown.

Complete the example.


# Angle Steps

## Info
In this example, the rotation of a cube should change in steps of exactly 15 degrees.

This sounds like a good case for [FloatToInt].

## CallToAction
Complete the example.


# Angle Steps (Revisited)

## Info
The previous example was a bit artificial.

Rounding floating-point values is common enough that TiXL provides dedicated operators for it.

## Info
The [Floor] operator converts a float to an integer and back.

It keeps the whole-number part and removes everything after the decimal point.

## CallToAction
Solve the previous example again, this time using [Floor].


# Rounding Up

## InfoFor(Ceiling)
Sometimes it is useful to round up to the next whole number.

The [Ceiling] operator does exactly that.

## CallToAction
Solve the example using [Ceiling].


# Rounding to Steps

## Info
Rounding is not limited to whole numbers.

Sometimes you want steps like 0.25, 10, or 100.

## CallToAction
Recreate the example by rounding to a custom step size.


# Precision

## Info
One important warning about floating-point values:

They are not infinitely precise.

Internally, most floating-point numbers are stored using 32 bits. This is a compromise that allows a wide range of values, but not equal precision everywhere.

Small values (close to zero) have higher precision.  
As values grow larger, the resolution becomes coarser and the steps between representable numbers increase.

## CallToAction
As an example of how visible this can become, look at the following setup.

Figure out how many zeros need to be added to the factors to reproduce the example.
