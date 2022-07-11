# NeuralStyleTransfer

Neural Style Transfer (NST) refers to a class of software algorithms that manipulate digital images, or videos, in order to adopt the appearance or visual style of another image. NST algorithms are characterized by their use of deep neural networks for the sake of image transformation. Common uses for NST are the creation of artificial artwork from photographs, for example by transferring the appearance of famous paintings to user-supplied photographs. Several notable mobile apps use NST techniques for this purpose, including DeepArt and Prisma. This method has been used by artists and designers around the globe to develop new artwork based on existent style(s).


## Problem

Given a style image and a content image, our goal is to output an image that represents both the style of one image with the content of another. The style image, typically an artwork, can be viewed as an image you want to "paint" the content image over. The content image represents the object(s) that you wish to include with the design of the style image. This is achieved via an optimization algorithm (that involves convolutional neural networks) that optimizes both the content features of the content image as well as the style features of the style image.


## Approach

We will generate artistic images using Style Transfer. It is an image processing technique by which styles and textures from one image can be transferred onto the other. For the project we will use VGG19 model, which is pretrained on more than million images from the ImageNet database. As such we only require a single pair of content image (image we want to transform) and style image (image in whose style we want to transform) for our project. Firstly, we will load and preprocess the content and style images. Then, we will use different layers of VGG19 model to extract content features from content image and style features from style image. A generated image will be then initialised from the content image. We will define content loss and style loss for comparing the generated image with the content image and the style image respectively.  Content loss and style loss will be aggregated to give total loss. To minimise the total loss we will iteratively calculate the gradients of the loss with respect to generated image, and then use an optimiser to update the generated image to get a new generated image whose total loss is low. Finally, generated image will be displayed with the content of content image and style of the style image.


Project Report Link: https://sites.google.com/view/neuralstyletransfer/home 
