# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I gaussian blurred/cannyied to extract the edges in the image. After that, I developed my region of interest, which was a trapezoid and developed the hough transformation to find the most important lines.

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by splitting up lines based on the (-) or (+) slopes. Then, I continuously added up all the slopes and y-intercepts for each line with a counter. After, I averaged up the slopes and y-intercepts to get my final answer.

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when there are other edges in by field of interest that messes with my lines.

Another shortcoming could be the lines are a bit shaky and could lead to an uncomfortable ride.


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to test more edge cases.

Another potential improvement could be to continue to refine the area of interest.
