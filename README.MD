# Build an Weather Classifier using tensorflow and GPU environtments on watson studio


# Overview

we will use PyTorch to build and train a deep learning model to classify images to 11 classes (dew, frost, hail, rain, rime, snow, fogsmog, glaz, lightning, rainbow, sandstorm) which can be used in various sectors such as transportation, agriculture, fisheries etc. We will use a pre-trained VGG16 and we will define our classifier and connect it to network, then train this classifier along with some of the last blocks of the network on our dataset.

In this notebook we will:

1- Obtain dataset from Kaggle.  
2- explore data and preprocess images before training.  
3- define our classifier to have an output layer of 11 outputs.  
4- train the last blocks of the network along with the classifier we defined.  
5- test the model we trained.  

This notebook uses python 3.10 + GPU environment which allow us to do the whole process and train complex model in the same place which is a notebook in Watson studio.
Learn more about available environments <a href="https://dataplatform.cloud.ibm.com/docs/content/wsj/analyze-data/gpu-environments.html"> Watson Studio environments.</a>




# Flow

    

![Flow](https://raw.githubusercontent.com/IBM/ASL-Pytorch/master/images/diagram.png)

1. Log into IBM Watson Studio.
2. Get your Kaggle API credentials
3. Run the Jupyter Notebook in Watson Studio.

# Instructions


1. [Sign up for Watson Studio](#1-sign-up-for-watson-studio)
2. [Create a new project](#2-create-a-new-project)
3. [Create the notebook](#3-create-the-notebook)
4. [Run the notebook](#4-run-the-notebook)
5. [Test your model](#5-Test-the-model)

### 1. Sign up for Watson Studio

We will use Watson studio to run this notebook, Watson studio is available through IBM cloud or IBM Cloud Paks For Data.

* To start you must have IBM cloud account, Get your for free <a href="https://cloud.ibm.com/registration">Here.</a>   
* From the catalog create a <a href="https://cloud.ibm.com/catalog/services/watson-studio">watson studio</a> with standard plan or more and make sure the region is dallas to enable GPU environment.  
* Alternatively, you can use the ```ASL_PyTorch-CPU``` Notebook if you are a Watson Studio Lite Plan user

![CREATE WS](/res/create%20watson%20studio.gif)  

### 2. Create a new project


From the Watson Studio home page, select `Creat a project`, then select the `Create an empty project` and choose a name for your project then press create .

![Create Project](/res/create%20a%20project.gif)  

* create a watson studio project <a href="https://www.youtube.com/watch?v=-CUi8GezG1I">see tutorial here.</a>  

### 3. Create the notebook 

* create a new notebook from watson studio with GPU support.    
    * the notebook should have a GPU support <a href="https://www.youtube.com/watch?v=RNIWtpnNBoo">click here to learn how to create a notebook with GPU support.</a>
    * Use the From URL option and    
    use this URL for GPU supported notebook: https://github.com/IBM/ASL-Pytorch/blob/master/ASL-GPU.ipynb \
    or use this URL for CPU notebook(LITE) : https://github.com/IBM/ASL-Pytorch/blob/master/ASL-CPU.ipynb

![NOTEBOOK](/res/create%20the%20notebook.gif)

### 4. Run the notebook 

To view your notebooks, select `Notebooks` in the project `Assets` list. To run a notebook, simply click on the `edit` icon listed in the row associated with the notebook in the `Notebooks` list.

![notebook](/res/training%20model.png)

Follow notebook instructions to load data and train the model.  

Cells are how notebooks are structured and are the areas where you write your code. To run a piece of code, click on the cell to select it, then press `SHIFT+ENTER` or press the play button in the toolbar above. Additionally, the Cell dropdown menu has several options to run cells, including running one cell at a time or to run all cells at once.

### 4. Test the model

The last two cells in the notebook is where we test our trained model.
run the last model many times to check different samples.

![Result](/res/confussion%20matrix.png)

![rain](/res/pred_rain.png)
![snow](/res/pred_snow.png)
![sandstorm](/res/pred_sandstorm.png)
![fogsmoke](/res/pred_fogsmog.png)
![lightning](/res/pred_lightning.png)
![glaze](/res/pred_glaze.png)
![rime](/res/pred_rime.png)
![frost](/res/pred_frost.png)

### check notebook result 

[Notebook with outputs](weather_classification.ipynb)  

# links

* learn more about [Tensorflow](https://www.tensorflow.org/)  
* [Create Watson Studio Notebooks](https://dataplatform.cloud.ibm.com/docs/content/wsj/analyze-data/creating-notebooks.html)
* [Learn more about GPU environments](https://dataplatform.cloud.ibm.com/docs/content/wsj/analyze-data/gpu-environments.html)

# Learn more

* [Introduction to TensorFlow ](https://developer.ibm.com/articles/transfer-learning-for-deep-learning): In this article, you can find an overview of the Tensorflow .

* [Build models using Jupyter Notebooks in IBM Watson Studio](https://developer.ibm.com/technologies/artificial-intelligence/tutorials/watson-studio-using-jupyter-notebook/)
  
* [Multiclass image classification of yoga postures using Watson Studio and Deep Learning as a Service](https://developer.ibm.com/tutorials/image-preprocessing-for-computer-vision-usecases/)
 


