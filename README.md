# **Face Recognition - using FaceNet**

Face recognition is an interesting task for `computer vision apps` because it gives the `face` of a person that you want to analyse. Also, a system like this can be combined with [FaceX](https://github.com/pauldamsa/FaceX) system in order to get more informations about the face of a person.

The **purpose** of this repository is to show you the performance of **FaceNet** on **LFW dataset**.
In order to see the whole code you have to check the **LFW & FaceNet - performance analysis.ipynb** notebook. In it you have all you need to know for getting **insights** about the performance of LFW dataset on Face Recognition task.
## Table of contents
* [General info](#general-info)
* [Requirements](#requirements)
* [Setup](#setup)
* [How to run](#how-to-run)
* [To-do List](#to-do-list)
* [Contact](#contact)

## General info
The directory **lfw** contains the images of LFW Dataset, but not all images because on GitHub you cannot push more than 100MB of files. Also, in the **facenet-weights.h5** you can find the weights of FaceNet.

This approach of using **FaceNet as embedder** is very nice, because it offers you the posibillity of **not training again** the network when a **new face** comes into play. Also, after my analysis I realised that how important is the choice of reference image. Reference image is that image that you want its embeddings and see the difference between others. The difference can be calculated as the euclidean/cosine/l2_euclidean distance between two faces.

There are 4 steps for face recognition task to realise:
1. Face detection
2. Face alignment
3. Face representation (FaceNet)
4. Face verification (distance)
<img src = "https://github.com/pauldamsa/Face-Recognition/blob/master/face-recognition-approach.png" height = "300" width="500">

In the below table we can see the performance of FaceNet with first image of each person as reference image. You can see in the notebook how the performance on different reference images. 
<img src = "https://github.com/pauldamsa/Face-Recognition/blob/master/10-persons%20analysis.png" height = "300" width = "1000">

## Requirements
* TensorFlow - version 2.2.0
* OpenCV - version 4.1.2
* matplotlib - version 3.2.1
* seaborn - version 0.10.1
* pandas - version 1.0.4
* numpy - version 1.18.4
* dlib - version 19.18.0
* virtualenv - version 20.0.16

## Setup
The setup is simple, you need:
1. Create a virtual environment `python -m venv name_of_your_env` or You can run in **Google Colab** the **LFW & FaceNet - performance analysis.ipynb** notebook.
2. Install the above packages with `pip install package_name`

## How to run
After you install the necessary packages you can run the app like this:
If you choose to run on your laptop or PC, I encourage you to install all necessary packages and just after that try to run the notebook.

## To-do list:
* Improve the performance of the model when the face is occluded or any other situations.

## Contact

If you want to add any improvements feel free to reach me at <paul_damsa9@yahoo.com>.
