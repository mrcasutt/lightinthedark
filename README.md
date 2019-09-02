# Light in the dark

Following the Fast.ai course by Jeremy Howard to build an app that can brighten hopelessly too dark images. 

This notebook uses best practices tought by Jeremy Howard to train a Unet and build a model. 

Images are downloaded from Google Images. A short script resizes the large image files to 3 sizes: 96px, 256px and 1200px
During this process, the images are darkend using Pil.enhance with a random brightness value between 0.2 and 0.5, additionaly text artifacts and random quality settings are used to "crappify" images.

The training is done in a couple of steps. Starting with small images, the last layers of the network are trained. After unfreezing the model and training the whole network these steps are repeatd with medium and larg sized images. 
