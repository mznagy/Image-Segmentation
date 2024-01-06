# Problem Statement
We intend to perform image segmentation. Image segmentation means that we can group
similar pixels together and give these grouped pixels the same label. The grouping
problem is a clustering problem. We want to study the use of K-means on the Berkeley
Segmentation Benchmark. Below we will show the needed steps to achieve the goal of
the assignment.
## 1. Download the dataset and understand the format
a. We will use Berkeley Segmentation Benchmark
b. The data is available at the following link.
http://www.eecs.berkeley.edu/Research/Projects/CS/vision/grouping/BSR/BSR_bs
ds500.tgz.
c. The dataset has 500 images. The test set is 200 images only. We will report our
results on the first 50 images of the test set only.

## 2. Visualize the image and the ground truth segmentation
a. Write your own function that reads an image and display an image with its
associated ground truth segmentation(s).
## 3. Segmentation using K-means(your implementation)
Every image pixel is a feature vector of 3-dimension {R,G,B}. We will use this feature
representation to do the segmentation.
a. We will change the K of the K-means algorithm between {3,5,7,9,11} clusters. You
will produce different segmentations and save them as colored images. Every color
represents a certain group (cluster) of pixels.
b. We will evaluate the result segmentation using F-measure, Conditional Entropy.
for image I with M available ground-truth segmentations. For a clustering of
K-clusters you will report your measures M times and the average of the M trials
as well. Report average per dataset as well.
c. Display good results and bad results for every configuration in a,b. Discuss
## 4. Big Picture
a. Select a set of five images and display their corresponding ground truth against
your segmentation results using K-means at K=5. Comment on the results.
b. Select the same five images and display their corresponding ground truth against
your segmentation results using Normalized-cut for the 5-NN graph, at K=5.
Comment on the results.
c. Select the same five images and contrast your segmentation results using
Normalized-cut for the 5-NN graph, at K=5 versus using K-means at K=5.
Comment on the results.
## 5. Extra
a. In the previous parts, we used the color features RGB. We didn’t encode
the layout of the pixels. We want to modify that for K-means clustering to
encode the spatial layout of the pixels
i. Suggest a way to modify the feature vector to include spatial
layout.
ii. Contrast the results you obtained in 4.a to the results you obtained
by considering the spatial layout.
