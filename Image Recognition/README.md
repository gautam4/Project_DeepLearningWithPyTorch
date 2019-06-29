# Project Image Recognition

# Introduction 
  
  This project implements and optimizes a CNN to perform a fine-grain classification task. The dataset used for this project involves images of ten different monkey species. The CNN architecture was structurally chosen after multiple trials of different architectures. Once the architecture was chosen, the learning rate was experimented with to optimize network performance. The learning rates were initially decreased by a factor of 10 starting with a learning rate of 0.01 for Trials 1-4. Based on the network performance from these trials, the learning rate was fine-tuned further in Trials 5-7. To achieve an optimal model with this architecture, a model was defined based on the results from Trials 5-7. 
  
# Getting Started 

  The data for this project can be obtained from Kaggle at the below link. The project code was run using Google Colab and therefore, Google Colab was used to upload the dataset.
  * Data Source: https://www.kaggle.com/slothkong/10-monkey-species

##### A note about the dataset
* The data contained a prime number, 1097, of images, resulting in in uneven batch sizes. To even the batch size, a random index was chosen and one image was excluded from the training data. This resulting in a total of 1096 images with an even batch size of 137. This removal of one image was decided because the classes are relatively equally represented and have similar numbers of images. 
    
## For Google Colab:
1. Remove a random image from the training dataset and save the training data as a zip, containing a labeled folder for each class's images. Save the validation file in a similar format. The formatting is important  because PyTorch's ImageFolder, which is used to import the data, requires a specific structure. For more information, see the PyTorch documentation [here](https://pytorch.org/docs/stable/torchvision/datasets.html#imagefolder). 
2. When connected to a runtime in Google Colab, confirm that the runtime type is set to GPU by going to Runtime--> Change Runtime Type --> Hardware Accelerator --> GPU. Then, run code cell 1-3.
3. In code cell 4, alter the name of the uploaded training data zip file to match the zip file uploaded. Then, run code cell 4.
4. In code cell 6, alter the name of the uploaded validation data zip file to match the zip file uploaded. Then, run code cell 5. 
6. From here, you can run the remaining cells as normal. The cells following each model's training use Google Colab's files library to download the model weights.

## For AWS or locally running this code:
1. Remove a random image from the training dataset and structure the dataset to contain a labeled folder for each class's images. Save the validation file in a similar format. The formatting is important  because PyTorch's ImageFolder, which is used to import the data, requires a specific structure. For more information, see the PyTorch documentation [here](https://pytorch.org/docs/stable/torchvision/datasets.html#imagefolder). 
2. Upload the training and validation data using Github or an alternative method. Code cells 3-6 are designed to work with Google Colab and may be ignored when running in a different environment. Once the datasets have been uploaded or can be accessed by this notebook, the code cells in "Building the Dataset" should successfully create the training, test, and validation dataloaders.
3. From this point, the remaining cells can be run as normal. The cells following each model's training use Google Colab's files library to download the model weights. To download the model weights, additional code dependent on the environment must be added.

# Instructions

## To observe Trials 1-4 and Trials 5-7:
   * Trials 1-4 are written in Project_ImageRecognition_LRs1-4.ipynb
   * Trials 5-7 are written in Project_ImageRecognition_LRs5-7.ipynb
   
   * Run the cells in sequence depending on your environment(See Getting Started)
   * Each Trial is structured as follows: Model Definition, Optimizer Definition, Model Training, Model Testing
   * After all the models are trained, the Training and Validation losses are plotted against each other 
   * For Project_ImageRecognition_LRs5-7.ipynb, an optimal model is defined, trained, and tested after comparing Trials 5-7
## To observe Trained models
* Load the network weights included in this repository and observe the Trial's comparative performance.

# Project Results/Discussion
* The result from this project, including a detailed discussion of the CNN's architecture, the approach taken, and final conclusions regarding an optimal model, are included in the Report_ImageRecognition.pdf
