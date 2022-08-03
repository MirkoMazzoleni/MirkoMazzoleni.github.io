---
layout: research
title: "An agent-based model to assess large-scale COVID-19 vaccination campaigns for the Italian territory: The case study of Lombardy region"
date: 2022-07-15
author: Mirko Mazzoleni
category: Journal
tags: [SysID, COVID]
comments: true
authors: "A. Cattaneo, A. Vitali, M. Mazzoleni, F. Previdi"       
post-card-type: research
card-image: ../images/2022-07-15-CMPB_Covasim/covasim.png
---

### Abstract
*Background*
In Italy, the administration of COVID-19 vaccines began in late 2020. In the early stages, the number of available doses was limited. To maximize the effectiveness of the vaccine campaign, the national health agency assigned priority access to at-risk individuals, such as health care workers and the elderly. Current vaccination campaign strategies do not take full advantage of the latest mathematical models, which capture many subtle nuances, allowing different territorial situations to be analyzed aiming to make context-specific decisions.
*Objectives*
The main objective is the definition of an agent-based model using open data and scientific literature to assess and optimize the impact of vaccine campaigns for an Italian region. Specifically, the aim is twofold: (i) estimate the reduction in the number of infections and deaths attributable to vaccines, and (ii) assess the performances of alternative vaccine allocation strategies.
*Methods*
The COVID-19 Agent-based simulator Covasim has been employed to build an agent-based model by considering the Lombardy region as case study. The model has been tailored by leveraging open data and knowledge from the scientific literature. Dynamic mobility restrictions and the presence of Variant of Concern have been explicitly represented. Free parameters have been calibrated using the grid search methodology.
*Results*
The model mimics the COVID-19 wave that hit Lombardy from September 2020 to April 2021. It suggests that 168,492 cumulative infections 2,990 cumulative deaths have been avoided due to the vaccination campaign in Lombardy from January 1 to April 30, 2021. Without vaccines, the number of deaths would have been 66% greater in the 80–89 age group and 114% greater for those over 90. The best vaccine allocation strategy depends on the goal. To minimize infections, the best policy is related to dose availability. If at least 1/3 of the population can be covered in 4 months, targeting at-risk individuals and the elderly first is recommended; otherwise, the youngest people should be vaccinated first. To minimize overall deaths, priority is best given to at-risk groups and the elderly in all scenarios.
*Conclusions*
This work proposes a methodological approach that leverages open data and scientific literature to build a model of COVID-19 capable of assessing and optimizing the impact of vaccine campaigns. This methodology can help national institutions to design regional mathematical models that can support pandemic-related decision-making processes.
[<strong>[Paper](https://www.sciencedirect.com/science/article/pii/S0169260722004114)</strong>, <strong>[Code]</strong>]

#### Reference
<blockquote>
A. Cattaneo, A. Vitali, M. Mazzoleni, F. Previdi, "An agent-based model to assess large-scale COVID-19 vaccination
campaigns for the Italian territory: The case study of Lombardy region," in Computer Methods and Programs in Biomedicine,  <a href="https://doi.org/10.1016/j.cmpb.2022.107029"> doi: 10.1016/j.cmpb.2022.107029 </a>, 2022.
</blockquote>


#### Bibtex
```
@article{CATTANEO2022107029,
title = {An agent-based model to assess large-scale COVID-19 vaccination campaigns for the Italian territory: The case study of Lombardy region},
journal = {Computer Methods and Programs in Biomedicine},
volume = {224},
pages = {107029},
year = {2022},
issn = {0169-2607},
doi = {10.1016/j.cmpb.2022.107029},
author = {Andrea Cattaneo and Andrea Vitali and Mirko Mazzoleni and Fabio Previdi},
}
```
