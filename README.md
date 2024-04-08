# Computer Vision Project

This Project was conducted in the context of a project submission for the lecture Computer Vision in the 2nd Semester -
SS2024 in the Master's AI Engineering.

## Project Description
The main objective of this project was to experiment around with a Classifier for the classification of the three classes
1. Balloon
2. Bicycle
3. Golf Cart

The Images for this Project have been downloaded from the following source (which is also referenced in the code, more to
the download of the images and more can be found in the Set Up Section below): https://storage.googleapis.com/openimages/web/download_v7.html

The Classifier was not build from scratch, as one of the objectives was to play with transfer-learning, in  our case the ResNet50
has been given to us as the Base Net.

The ResNet50 is a convolutional neural network architecture that consists of 50 layers developed by Microsoft Research. It's a variant of the ResNet (Residual Network) model, known for its deep structure,
which addresses the vanishing gradient problem in deep learning by introducing skip connections or shortcuts that allow
gradients to flow more directly during training. 

These were the tasks we were experimenting around with and which will be used later for the sake of interpretation of our results:
1. Experimenting with transfer learning: Using a imagenet pretrained ResNet50 architecture, training the model and estimation of the testset accuracy 
2. Experimenting with data augmentation: Add data augmentation (Random flip, Random rotate, Random translation) and train again, discuss results 
3. Experimenting with different architectures
4. Testing a few of our images from the internet and showing the activation maps 
5. Discussing several questions (accuracy, infrastructure, inference time, number of parameters, performance of categories, confusion matrix, challenges & learnings)

The Execution of these tasks/the code to these can be found in the Jupyter Notebook in this
Repository/Folder titled " _ComputerVision.ipynb_ ".

## Project Set Up

Before the Project Set Up will be explained, the project architecture or technical system background is elaborated.
This technical system background does not have to be recreated for the project to be run-able. The only difference the technical
set up makes for you, is the fact that the project might be running smoother depending on your infrastructure, or the other way
around.

### Infrastructure
The models were trained using Google Colab on the CPU. The A100 GPU has been tested for this project as well, but since no significant
difference in runtime has been noted the project was kept on the CPU. 

The data used for training and testing and the trained models are saved at the following Google Drive folder: 
https://drive.google.com/drive/folders/1gxBX50hlUKxGlkX4fy4ztCJlBqsuyWJx?usp=drive_link

- This folder also has stored all other to the project relevant files and folders and has the folder structure as intended in the project which means no
changes have to be made.
- Extras which do not have to be done when running the jupyter-notebook through the one drive folder and google colab will be mentioned in the Colab Set Up Section.

### Overall Requirements

When talking about overall requirements which do not change we are referencing the libraries which need to be installed.
The libraries always need to be installed in your environment. Please run the following code in the environment you are
running the code (through your package manager) in or directly in the notebook.

````python
# Install the required libraries from the requirements.txt file
!pip install -r requirements.txt
````
The requirements.txt file should be located on the same level as the notebook in no other extra sub-folder as per our set up. If this has been 
cahnged then please adapt the command accordingly.

### Colab and OneDrive SetUp

If you want to follow and work with our one-drive set up then please follow this project setup here.
**Requirements:**
1. Installed Libraries as explained in prior section
2. Access to the One Drive Folder (found here: https://drive.google.com/drive/folders/1gxBX50hlUKxGlkX4fy4ztCJlBqsuyWJx?usp=drive_link
)
3. Possibly a Google Account would be requirement by One Drive and Colab

**Follow these instructions to be able to work with the code:**
1. Install the Libraries as already explained
2. Open the Jupyter Notebook provided
3. Run the Imports Cell and then Skip to the "Model training part"

If everything has been followed correctly no issues should be coming up.

### Local SetUp
When it comes to the local set up the following needs to be considered. **Please follow the requirements** listed:
1. Installed Libraries as explained in the prior section
2. Depending on your preferences either download 
   3. the full folder
   4. only download the notebook to a local folder of your choice (if only the notebook is installed localy you will have to go through the image downloading and test/train split)


**Follow these instructions to be able to work with the code:**
1. Install the Libraries as already explained
2. Open the Jupyter Notebook provided
3. In cells with filepaths, please set it to your local path
4. If you have not downloaded all from the repo then please run the cells step by step (All the folders such as train and split will be created automatically, only paths need to be adapted in the code)
5. If all had been downloaded you can skip to the model training part, just make sure to change the filepaths to yours

6. There is one part in the code in which we test the models with images from the internet - here either use your own and change the filepath completely or download the folder "ImagesFromInternet" for the same results and change the filepath to where the folder is located

#### Findings and other Lessons Learned
Please see the presentation slides for more information 
