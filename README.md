# TensorFlow-Powered Vision For Pi-based robot

***

* TensorFlow Version: 1.0.1
* [Written by Korean](https://github.com/leehaesung/TensorFlow-Powered_Robot_Vision/blob/master/README_Korean.md)

## Introduction

This is a Pi-based robot to implement visual recognition([Inception V3](https://research.googleblog.com/2016/03/train-your-own-image-classifier-with.html)). The TensorFlow-Powered vision can recognize many objects such as people, car, bus, fruits, and so on. 

* Hardware: Raspberry-Pi2, Sony PS3 Eye Camera
 
   (Available to use Logitech C270 USB camera with Raspberry Pi)

* Software: TensorFlow(v1.0.1), Jupyter-Notebook

![Structure.png](https://github.com/leehaesung/TensorFlow-Powered_Robot_Vision/blob/master/ImageFiles/Structure.png)


## My motivation
 I was so curious about excellence of the image recognition with TensorFlow on Raspberry Pi. Also, the Jupyter notebook is very convenient to instantly code as a quick prototype. So, in terms of error rate of the image classification, Inception V3(3.46%) is more excellent than human(5.1%) whereas raspberry pi's processing speed is very slow compare to my laptop.  

([Table: Jeff Dean's Keynote @Google Brain](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/44921.pdf)). 
 
 ![Chart_IR.png](https://github.com/leehaesung/TensorFlow-Powered_Robot_Vision/blob/master/ImageFiles/Chart_ImageRecognition.png)


* Schematic diagram of Inception-v3 

![InceptionV3.png](https://github.com/leehaesung/TensorFlow-Powered_Robot_Vision/blob/master/ImageFiles/InceptionV3.png)


## Requirements and Installation

 * Install a webcam driver on your Rapsberry Pi.
 ```
 sudo apt-get install fswebcam
 ```
 
 * Test your webcam.
 ```
 fswebcam test.jpg
 ```

 * TensorFlow (V1.0.1): [How To Install TensorFlow on Raspberry Pi](https://www.instructables.com/id/Google-Tensorflow-on-Rapsberry-Pi/)
 
 * Jupyter-Notebook: [How To Install Jupyter-Notebook on Raspberry Pi](https://www.instructables.com/id/Jupyter-Notebook-on-Raspberry-Pi/)
 
 
## Quick Start

* You should install both TensorFlow(v1.0.1) and Jupyter notebook on your Raspberry Pi.

* First, clone the TensorFlow-Powered_Robot_Vision git repository here. This can be accomplished by:
```
cd /home/pi/Documents
git clone https://github.com/leehaesung/TensorFlow-Powered_Robot_Vision.git
```
next, cd into the newly created directory:
```
cd TensorFlow-Powered_Robot_Vision
``` 
Drive your jupyter notebook on your Raspberry Pi.
```
jupyter-notebook
```
The pre-trained data(inception_v3.ckpt) will automatically download when driving the Jupyter notebook. (Where: /pi/home/Documents/datasets/inception)


## Source Codes

* [TensorFlow-Powered_Robot_Vision.ipynb](https://github.com/leehaesung/TensorFlow-Powered_Robot_Vision/blob/master/TensorFlow-Powered_Robot_Vision.ipynb)
* [imagenet_class_names.txt](https://github.com/leehaesung/TensorFlow-Powered_Robot_Vision/blob/master/datasets/inception/imagenet_class_names.txt)
* inception_v3.ckpt (When implementing the jupyter notebook)


## Results of Object Recognition 

* Wow! The result is really awessome!!

![RecognitionResult.png](https://github.com/leehaesung/TensorFlow-Powered_Robot_Vision/blob/master/ImageFiles/Result_96.25.png)


## How To Retrain 

* [This CodeLab(Google) is really useful in learning this stuff](https://codelabs.developers.google.com/codelabs/tensorflow-for-poets/?utm_campaign=chrome_series_machinelearning_063016&utm_source=gdev&utm_medium=yt-desc#0)
* [How to Retrain Inception's Final Layer for New Categories](https://www.tensorflow.org/tutorials/image_retraining)


## References

* [Rethinking the Inception Architecture for Computer Vision (Paper)](https://arxiv.org/abs/1512.00567)
* [Image Recognition::Tensorflow.org (Web)](https://www.tensorflow.org/tutorials/image_recognition)
* [Hands-On Machine Learning with Scikit-Learn and TensorFlow (Book)](https://www.amazon.com/Hands-Machine-Learning-Scikit-Learn-TensorFlow/dp/1491962291/ref=sr_1_1?ie=UTF8&qid=1494573194&sr=8-1&keywords=hands+on+machine+learning+with+scikit+learn+and+tensorflow)
* [Train your own image classifier with Inception in TensorFlow (Blog)](https://research.googleblog.com/2016/03/train-your-own-image-classifier-with.html)
* ["Large-Scale Deep Learning for Building Intelligent Computer Systems," a Keynote Presentation from Google](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/44921.pdf)
* [How Convolutional Neural Networks work (YouTube)](https://www.youtube.com/watch?v=FmpDIaiMIeA)
