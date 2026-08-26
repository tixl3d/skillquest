# Helicopter Camera

## Info
So far, the [Transform] operator has been used to move objects.

Alternatively, the camera itself can be moved to view the scene from different positions and directions.

## Info
Within SkillQuest, interactive camera controls are disabled to keep things focused.

Camera movement is therefore controlled entirely through operators.

## Info
A simple but effective operator for this is [OrbitCamera].

It rotates the camera around a center point and provides parameters to control distance and orientation.


# Jump Cuts

## Info
Many [OrbitCamera] parameters come in pairs.

The first value defines the base angle, while the second adds a wobble component for secondary motion.

## Info
This allows the creation of more dynamic orbital flight paths.

## CallToAction
These parameters are already adjusted in this example.

Control the random offset so the camera jumps to a new random position on every beat.


# Camera Zoom

## Info
The [Camera] operator is the main camera operator in TiXL.

It defines a camera by setting a view position and a target.

## CallToAction
In this example, animate the FieldOfView parameter to zoom into the image.


# Camera Move

## Info
In this case, the goal is to keep the moving cube within the camera view.

## CallToAction
Connect the operators so the camera follows the cube.

All parameters are already set correctly.


# Camera Override Rules

## Info
Like [Transform], a camera only affects its input.

This means it applies only to operators connected on its left side.

## Info
Unlike [Transform], cameras cannot be combined.

The last camera in the chain (furthest to the left) overrides all previous cameras.

## CallToAction
Replicate the example by arranging the camera operators correctly.


# Scene in a Scene

## Info
[RenderTarget] establishes a new default camera for everything rendered inside it.

This keeps scenes cleanly separated.

## Info
In this example, a secondary scene is rendered and then used as a texture on a cube.

## CallToAction
Replicate the example.
