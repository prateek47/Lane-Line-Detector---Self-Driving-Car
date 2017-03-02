**Finding Lane Lines on the Road** 

### Reflection

#### Currently My pipelines consist of:

* I converted the images to grayscale.
* Apply gaussian Noise kernel for smoothing between different layers
* Keep only the region of interest, which is defined by the polygon I had created(in the center)
* Run the Hough line detector
* 

Keep only yellow and white pixels, black out all other pixels: filter_colors()

Filter Hough lines by slope and endpoint location, and separate them into candidate right/left lane line segments. Then run linear regression on candidate right/left lane line segment endpoints, to create right/left lane line equations. From these equations, draw right/left lane lines on the image: draw_lines()
I tuned the parameters for the Canny Edge Detector and Hough Line Detector specifically to fit this problem. As a starting point, I used the parameters presented in the quiz solution of the Hough Transform lecture.
Potential shortcomings
The algorithm I created is likely overfitted to the data available in this project. For example, the algorithm may fail during night time. Or, it may fail in bad weather, such as rain or snow. Even during sunny days, if the road curves more sharply, my algorithm may also fail, because I am trying to extrapolate straight lane lines.
Possible improvements
To start, I would test my algorithm on highway roads, but with different weather conditions, such as night time, rain, snow, etc. I would also test my algorithm when there is heavy traffic on the highway. Then, I would see how/if the algorithm fails in those situations. From there, I can figure out ways to improve the algorithm to make it more robust.
Further, I would test my algorithm on different road types, i.e. roads that are not highways. Examples would be country roads or urban roads.



###2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


###3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
