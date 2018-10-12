# Historical Storm Data Analysis with HBase (Draft)
## authors: Divya Rajendran, Pramod Duvvuri

## Abstract


## INTRODUCTION ##

With the disastrous effects of the increasing number of storms all around the world, we thought of taking storm dataset for entire Asia Pacific region and visually analyze the effects of various variables on the storms. We want to check any patterns in the storm data and visualize them geographically so that it might help us to make useful inferences on the storm data. We have identified a data set on data.world[@fa18-523-57-DataSet] and we aim to identify the various correlations among the attributes and understand if they can help explain the change in frequency of the storms. Data World is a community where we find open datasets from various organizations containing varying data attributes according to the need. The data is saved in a graph database HBase. The output of our visualization is shown on jupyter notebook.


## IMPLEMENTATION ##

### Data set ### 
The data set for the various storms in Asia Pacific region for the years between 1956 and 2017. We would choose an initial subset of data to visualize locally and then implement the same visualizations on the entire data. The data set contains attributes like region, latitude, longitude, storm number, name, date and time, speed, pressure, category type.

### Related Work ###
We have identified an earlier work on tropical storm data using R by Stoltzman consulting LLC and are planning to use it as a base to visualize our data using Python[@fa18-523-57-related-work].

### Visualization ###
1.	Category of storms in different latitude and longitude is visualized to identify the variation in category of storms in those location.
2.	Category of storms in different regions is visualized to check the correlation between them.
3.	Correlation between Speed, pressure and category type is identified by visually analyzing them.
4.	Correlation between latitude, longitude and speed, pressure is to be explored.
5.	Concentration of storms in different regions should be visually explored.

## TECHNOLOGIES TO BE USED ##
1.	Python is an object-oriented programming language we plan to use in this project [@fa18-523-57-Python]
2.	Apache HBase is a graph database which runs onHadoop HDFS, we plan to utilize this database to save our huge data and work on [@fa18-523-57-Apache_HBase].
3.	Matplotlib is a 2D visualization library containing plotly which gives us publication ready images and we aim to utilize for identifying correlation between various attributes [@fa18-523-57-matplotlib].
4.	Seaborn is a visualization tool based on Matplotlib used to draw attractive statistical plots and we aim to show the change in number of storms per year [@fa18-523-57-Seaborn].
5.	Altair is a statistically aimed visualization library which produces output plots which are easily shown on a website [@fa18-523-57-Altair].
6.	D3.js is a visualization library based on Javascript which is vastlyy implemented per SVG and HTML formats [@fa18-523-57-D3js].

## Visualization samples ##

### Visualization 1 ###
![alt text](https://www.stoltzmaniac.com/wp-content/uploads/2017/09/unnamed-chunk-2-1-2.png “Basic Plot”)
### Visualization 2 ###
![alt text](https://www.stoltzmaniac.com/wp-content/uploads/2017/09/unnamed-chunk-5-1-2.png “Category wise Storms”)
### Visualization 3 ###
![alt text](https://www.stoltzmaniac.com/wp-content/uploads/2017/09/unnamed-chunk-9-1-2.png “Heat Map of storm concentration”)
### Visualization 4 ###
![alt text](https://www.stoltzmaniac.com/wp-content/uploads/2017/09/unnamed-chunk-11-1-2.png “Correlation between attributes”)


### Conclusions ###
TBD
