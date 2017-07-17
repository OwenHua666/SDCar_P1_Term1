# **Finding Lane Lines on the Road** 

## Author: Owen Hua
## Date: 07/17/2017

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

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I .... 

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by ...

If you'd like to include images to show how the pipeline works, here is how to include an image: 




### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
