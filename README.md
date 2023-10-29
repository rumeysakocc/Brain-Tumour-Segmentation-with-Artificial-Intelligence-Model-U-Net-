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

### Precise Image Segmentation:
U-Net is a model that can provide precise segmentation on a pixel basis. It has the ability to recognise the subtle structures of images and segment them in detail. It is used to precisely classify organs, tissues or lesions, especially in areas such as medical imaging.

### Efficient Data Usage:
U-Net, which is efficient in terms of data usage, can produce effective results even with limited data. This feature is especially useful when training models for rare diseases or specific conditions in medical fields.

### Application Diversity:
The U-Net model is suitable for medical imaging, cellular imaging, microscopic imaging and many other fields. Thanks to its customisable architecture, it can work with images of different sizes and perform segmentation tasks.

### Deep Learning and Image Processing Integration:
U-Net combines deep learning and image processing techniques. It performs feature extraction to better understand and classify the features of images.

### Good Generalisation Capability:
U-Net generally performs well on new data that is different from the training data set. This generalisation ability is very important when used in real world applications.
![Seg](https://github.com/KocHanim/Brain-Tumour-Segmentation-with-Artificial-Intelligence-Model-U-Net-/assets/115664157/ec3864f8-2dac-47b2-8dd5-6bf59e338f72)


# Project Details 
-> Data set used in the project "https://www.kaggle.com/datasets/aryashah2k/brain-tumor-segmentation-brats-2019"

Dice coefficient was used in the project:
The Dice coefficient is a statistical method that measures how similar two clusters are. The reason for using it with U-Net is to evaluate how well the segmentation map matches the real map.

<img src="https://miro.medium.com/v2/resize:fit:1400/1*tSqwQ9tvLmeO9raDqg3i-w.png" alt="images" align="right" width="500" height="300">
-> U-Net is a convolutional neural network model for medical image segmentation. U-Net makes the segmentation map more accurate and sharp by preserving the size of the input image. U-Net uses short connections between the collapse and expansion layers. In this way, it recovers lost features and achieves better learning performance.

The Dice coefficient is used to evaluate how well the segmentation map matches the true map. The Dice coefficient is calculated as the ratio of the intersection of two clusters to their union. The Dice coefficient takes a value between 0 and 1. 0 indicates that the two clusters are not similar at all; 1 indicates that they are completely similar.
<br>
<br>

-> Within the project, the same data set was trained only once with 2 different U-Net methods. For a healthy model, at least 50-100 trainings should be performed. What I want to show here is how successful the model is with only 1 training. One of the models was trained on GoogleColab while the other was trained on Kaggle. GoogleColab training was performed with only 35 data. But despite this, the prediction results were remarkable. The model trained via Kaggle used CPU and achieved 97% success in a single training. The success of the models is directly related to the preprocessing stage of the data. The more meaningful and legible our data set is for the model, the more success we will get. 


![result](https://github.com/KocHanim/Brain-Tumour-Segmentation-with-Artificial-Intelligence-Model-U-Net-/assets/115664157/3b7c7505-69dd-41d0-a27e-9180d953da8d)
