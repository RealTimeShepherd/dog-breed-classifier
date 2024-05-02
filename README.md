# Dog breed classifier project
## Background

This repository contains a Jupyter notebook with starting code provided by Udacity as a way to teach Convolutional Neural Networks

I have also created a blog post to summarise my own learning as I undetook this course:
https://medium.com/@paul.c.shepherd/how-can-a-machine-understand-what-its-looking-at-find-out-below-14130790d042

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
