# What İs The U-Net 

<img src="https://www.frontiersin.org/files/Articles/482352/fonc-09-00964-HTML/image_m/fonc-09-00964-g002.jpg" alt="images" align="right" width="500" height="300">

U-Net is a kind of Convolutional Neural Network (CNN) model designed for medical image segmentation. U-Net has a symmetric structure that preserves the size of the input image and recovers lost features. 
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
-> Data set used in the project "https://www.med.upenn.edu/cbica/brats2020/#:~:text=BraTS%202020%20utilizes%20multi%2Dinstitutional,)%20brain%20tumors%2C%20namely%20gliomas."

Dice coefficient was used in the project:
The Dice coefficient is a statistical method that measures how similar two clusters are. The reason for using it with U-Net is to evaluate how well the segmentation map matches the real map.

<img src="https://miro.medium.com/v2/resize:fit:1400/1*tSqwQ9tvLmeO9raDqg3i-w.png" alt="images" align="right" width="500" height="300">
-> U-Net is a convolutional neural network model for medical image segmentation. U-Net makes the segmentation map more accurate and sharp by preserving the size of the input image. U-Net uses short connections between the collapse and expansion layers. In this way, it recovers lost features and achieves better learning performance.

The Dice coefficient is used to evaluate how well the segmentation map matches the true map. The Dice coefficient is calculated as the ratio of the intersection of two clusters to their union. The Dice coefficient takes a value between 0 and 1. 0 indicates that the two clusters are not similar at all; 1 indicates that they are completely similar.
<br>
<br>

-> Within the project's scope, i trained the same dataset with 2 different U-Net methods only once. To ensure a healthy model, at least 50-100 trainings are recommended.  However, I wish to demonstrate the model's success with just one training.I trained one model on GoogleColab with GPU and the other on Kaggle. GoogleColab's training used only 20 data, yet the prediction results were impressive. The Kaggle-trained model attained 97% success by using a CPU during a single training session. A more understandable and significant dataset will result in higher success rates. The success rate of our models is linked to the data's pre-processing phase.  We divide the data into Flair, t2, and segmentation layers to achieve this.  It's possible that your computer's RAM capacity will be insufficient to run these models. In this instance, you may experience a memory fault. To resolve this issue, it is advised that you reduce the size of the data set you provide to the model by half.

The figure below shows a comparison of the computer prediction and the real-life prediction of the GoogleColab model trained with only 20 data.  


![result](https://github.com/KocHanim/Brain-Tumour-Segmentation-with-Artificial-Intelligence-Model-U-Net-/assets/115664157/3b7c7505-69dd-41d0-a27e-9180d953da8d)

*Can you hear it? The noise of the future!*

# Author:
Rumeysa KOÇ

# References:
https://lmb.informatik.uni-freiburg.de/people/ronneber/u-net/


https://www.geeksforgeeks.org/u-net-architecture-explained/


Todeschini R, Ballabio D, Consonni V, Mauri A, Pavan M: CAIMAN (Classification And Influence Matrix Analysis): A new approach to the classification based on leverage-scaled functions. Chemometrics Intell Lab Syst 2007, 87:3-17.


https://radiopaedia.org/articles/dice-similarity-coefficient





