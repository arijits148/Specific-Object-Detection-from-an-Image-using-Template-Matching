# Specific Object Detection from an image using Template Matching

In this project a specific character has been detected and identified from an image of several characters. Here I have taken an image of group of several Barcelona Players. From that image messi has been identified and detected using template matching.

Template matching is a technique in computer vision used for finding a subimage of a target image which matches a template image. This technique is widely used in object detection fields such as surveillance, vehicle tracking, robotics, medical imaging, and manufacturing.

There are a variety of methods to perform template matching, but in this case I have used the correlation coefficient which is specified by the flag cv2.TM_CCOEFF.

So what exactly is the cv2.matchTemplate function doing? Essentially, this function takes a “sliding window” of messi's query image and slides it across the input image from left to right and top to bottom, one pixel at a time. Then, for each of these locations, it computes the correlation coefficient to determine how “good” or “bad” the match is.

Regions with sufficiently high correlation can be considered “matches” for the template of messi. From there, all I need is a call to cv2.minMaxLoc to find where my “good” matches are. That’s really all there is to template matching!

## Requires
   * Python
   * Numpy
   * OpenCV
   
## Input Image
![messi](https://user-images.githubusercontent.com/40036314/48658993-e1c7bb00-ea70-11e8-8b97-c9c8bdb5583f.jpg)

## Output
![screenshot from 2018-11-17 13-48-39](https://user-images.githubusercontent.com/40036314/48659000-f7d57b80-ea70-11e8-8ead-769ca45f6ee5.png)
