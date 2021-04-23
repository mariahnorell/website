---
title: Data Science with NVIDIA Rapids
subtitle: ''
date: 2016-04-20T00:00:00Z
summary: ''
draft: false
featured: false
authors:
  - admin
lastmod: 2020-12-13T00:00:00Z
tags:
  - Python
  - Data Science
  - NVIDIA
  - RAPIDS

categories:
  - Programming
  - Data Science

projects: []
image:
  caption: 'Image credit: [**NVIDIA**](https://www.nvidia.com/en-us/deep-learning-ai/software/rapids/Y)'
  focal_point: ""
  placement: 2
  preview_only: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.

---

## Conference Experience

This past week, I attended [NVIDIA's GTC](https://www.nvidia.com/en-us/gtc/) conference to deepen my understanding of machine learning and artificial intelligence. To me, the most rewarding part of the conference was the hands-on training session I attended. I heard about GTC through an organization I'm a member of called [Women in Data](https://www.womenindata.org/) where the mission is to "close the gender gap and increase diversity in data careers".

It was exciting to get my hands on a real-world project to elevate my skills in the [Fundamentals of Accelerated Data Science with RAPIDS](https://www.nvidia.com/content/dam/en-zz/Solutions/deep-learning/deep-learning-education/DLI-Workshop-Fundamentals-of-Accelerated-Data-Science-with-RAPIDS.pdf) workshop. Through a mixture of instructor-led and self-paced lab sections, I learned all about GPU-accelerated data manipulation, machine learning, and conducted an in-depth biodefense simulation analysis on population data.

## Learning RAPIDS

During the workshop I learned all about RAPIDS, which is a collection of data science libraries and APIs. Specifically, the libraries allow for end-to-end GPU acceleration for common, everyday data science workflows. One library I learned about was cuDF (which is almost identical to Pandas). In some of the labs, I was able to compare processing times from both cuDF and Pandas and was blown away with just how efficient the cuDF method was. For example, in one scenario I tested, there was over 60 million rows of data to process and while Pandas took about 30 seconds, cuDF only took 3 seconds. Seriously fast!



## Biodefense Simulation Project

The simulation was broken down into three scenarios. In scenario one I identified geographic clusters, calculated the spread for each cluster, and compared the density of infected vs. uninfected people. Next, I determined the number of individuals closest to each hospital and prepared road directions for ambulances to hospitals based on coordinates. Finally, I calculated the key factors associated with higher rates of infection and visualized all the results with dynamic graphs.

Tools Used:

* cuDF, cuPy, cuGraph, cuXfilter
* cuML (K-means, DBSCAN, logistic regression, k-nearest neighbors, XGBoost)

Additional Information:

* [RAPIDS Source Code](https://github.com/rapidsai)
* [Conda Packages](https://anaconda.org/rapidsai)

After successfully completing the simulation analysis, I passed the assessment and received a [certificate of competency](https://courses.nvidia.com/certificates/41e25296023f4f01ab2b42339591719c) from NVIDIA's Deep Learning Institute!