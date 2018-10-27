# Historical Storm Data Analysis with HBase :hand: fa18-523-57, fa18-523-58

Divya Rajendran, Pramod Duvvuri

October 13, 2018

---

Keywords: E534, Data Visualization, Big Data Technologies, HBase, Python

---

## Abstract

The decisions people make these days are all data driven. The amount of data we collect has increased exponentially and this makes it harder to visualize and understand. We can overcome this hurdle by sampling or visualizing subsets of the data. The only thing one should remember is to pick a good sample of the data or to repeat the process of sampling and visualizing the data subset. In this project, we aim to visualize the historical storm dataset and make inferences from our visualizations.


## Introduction

With the disastrous effects of the increasing number of storms all around the world, we thought of taking storm dataset for entire Asia Pacific region and visually analyze the effects of various variables on the storms. We want to check any patterns in the storm data and visualize them geographically so that it might help us to make useful inferences on the storm data. We have identified a data set on data.world[@fa18-523-57-DataSet] and we aim to identify the various correlations among the attributes and understand if they can help explain the change in frequency of the storms. Data World is a community where we find open datasets from various organizations containing varying data attributes according to the need. The data is saved in a graph database HBase. The output of our visualization is shown on jupyter notebook.


## Implementation

### Data set

The data set for the various storms in Asia Pacific region for the years between 1956 and 2017. We would choose an initial subset of data to visualize locally and then implement the same visualizations on the entire data. The data set contains attributes like region, latitude, longitude, storm number, name, date and time, speed, pressure, category type.

### Related Work

We have identified an earlier work on tropical storm data using R by Stoltzman consulting LLC and are planning to use it as a base to visualize our data using Python[@fa18-523-57-related-work].

### Visualization

1. Category of storms in different latitude and longitude is visualized to identify the variation in category of storms in those location.
2. Category of storms in different regions is visualized to check the correlation between them.
3. Correlation between Speed, pressure and category type is identified by visually analyzing them.
4. Correlation between latitude, longitude and speed, pressure is to be explored.
5. Concentration of storms in different regions should be visually explored.

## Technologies To Be Used

1. Python is an object-oriented programming language we plan to use in this project [@fa18-523-57-Python]

2. Apache HBase is a graph database which runs onHadoop HDFS, we plan to utilize this database to save our huge data and work on [@fa18-523-57-Apache_HBase].

3. Matplotlib is a 2D visualization library containing plotly which gives us publication ready images and we aim to utilize for identifying correlation between various attributes [@fa18-523-57-matplotlib].

4. Seaborn is a visualization tool based on Matplotlib used to draw attractive statistical plots and we aim to show the change in number of storms per year [@fa18-523-57-Seaborn].

5. Altair is a statistically aimed visualization library which produces output plots which are easily shown on a website [@fa18-523-57-Altair].

6. D3.js is a visualization library based on Javascript which is vastlyy implemented per SVG and HTML formats [@fa18-523-57-D3js].

## Visualization Samples

### Visualization 1

Image here

<!---  ![Basic_Plot](images/Basic_Plot.png) -->

### Visualization 2

Image here

<!---  ![Category_wise_Storms](images/Storms_per_category_plot.png) -->

### Visualization 3

Image here

<!---  ![Heat_Map_of_storm_concentration](images/Heat_map_plot.png) -->

### Visualization 4

Image here

<!--- ![Correlation_between_attributes](images/relationship_plot.png) -->

### Visualization 5

Image here

<!--- ![Geographic](images/Geographic_Plot.png) -->

## Summary

This section will contain the inference and conclusions we draw after visualizing the dataset used in this project

## Future Work

In this project, our main aim was to visualize the dataset. After visualizing and making inferences, we would like to propose a model that uses machine learning pattern in our data. We hope to use unsupervised machine learning algorithms to find clusters in our data. This might help us identify further patterns in the data that could not have been possible with just plain visualization of the data. The main problem that we have identified in building such a model is the availability of resources required to run the algorithm without any interruption. Using a local computer resources for running such a model would not be feasible. Hence, we hope to deploy such a model in the cloud and utilize its power and resources for machine learning.

## Acknowledgements

The authors would like to thank Dr. Gregor von Laszewski for giving the opportunity to work on this project and for providing valuable feedback during the duration of our project. The authors would also like to thank the associate instructors of this class for their help and prompt responses to our questions on Piazza.

## Bibliography

## Work Breakdown

The authors Divya Rajendran and Pramod Duvvuri have contributed equally in preparing this draft. We shall co-ordinate to equally divide the work that is required to complete the project and the final report before the deadline in December, 2018. Our contributions towards the completion of the project shall be updated in our respective notebook markdown files in our respective git repositories and a summary of our individual contributions shall be added in the final report.
