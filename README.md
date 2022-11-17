# Bone-Fracture-Detection
MI - CS302 - Project     

PPT Link -  
https://www.canva.com/design/DAFRenrX65w/eVo84ZqYj8EoHXUXqS97ig/view?utm_content=DAFRenrX65w&utm_campaign=designshare&utm_medium=link&utm_source=publishsharelink

Dataset -   
  https://www.kaggle.com/datasets/andradaolteanu/rsna-fracture-detection  
  https://www.kaggle.com/competitions/rsna-2022-cervical-spine-fracture-detection/

## Abstract and Scope
The skeletal system of the human body comprising of over 200 bones is a very essential component. Bones allow for movement, provide protection and structure to the human body. Bone fractures occur due to trauma, overuse or other diseases. Bone fractures are painful to endure and patients suffering from such a condition benefit from quick and accurate diagnosis which will enable them to access the right treatment. Doctors use X-Ray images to identify the fractured bone. The manual detection is often time-consuming and there is also a high chance of error. Hence, this project aims to automate the process and help doctors identify fractures quicker which will enable patients to get the right treatment faster.

## Feasibility Study
Doctors rely on X-ray images to identify fractures. Manual inspection of multiple X-rays can be time-consuming and often a tedious process. Radiologists may sometimes overlook or fail to notice certain details due to high pressure and workloads. This project aims to assist doctors and radiologists, to prevent this from happening and provide the right diagnosis as soon as possible. 
  
  
## Dataset Description  
The dataset is split into multiple folders with different data. The first folder - zip_png_images contains different folders, each containing the CT scan images of a unique study instance pertaining to a particular patient scan. The images are in png format.  
Train.csv contains informatation on each study instance. It consists of multiple rows including study instance id, patient overall, total fractures and c1 through c7.  
    - Patient overall indicates if there is a broken bone or not.  1 for fracture and 0 for no fracture  
    - Total fractures indicates number of broken vertebrae  
    - c[1-7] tells if a given vertebrae for given study instance id is fractured or not    
    
![image](https://user-images.githubusercontent.com/66276711/202347553-2592b04c-3f44-41d1-bbf3-9e52dec4063c.png)
  
   
## What is CNN? Why is CNN used for image classification?  
Convolutional Neural Network is a type of Neural Network commonly used for applications in computer vision (image processing) and speech recognition or NLP models. The convolutional layer reduces the high dimensionality of images without losing important features or information and hence, is suited for image processing models.  A CNN uses adjacent pixels to down-sample the image into features by convolution and then uses prediction layers to predict the target values. Multiple convolution filters or kernels are run over the image. Each filter extracts different features from the image.   

  
CNNs also require minimal pre-processing as compared to other algorithms as they have the ability to learn or recognize the important characteristics (filters).  
  
CNN architecture is similar to the connectivity patters of neurons in the human brain. It was inspired by the visual cortex. It is made up of neurons who have learnable weights and biases. Each neuron receives numerous number of inputs and then it takes a weighted sum over them, where it passes it through an activation function and responds back with an output.
    
    
## Model 
### Conv2D
Conv2d is a used to create a 2D convolutional layer. A convolutional layers extracts features from the input image by applying filters. Multiple convolutional layers filters of kernels are applied to train the model.  
The model in this project consists of 3 CNN layers with 16, 8, 4 feature maps and 3x3 kernels

### Max Pooling
Max Pooling is used to basically summarize the features of a filter. Max Pooling is pooling operation that selects the max element from region of feature map covered by filter.  The output produced would consist of the most prominent features of the previous feature map. Max Pooling reduces the dimension of the filtered image at each convolutional layer.

## Batch Normalization
Batch Norm is just another network layer that gets inserted between a hidden layer and the next hidden layer. Its job is to take the outputs from the first hidden layer and normalize them before passing them on as the input of the next hidden layer.  

### Flatten
This layer reduced the 2- dimensional feature vector into an array that is feed to a fully connected layer.

## Dense  
The dense layer is a neural network layer that is connected deeply, which means each neuron in the dense layer receives input from all neurons of its previous layer.

### Dropout
Dropout is a regularization technique used to reduce over-fitting on neural networks. Usually, deep learning models use dropout on the fully connected layers, but is also possible to use dropout after the max-pooling layers, creating image noise augmentation

## Model Architecture
![image](https://user-images.githubusercontent.com/66276711/202347277-7dabfb91-5ce8-4ae0-a906-1ba9583cf735.png)


### Loss Function - Categorical Crossentropy
A loss function is a method of evaluating how well the model models the dataset. Lower the loss, better the model.  The loss function used in this model is categorical crossentropy.
Categorical crossentropy is the best suited loss function for multi-class classifications  
  
  
## Accuracy and Loss Metrics  
Accuracy - 85.38  
AUC Score - 0.76
