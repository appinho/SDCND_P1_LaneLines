# **Finding Lane Lines on the Road** 

## Writeup

[//]: # (Image References)

[image1]: ./test_images_output/gray_solidWhiteCurve.jpg "Grayscale"
[image2]: ./test_images_output/blur_solidWhiteCurve.jpg "Blurred grayscale"
[image3]: ./test_images_output/edge_solidWhiteCurve.jpg "Edge detection"
[image4]: ./test_images_output/roi_solidWhiteCurve.jpg "Masked edge detection"
[image5]: ./test_images_output/hough_solidWhiteCurve.jpg "Hough Lines"
[image6]: ./test_images_output/solidWhiteCurve.jpg "Result"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps and is visualized step by step with the "solidWhiteCurve.jpg" example.
First, I read the image to obtain an input which can be seen here.

![Screenshot]([image1])


from the test_image folder. converted the test images to grayscale, then I .... 

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by ...

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
