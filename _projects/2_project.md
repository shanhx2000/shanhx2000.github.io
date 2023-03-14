---
layout: page
title: Theta-Flows
description: Parameterized Trajectory Generation with Normalized Flows
img: assets/img/project_ThetaFlow_result0.png
importance: 1
category: research
---

This is a research project done at Umich ARM lab, instructed by Thomas Power and Prof. Dmitry Berenson. 
Thomas Power contributes the framework of the trajectory generation and teaches a lot about the normalizing flows. 
The detailed report of this project can be found [here](https://drive.google.com/file/d/1ca3pYTYiuBVYjmdLyDpjJT9y2f2jh-N4/view?usp=sharing). 

Sampling-based methods are helpful in some trajectory
generation due to its advantage in parallelable computing.
The normalizing flows can be used given its ability of effi-
ciently sampling and exactly evaluating. During some usages
of the trajectory generation methods, they requires a switch
in strategies when sampling. This project aims to extend a
current flows design for trajectory generation to allow for the
changing sampling strategy. A parameterized normalizing flows,
which we named theta-flows, and its training procedures are
proposed. The idea of theta-flows is tested with a miniature
implementation over simple distributions and is also tested with
the trajectory generation context. In general, the results indicate
the method is feasible.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/project_ThetaFlow_structure.png" title="ThetaFlow_structure" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/project_ThetaFlow_training.png" title="ThetaFlow_training" class="img-fluid rounded z-depth-1" %}
    </div>
</div>


To sum up, the theta-flows for trajectory generation can
be used to provide different generation strategies in working.
The results showcased step by step that the implementation
is correct and workable. Although the result for the span
control is not ideal, the feasibility of theta-flows is still
verified with the velocity control. As shown in the Discussion
section, some defects of the theta-flows when handling more
cost functions are stilled remain to be explored. Overall, the
expectation of this project is fulfilled while having some
space to elevate.