README - MICHAEL'S FINAL PROJECT

My project is not complete, and what I present here is as far as I was able to get.

When run, this code will successfully accomplish the following:

1) Identification of the gut region in a sample brightfield image of the hindgut of a zebrafish, taken on the HTP lightsheet microscope in Klamath.
2) Generation of a mask that removes all parts of an image that do not overlay with the specified gut region.
3) Apply the mask to a sample set of images of a transgenic zebrafish (mpo:GFP) that correspond to the brightfield image used to generate the mask.
4) Display images of the original brightfield image, the masked brightfield image, and all masked images in the z-stack.
*NOTE:  The z-stack images will look like there are no neutrophils unless you look closely. about 20-25% of the way down in the images, you can see several neutrophils.

What my code does not yet do:

1) I wasn't able to link up my gut identification code with Teddy's neutrophil counting code, because I wasn't able to figure out what data form a 3-D image stack
is packed as, and I wasn't able to modify my pathlist function to fit into Teddy's code. I feel like I can do this with more time, but really I just need to sit
down with Teddy to understand how to specify the image stack's data type. I included Teddy's code at the end of my notebook, so when you run this it will do everything
listed above, and then throw the error: "NameError: name 'images' is not defined"

2) Also, my code currently does not automatically identify the region markers that specify the full gut. I believe with some more work I can either accomplish this,
or tweak the parameters in my functions so that the hindgut is regularly being identified with a single region marker. I also played around a bit trying to watershed
a RAG thresholded image, which was providing some benefits but also some problems. It's another potential solution I'm going to try.