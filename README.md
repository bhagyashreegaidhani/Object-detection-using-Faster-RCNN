# Object-detection-using-Faster-RCNN
We will be working on a healthcare related dataset and the aim here is to solve a Blood Cell Detection problem. Our task is to detect all the Red Blood Cells (RBCs),
White Blood Cells (WBCs), and Platelets in each image taken via microscopic image readings.
The reason for choosing this dataset is that the density of RBCs, WBCs and Platelets in our blood stream provides a lot of information about the immune system and hemoglobin. This can help us potentially identify whether a person is healthy or not, and if any discrepancy is found in their blood, actions can be taken quickly to diagnose that.
Manually looking at the sample via a microscope is a tedious process. And this is where Deep Learning models play such a vital role. 
They can classify and detect the blood cells from microscopic images with impressive precision.
Note that we will be using the popular Keras framework with a TensorFlow backend in Python to train and build our model.
Setting up the System
Before we actually get into the model building phase, we need to ensure that the right libraries and frameworks have been installed. The below libraries are required to run this project:

pandas
matplotlib
tensorflow
keras – 2.0.3
numpy
opencv-python
sklearn

Data Exploration:
train_images: Images that we will be using to train the model. 
We have the classes and the actual bounding boxes for each class in this folder.
test_images: Images in this folder will be used to make predictions using the trained model. 
This set is missing the classes and the bounding boxes for these classes.
train.csv: Contains the name, class and bounding box coordinates for each image such as,
xmin,ymin=coordinates of top left corner of the bounding box/rectangle.
xmax,ymax=coordinates of the bottom right corner of the bounding box/rectangle
There can be multiple rows for one image as a single image can have more than one object.

Implementing FastRCNN model.Downlad model from following git repository.
If you are using jupyter notebook on local machine then run below command
!git-clone https://github.com/kbardool/keras-frcnn.git
on google colab run=git clone https://github.com/kbardool/keras-frcnn.git

In order to train the model on a new dataset, the format of the input should be:

filepath,x1,y1,x2,y2,class_name
where,

filepath is the path of the training image
x1 is the xmin coordinate for bounding box
y1 is the ymin coordinate for bounding box
x2 is the xmax coordinate for bounding box
y2 is the ymax coordinate for bounding box
class_name is the name of the class in that bounding box




