# Object_Detection_YoloV4
Object Detection Model

### Objective
Object detection simply means identifying the objects in a particular image. As we know how our models detect objects present in an image- first by finding the location of objects, creating bounding boxes around those objects, and classifying that bounding box, that is, what is the object present in that bounding box.

### It is a challenging problem to build a model for:

- the object recognition: finding where is the object,
- object localization: creating bounding boxes around an object,
- object classification: what is the object present in that box.

### Detect objects in both images and video streams using Deep Learning, OpenCV, and Python.

I’ll be using YOLOv4 in this project, in particular, YOLO trained on the COCO dataset.

The COCO dataset consists of 80 labels, including, but not limited to:

- People
- Car
- Motorcycle

You can find a full list of what YOLO trained on the COCO dataset can detect <a href="https://github.com/pjreddie/darknet/blob/master/data/coco.names" 


## 
- Pandas
- Matplotlib
- numpy
- OpenCV
- PYQT
- LabelImg
- OIDv4 Toolkit (Used to download images from google open source)




In prediction.png you can see that YOLO has not only detected each person in the input image, but also has detected car and mototcycle as well!


<img src="https://github.com/vishalsingh3363/Object_Detection_YoloV4/blob/main/prediction.png">


## To Download trained weights
`!wget https://github.com/AlexeyAB/darknet/releases/download/darknet_yolo_v3_optimal/yolov4.conv.137` 



## To Run the project

- `!./darknet detector train data/Person_Car/image_data.data cfg/yolov4_train.cfg yolov4.conv.137 -dont_show`


In the Image, you can see not only the Car, people, and  motorbikes are detected!

The YOLO object detector is performing quite well here. 

## Limitation:
### Arguably the largest limitation and drawback of the YOLO object detector is that:

- It does not always handle small objects well

- It especially does not handle objects grouped close together


