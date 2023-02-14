## Goal of Notebook:
 image compression to 16 colors using k-means clustering </br>
 https://github.com/ahmed-kamal91/Image-Compression-using-K-means/blob/main/K-means%20Clustering%20Application%20Notebook.ipynb

<img width="550" alt="" src="https://user-images.githubusercontent.com/91970695/218614558-57cef9d3-5439-4667-b6ee-01ceb8e82087.png">

## What K-means clustering?
Simply,algorithm group unlabeled data into clusters for some business purpose </br>

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


## convert image to suitable input:
<pre>
m, n, _ = image.shape
res_image = image / 255
res_image = image.reshape(m * n , 3)
</pre>

![intro](https://user-images.githubusercontent.com/91970695/218751414-6e10882b-8bfd-4e2f-890c-905eb5873c20.png)


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

![dsddsd](https://user-images.githubusercontent.com/91970695/218744923-b9371dbf-6366-4ffa-937b-105dda0ce9b3.gif)

## update centriod :

![hole size](https://user-images.githubusercontent.com/91970695/218781489-476126c6-b568-489d-b0c6-b9165e4c4e17.gif)

