# **Finding Lane Lines on the Road** 

_Author: Owen Hua_

_Date: 07/17/2017_

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./test_images_output/solidWhiteCurveLD.jpg "Rawlines Picture"

---
### Lane Finding Pipeline (list criteria and meets the specification)

* Does the pipeline for line identification take road images from a video as input and return an annotated video stream as output?
 
  _Yes. Here is the link for you to download the output video: https://github.com/OwenHua666/SDCar_P1_Term1/blob/master/test_videos_output/solidWhiteRight.mp4_
* Has a pipeline been implemented that uses the helper functions and / or other code to roughly identify the left and right lane lines   with either line segments or solid lines? 

  _Yes, and I show one of my result below_

![alt text][image1]


* Have detected line segments been filtered / averaged / extrapolated to map out the full extent of the left and right lane boundaries?

  _Yes. Here isthe link for you to download the output video: https://github.com/OwenHua666/SDCar_P1_Term1/blob/master/test_videos_output/solidYellowLeft.mp4_
  
### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. First, I converted the images to grayscale. Second, I apply Gaussian smoothing to the grayscale image. Third, I retrive edges from the grayscale image using Canny Edge Detection algorithm. Fourth, I create a mask to only keep the edges in the region of interest. Finally, I use Hough Transformaton to find the line in the image. 

In order to draw a single line on the left and right lanes, I modified the draw_lines() function. Based on the slopes of line segments found from Hough Transformation Line Detection, I mark the line segments as "left Lane" (slope < 0) and "Right Lane" (slope > 0). Then, I average each of the two lane groups to find mean points and slopes. Finally, I draw the two averaged lanes from the bottom of the image to the far end of interest. This is down by using (y2 - y1) = k * (x2 - x1).

Note: _The Pipeline described above is simple. So, I don't attach an image for it._

### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
