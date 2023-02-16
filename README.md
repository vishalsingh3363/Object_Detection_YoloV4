# Object_Detection_YoloV4
Object Detection Model


# YOLO-object-detection-with-OpenCV
Object detection using YOLO object detector

### Detect objects in both images and video streams using Deep Learning, OpenCV, and Python.

I’ll be using YOLOv4 in this project, in particular, YOLO trained on the COCO dataset.

The COCO dataset consists of 80 labels, including, but not limited to:

- People
- Car
- Cars 
- Motorcycle

You can find a full list of what YOLO trained on the COCO dataset can detect <a href="https://github.com/pjreddie/darknet/blob/master/data/coco.names" 

## YOLO object detection in images

## Installation

- `pip install numpy`
- `pip install opencv-python`
- `pip install pyqt`

## To Run the project

- `python yolo.py --image images/baggage_claim.jpg`

## Screenshots
![Image](/Object%20dection%20using%20image/1.png)

Here you can see that YOLO has not only detected each person in the input image, but also the suitcases as well!

Furthermore, if you take a look at the right corner of the image you’ll see that YOLO has also detected the handbag on the lady’s shoulder.

<img src="https://github.com/yash42828/YOLO-object-detection-with-OpenCV/blob/master/Object%20dection%20using%20image/2.png">

YOLO is able to correctly detect each of the players on the pitch, including the soccer ball itself. Notice the person in the background who is detected despite the area being highly blurred and partially obscured.

## YOLO object detection in video streams

## Installation

- `pip install numpy`
- `pip install opencv-python`


## To Download trained weights
`!wget https://github.com/AlexeyAB/darknet/releases/download/darknet_yolo_v3_optimal/yolov4.conv.137` 



## To Run the project

- `!./darknet detector train data/Person_Car/image_data.data cfg/yolov4_train.cfg yolov4.conv.137 -dont_show`


In the Image, you can see not only the vehicles being detected, but people, as well as the motorbikes, are detected too!

The YOLO object detector is performing quite well here. 

## Limitation:
### Arguably the largest limitation and drawback of the YOLO object detector is that:

- It does not always handle small objects well
- It especially does not handle objects grouped close together
- The reason for this limitation is due to the YOLO algorithm itself:

The YOLO object detector divides an input image into an SxS grid where each cell in the grid predicts only a single object.
If there exist multiple, small objects in a single cell then YOLO will be unable to detect them, ultimately leading to missed object detections.
Therefore, if you know your dataset consists of many small objects grouped close together then you should not use the YOLO object detector.


