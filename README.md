# Face Mask Detector: Detect Mask-Wear Correctness

![Face Mask Detector Logo](https://user-images.githubusercontent.com/25768661/128629709-bedaada8-05d9-413a-a537-7c593a11fab6.png)

# What is Face Mask Detector? 
* A python program that detects if mask is worn, not worn or worn incorrectly. The program is based on yolov5 model which was trained on custom dataset.
* The project was a part of a [Kaggle Competition](https://www.kaggle.com/c/cvsc21objectcounting/overview) and got the first ranking in the [leaderboard](https://www.kaggle.com/c/cvsc21objectcounting/leaderboard).

## Table of contents
* [Technologies](#technologies)
  * [Dataset](#dataset)
  * [Model](#model)
  * [Setup](#setup)
  * [Features](#features)
    + [Use Still Image](#use-still-image)
    + [Use Live Camera](#use-live-camera)

## Technologies
* Programming Language: Python 
* GUI Framework: Tkinter
* Deep Learning: [Yolov5](https://github.com/ultralytics/yolov5)

## Dataset
* The model was trained on a dataset:
  * [Training Set](https://drive.google.com/drive/folders/1JZSwHkrQun8CTqFIcaKtn8KVi62M1-nO) containing 3 classes:
    * With Mask: x images.
    * Without Mask: x images.
    * Mask Worn Incorrectly: x images. 
  * [Testing Set](https://drive.google.com/drive/folders/1LYO8MpTf4-7HoUw8IjDMMVThk5yiXnrO) which was used for evaluation in kaggle.

## Model
The project was based on [Yolov5](https://github.com/ultralytics/yolov5) training on custom dataset, The dataset was training on Yolov5L model. For more information check : [Yolov5 Repo](https://github.com/ultralytics/yolov5).

The model was trained for 1000 epochs with 16 batches and got the following results:
* 0.4 MCRMS training error
* 0.5 MCRMS testing error

## Setup

To run the python application you need to install the requirements (It is preffered to start a new environment and install all the requirements) using the following command

```bash
 pip install -r requirements.txt
```



## Features
### Use Still Image
Browse and select any image, The program will automatically detect the faces and each face will passed to the pre-trained model for classification.

The output will be automatically displayed and also saved in `./runs/detect/` directory.

![Mask Still Image](https://user-images.githubusercontent.com/25768661/128630138-b4bf9a40-9a48-4a1d-bd5f-69288bc16993.gif)

More Examples:
![woman-mask-split-04-ht-jt-210316_1615932165011_hpEmbed_4x3_992](https://user-images.githubusercontent.com/25768661/128630232-2ba0c0d3-c09d-4ced-9c6c-69e9f708ac32.jpg)

![face-recognition-test](https://user-images.githubusercontent.com/25768661/128630234-f6cd57ab-17b3-4e3e-a5f3-f4099e1af6d8.jpg)

![GettyImages-1223601728_2_preview-c-d040c4f](https://user-images.githubusercontent.com/25768661/128630235-f3be345b-5f59-41ce-8168-9181d2050768.jpg)

### Use Live Camera
Instead of using an image, If you have a camera in your PC/Laptop, you can press "Use Live Camera" to get the classification done on the camera input.

Each frame will be passed to the model for classification and the output will be automatically shown and also the video will be saved in `./runs/detect/` directory.

![index](https://user-images.githubusercontent.com/25768661/128634496-15bd98da-2a4f-45a2-924c-7342e8a85550.png)

