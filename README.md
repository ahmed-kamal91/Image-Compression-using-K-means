# Image-Compression-using-K-means
compress image to 16 colors based on Scratched K-means Clustering. 

## why K-mens clustering:
 group unlabeled data into clusters for some business purpose ? </br>

## How k means clustering work:

assume:
we have data has 2 features x1, x2 , represented in x and y axis. </br>
and need to group these points into 3 clusters, so we: </br></br>

![gif](https://user-images.githubusercontent.com/91970695/218606427-873ac7a9-ffb1-4cce-b36a-ca02ffb2cece.gif)

* randomly taking 3 points values for initialize centroid for each cluster we want to make.</br>
* repeat </br>
    { </br>
    * Assign each data point to cluster based on the closest centroid.</br>
    * Compute means for each cluster and update centroids.</br>
}</br>



