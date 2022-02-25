# [Static3DModel-Dune](https://github.com/LegoGuy32109/Static3DModel-Dune)
*Static 3D Model assignment for Advanced Game Development class*

![Render of project](https://github.com/LegoGuy32109/Static3DModel-Dune/blob/main/Render.png?raw=true)

### My scene consists of:
* A **large** plane subdivideded a lot of times to resemble sand dunes (Manipulated with proportional edits)
* Multiple cones shaped to look like teeth
* Some extruded cubes that consist of the marble ruins
* A cylinder edited to look like a Sandworms maw
* Multiple procedrual textures (that I will get into)
* A little man running away from the scary sandworm (didn't walk arythmically)

## The textures
I have a marble texture consisting originally of a wave texture, with distortion applied to it. I fed that color through a ColorRamp to lower the blacks, and make it look more marbley. That is then fed as the color channel for a Principled BSDF which is then attached to the model of the ruins.

The other custom texture (that isn't just color) Is the Sand Worm's skin. I use a noise texture as the factor between two different colors, poop brown and bear brown, that adds those dark spots to the great sand beast. I also have a noise texture to add to the displacement of the model, which has a lower scale, detail, but higher roughness and the tiniest bit of distortion compared to the dark spots to give the skin a leathery dry look.

Almost forgot, the reason the sand looks so great is in addition to a yellow BSDF I have another noise texture (Noise textures are awesome) with a higher distortion in the displacement part of the model, so it adds all those awesome swirls.

## Woah, Cylinder to Sand Worm?
Crazy I know, I removed the ends of a 64 faced cylinder then used proportion editing (with the O key) to drag three parts of the model up to make the mouth flaps of the beast. This rounds it off so they're good looking flaps. I then used the snap to face tool (ctrl-tab) and took a modified cone shaped like a tooth, and duplicated it all over the inside of the maw. This saved so much time then trying to angle each tooth to face the right direction. Last but not least, I used an array modifier conrolled by an empty to angle the duplications into the ground. It's hard to tell but it's there, and that's how I made the worm so long.

## And the little guy, will he be ok?
No.

I made him the same way we make little dudes from cubes with a multiresolution modifier. I was going to pose him with armature bones but it wasn't working for me. In the future I would like for him to have armature bones so I could pose him. He's wearing a skin suit so he can convserve his water, with his little face poking out. Another thing I wanted to have happen was texture paint the inside of the beast's mouth so it would look more like the inside of a worm. Or at least add a pink shimmer around the teeth. I was able to get texture paint working, but I didn't like the results and went full procedural. Next time I will try harder to make texture paint look good.

This was my first time actually using procedural textures for a project, everything I have done in blender before never used texture nodes and just used the Diffuse option. I am very content with the results I could get with more in depth texture manipulation. I am sure to probably use a noise texture for everything in the future now, they are so fun.

*checks canvas assignment*
Uh, I have one camera to render the scene, I have a sun light source applying light to the whole scene at an angle to get that sweet shadow. I'm not sure if it counts as a primitive object but there's a suzanne head in the scene too.

## Reference
This image from the David Lynch movie *Dune*

![Sandworm Reference](https://nerdist.com/wp-content/uploads/2020/04/Sandworm-Dune-Lynch.png?raw=true)
