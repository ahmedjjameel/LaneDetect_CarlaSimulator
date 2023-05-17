## Lane Detection using Carla Simulator


![ezgif com-resize (1)](https://github.com/ahmedjjameel/LaneDetect_CarlaSimulator/assets/81799459/31a116f9-f3ba-4067-8949-ec8983588f97)


In this project, a lane detection algorithm has been implemented using Carla Simulator. 
This project implements a real time object detection using YOLO algorithm. YOLO is an object detection algorithm which stands for You Only Look Once.

Yolo is a deep learning algorythm which came out on May 2016 and it became quickly so popular because it’s so fast compared with the previous deep learning algorythms. With yolo we can detect real time objects at a relatively high speed. With a GPU we would be able to process over 45 frames/second while with a CPU around a frame per second.


OpenCV dnn module supports running inference on pre-trained deep learning models from popular frameworks like Caffe, Torch and TensorFlow.

The following steps were performed for lane detection:

1.	Compute the camera calibration matrix and distortion coefficients given a set of chessboard images.
2.	Apply a distortion correction to raw images.
3.	Use color transforms, gradients, etc., to create a thresholded binary image.
4.	Apply a perspective transform to rectify binary image ("birds-eye view").
5.	Detect lane pixels and fit to find the lane boundary.
6.	Determine the curvature of the lane and vehicle position with respect to center.
7.	Warp the detected lane boundaries back onto the original image.
8.	Output visual display of the lane boundaries and numerical estimation of lane curvature and vehicle position.


## Camera calibration
The camera was calibrated using the chessboard images in 'camera_cal/*.jpg'. The following steps were performed for each calibration image:
1.	Convert to grayscale
2.	Find chessboard corners with OpenCV's findChessboardCorners() function, assuming a 9x6 board
After the above steps were executed for all calibration images, I used OpenCV's calibrateCamera() function to calculate the distortion matrices. Using the distortion matrices, I undistort images using OpenCV's undistort() function.



![ezgif com-video-to-gif---](https://user-images.githubusercontent.com/81799459/224973024-9515cab1-b538-471e-9cdf-19f690e884fc.gif)



![ezgif com-video-to-gif](https://user-images.githubusercontent.com/81799459/224996252-591de079-c794-4cdb-86b4-3815b1e16239.gif)








