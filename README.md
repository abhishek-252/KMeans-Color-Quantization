# KMeans-Color-Quantization
K-means clustering is a simple unsupervised learning method. This method can be applied to implement color quantization in an image by finding clusters of pixel values. Another useful application would be automatic classification of phonemes in a speech signal by finding clusters of formant values for different speakers.

# Theory
Clustering algorithms in general are used to group similar data points together. Data points that are similar are assigned a value that represents the average value of all points in that cluster. If additional data points are collected, they can be compared to the average values of other clusters and assigned to the closest one. K-means is an iterative algorithm that implements clustering by starting with randomly assigned centroid locations as the center of each cluster. In each iteration, the data points closest to each centroid are determined and the total error is calculated by adding up the total distance from each point to its corresponding centroid. Then, the centroids are adjusted until they are representative of each cluster and total error is minimized.

# Color Quantization Application
In the field of image processing, a common problem is determining how to display a color image on a device that can only display a limited number of colors without sacrificing much image quality. Color image are typically stored as three parallel matrices where each matrix represents the red, green, and blue components of the image. Each component can range from 0 to 255 which means that 256^3 colors can be represented. Since the human eye can't distinguish nearly that many unique colors, it makes sense to choose a limited amount of colors to represent a color image.

Using k-means, combinations of colors can be quantized into a certain number of levels. This works well because the human eye can't perceive the full color spectrum. In the context of k-means, these quantized color levels would be the centroids. For each pixel, the closest centroid is determined by treating each pixel as a vector of <r,g,b> and using the distance formula to find the distance between the pixel and each centroid. The algorithm assigns each centroid a color value that represents the average of all the pixels that were closest to that centroid.

# The images below show the result of using k-means to quantize a color image :
