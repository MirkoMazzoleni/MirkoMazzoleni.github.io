---
layout: research
title: "Visualizing Classification Results: Confusion Star and Confusion Gear"
date: 2021-12-22
author: Mirko Mazzoleni
category: Journal
tags: [MachineLearning, Visualization]
comments: true
authors: "A. Luque, M. Mazzoleni, A. Carrasco and A. Ferramosca"       
post-card-type: research
card-image: ../images/2021-12-22-IEEE_ACCESS_confusion_gears/confusion_gear.png
---

### Abstract
Recent developments in machine learning applications are deeply concerned with the poor interpretability of most of these techniques. To gain some insights in the process of designing data-based models it is common to graphically represent the algorithm’s results, either in their final or intermediate stage. Specially challenging is the task of plotting multiclass classification results as they involve categorical variables (classes) rather than numeric results. Using the well-known MNIST dataset and a simple neural network as an example, this paper reviews the existing techniques to visualize classification results, from those centered on a particular instance or set of instances, to those representing an overall performance metric. As classification results are commonly summarized in the form of a confusion matrix, special attention is paid to its graphical representation. From this analysis, a new visualization tool is derived, which is presented in two forms: confusion star and confusion gear. The confusion star is centered on the classification errors, while the confusion gear focuses on the classification hits. The proposed visualization tools are also evaluated when facing: (i) balanced and imbalanced classifiers issues; (ii) the problem of representing errors with different orders of magnitude. By using shapes instead of colors to represent the value of each matrix cell, the new tools significantly improve the readability of the confusion matrices. Furthermore, we show how the area enclosed by the confusion stars and gears are directly related to standard classification metrics. The new graphic tools can be also usefully employed to visualize the performances of a sequence of classifiers.
[<strong>[Paper](https://ieeexplore.ieee.org/document/9658486)</strong>, <strong>[Code](https://github.com/amalialuque/confusionstar)</strong>]

#### Reference
<blockquote>
A. Luque, M. Mazzoleni, A. Carrasco and A. Ferramosca, "Visualizing Classification Results: Confusion Star and Confusion Gear," in IEEE Access,  <a href="https://doi.org/10.1109/ACCESS.2021.3137630"> doi: 10.1109/ACCESS.2021.3137630 </a>, 2021.
</blockquote>


#### Bibtex
```
@ARTICLE{9658486,  
author={Luque, Amalia and Mazzoleni, Mirko and Carrasco, Alejandro and Ferramosca, Antonio},  
journal={IEEE Access},   
title={Visualizing Classification Results: Confusion Star and Confusion Gear},   
year={2021},  
volume={},  
number={},  
pages={1-1},  
doi={10.1109/ACCESS.2021.3137630}
}
```
