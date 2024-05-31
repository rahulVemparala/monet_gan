
# ISM 6930: Tech Foundation of AI (Fall 2023) - Final Project
This repository contains the code and write-up for our final project in ISM 6930: Tech Foundation of AI. The project focuses on applying a Cyclic Generative Adversarial Network (CycleGAN) for image-to-image generation and style transfer.

## Project Goal
Our objective was to develop a model that could transform modern photos into paintings resembling the artistic style of Oscar-Claude Monet.

## Dataset
The project utilizes a dataset consisting of two categories:

Monet Paintings: A collection of original Monet paintings.
Photos: A collection of high-quality scenic photographs.
The images are pre-processed to a uniform size of 256x256 pixels.

## Methodology
Data Preprocessing:

### Resizing images to 256x256 pixels
Normalizing pixel values to a range of -1 to 1
Storing data in TFRecord format for efficient processing
Model Architecture:

### Generator: 
- U-Net with skip connections for preserving spatial details.
### Discriminator: 
- Convolutional neural network for image classification.

## CycleGAN Implementation:
Two generators and two discriminators enable style transfer in two directions:
- Photo to Monet (desired direction)
- Monet to Photo (not used in this project)

## Training Process:
Training on the entire Monet and Photo dataset.

## Key training parameters:
- Epochs: 25
- Learning rate: 2e-4
- Batch size: 1
- Loss Functions:

**Cyclic Consistency Loss**: Measures the difference between the original photo and the reconstructed photo from the generated Monet style image.
**Adversarial Loss**: Evaluates the generator's ability to deceive the discriminator.
**Generator Loss**: Combines cyclic consistency loss and adversarial loss.
**Discriminator Loss**: Assesses the discriminator's performance in classifying real and generated images.

## Results
The trained model successfully generated 7,308 images replicating the style of Monet paintings.

## Submission
(Kaggle Submission Link)[https://www.kaggle.com/competitions/gan-getting-started/submissions#]
