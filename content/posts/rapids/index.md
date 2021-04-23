---
title: Data Science with NVIDIA Rapids
subtitle: Learning
date: 2016-04-20T00:00:00Z
summary: ''
draft: false
featured: false
authors:
  - admin
lastmod: 2020-12-13T00:00:00Z
tags:
  - Academic
  - Python
  - Data Science
  - NVIDIA
  - Pandas
  - NumPy
  - cuDF
  - cuML

categories:
  - Programming
  - Data Science
projects: []
image:
  caption: ""
  focal_point: ""
  placement: 2
  preview_only: false
---

## GTC

This past week, I attended [NVIDIA's GTC](https://www.nvidia.com/en-us/gtc/) conference to deepen my understanding of machine learning and artificial intelligence. I heard about GTC and was able to attend through an organization I'm a member of called [Women in Data](https://www.womenindata.org/) where the mission is to "close the gender gap and increase diversity in data careers".

To me, the most rewarding part of the conference was the hands-on training session I attended called the [Fundamentals of Accelerated Data Science with RAPIDS](https://www.nvidia.com/content/dam/en-zz/Solutions/deep-learning/deep-learning-education/DLI-Workshop-Fundamentals-of-Accelerated-Data-Science-with-RAPIDS.pdf). As a data scientist who is relatively new to the machine learning space, I was excited to get my hands on a real-world project that could help me elevate my skills. Through a mixture of instructor-led and self-paced sections, I learned all about GPU-Accelerated Data Manipulation, Machine Learning, and put it all together by conducting an in-depth analysis on population data to help stave off a simulated epidemic in the UK.

## RAPIDS

During the training session, I got to learn all about RAPIDS, which is a collection of data science libraries. Specifically, they allow for end-to-end GPU acceleration for common data science workflows. There were some labs we completed durign the trainings that showed a side-by-side comparison on Pandas and cuDF (the equivalent) run times and I was blown away by the processing time.

## Biodefense Simulation Project

Data: Multiple weeks of data (roads, hospitals, infection rates from population) of virulent epidemic
Scope: Learned core tools to use RAPIDS for everyday data science tasks & scalability methods from workstations and clusters to cloud and HPC

Tasks:

* Calculated measures of geographic spread for each cluster of infected persons
* Compared density of infected vs. uninfected people in each cluster region
* Determined number of individuals closest to each hospital in country
* Prepared road directions for ambulances to hospitals based on coordinates
* Completed logistic regression and decision tree analysis of data to understand magnitude of factors relative impact on risk
* Visualized results with dynamic graphs

Tools Used:

* cuDF, cuGraph, cuXfilter
* cuML (K-means, DBSCAN, logistic regression, k-nearest neighbors, XGBoost)
