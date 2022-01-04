# Obect_Tracking_System_Based_on_Lucas_Kanade
This project contains an implementation of video object tracking with conner detections, k-means key point clustering, and Iterative Lucas-Kanade (ILK) algorithm with pyramid hierarchy.

## Features
This project aims at 
tracking salient feature points appearing in the first frame throughout the whole video with their 
trajectories plotted. The program is compliant with online fashion, which means that the 
rendered video will be played in real-time with a new window prompted when the program 
starts running. There are multiple extra multiple features implemented to enhance its 
functionalities, which are listed as follows:

1. Self-implemented Harris corner detection algorithm for feature identifications.
2. Self-implemented Lucas-Kanade algorithm for optic flow calculations. 
3.  Self-defined feature cleaner including:
  * An adaptive threshold mechanism
  * A minimal distance discriminator to reject excessively dense features.
  * A K-means clustering for optimizing the selection of feature points. 
4. Image warping and iterative LK algorithm for higher accuracies. 
5. Pyramid Lucas-Kanade implementation for large movement robustness.
6. Real-time video capturing and tracking

![](https://github.com/Jeffrey0Liao/Obect_Tracking_System_Based_on_Lucas_Kanade/blob/main/resources/1.JPG "")

## Methods
### Harris Corner Detection
![](https://github.com/Jeffrey0Liao/Obect_Tracking_System_Based_on_Lucas_Kanade/blob/main/resources/e1.JPG "")
### Lucas-Kanade Optic Flow
![](https://github.com/Jeffrey0Liao/Obect_Tracking_System_Based_on_Lucas_Kanade/blob/main/resources/e2.JPG "")
### Iterative Lucas-Kanade
![](https://github.com/Jeffrey0Liao/Obect_Tracking_System_Based_on_Lucas_Kanade/blob/main/resources/e3.JPG "")
### Pyramid ILK
1. Build image pyramids for both the old frame and the new frame through down sampling. 
2. Down sampling the input features.
3. Starting from the smallest level, use ILK to compute its optic flow.
4. Up sample the features and the motion maps from the current level.
Equation 7
5. Use this as the initial input of the ILK of the subsequent level.
6. Repeat 3 to 5 until the last level of the pyramid.

## Results
![](https://github.com/Jeffrey0Liao/Obect_Tracking_System_Based_on_Lucas_Kanade/blob/main/resources/2.JPG "Preliminary Results")
## Usage


For full report please visit [here](https://github.com/Jeffrey0Liao/Obect_Tracking_System_Based_on_Lucas_Kanade/blob/main/resources/CV_cw1_report_20030694.pdf)
