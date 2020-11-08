# sift-based-opencv-object-detection

We have a astronomical space main image that every part of image is similar to each other and our goal is detect given subimage of this main image.

Requirement modules:
OpenCV (v3.3.1)
OpenCV-contrib (v3.3.1)
Matplotlib

Note: OpenCV version should be under v3.4 because SIFT can not be used above v3.4

We have 3 images thich named 'a', 'b' and 'c'. 'a' image is widescale space image, 'b' is one cropped part of 'a' and 'c' is cropped, rotated and scaled part of 'a'.

Our approach is extracting features from images and matching image pairs by keypoints.
I've used ORB before SIFT but keypoints was significantly useless. I tried to increase number of found keypoints but nothing changed. Then I downgraded OpenCV and used SIFT.

We have used brute force knn matcher to match keypoints by descriptions.

