# Project Transfer Learning

## Introduction

This project applies Transfer learning to solve a fine-grain classification task. The aim with this project was to apply transfer learning and to comparatively study some of the pretrained models available in PyTorch. The dataset used for this project involves images of ten different monkey species.The pretrained models were either ResNet or VGG derived and varied in the number of layers in the pretrained model. Models R1-R5 were derived from ResNet-18,34,50,101,152.Models V1-V3 were derived from VGG-13,16,19 and Models V4-V6 from VGG-13,16,19 with Batch Normalization. 

## Getting Started
The data for this project can be obtained from Kaggle at the below link. The project code was run using Google Colab and therefore, Google Colab was used to upload the dataset.

* Data Source: https://www.kaggle.com/slothkong/10-monkey-species

##### A note about the dataset

* The data contained a prime number, 1097, of images, resulting in in uneven batch sizes. To even the batch size, a random index was chosen and one image was excluded from the training data. This resulting in a total of 1096 images with an even batch size of 137. This removal of one image was decided because the classes are relatively equally represented and have similar numbers of images.

### For Google Colab: 

1. Remove a random image from the training dataset and save the training data as a zip, containing a labeled folder for each class's  images. Save the validation file in a similar format. The formatting is important because PyTorch's ImageFolder, which is used to import the data, requires a specific structure. For more information, see the PyTorch documentation [here](https://pytorch.org/docs/stable/torchvision/datasets.html#imagefolder).
2. When connected to a runtime in Google Colab, confirm that the runtime type is set to GPU by going to Runtime--> Change Runtime Type -->    Hardware Accelerator --> GPU. Then, run code cell 1-3.
3. In code cell 4, alter the name of the uploaded training data zip file to match the zip file uploaded. Then, run code cell 4.
4. In code cell 6, alter the name of the uploaded validation data zip file to match the zip file uploaded. Then, run code cell 5.
5. From here, you can run the remaining cells as normal.

### For AWS or locally running this code:

1. Remove a random image from the training dataset and save the training data as a zip, containing a labeled folder for each class's  images. Save the validation file in a similar format. The formatting is important because PyTorch's ImageFolder, which is used to import the data, requires a specific structure. For more information, see the PyTorch documentation [here](https://pytorch.org/docs/stable/torchvision/datasets.html#imagefolder).
2. Upload the training and validation data using Github or an alternative method. Code cells 3-6 are designed to work with Google Colab and may be ignored when running in a different environment. Once the datasets have been uploaded or can be accessed by this notebook, the code cells in "Building the Dataset" should successfully create the training, test, and validation dataloaders.
3. From this point, the remaining cells can be run as normal. 

