# faceAR


- Automatically identify different regions of a detected face, and use those regions to overlay assets such as textures and models in a way that properly matches the contours and regions of an individual face

- Use the 468-point facemesh that is provided by ARCore to apply a custom texture over a detected face

- For tips and practices on creating custom assets,, refer to [Creating Assets](https://developers.google.com/ar/develop/developer-guides/creating-assets-for-augmented-faces) for Augmented Faces.

- we will be creating two files from .fxb i.e, .sfa and .sfb, .sfb is for rendering and .sfa is human readable.
- Use ModelRenderable.Builder to load the *.sfb
- When a user's face is detected by the camera, ARCore performs these steps to generate the augmented face mesh, as well as center and region poses:

1) It identifies the center pose and a face mesh.
2) The center pose is the physical center point of the user's head (in other words, inside the skull). This is behind the nose.
The face mesh consists of hundreds of vertices that make up the face, and is defined relative to the center pose.
3) The AugmentedFace class uses the face mesh and center pose to identify face region poses on the user's face. These regions are:
- Left forehead (LEFT_FOREHEAD)
- Right forehead (RIGHT_FOREHEAD)
- Tip of the nose (NOSE_TIP)
4) The AugmentedFace class extends the Trackable class.

