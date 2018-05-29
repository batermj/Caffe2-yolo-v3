# Caffe2-yolo-v3
A Caffe2 implementation of a YOLO v3 Object Detector

This repository contains code for a object detector based on YOLOv3: An Incremental Improvement, implementedin Caffe2. The code is based on the official code of YOLO v3.


Implement YOLO v3 from scratch

Now, the code only contains the detection module,(training module code may be come on later.)
Requirements

    Python 2.7
    OpenCV
    Caffe2

Intall the YOLOModule
  I  assume　you have already installed the Caffe2 from source.
  1. Make the yolo op as a module:If your Caffe2 older one(https://github.com/caffe2/caffe2),cut the Yolo folder to the Caffe2-master/modules;if your Caffe2 is newer(https://github.com/pytorch/pytorch)cut the Yolo folder to the pytorch-master/modules,the open the CMakeList in the modules folder and add a line with content add_subdirectory(Yolo),and close it.
  2.recompile the whole Caffe2 Project:assume Curent dir is Caffe2-master
    mkdir build
    cd build
    cmake ..
    make install -j8
   3.If success, default in the /usr/local/lib/,we could see generate a so file named libcaffe2_yolo_ops_gpu.so.

The init_net.pb and predict_net.pb is convert from the original model https://pjreddie.com/media/files/yolov3.weights.

CPPDemo
  
PythonDemo

