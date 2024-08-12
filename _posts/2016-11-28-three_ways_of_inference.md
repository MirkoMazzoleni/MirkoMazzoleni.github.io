---
layout: post
title: The three ways of statistical inference
subtitle:
date: 2016-11-28
author: Mirko Mazzoleni
categories: thoughts
tags:
thumbnail: /assets/img/posts/2016-11-28-three_ways_of_inference/three_ways.jpeg
---

I recently skipped through the course [*Improving your statistical inferences*](https://www.coursera.org/learn/statistical-inferences), held on the [Coursera](https://www.coursera.org/) MOOC platform. The lessons are taught by Daniel Lakens, associate professor at the department of Human-Technology Interaction, Eindhoven University of Technology.
 
I've found fascinating his comparison about the different conceptual frameworks of statistical inference that exist nowadays.
Considering the following yoga philosophies, the [three paths of realization](https://en.wikipedia.org/wiki/Three_Yogas) are:

+ The **Karma** yoga
+ The **Jnana** yoga
+ The **Bhakti** yoga

These disciplines entail different meanings. Respectively, they are known as:

+ The path of **Action**
+ The path of **Knowledge**
+ The path of **Devotion**

But what does this have in common with statistical inference? In day-by-day work, the researcher faces three fundamental questions:

+ What should I **do**?
+ What’s the **relative evidence**?
+ What should I **believe**?

The Path of Action gives us a guideline to act. It searches for rules to govern our behavior such that, in
the long run, we will not be wrong too often. This is the hypothesis testing framework. The well known problem with NHST (Null Hypothesis Significance Testing) is that a rule to govern our behavior in the long run, tells us nothing about the current test.

The Path of Knowledge is based on actually observed data (which is what matters isn't it?). Standing on the concept of Likelihoods, the aim here is to compare the likelihood of different hypothesis via the likelihood ratio, given the data (and the chosen model). A discussion on the likelihood approach to inference can be found in the textbook [Statistical Evidence: A Likelihood Paradigm](https://www.amazon.com/Statistical-Evidence-Likelihood-Monographs-Probability/dp/0412044110/ref=sr_1_1?s=books&ie=UTF8&qid=1480364103&sr=1-1&keywords=Statistical+Evidence%3A+A+Likelihood+Paradigm) by Richard Royall (1997).

We arrived, finally, to the last way: the Path of Devotion. Here, personal experience, intuition and previous knowledge can be leveraged to assess the evidence degrees of belief. Based on likelihoods, it lets us to incorporate prior information on our computations. Bayes factors, the relative evidence for one model to another, is used to compare the different hypothesis. Bayesian inference can be obviously used to perform parameter estimation, specifying in the same way a prior distribution on possible parameters values. The book [Doing Bayesian Data Analysis](https://www.amazon.com/Doing-Bayesian-Data-Analysis-Second/dp/0124058884/ref=sr_1_1?ie=UTF8&qid=1480365777&sr=8-1&keywords=doing+bayesian+data+analysis), by John Kruschke (2014), is an excellent practical guide to get started with modern Bayesian procedures.

Concluding, statistical inference frameworks can be thought in light of the three yoga paths:

+ The path of **Action**: Neyman-Pearson
+ The path of **Knowledge**: Likelihoods
+ The path of **Devotion**: Bayesian statistics

The presented material is borrowed from the course taught by Daniel Lakens. Definitely a must follow course, full of inspiring insights as the presented ones.
