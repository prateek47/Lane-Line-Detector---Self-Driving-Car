## **Finding Lane Lines on the Road** 

### Reflection

#### Currently My pipelines consist of:

* I converted the images to grayscale.
* Apply gaussian Noise kernel for smoothing between different layers
* Keep only the region of interest, which is defined by the polygon I had created(in the center)
* Run the Hough line detector
 * Hough line is used to detect straight lines, we filer these lines by slope and endpoint location, and separate them into right/left lane line segments. Then run linear regression to create right/left lane line equations. From these equations, draw right/left lane lines on the image: draw_lines().
 * Tuned the parameters for the Canny Edge Detector and Hough Line Detector specifically to fit this problem. I used the parameters in the quiz solution to start with and then improved on it.
* Lay out the Hough lines images on the color images and then draw lines on the edge images.

#### Potential shortcomings:

* The algorithm is likely to overfit the data, as the data consist on only clear images, but the algorithm may fail during night time or bad weather, such as rain or snow.
* Even with sharper turn, the algorithm might not be able to detect the entire lane to the entire stretch of the road the camera can see because the algorithm is trying to extrapolate straight lane lines.

#### Possible improvements: 

* Firstly, I would add images with different weather situations and day times, such as evening, night etc
* Secondly, the data should consist of more cars, that might and might not be cutting the lanes, which would help us figure out weather other objects in the picture effect detection and extrapolation and make it more robust.
* Test the algorithm, on different road types, such as highways, residential roads, etc.

