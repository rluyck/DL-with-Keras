# Deep Learning with Keras

- This repository contains the data and my notebooks produced during the Keras with TensorFlow Course (freecodecamp.org)

## Course and notebooks overview

1. [Introduction to Keras sequential model](https://github.com/rluyck/DL_with_Keras/blob/main/Keras_DL_Intro.ipynb)
  - data preparation
    - shuffle
    - minmaxscaler
  - building, compiling and training (fitting) the model
  - predicting (inference)
  - confusion matrix
  - saving and loading the model
    - model.save() -> save everything (architecture, weights, training config, optimizer,...)
    - model.to_json() -> only save architecture
    - model.save_weights() -> only save weights..

2. [Creating a train/validation/test set of cat and dog images](https://github.com/rluyck/DL_with_Keras/blob/main/Train_Val_Test_CatDog.ipynb)

3. [Building a CNN for distinguishing cat and dog images](https://github.com/rluyck/DL_with_Keras/blob/main/CNN_CatDog.ipynb)
  - we'll be using the vgg16 model: a convolutional neural network that is 16 layers deep. You can load a pretrained version of the network trained on more than a million images from the ImageNet database. The pretrained network can classify images into 1000 object categories, such as keyboard, mouse, pencil, and many animals.
  - image preparation: preprocess the images in the same way the images were fed to the vgg16 model when it was being trained. We'll be using the Keras ImageDataGenerator for this, it generates batches of tensor image data with real-time data augmentation.
  - model 1
    - building, compiling and training (fitting) the model
    - predicting (inference)
    - confusion matrix
    - result: the model overfits.. training accuracy: 0.9980, while val_accuracy: 0.6100
  - model 2
    - fine tune the last layer of the vgg16 model
    - building, compiling and training (fitting) the model
    - predicting (inference)
    - confusion matrix
    - result: much better, accuracy: 0.9920 - val_accuracy: 0.9700 
4. [Introduction to MobileNet](https://github.com/rluyck/DL_with_Keras/blob/main/MobileNet_Images.ipynb) 
  - we'll be using MobileNet, a model developed by Google. It is trained on the ImageNet dataset, a large dataset of 1.4M images and 1000 classes.    
    - lightweight deep CNN
    - low power, latency 
    - smaller size, hence usefull for "mobile" devices
    - VGG16 = 553 MB (138,000,000 parameters)
    - MobileNet = 17 MB (4,200,000 parameters)
    
5. [Fine-tuned MobileNet](https://github.com/rluyck/DL_with_Keras/blob/main/MobileNet_SignLanguage.ipynb) 
  - Dataset: sign language digits dataset 
  - create train/val/test set
  - data preparation
  - modify the functional model
  - compiling and training (fitting) the model
  - predicting (inference)
  - confusion matrix
  
 6. [Data Augmentation](https://github.com/rluyck/DL_with_Keras/blob/main/Data_Augmentation.ipynb) 
   - data augmentation means modifying excisting images (flipping H/V, rotating, zooming in/out, changing color, cropping etc...) to simply have more data to train on and hopefully reducing overfitting in case you have few data
