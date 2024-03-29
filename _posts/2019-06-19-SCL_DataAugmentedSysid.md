---
layout: research
title: "Nonlinear system identification via data augmentation"
date: 2019-06-19
author: Mirko Mazzoleni
category: Journal
tags: [Semisupervised, SysID, DataAugmentation, KernelMethods]
comments: true
authors: "S. Formentin, M. Mazzoleni, M. Scandella, F. Previdi"       
post-card-type: research
card-image: ../images/2019-06-19-SCL_DataAugmentedSysid/dynamic_connections.png
---


### Abstract
This paper presents a novel nonparametric approach to the identification of nonlinear dynamical systems. The proposed methodology exploits the potential of manifold learning on an artificially augmented dataset, obtained without running new experiments on the plant. The additional data are employed for approximating the manifold where input regressors lie. The knowledge of the manifold acts as a prior information on the system, that induces a proper regularization term on the identification cost. The new regularization term, as opposite to the standard Tikhonov one, enforces local smoothness of the function along the manifold. A graph-based algorithm tailored to dynamical systems is proposed to generate the augmented dataset. The hyperparameters of the method, along with the order of the system, are estimated from the available data. Numerical results on a benchmark Nonlinear Finite Impulse Response (NFIR) system show that the proposed approach may outperform the state of the art nonparametric methods.
 [<strong>[Paper]()</strong>,
<strong>[ScienceDirect](https://www.sciencedirect.com/science/article/pii/S0167691119300532)</strong>,
<strong>Code</strong>]



#### Reference
<blockquote>
	S. Formentin, M. Mazzoleni, M. Scandella and F. Previdi, "Nonlinear system identification via data augmentation", <strong>Systems & Control Letters</strong>, 2019. <a href="https://doi.org/10.1016/j.sysconle.2019.04.004">, doi: 10.1016/j.sysconle.2019.04.004 </a>, ISSN: 0167-6911, pp. 56-63.
</blockquote>

#### Bibtex
```
@article{FORMENTIN201956,
title = "Nonlinear system identification via data augmentation",
journal = "Systems & Control Letters",
volume = "128",
pages = "56 - 63",
year = "2019",
issn = "0167-6911",
doi = "https://doi.org/10.1016/j.sysconle.2019.04.004",
url = "http://www.sciencedirect.com/science/article/pii/S0167691119300532",
author = "Simone Formentin and Mirko Mazzoleni and Matteo Scandella and Fabio Previdi",
keywords = "System identification, Semi-supervised learning"
}
```
