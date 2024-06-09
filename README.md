This file is in the public domain. Where a public domain declaration is not recognized, you are granted a license to freely use, modify, and redistribute this file in any way you choose.



# DoomGlowUnity

This is a faux volumetric light glow originally used in Doom 3. The Unity version (by Sean 'sh0v0r' Edwards) is based on the Unreal port of this effect (by Tim Sabo). New features by Super Whimsy.

![alt text](https://media2.giphy.com/media/v1.Y2lkPTc5MGI3NjExaWE2bzA2M3M5MnBmMGd6cHJtb2J1cTgxaGdhMGR6eGc1NXQycDV0NCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/eBTqYoBE4AU77siExH/giphy.gif "DoomGlowUnity")

Updates:

* Updated for modern Unity. This demo was made in Unity 2021.3.15f1 (URP), but should work in any modern Unity version.
* Glow fades out when below this distance (fadeDistanceMin)
* Glow has a distance to achieve max opacity (fullDistance)
* Glow fades out when exceeding this value (fadeDistanceMax)
* Glow can optionally follow dynamic objects (vehicles, enemies) with objectToFollow field
* Created Sample Scene


## Demo

DoomGlow > Sample_Scene > DoomGlow_Scene

A simple demo to showcase distance based fading and following a dynamic object.

## Basics

To implement in your project:
1. Create an empty parent transform, Add the DoomGlowManager component.
2. Create a Unity Quad as a child and add the DoomGlow component. You can have many siblings, the manager will collect them all and call their update methods.
3. Create a Material for the Quads with the Mobile Additive material and a simple small texture.
4. Configure the Doom Glow Components Mesh and Camera references. The mesh is the quad you'd like to DoomGlow. The camera is the main player camera of your scene.
5. Position and scale your quads where you want them.
6. Adjust the Push Distance, Fade Distance, and Color.



--

### Changelog

**DoomGlow code**
tim.tili.sabo@gmail.com -- http://yzergame.com/doomGlare.html

**Ideas by Simon**
https://simonschreibt.de/gat/doom-3-volumetric-glow/

**Unity Port: Sean 'sh0v0r' Edwards**
https://github.com/sh0v0r/DoomGlowUnity
This is a port of the Unreal Version by: @hollowdilnik https://twitter.com/hollowdilnik/status/1538098146588430336
it doesn't support all of the same features
It has been optimised and uses a parent Manager class to call the Update Mesh method if it is visible
The original Unity version relied on Screen Space conversions which didn't work well with VR

**Feature Updates: SuperWhimsy**
