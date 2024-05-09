# Dog breed classifier project
## Background

This repository contains a Jupyter notebook with starting code provided by Udacity as a way to teach Convolutional Neural Networks

I have also created a blog post to summarise my own learning as I undertook this course:
https://medium.com/@paul.c.shepherd/how-can-a-machine-understand-what-its-looking-at-find-out-below-14130790d042

## Rubric measures

### Project definition

#### Project Overview:
The project is focused on developing a Dog Identification App as part of a Udacity Nanodegree project. The app aims to classify images of dogs according to their breeds. It is designed to work with both user-supplied images and a provided dataset of dog images and human images. The goal is to create an algorithm that can accurately identify the breed of a dog or find the closest dog breed resemblance for a detected human.

#### Problem Statement:
The main problem that needs to be solved is to develop an algorithm that can accurately classify images of dogs based on their breeds or which breed of dog the image most resembles. The algorithm should be able to detect whether a dog or a human is present in an input image and provide an estimate of the dog breed (if dog) or the closest dog breed resemblance (if human).

To solve this problem, a series of models need to be developed for different tasks, including detecting humans in an image, detecting dogs in an image and inferring the dog breed. The challenge lies in piecing together these models and ensuring they work seamlessly to achieve good results.

#### Metrics:
The performance of the models will be measured using a simple accuracy metric, specifically for the dog or (human) face detections. The accuracy score will be calculated by supplying 100 images of either dogs or humans to the models and tallying the correct identifications made by each model.

The choice of accuracy as the metric is justified based on the problem characteristics. Since the goal is to correctly classify the dog images into their respective breeds, accuracy provides a straightforward measure of how well the model performs. Higher accuracy values indicate a more successful model in accurately identifying dogs or faces.

### Analysis

#### Data exploration
The dataset provided for the Dog Identification App project consists of dog images and human images.

1. Dog Images:
   - Total dog categories: 133
   - Total dog images: 8351
   - Training dog images: 6680
   - Validation dog images: 835
   - Test dog images: 836

2. Human Images:
   - Total human images: 13233

The dog image dataset is partitioned into three sets: training, validation, and test sets. The training set consists of 6680 dog images, which will be used to train the model. The validation set has 835 dog images, which will be used to evaluate the model's performance during training. The test set contains 836 dog images, which will be used to assess the final model's generalisation ability.

In addition to the dog images, there are 13233 human images included in the dataset. These images will be used to assess the accuracy of the face detector models

### Conclusion

#### Reflection
Throughout this Udacity project, the end-to-end problem solution was achieved by utilising pretrained models such as OpenCV for human face detection, ResNet-50 for dog detection, and VGG-19 for dog breed detection. The algorithm successfully tested the submitted image for dog or face detection using OpenCV and ResNet-50, and then utilised VGG-19 to detect the dog breed or the closest resemblance if a human face was detected.

One particular aspect of the project that I found interesting was the use of Convolutional Neural Networks (CNNs). As someone new to this field, CNNs initially appeared complex with multiple layers of processing and unfamiliar terminology. However, diving into the project allowed me to gain a deeper understanding of how CNNs work and their application in image classification tasks. The opportunity to explore and comprehend CNNs was a rewarding experience during this project.

#### Improvements
One aspect that could be improved in the implementation is handling images of mongrel dogs or dogs without a recognisable breed. During testing, the current solution was shown to misclassify such dogs by assigning them a breed that is not accurate. To address this, one potential solution would be to incorporate a mechanism to detect when a dog image does not belong to any of the recognised breeds. This could involve adding an additional classification category for "Unknown Breed" or adding a separate model dedicated to identifying mixed breed dogs.

Other improvements might involve using transfer learning on a larger and more comprehensive dataset to improve the classification capabilities of the pre-trained models

Given my newfound understanding of CNNs I was inspired to create a blog post detailing what I had discovered about the inner workings of the CNN pipeline with some visualisations of the functionality. Link is at the top of this readme.

## Libraries used

[NumPy](https://numpy.org/) for data analysis

[Matplotlib](https://matplotlib.org/) for plotting data

[PIL](https://pillow.readthedocs.io/) for image processing

[keras](https://keras.io/) for Neural networks

[OpenCV](https://opencv.org/) for face detection

[ResNet-50](https://keras.io/api/applications/resnet/) for dog detection

[VGG-16 and VGG-19](https://keras.io/api/applications/vgg/) for dog breed predictions

## Project motivation

I have created this project as part of a [nanodegree](https://www.udacity.com/blog/2016/07/nanodegree-101.html) course from [Udacity](https://www.udacity.com/)

I was motivated to take the course as I find data science a fascinating subject and I'm very keen to increase my own knowledge on the subject, both for professional and personal reasons

## File descriptions

- README.md: This file
- dog_app.ipynb: A jupyter notebook with starting code provided by Udacity to develop and run the dog breed application
- extract_bottleneck_features.py: A script for extracting the bottleneck features from the pre-trained models

## Using this project

You first must have all of the libraries mentioned above installed on your machine as well as software that supports the use of Jupyter notebooks
Run all of the cells in order to activate all of the functions required to use the app
The cells that run the app are located in the final Step 7: Test Your Algorithm

To run the app, you need an image of exactly 250x250 pixels.
Either modify the existing cells or add a new cell invoking the dogface_detector function and passing the path to the image
The app will decide if it finds a dog or a face in the image, if it find neither, it will exit with an error
If it finds a dog, it will guess the dog's breed
If it finds a face, it will tell you what dog the face most looks like!

## Acknowledgements

This project is subject to the GNU license GPL v3 https://www.gnu.org/licenses/gpl-3.0.en.html
Author: Paul Shepherd

Acknowledgements: Thanks to Udacity and the Data Science course which has taught me all of the techniques used in creating this app
