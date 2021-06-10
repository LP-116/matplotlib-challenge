# Matplotlib Challenge
## Matplotlib Homework - The Power of Plots

---
### Task

In this task we are working for Pymacceuticals Inc. a company that specicialises in anti-cancer pharmaceuticals. The most recent animal study consisted of 249 mice with a SCC (squamous cell carcinoma) tumor growth that have been treated with a variety of drug regimens. Over 45 days, tumor development was observed and measured and we have been asked to analyse the data. Predominately, we have been asked to compare the performance of the drug Capomulin against the other treatment regimens. 

We have been given 2 csv files to work with - _Mouse_metadata.csv_ and _study_results.csv_

----
### Method

To start the analysis the 2 csv files are merged into one data set.
We then want to check for an duplicate entries in the data set so our analysis is based on accurate data. Upon checking the data set, 249 mice were identified but 1 of the mice had duplicate timepoints. All data associated to the duplicated mouse was removed from the data set resulting in the analysis of 248 mice.

To start the analysis we created a summary statistics able of the mean, median, variance, standard deviation, and SEM of the tumor volume for each regimen.
To do this we used the below methods:

* .mean() - to calculate the average.
* .median() - to calculate the median (or middle) value.
* .var() - to calculate the variance.
* .std() - to calculate the standard deviation.
* .sem() - to calculate the SEM.

Then we generated a number of graphs to get a visual representation of the data.

* Based on all mice tested, a bar graph was created showing the total number of timepoints for each drug regimen.
* A pie graph was completed showing the gender distribution of the study.
* A boxplot on Tumor Volume was completed for 4 treatments - Capomulin, Ramicane, Infubinol, and Ceftamin.
* A line chart to show tumor volume by timepoint for a single mouse from the Capomulin treatment group.
* A scatter plot that shows the average Tumor Volume by mouse weight for each mouse in the Capomulin regimen.

The correlation coefficient and linear regression model was then completed.

A number of different methods were used to complete the graphs, these include:

* .count() - to get the number of timepoints.
* plt. or .plot() - to plot the data 
* .loc - to get specific information we required for the graphs.
* .groupby - to group the data so that we could get results based on a whole part of the data.
* .tail() - to get the last line of a dataset
* .quantile() - to calculate the quartiles for the IQR calculation.
* .append() - to add data to a list.
* Plus a number of graph related methods to assign graph labels and legends and to create the graph.

Note: For further detail regarding how each method was used, please refer to the comments within the pymaceuticals_start jupyter notebook. 

----
### Results

After completing the analysis the below observations have been made:
1.	Based upon the number of timepoints in the dataset, Capomulin and Ramicane have the most data recorded and Propriva has the least amount of data recorded. The reason for this is not clear and could be caused by a range of things e.g. the data simply wasn’t recorded or perhaps the mouse did not survive the entire time and therefore no more data could be recorded.

![Bar graph](https://user-images.githubusercontent.com/82348616/121468596-69de8900-c9fe-11eb-92c5-149d8994e3ef.PNG)

2.	The gender distribution of the mice in the experiment was very even but contained slightly more male mice than female mice (51% male mice vs 49% female mice).

![Pie chart](https://user-images.githubusercontent.com/82348616/121468656-84186700-c9fe-11eb-9d4b-17fbf2660e0e.PNG)

3.	Out of the 4 drug treatments only Infubinol shows any outliers – and the value of this outlier is bordering on acceptable. This gives us confidence that the data has been recorded correctly. Lots of outliers could indicate a problem with the dataset.

![Boxplot](https://user-images.githubusercontent.com/82348616/121468688-8da1cf00-c9fe-11eb-9f6e-655f627896b8.PNG)

4.	The mean and median of each drug is similar which indicates symmetrical distribution of the data.

![mean and median](https://user-images.githubusercontent.com/82348616/121468747-aa3e0700-c9fe-11eb-8b54-08526dc4e0c3.PNG)

5.	The correlation coefficient between mouse weight and tumor volume is 0.84 which indicates a strong positive correlation. The R-squared value is 0.7 which again identifies a strong effect.

![linear regression graph](https://user-images.githubusercontent.com/82348616/121468718-a01c0880-c9fe-11eb-8c7e-516ea7c12e33.PNG)

6.	Based upon the graph of 1 mouse in the Capomulin treatment group, there is a clear downward trend in the data. This could indicate the Capomulin is successful at reducing the tumor growth however further analysis on other mice within the group would need to be completed to verify this outcome. Further analysis on mice within other drugs would also need to be done to determine if they are more/less successful.

![X401 graph](https://user-images.githubusercontent.com/82348616/121468734-a4e0bc80-c9fe-11eb-80ce-dd11f5280c4e.PNG)

----
### Files

To run the code and view the results, please use the *pymaceuticals_starter.ipynb*  file located in the main branch of this repository.
The main branch of this repository also contains a folder called _data_ which contains the csv files used in the data and this ReadMe file.



