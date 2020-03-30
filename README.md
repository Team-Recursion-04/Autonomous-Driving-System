# **Autonomous Driving** 

<div align="center">
  <a href="https://github.com/badges/shields/graphs/contributors" alt="Contributors"> <img src="https://img.shields.io/github/contributors/Team-Recursion-04/Autonomous-Driving-System" />
<img src="https://img.shields.io/github/license/Team-Recursion-04/Autonomous-Driving-System">	
<img src="https://img.shields.io/github/stars/Team-Recursion-04/Autonomous-Driving-System">
<img src="https://img.shields.io/github/forks/Team-Recursion-04/Autonomous-Driving-System">
<img src="https://img.shields.io/github/issues/Team-Recursion-04/Autonomous-Driving-System">
<img src="https://img.shields.io/badge/PRs-welcome-informational">
</div>

#### Demo:


#### **(1) Lane detection**

![gif_demo1][demo1_gif]

#### **(2) Vehicle Detection**

![gif_demo2][demo2_gif]

---


#### How to run the code

(1) Download weight URL for YOLO

[here](https://github.com/gliese581gg/YOLO_tensorflow) and save it to the [weights](weights) folder.
The link is also  specified [here](https://github.com/Team-Recursion-04/Autonomous-Driving-System/blob/master/weights/put_weights_here.txt)

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
[image8]: ./examples/yolo_1.png
[image_yolo1]: ./examples/yolo1.png
[image_yolo2]: ./examples/yolo2.png
[video1]: ./project_video.mp4
[demo1_gif]: ./examples/demo1.gif
[demo2_gif]: ./examples/demo2.gif


### You Only Look Once (YOLO)
`yolo_pipeline.py` contains the code for the yolo pipeline. 

YOLO is an object detection pipeline baesd on Neural Network. Contrast to prior work on object detection with classifiers 
to perform detection, YOLO frame object detection as a regression problem to spatially separated bounding boxes and
associated class probabilities. A single neural network predicts bounding boxes and class probabilities directly from
full images in one evaluation. Since the whole detection pipeline is a single network, it can be optimized end-to-end
directly on detection performance.


![alt text][image_yolo1]


#### Example of test image
![alt text][image8]

---

## Developers:

[Vedant Khairnar](http://vedantkhairnar.ml/)

Pranav Manbhekar

Vishal Kriplani

Piyush Chotiya
