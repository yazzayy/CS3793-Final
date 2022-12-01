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

Place **extract_traffic_lights.py** & **object_detection.py** in a directory,
 and create a folder called **traffic_light_input** and place your desired images there.
I used [The Bosch Small Traffic Lights Dataset](https://hci.iwr.uni-heidelberg.de/content/bosch-small-traffic-lights-dataset).

Run
```bash
python extract_traffic_lights.py
```
