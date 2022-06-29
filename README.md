# Grocery Item Detection

Object detection is a computer vision task that requires object(s) to be detected, localized and classified. The model must be able to classify the object represented by the bounding box. YOLO “You Only Look Once” is a state-of-the-art real-time deep learning algorithm used for object detection, localization and classification in images and videos. This algorithm is very fast, accurate and at the forefront of object detection based projects.

Each of the versions of YOLO kept improving the previous in accuracy and performance. Then came YOLOv4 developed by another team, further adding to performance of model and finally the YOLOv5 model was introduced by Glenn Jocher in June 2020. This model significantly reduces the model size (YOLOv4 on Darknet had 244MB size whereas YOLOv5 smallest model is of 27MB). YOLOv5 also claims a faster accuracy and more frames per second than YOLOv4 as shown in graph below.

![image](https://user-images.githubusercontent.com/64592084/135288675-d83a0635-53de-4412-81ef-153a186c4c1b.png)

## Dataset

The dataset is obtained by scraping grocery images for five different product categories - chips, chocolate, icecream, maggi, softdrink. Each class consists of 80 images.
The dataset is then divided into train and validation set in the ratio (85:15) with 68 images in the training set and 12 in the validation set for each of the five categories.
Online image annotations for all 400 image were created on [makesense.ai] (https://www.makesense.ai/) in YOLOv5 supported format.
The dataset was zipped and saved in Google Drive for further use in Google Colab.

## Network Architecture

The network is saved as custom_data.yaml file
```
train: ../dataset/images/train/
val: ../dataset/images/val/ 

# Classes
nc: 5  # number of classes
names: ['chips', 'chocolate', 'icecream', 'maggi', 'softdrink']  # class names
```

## Training

The training process starts. I defined the image size (img) to be 640x640, batch size 16 and the model is run for 30 epochs. 

## Results

### (I) Object detection using Yolov5
Following images show the result of YOLOv5 algorithm.
![Frame(0)]("https://user-images.githubusercontent.com/64592084/176429125-ae71c384-3310-43f7-8ff4-9a5119c3462b.png")
![Frame(30)](https://user-images.githubusercontent.com/64592084/135299136-2c1f5087-186d-474d-8648-d025245867a3.jpg)
![Frame(60)](https://user-images.githubusercontent.com/64592084/135299970-a5e3ba60-47d3-4da3-9776-f3e86dbf1b86.jpg)


### (II) Bill generation
![image](https://user-images.githubusercontent.com/64592084/135299702-c2054949-df07-42bc-aa45-2771c8ad3628.png)

## Conclusion
A chaotic process like shopping can also be automated. AI opens plethora of opportunities for new and innovative shopping experience in the retail sector and I have tried to build an easy and effective self-checkout solution!




