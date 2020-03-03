# Finger-Detection-and-Counting-using-OpenCV
A system which detects a human hand, segments the hand, counts the number of fingers being held up and displays the finger count, from a live video input.  

Programming Language: Python Library: OpenCV​

Libraries to install:

pip install opencv-python


pip install numpy


pip install -U scikit-learn

Explanation:

- Begin by creating a region of interest in a live video frame, where the hand is to be inserted for counting.

- Once the hand is detected, it is isolated by applying thresholding techniques, Binary Thresholding in this case using opencv.

- To the thresholded hand segment, a polygon is drawn around the hand to identify the extreme points, using Convex Hull technique.

- Using the intersection of the extreme points in the polygon (Top, Bottom, Left, Right), the center of the hand is calculated. 

- The point furthest away from the center of the hand is identified and a ratio of that distance say 80% is used as the radius for a circle, which is drawn around the center of the hand (For visualization purposes, we may think of this as the palm region). 

- Any points outside the circle and far away from the bottom are concluded to be the extended fingers.

- Return the total count of these identified points.




![](Images/Finger_Detection.png)




You can view the video here !


"https://www.youtube.com/embed/5LWbOa1za4U" 
