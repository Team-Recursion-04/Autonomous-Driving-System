# **Autonomous Driving** 

<div align="center">
  <a href="https://github.com/badges/shields/graphs/contributors" alt="Contributors"> <img src="https://img.shields.io/github/contributors/Team-Recursion-04/Autonomous-Driving-System" />
<img src="https://img.shields.io/github/license/Team-Recursion-04/Autonomous-Driving-System">	
<img src="https://img.shields.io/github/stars/Team-Recursion-04/Autonomous-Driving-System">
<img src="https://img.shields.io/github/forks/Team-Recursion-04/Autonomous-Driving-System">
<img src="https://img.shields.io/github/issues/Team-Recursion-04/Autonomous-Driving-System">
<img src="https://img.shields.io/badge/PRs-welcome-informational">
</div>

[image8]: ./examples/yolo_1.png
[image_yolo1]: ./examples/yolo1.png
[demo1_gif]: ./examples/demo1.gif
[demo2_gif]: ./examples/demo2.gif

#### Demo:


#### **(1) Path Lane Detection**

![gif_demo1][demo1_gif]

#### **(2) Automobile Detection**

![gif_demo2][demo2_gif]

---


#### Instructions : 

(1) Download weight URL for YOLO

[here](https://github.com/gliese581gg/YOLO_tensorflow) and save it to the [weights](weights) folder.


(2) If you want to run the demo, you can simply run:

```sh
python main.py
```

### You Only Look Once (YOLO)

You only look once (YOLO) is a state-of-the-art, real-time object detection system. On a Pascal Titan X it processes images at 30 FPS and has a mAP of 57.9% on COCO test-dev.

YOLOv3 is extremely fast and accurate. In mAP measured at .5 IOU YOLOv3 is on par with Focal Loss but about 4x faster. Moreover, you can easily tradeoff between speed and accuracy simply by changing the size of the model, no retraining required!

YOLOv3 uses a few tricks to improve training and increase performance, including: multi-scale predictions, a better backbone classifier, and more.

![alt text][image_yolo1]


#### Example of test image
![alt text][image8]

---

## Developers:

[Vedant Khairnar](http://vedantkhairnar.ml/)

Pranav Manbhekar

Vishal Kriplani

Piyush Chotiya
