---
layout: post
title: KMeansCustom – a K Means Algorithm Implementation
image: /img/1062px-K_Means_Example_Step_1.svg.png
---

KMeansCustom is my own creation of the K Means Clustering Algorithm.  If [SKLearn](https://scikit-learn.org/stable/modules/generated/sklearn.cluster.KMeans.html) gets a 9 for their version, KMeansCustom gets about a 2.  So you probably won’t want to actually use KMeansCustom.  However, creating algorithms is a great way to learn about algorithms and improve your coding skills.  So if you aren’t sure if you prefer math or programming creating data science algorithms is a great way to kill two birds with one stone; you learn to program, and get a real understanding of what the data science products do under the hood.
In this post I’ll explain a bit about how a k means clustering algorithm works, and provide some instructions in the event that you really want to use my creation.

#### What does a k means algorithm do?

It’s actually not all that complicated when it comes down to it.  To start the algorithm randomly assigns however many centroids you have requested.  Those centroids are any random points between the min and max points in the data set.  Once those points are assigned the algorithm will calculate the Euclidean distance from each data point to the centroids.  Now each data point will be assigned a centroid group based on which one they are closest to.  Then we take the average location of all of the data points in each centroid group and move the centroid to the average location. When the centroids are moved we then repeat the italicized portion at least once, but up to the max number of iterations selected. The algorithm loops through the italicized portion until either no data points move for an iteration or it reaches the maximum number of iterations.  

### A little bit about KMeansCustom for the data scientists that are curious:

Class KMeansCustom(k=3, max_iterations=500)

# Parameters:
* K: int, default=3
  - This is the number of clusters to form and the number of centroids to generate.
* Max_iterations=500
  - This is the maximum number of iterations you would like the algorithm to loop through.  Keep in mind the algorithm will automatically end as soon as two iterations repeat the same cluster groups.

# Attributes:
* Fit: intakes a Panda’s data frame (data)
  - This will return a dictionary list of the centroids, as well as the clusters.  These out uts will be save as self.centroids for the centroids and self.closeRoids for the clusters.  
* Pred: intakes values to see what cluster a new data point would belong to(x,y)
  - The output will let you know what cluster the new data point would belong to.  

This class will only work with 2-dimensional data sets.  As it was a learning experience, and I was pressed for time, it’s not the greatest tool for use, but it was a great tool for learning.

[Here is the Github repo!](https://github.com/CJRicciardi/CS-Build-1)
