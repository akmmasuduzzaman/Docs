## The workflow of the process of face Expression is as follows:
- The image is taken input and the masked image of the image is made using mediapipe library. The mask image contains white area as the face skin and rest all is black. 
- Then the init image and the masked image is put into the stable diffusion pipeline in which the the realistic vision inpainting model is used as the main model. The prompt is passed in which contains the intensity and the expression taken input from the user. 
- Then, inpainting model changes the face expression and produces a result
- The result then is used to face swap using the original image to preserve the face of the original input
