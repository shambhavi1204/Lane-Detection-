# Lane-Detection-
Lane detection algorithm for autonomous bot.
Fusion Lane Detection Model:

FCN-8 : This model worked well for detecting lanes in bright as well as dim environment but it had lot of noise in the output prediction from the model. As a result, 	it became difficult to distinguish lanes from different obstacles that were getting detected alongside.

UNET :  This model because of its backbone network could extract spacial features very well but due to constant downsampling and upsampling of images, it starts to 	lose details in the input image. Thereby, resulting in a comparatively less noisy output image. The problem with this model is that it also fails to detect the 	lanes in certain environment and the output seemed to be slightly affected by the lighting condition.

Fusion : Therefore we came up with a model that combined both unet and fcn-8 architecture and tried to get the best of two models. we fed the input image to UNET model 	and fed the output from UNET to FCN-8. This was done keeping in mind that UNET would give me output image which will be less noisy and then the FCN-8 model can 	extract the lanes more effectively from a less noisy image. The resultant output seemed to have far better lane detection than any of the two working 	individually. Though the image is slightly noisy.
