# **Finding Lane Lines on the Road** 

## Writeup

[//]: # (Image References)

[image0]: ./test_images/solidWhiteCurve.jpg "Input image"
[image1]: ./test_images_output/gray_solidWhiteCurve.jpg "Grayscale"
[image2]: ./test_images_output/blur_solidWhiteCurve.jpg "Blurred grayscale"
[image3]: ./test_images_output/edge_solidWhiteCurve.jpg "Edge detection"
[image4]: ./test_images_output/roi_solidWhiteCurve.jpg "Masked edge detection"
[image5]: ./test_images_output/hough_solidWhiteCurve.jpg "Hough Lines"
[image6]: ./test_images_output/solidWhiteCurve.jpg "Result"

---

### 1. Pipeline

My pipeline consisted of 5 steps and is visualized step by step by the "solidWhiteCurve.jpg" example.
First, the image is read to obtain an input which can be seen here.

[image0]

Second, the image is converted into a grayscale image.

[image1]

Third, the grayscale image is blurred by a gaussian filter for smoothing.

[image2]

Next, the blurred image is used within an edge detection step to find all edges within the picture.

[image3]

This turns out to be a binary image where the edges are shown in white and all areas without edge information in black.
Then, a region of interest is defined and used as mask to only consider the edges from the lower triangle of the image. This step is useful to filter out all other edges that are not occuring from the street.

[image4]

A hough transformation is applied to detect only lines from all leftover edges.

[image5]

Finally, all lines are separated into falling and rising lines by calculating their slopes. The end points of all rising/falling lines are store in separate arrays. Each of this arrays is used by numpy's polyfit function with degree 1 to perform a linear regression. As a result two final lines are calculated which are visualized red on the input image for comparison.

[image6]

### 2. Potential shortcomings


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
