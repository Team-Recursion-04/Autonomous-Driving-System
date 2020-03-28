# **Autonomous Driving** 

<div align="center">
<img src="https://img.shields.io/github/license/Team-Recursion-04/Autonomous-Driving-System">	
<img src="https://img.shields.io/github/stars/Team-Recursion-04/Autonomous-Driving-System">
<img src="https://img.shields.io/github/forks/Team-Recursion-04/Autonomous-Driving-System">
<img src="https://img.shields.io/github/issues/Team-Recursion-04/Autonomous-Driving-System">
<img src="https://img.shields.io/badge/PRs-welcome-informational">
</div

#### 1. Dependencies

* Python3.5, CUDA8 , OpenCV3, tensorflow

#### 3. Running the code

(1) Download weights for YOLO

Download the weights from [here](https://github.com/gliese581gg/YOLO_tensorflow) and save it to
the [weights](weights) folder.

(2) To run the demo simply run
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

YOLO is an object detection pipeline baesd on Neural Network. A single neural network predicts bounding boxes from full images in single evaluation. Since the whole detection pipeline is a single network, it can be optimized end-to-end directly on detection performance.
The object detection task consists in determining the location on the image where certain objects are present, as well as classifying those objects. Previous methods for this, like R-CNN and its variations, used a pipeline to perform this task in multiple steps. This can be slow to run and also hard to optimize, because each individual component must be trained separately. YOLO, does it all with a single neural network.

#### Example of test image
![alt text][image8]

---

### Discussion

Using YOLO based approach accuracy is quite satisfactory.It may fail to detect the small car in distance.
