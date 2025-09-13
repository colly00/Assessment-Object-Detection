# Household Items Object Detection (YOLOv5)

This project builds an AI system that detects and recognizes household items in images. Using the YOLOv5 deep learning model, the system can automatically look at a picture and highlight where specific objects are, such as a Couch, Door, Microwave, or Window.

Think of it like giving a computer "eyes" to see and identify things inside your home.

## Project Overview
The idea behind this project was to train an object detection model that could recognize common household items. In the first version of the project, I trained YOLOv5 to detect 10 different household objects. That version can be found here:
First Model Repository (10 Objects)https://github.com/colly00/House_Hold-object-Detection

### For this new project, I refined the dataset and focused only on 4 key objects based on assessment requirement:
Couch
Door
Microwave
Window
This cleaner dataset made the model more specialized and improved its performance.

## Dataset
Source: Roboflow dataset (annotated in YOLO format)
Size: 246 images
Training set: 172 images
Validation set: 49 images
Test set: 25 images

### Annotation format: YOLOv5 text files (.txt with bounding boxes)
Each image comes with a label file that tells the model where objects are located and which class they belong to.


## Training
To train the model on the dataset:
Uses 640x640 image size
Trains for 50 epochs
Starts training from YOLOv5’s small pretrained weights (yolov5s.pt)

## Evaluation & Results
**The model was evaluated on the validation set. Results include precision, recall, mean average precision (mAP), and a confusion matrix.**
Validation Results:
Precision (P): 0.839
Recall (R): 0.911
mAP@0.5: 0.927
mAP@0.5:0.95: 0.815

# Future Work
Train on more images to improve robustness.
Try YOLOv8 for better accuracy and speed.
Deploy the model as a simple web or mobile app (Flask/FastAPI).

# Summary
This project shows how AI can learn to recognize household objects from images. Starting from a dataset of everyday items, I trained a YOLOv5 model that can now detect Couch, Door, Microwave, and Window with high accuracy.
It’s a step toward building computer vision systems that can help with home automation, robotics, and accessibility technologies.
