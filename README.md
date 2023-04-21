# Classifying MRI images with or without Alzheimer's Disease

The dataset is from https://www.kaggle.com/datasets/tourist55/alzheimers-dataset-4-class-of-images. It contains a training and testing folder. For my project, I refactored the images into the following organization:

- AlzheimersDataset/Positive with all 3200 positive images named pos(i)
- AlzheimersDataset/Negative with all 3200 negative images named neg(i)

This way I can do binary classification and create my own randomized training and testing sets. Find the reorganized dataset here: https://www.dropbox.com/s/9nffhc867a7zjxz/AlzheimersDataset.zip?dl=0

# To run:

## Most files:

Download the dataset using the dropbox link above. Open the notebook files in JupyterLab and run.

## PCA folder:

First, run myPCA.ipynb to see how the principal components are generated and saved. Then run SparkML.ipynb to train the SparkML models.

## VertexAI folder:

1. Create a bucket in GCP named az-bucket-1.
2. Upload the Negative and Positive folders from the dataset.
3. Upload the csv file containing the image paths and labels.
4. Create a managed dataset in VertexAI using this csv file.
5. Train an AutoML model using the managed dataset.

## PowerPoint folder:

Contains the presentation pptx file.
