---
layout: page
title: K-MPFH
description: Efficient Point Feature Histogram via K-Means Filtering
img: assets/img/project_PFH_KMEANS_curvature_selection.png
importance: 1
category: course
---

It is a course project for EECS498-001 at Umich.
The detailed report of this project can be found [here](https://drive.google.com/file/d/1L_rue4NSZ71iahpAwQPX-7jez5Xfr-6m/view?usp=sharing). 

Registration is known as one topic of point cloud processing which deals with the prob-
lem of consistently aligning multiple 3D point cloud data views into a complete model[1]. It
aims to find the relative poses among independently acquired views under a global coordi-
nate framework. As the relative positions and orientations are obtained, the intersecting areas
can be firmly overlapped, which is quite useful in 3D object detection, 3D model construction,
Augmented Reality, and many other 3D vision related areas. The Iterative Closest Point (ICP)
algorithm is one of the most popular methods for 3D object registration, which is designed to
find the correspondence between two datasets of points, and solve out the optimal transfor-
mation by minimizing the distance between fitted point cloud and target point cloud[2]. ICP
assumes that the correspondence of each point is given.

However, it is rarely true to have complete point-to-point correspondence in real life sit-
uations. For example. in the case of the registration of partially overlapping and unorganised
point clouds without good initial alignment, these methods are not appropriate enough since
it becomes difficult to find the correspondence. This leads to various approaches to obtain cor-
respondence by extracting features from datasets. [3] focuses on tradeoff between the error in
feature values due to noise against the error in positions due to misalignment; [4] considers
color information as well as 3D information in registration; [5] utilizes the change of geometric
curvature and approximate normal vector of the surface formed by a point and its neighbour
to predict the correspondence. In this paper, we would like to implement the registration based
on the Point Feature Histogram (PFH) algorithm, which focuses on estimating a rigid transfor-
mation that approximately registers the input datasets[1]. PFH provides a good start for ICP
algorithm, and has good performance with noisy data.

PFH is motivated by finding correct point-to-point correspondences in real-world noisy
data scans, and computing rigid transformations that roughly align them using geometric con-
straints, while its time complexity is inevitably high. To boost the efficiency as well as guarantee
the high performance, we designed K-Means PFH(K-MPFH) which applies K-Means clustering
method to first filter useless points. In the following we will first describe the details of imple-
mentation of PFH, and then explain our unique extensions on PFH, and finally the experiments
and benchmark of our model.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/project_PFH_KMEANS_experiment_results.png" title="Results of experiments" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
