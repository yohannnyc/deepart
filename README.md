# TensorFlow implementation of "A Neural Algorithm of Artistic Style"

With their 2015 paper, Gatys et al. allow us to do a bit of time travelling and invite our favorite artists to paint a scenery we love or portraits of family members.
They showed that we could use Convolution Neural Networks to mix the content of an image with the style of another.
They used the pretrained VGG-Network CNN, its 16 convolutional and 5 pooling layers.
Reconstruction of the content image: lower layers simply reproduce the exact pixel values of the original image. Higher layers in the network capture the high level content in terms of objects and their arrangement in the input image. Hence we use the 4th convolution layer
To extract the style of an image, we compute the correlations between the different filter responses over the multiple layers. We obtain a multi-scale representation that captures the texture but not the arrangement of objects.
