For my(Darren's) postprocess, I wanted to make a color distortion. In trying to find inspiration to use, I looked at the blendables postprocess
example from the content examples. The effect was similar to what I was going for, but I wanted to make the colors more psychidelic and interesting
to look at. To do that, I connected a SceneTexture:PostProcessInput0 node to a custom node that multiplied, frac'd, and divided the original float4 color.
Originally, I also attempted to include the SceneTexture functions and output as a part of the custom node, but the FMaterialCompiler that I needed to
use is a class and can't be accessed from custom nodes in the material editor. 

My result is that images in the volume retain much of their original color when the pixels are dark, but rapidly starts kaleidoscoping when light hits the surface of the object.