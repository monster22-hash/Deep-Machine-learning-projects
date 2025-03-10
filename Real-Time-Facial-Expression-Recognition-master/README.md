# Real Time Facial Expression Recognition
![blog_picture](https://user-images.githubusercontent.com/26830527/48616166-15341800-e993-11e8-9d25-1d1145a6b87d.png)

## Description
Computer animated agents and robots bring new dimension in human computer interaction which makes it vital as how computers can affect our social life in day-to-day activities. Face to face communication is a real-time process operating at a a time scale in the order of milliseconds. The level of uncertainty at this time scale is considerable, making it necessary for humans and machines to rely on sensory rich perceptual primitives rather than slow symbolic inference processes.<br><br>
In this project we are presenting the real time facial expression recognition of seven most basic human expressions: ANGER, DISGUST, FEAR, HAPPY, NEUTRAL SAD, SURPRISE.<br><br>
This model can be used for prediction of expressions of both still images and real time video. However, in both the cases we have to provide image to the model. In case of real time video the image should be taken at any point in time and feed it to the model for prediction of expression. The system automatically detects face using HAAR cascade then its crops it and resize the image to a specific size and give it to the model for prediction. The model will generate seven probability values corresponding to seven expressions. The highest probability value to the corresponding expression will be the predicted expression for that image.
## Business Problem
However, our goal here is to predict the human expressions, but we have trained our model on both human and animated images. Since, we had only approx 1500 human images which are very less to make a good model, so we took approximately 9000 animated images and leverage those animated images for training the model and ultimately do the prediction of expressions on human images.<br><br> 
For better prediction we have decided to keep the size of each image <b>350*350</b>.<br><br>
<b>For any image our goal is to predict the expression of the face in that image out of seven basic human expression</b>
## Problem Statement
<b>CLASSIFY THE EXPRESSION OF FACE IN IMAGE OUT OF SEVEN BASIC HUMAN EXPRESSION</b>
## Source Data
We have downloaded data from 4 different sources.<br>
1. Human Images Source-1: http://www.consortium.ri.cmu.edu/ckagree/
2. Human Images Source-2: http://app.visgraf.impa.br/database/faces/
3. Human Images Source-3: http://www.kasrl.org/jaffe.html
4. Animated Images Source: https://grail.cs.washington.edu/projects/deepexpr/ferg-db.html
## Real-World Business Objective & Constraints
1. Low-latency is required.
2. Interpretability is important for still images but not in real time. For still images, probability of predicted expressions can be given.
3. Errors are not costly.
## How to Run the Model
After downloading data from the aforementioned sources you have to structure the data into separate folders corresponding to the seven class labels. Then you can use the code in the file "FacialExpressionRecognition.ipynb" to train the model. You can add or delete layers in MLP part of the model based on your data and results. Don't forget to save your model after each epoch. 
Then for real time prediction you can run the file "Real_Time_Prediction.ipynb".
## Prerequisites
You need to have installed following softwares and libraries in your machine before running this project.
1. Python 3
2. Anaconda: It will install ipython notebook and most of the libraries which are needed like sklearn, pandas, seaborn, matplotlib, numpy, PIL.
3. OpenCV
4. keras
## Installing
1. Python 3: https://www.python.org/downloads/
2. Anaconda: https://www.anaconda.com/download/
3. OpenCV: pip install opencv-python
4. Keras: pip install keras
## Built With
* ipython-notebook - Python Text Editor
* OpenCV - It is used for processing images
* Keras - Deep Learning Library
* Sklearn: It is a Machine Learning library but here it is used just to calculate accuracy and confusion matrix.
## Authors
* Rahul Kumar - Complete work  
