# Image-Colorization
Colorizing Grayscale Images using Hybrid AutoEncoder and CNN Architecture

# Problem Statement:
Automatic Colorization of gray scale landscape images using a hybrid CNN and autoencoder method

# What is Image Colorization:
Image colorization is the process of adding color to a grayscale image or a black and white image. It involves mapping the intensity values of the grayscale image to a color space, such as RGB, and then filling in the missing color channels to produce a full-color image. 

# Literature Survey:
R. Zhang, P. Isola, and A. A. Efros, "Colorful Image Colorization," in European Conference on Computer Vision (ECCV), 2016, pp. 649-666. 						
Proposed a deep learning-based approach for automatic colorization of grayscale images. 
The proposed model consists of two parts: 
  * Fully convolutional network (FCN) FCN takes the grayscale image as input and outputs a two-dimensional chrominance map, which encodes the color information of the image 
    Global color distribution (GCD) network that maps the predicted chrominance values to a plausible color distribution which is used to colorize the grayscale image.

Nihalaani, Rachaell, Simran Mansharamani, and Juhi Janjua. "Image Colorization Using Autoencoders." International Journal of Computer Applications 176, no. 16 (2021): 7-12.
Proposed a method for colorizing landscape grayscale images has been presented using Convolutional AutoEncoders.
  * Grayscale image passed through encoder network, which learns to encode the underlying features of the grayscale image into a compressed representation. 
    Compressed representation then fed into a decoder network, which learns to reconstruct the original grayscale image from the compressed representation. 
    Decoder network is modified to predict the chrominance values of each pixel in the image instead of just the grayscale values.

# DATASET DESCRIPTION
* Color : RGB
* Type : Landscape images
* Image Size: 224*224
* Divided into 3 sub directories:
  * Training : 3200
  * Testing : 1000
  * Validation: 800
* FEATURES
  * Coast
  * Desert 
  * Forest 
  * Glacier 
  * Mountains
* DATASET LINK : 
  * https://www.kaggle.com/datasets/utkarshsaxenadn/landscape-recognition-image-dataset-12k-images

# DATA PREPROCESSING
* Resizing the images
* Normalizing pixel values : Divide by 255.0
* Converting the images to array
* Converting the image array to LAB format
  * Separates color information (ab) from lightness information (L), allows for more accurate color representation.
  * More robust to lighting changes, useful when colorizing images taken under different lighting conditions.
  * Grayscale image as input, complexity of color channels reduced from 3 to 2 (comparison to RGB)
    
# MODEL
* Input: L channel of the image which is grayscale (denoted by X)
* Output: A and B channels of the image which represents color  (denoted by Y)
* Train Test Split: 80:20
* Loss Function: Mean Squared Error
* Optimizer: Adam
* Metrics: Accuracy





  








