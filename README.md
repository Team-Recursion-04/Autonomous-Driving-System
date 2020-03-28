# **Vehicle Detection for Autonomous Driving** 

## Objective

#### A demo of Vehicle Detection System: a monocular camera is used for detecting vehicles. 


#### [**(1) Highway Drive (with Lane Departure Warning)**](https://youtu.be/Brh9-uab7Qs) (Click to see the full video)

[![gif_demo1][demo1_gif]](https://youtu.be/Brh9-uab7Qs)

#### [**(2) City Drive (Vehicle Detection only)**](https://youtu.be/2wOxK86LcaM) (Click to see the full video)

[![gif_demo2][demo2_gif]](https://youtu.be/2wOxK86LcaM)

---

### Code & Files

#### 1. Our project includes the following files

* [main.py](main.py) is the main code for demos
* [yolo_pipeline.py](yolo_pipeline.py) is the car detection pipeline with a deep net [YOLO (You Only Look Once)](https://arxiv.org/pdf/1506.02640.pdf)
* [visualization.py](visualizations.py) is the function for adding visalization
* [calibration.py](calibration.py) contains the script to calibrate camera and save the calibration results
* [lane.py](model.h5) contains the lane class 
* [examples](examples) folder contains the sample images and videos


#### 2. Dependencies & my environment

Anaconda is used for managing my [**dependencies**](https://github.com/udacity/CarND-Term1-Starter-Kit).
* You can use provided [environment-gpu.yml](environment-gpu.yml) to install the dependencies.
* OpenCV3, Python3.5, tensorflow, CUDA8  
* OS: Ubuntu 16.04

#### 3. How to run the code

(1) Download weights for YOLO

You can download the weight from [here](https://drive.google.com/open?id=0B5WIzrIVeL0WS3N2VklTVmstelE) and save it to
the [weights](weights) folder.

(2) If you want to run the demo, you can simply run:
```sh
python main.py
```


### **Approach : Neural Network**


[//]: # (Image References)
[image1]: ./examples/car_not_car.png
[image2]: ./examples/hog_1.png
[image2-1]: ./examples/hog_2.png
[image3]: ./examples/search_windows.png
[image4]: ./examples/heat_map1.png
[image5]: ./examples/heat_map2.png
[image6]: ./examples/labels_map.png
[image7]: ./examples/svn_1.png
[image8]: ./examples/yolo_1.png
[image_yolo1]: ./examples/yolo1.png
[image_yolo2]: ./examples/yolo2.png
[video1]: ./project_video.mp4
[demo1_gif]: ./examples/demo1.gif
[demo2_gif]: ./examples/demo2.gif


### You Only Look Once (YOLO)
`yolo_pipeline.py` contains the code for the yolo pipeline. 

[YOLO](https://arxiv.org/pdf/1506.02640.pdf) is an object detection pipeline baesd on Neural Network. Contrast to prior work on object detection with classifiers 
to perform detection, YOLO frame object detection as a regression problem to spatially separated bounding boxes and
associated class probabilities. A single neural network predicts bounding boxes and class probabilities directly from
full images in one evaluation. Since the whole detection pipeline is a single network, it can be optimized end-to-end
directly on detection performance.

![alt text][image_yolo2]

Steps to use the YOLO for detection:
* resize input image to 448x448
* run a single convolutional network on the image
* threshold the resulting detections by the model’s confidence

![alt text][image_yolo1]

`yolo_pipeline.py` is modified and integrated based on this [tensorflow implementation of YOLO](https://github.com/gliese581gg/YOLO_tensorflow).
Since the "car" is known to YOLO, I use the precomputed weights directly and apply to the entire input frame.

#### Example of test image
![alt text][image8]

---

### Discussion

YOLO based approach achieves real-time and the accuracy are quite satisfactory. Only in some cases, it may failure to
detect the small car thumbnail in distance.In order to correctly identify the car in distance, we might need to either crop the image or retrain the network.
