# Helicopter camera

## Info

So far we have used the [Transform] op to move things around. Alternatively we can move the camera to look at things from different positions and directions.

## Info

Within the SkillQuest interactive camera control is disabled to keep things simple. So we'll have to use operators for this.

## Info

A simple but effect operator is [OrbitCamera]. It spins the camera around a center and has parameters that allows to control its distance and orientation.

## Info

# Jump cuts

## Info

Many parameters of [OrbitCamera] come in pairs of two where the first component describes the actual angle and the second adds a "wobble" amount to add some secondary camera movement.

## Info

With this you can define some interesting orbital flight paths.

## CallToAction

We already adjust these parameters in this example.

Your task is to control random offset so we set a camera to a new random position on every beat.

# Camera Zoom

## Info
The [Camera] operator is the workhorse for most camera work in TiXL. It defines a gemara by setting a view position and target.

## CallToAction

In this example the FieldOfView needs to be animated so that we zoom into the image.

# Camera move

## Info

In this case we want to keep that moving cube in view.

## CallToAction

Try to connect operators. All parameters are already set correctly.


# ???

## Info

Just like [Transform] the camera only affects its input (i.e.everything connected on its left side).

## Info

But unlike [Transform] camera can't be combined. The last camera (the one furthest to the left) will override all previous cameras.

## CallToAction

Try to replicate this example.

# Scene in a scene

## Info

A very important detail is that [RenderTarget] sets a new default camera for all its content.

This will neatly keep scenes apart.

## Info

In this example we render another scene on then use it as texture for a cube.

## CallToAction

Try to replicate the example.

