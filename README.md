# What İs The U-Net

<img src="https://www.frontiersin.org/files/Articles/482352/fonc-09-00964-HTML/image_m/fonc-09-00964-g002.jpg" alt="images" align="right" width="500" height="300">

U-Net is a kind of Convolutional Neural Network (CNN) model designed for medical image segmentation1. U-Net has a symmetric structure that preserves the size of the input image and recovers lost features. 
The features of U-Net that distinguish it from CNN are as follows:

U-Net does not use padding to preserve information at the edges of the input image.
U-Net uses skip connections between the downsampling and upsampling layers. This allows low-level features to be combined with high-level features.
U-Net uses sigmoid activation function instead of softmax in the last layer to produce the segmentation map.
The working logic of U-Net is as follows:

The input image passes through four narrowing layers consisting of convolution, ReLU and max pooling. These layers create feature maps of the image.
The output of the contraction layers enters four expansion layers consisting of convolution, ReLU and transpose convolution. These layers approximate the segmentation map by upsampling the feature maps.
Each of the expansion layers establishes short links with the corresponding outputs of the collapse layers. In this way, lost features can be recovered.
The output of the last expansion layer enters the last convolution layer. This layer generates a class probability for each pixel using a sigmoid activation function

# Project Details 
-> Data set used in the project "https://www.kaggle.com/datasets/aryashah2k/brain-tumor-segmentation-brats-2019"

Dice coefficient was used in the project:
The Dice coefficient is a statistical method that measures how similar two clusters are. The reason for using it with U-Net is to evaluate how well the segmentation map matches the real map.

U-Net is a convolutional neural network model for medical image segmentation. U-Net makes the segmentation map more accurate and sharp by preserving the size of the input image. U-Net uses short connections between the collapse and expansion layers. In this way, it recovers lost features and achieves better learning performance.

The Dice coefficient is used to evaluate how well the segmentation map matches the true map. The Dice coefficient is calculated as the ratio of the intersection of two clusters to their union. The Dice coefficient takes a value between 0 and 1. 0 indicates that the two clusters are not similar at all; 1 indicates that they are completely similar.

