# Face-Generation
This project uses generative adversarial networks (GANs) to generate new images of faces.

## Project Source

This repository contains project#4 related to Udacity's [Deep Learning Nanodegree program](https://github.com/udacity/deep-learning-v2-pytorch/blob/master/project-face-generation).

## Get the Data

The dataset was aquired from [CelebFaces Attributes Dataset](http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html) to train our adversarial networks.
This dataset is more complex than the number datasets (like MNIST or SVHN) and so, you should prepare to define deeper networks and train them for a longer time to get good results. It is suggested that you utilize a GPU for training.

## Pre-processed Data
Since the project's main focus is on building the GANs, we've done some of the pre-processing for you. Each of the CelebA images has been cropped to remove parts of the image that don't include a face, then resized down to 64x64x3 NumPy images. Some sample data is show below.
![processed face data](https://github.com/Nourah-AlMutlaq/Face-Generation/blob/main/processed_face_data.png?raw=true)

## Generator Samples from training
Samples of images from the generator trained models.
![Output](https://github.com/Nourah-AlMutlaq/Face-Generation/blob/main/output.png?raw=true)

## Strengths and Weaknesses of my trained models.
- Most of the generated images are white and celebrity faces as expected due to the dataset's bias.
- The samples don't look so perfect, however, some of the generated images look so pretty. This could return to the number of epochs. Moreover, the size of the model is reasonable and deep enough for the size of the input images. The optimizer with tuned hyperparameters is selected based on the DCGAN paper.
- For improving the model, the label smoothing strategy could help the model to generalize better and avoid making extreme predictions. Also, adding dropout layers may help to enhance the training process.
- According to the training loss graph, setting 20 epochs could enough to get a good result, as the generator loss increases after epoch = 20 (approximately).
