## Goal of Notebook:
 image compression to 16 colors using k-means clustering
 https://github.com/ahmed-kamal91/Image-Compression-using-K-means/blob/main/K-means%20Clustering%20Application%20Notebook.ipynb

![Untitled](https://user-images.githubusercontent.com/91970695/218614558-57cef9d3-5439-4667-b6ee-01ceb8e82087.png)

## What K-mens clustering  ?:
Simply,algorithm group unlabeled data into clusters for some business purpose ? </br>

## How k means clustering work:

assume:
we have data has 2 features x1, x2 , represented in x and y axis. </br>
and need to group these points into 3 clusters, so we: </br>


<img width="350" alt="" src="https://user-images.githubusercontent.com/91970695/218611026-2fd1f16e-b117-427a-a578-01d815c90f33.png">

* randomly taking 3 points values for initialize centroid for each cluster we want to make.</br>
* repeat </br>
    { </br>
    * Assign each data point to cluster based on the closest centroid.</br>
    * Compute means for each cluster and update centroids.</br>
}</br>

<img width="600" alt="figure 2" src="https://user-images.githubusercontent.com/91970695/218606738-aeba0b7b-8aeb-4637-8af1-1a36dd20bd18.png">

## Assign data to clusters using the closest distance between cetroids:

<pre>
   AssignedClusters = np.zeros(res_image.shape[0], dtype=int)  
   for i in range(res_image.shape[0]):
       Distances = []
       for j in range(K):
           distance = np.linalg.norm(res_image[i] - centroids[j])
           Distances.append(distance)
       AssignedClusters[i] = np.argmin(Distances)
</pre>

![ezgif-3-0fa2173e4e](https://user-images.githubusercontent.com/91970695/218728256-09a9e18c-c8e7-4a66-907c-a43537bc1d35.gif)

