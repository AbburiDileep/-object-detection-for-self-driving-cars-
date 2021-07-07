# -object-detection-for-self-driving-cars-

EXPLORATION:

A self-driving car (sometimes called an autonomous car or driverless car) is a vehicle that uses a combination of sensors, cameras, radar and artificial intelligence (AI) to travel between destinations without a human operator.
To qualify as fully autonomous, a vehicle must be able to navigate without human intervention to a predetermined destination over roads that have not been adapted for its use.

1.Object Detection with Yolo:	

we introduce the architecture of the object detector YOLO. YOLO is a fully CNN (FCN). It contains only convolutional layers and is invariant to the size of the input image. YOLO takes a different approach to object detection since it “looks” at each image once as indicates its name: You Only Look Once. YOLO converts the input image into a grid by S ×S cells and each of these cells is subject for the prediction of N bounding boxes enclosing the object. For each bounding box, a particular object belonging to a speciﬁc cl
class is detected with a score representing the level of conﬁdence. Classes can be cars, buses, pedestrians, trucks, trafﬁc lights, and all other things showing up along the way

Implementation:

Object detection is actually a two-part process, image classification and then image localization. Image classification is determining what the objects in the image are, like a car or a person, while image localization is providing the specific location of these objects, as seen by the bounding boxes.
To perform image classification, a  convolutional neural network is trained to recognize various objects, like traffic lights and pedestrians. A convolutional neural network performs convolution operations on images in order to classify them.

Object Localization:

We use an algorithm called non-max suppression. While training the network, we compare our bounding box results from the CNN to the actual bounding box. 
Our cost function is the area of intersection divided by the area of union of the two bounding boxes.
The closer this number, also called IoU (intersection over union), is to 1, the better our prediction .
After training our network to predict the bounding boxes across our training set and as we start to test it, we must also take into consideration that parts of the same object may be in multiple grid cells, resulting in multiple bounding boxes. 
This calls for non-max suppression

YOLO Algorithm:

The YOLO algorithm only needs to run the entire image once through the CNN once, while the sliding window algorithm is much more computationally expensive. 
YOLO uses features from the entire image to predict each bounding box and their classes which it does simultaneously.
Similar to humans, YOLO can pretty much immediately recognize where and what objects are within a given image.
![image](https://user-images.githubusercontent.com/80278260/124706175-7cbc7e80-df14-11eb-9aa0-5e2fba804ba0.png)


