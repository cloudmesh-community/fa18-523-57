# Historical Storm Data Analysis with Cosmos DB :hand: fa18-523-57 fa18-523-58


| Divya Rajendran, Pramod Duvvuri
| divrajen@iu.edu, vduvvuri@iu.edu
| Indiana University, Indiana University
| hid: fa18-523-57 fa18-523-58
| github: [:cloud:](https://github.com/cloudmesh-community/fa18-523-57/blob/master/project-report/report.md)
| code: [:cloud:](https://github.com/cloudmesh-community/fa18-523-57/tree/master/project-code)

---

Keywords: e534, hid fa18-523-57, fa18-523-58, [Data Visualization](#Visualization), Data Analysis, Cosmos DB, [Machine Learning](#Machine-Learning)

---

## Abstract

The decisions people make these days are all data driven. The amount of data we collect has increased exponentially and this makes it harder to visualize and understand. We can overcome this hurdle by sampling and visualizing subsets of the data. Sampling refers to the process of collecting random subsets of the data. The only thing one should remember is to pick a good sample of the data or to repeat the process of sampling and visualizing the data subset. In this project, we visualized the historical storm dataset and obtained inferences from our visualizations.

## Introduction

With the disastrous effects of the increasing number of storms all around the world, we thought of taking storm dataset for entire Asia Pacific region and visually analyze the effects of various variables on the storms. We want to check any patterns in the storm data and visualize them geographically so that it might help us to make useful inferences on the storm data. We have identified a data set on data.world[@fa18-523-57-DataSet], a community where we find open datasets from various organizations containing varying data attributes according to the need. We try to identify the various correlations among the attributes and understand if they can help explain the change in frequency of the storms.  

## Implementation

### Data set

The data set for the various storms in Asia Pacific region for the years between 1956 and 2017. We have chosen an initial subset of data to visualize locally and then implement the same visualizations on the entire data. The data set contains attributes like region, latitude, longitude, type of category, name, date and hour, speed, and pressure. There are more than 190,000 rows in the dataset. We clean the data for any duplicates, null values and any redundant data before we generate any visualizations.

Our dataset contains five different regions surrounding the oceans like Indian Ocean, Atlantic Ocean, Southern Pacific Ocean, West Pacific Ocean, and Eastern Pacific Ocean and the regions are named according to the ocean covering the locations. We have four different storm types like S for Tropical Storms, H for Hurricanes, D for Depressions, and U for low pressure and high speed storms.

### Related Work

We have identified an earlier work on tropical storm data using R by Stoltzman consulting LLC and have used it as a base reference to visualize our data using Python [@fa18-523-57-related-work].

## Technologies Used

1. Python is an object-oriented programming language we have utilized in this project [@fa18-523-57-Python].
2. The data is being stored on an Microsoft Azure Cosmos DB [@fa18-523-57-Azure] instance and we will be using Mongo API to connect and retrieve the data. The data is stored in the cloud, we are using and instance of Microsoft Cosmos DB, a NoSQL database, for storage. The output of our visualization is shown on jupyter notebook.
3. Matplotlib is a 2D visualization library containing a module plotly which gives us publication ready images and we aim to utilize this library to show basic correlation between attributes [@fa18-523-57-matplotlib].
4. Seaborn is a visualization tool based on Matplotlib used to draw attractive statistical plots and we aim to show the change in number of storms per year and other advanced correlations between different attributes [@fa18-523-57-Seaborn].
5. Folium is an interactive mapping tool which plots the data on a map based on the latitude and longitude values [@fa18-523-57-Folium].

## Visualization

This section contains visualizations of the data and the inferences we draw from them and mostly contains our analysis and inferences from them. We attempt to answer a few research question through these visualizations.

1. We start with the basic relationship between the number of unique storms per Year

    ![Storms per Year](images/fa18_523_57_Storms_per_Year.PNG){#fig:storms_per_year}

    We have plotted a linear relationship model between the number of storms and the storm year. We can see from the plot that the rate of increase number of unique storms through the years 2000 to 2010 and then reduce to the same rate as between the years 1950 to 1990. But, we cannot assume that the number of storms increased every year, we need to look at other factors such as correlation between other attributes describing the storms.
2. Number of Storms per basin

    ![Storms per Region](images/fa18_523_57_Storms_per_Basin.png){#fig:storms_per_basin}

    We plotted a horizontal bar graph between number of storms occurred in each region and identified that Western Pacific Ocean region had higher number of storms than in other regions.
3. Number of storms per year per region

    ![Storms per Year and  Region](images/fa18_523_57_Storms_per_year_region.png){#fig:storms_per_year_per_region}

    We plotted a bar graph between number of storms per year colored by the region in which the storm was observed. The storms were increasing each year in every region and we found that the storms in the region "West Pacific Ocean", were higher than the storms in region "Eastern Pacific Ocean" during the years 1950 to 1965 and decreased during the years 1965 to 1994. As per our plot, the regions "West Pacific Ocean" and "Eastern Pacific Ocean" had higher number of storms during 1950 and 2000.
4. Number of storms per region per type of storm

    ![Storms per Region and type over the years](images/fa18_523_57_Storms_per_year_region_type.png){#fig:storms_year_region_type}

    We took another step and plotted a pairwise plot between the storm count per region and category type over the years and we observed that in all the five regions, we had sizable number of storms of types D, H and S when compared to the storm type U.
5. Relationship between wind and pressure

    ![relationship between wind and pressure](images/fa18_523_57_pressure_speed_histogram.png){#fig:relation_wind_press_region}

    When we plot the linear relationship plot between speed and pressure along with their distributions, we can see that the pressure distribution looks more normal. We clearly observe that the pressure is inversely proportional to speed, that is, higher the speeds lower the pressure and vice-a-versa.
6. Correlation between Speed, pressure and category type is identified by visually analyzing them.
    ![Correlation between speed, pressure and type of storm](images/fa18_523_57_pressure_speed_type_region.png){#fig:relation_wind_pressure_region}

    When we plotted the factted plot of wind speed, pressure and category of storm type we observed that the type "D- Depression" storms are of higher pressure and lower speed and storm type "U" is of lower pressure and higher speed. We also observed that the storms of type "S - Tropical Storms" are more prevalent in region "West Pacific Ocean" and are of lesser speeds when compared to other types of storms.
7. Heat Map of Eastern Pacific region

    ![Heat Map of Eastern Pacific Region](images/fa18_523_57_HeatMapE.png){#fig:Heat_Map_Eastern_Pacific}

    When we plotted a heat map for Eastern Pacific region, we see that the major portion of  storms are concentrated in the ocean itself and then as they make landfall the storms decrease in number.

We have created an interactive map showing the distribution of different storm categories and regions. The interactive html files are available in our <https://github.com/cloudmesh-community/fa18-523-57/tree/master/project-report/images/interactive> folder and the code for these interactive maps is available in our jupyter notebook.

## Machine Learning

### Multinomial Naive Bayes

Multinomial Naive Bayes (MNB) is a simple classifier that uses the Bayes Theorem and assumes independence between the features and is used for multinomially distributed data, since the data is represented in sparse matrix of word vectors this would be ideal for such scenarios. We shall use *sklearn.naive_bayes.MultinomialNB* implementation in our project. We have used various train/test splits to analyze the accuracy of our model. The same has been represented in terms of error in the plot below. The highest accuracy we got was when we used the 80/20 train-test split which gave us an accuracy of split gave us an accuracy of 13.4 % (rounded to nearest decimal point)

## Summary

From our visualizations we identified that storms increased each year with different points of origination and that there were many storms in Western Pacific ocean region than in other regions. We identified that the pressure and speed have an effect on storm type and they separate storms into Hurricanes, Tropical Storms, Depressions and low pressure storms. We identified that the higher speed storms are more likely to occur in West Pacific Ocean region.

## Future Work

In this project, our main aim was to visualize the dataset. After visualizing and making inferences, we would like to propose a model that uses machine learning pattern in our data. We hope to use unsupervised machine learning algorithms to find clusters in our data. This might help us identify further patterns in the data that could not have been possible with just plain visualization of the data. The main problem that we have identified in building such a model is the availability of resources required to run the algorithm without any interruption. Using a local computer resources for running such a model would not be feasible. Hence, we hope to deploy such a model in the cloud and utilize its power and resources for machine learning.

## Acknowledgement

The authors would like to thank Dr. Gregor von Laszewski for giving the opportunity to work on this project and for providing valuable feedback during the duration of our project. The authors would also like to thank the associate instructors of this class for their help and prompt responses to our questions on Piazza. The authors would also like to thank Microsoft for providing a free trial of Azure Cloud services.

## Work Breakdown

The authors Divya Rajendran and Pramod Duvvuri have contributed equally in preparing this report. We shall co-ordinate to equally divide the work that is required to complete the project and the final report before the deadline in December, 2018. Our contributions towards the completion of the project shall be updated in our respective notebook markdown files in our respective git repositories and a summary of our individual contributions shall be added in the final report.
