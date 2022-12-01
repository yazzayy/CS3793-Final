# CS3793-Final

# Traffic light detection using tensorflow
## Prerequisites
- Python 3.7 or higher with [OpenCV installed](https://automaticaddison.com/how-to-set-up-anaconda-for-windows-10/)
- You have [TensorFlow 2 Installed](https://www.tensorflow.org/install).
  - Windows 10 Users, see [this post](https://automaticaddison.com/how-to-install-tensorflow-2-on-windows-10/).
  - If you want to use GPU support for your TensorFlow installation, you will need to follow [these steps](https://www.tensorflow.org/install/gpu). If you have trouble following those steps, you can follow [these steps](https://automaticaddison.com/real-time-object-recognition-using-a-webcam-and-deep-learning/#install_tf_gpu) (note   that the steps change quite frequently, but the overall process remains relatively the same).
  - [This post](https://automaticaddison.com/predict-vehicle-fuel-economy-using-a-deep-neural-network/) can also help you get your system setup, including your virtual environment in Anaconda (if you decide to go this route).
- [This tutorial is not a prerequisite](https://tensorflow-object-detection-api-tutorial.readthedocs.io/en/latest/index.html), but it is one of the best tutorials on the Internet for the step-by-step process of how to detect objects in an image or a video using Tensorflow 2.

## Installation and Setup
We now need to make sure we have all the software packages installed. Check to see if you have OpenCV installed on your machine. If you are using Anaconda, you can type:
```bash
conda install -c conda-forge opencv
```
Alternatively, you can type:
```bash
pip install opencv-python
```
Make sure you have NumPy installed, a scientific computing library for Python.

If you’re using Anaconda, you can type:
```bash
conda install numpy
```

Alternatively, you can type:
```bash
pip install numpy
```
Install Matplotlib, a plotting library for Python.

For Anaconda users:
```bash
conda install -c conda-forge matplotlib
```
Otherwise, you can install like this:
```bash
pip install matplotlib
```

# Step 1: Extract cropped traffic lights from images.

Files: Place **extract_traffic_lights.py** & **object_detection.py** in a directory

I used [The Bosch Small Traffic Lights Dataset](https://hci.iwr.uni-heidelberg.de/content/bosch-small-traffic-lights-dataset).

Folders: Create a folder called **traffic_light_input** and place your desired images there, and create an empty folder **traffic_light_cropped**.

Then, run
```bash
python extract_traffic_lights.py
```
and you will get cropped images in **traffic_light_cropped**.


Example image:

![alt text](https://i.imgur.com/6Obt1bR.jpg)

## Step 2: Separate traffic lights by color

Folders: create a new folder in the main directory (where the .py files are) called **traffic_light_dataset**. Inside this folder create 4 new folders: 
1. **0_green**
2. **1_yellow**
3. **2_red**
4. **3_not**

After that, find some of the cropped images we generated in the previous step, and place them in the corresponding folder.

An example for each:

- **0_green**:

![alt text](https://i.imgur.com/mkEQmGs_d.webp?maxwidth=760&fidelity=grand)


- **1_yellow**:

 ![alt text](https://i.imgur.com/unkYDRP.jpg)
 
 
- **2_red**:

 ![alt text](https://i.imgur.com/e0EqLYO.jpg)
 
 
- **3_not**:

 ![alt text](https://i.imgur.com/M1uuG80.jpg)
