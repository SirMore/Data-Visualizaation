# Data-Visualization
The following are my personal projects, mostly school-related projects in data visualizations will be hosted here.

## ⚡⚡ Home Work 4
**Question:**

 Use the provided data at the [website](https://ourworldindata.org/coronavirus/country/united-states?country=~USA) or All of Us data to complete the following visualization of amounts. Choose a state or region in the US and display the amounts of either hospitalizations for COVID-19 or Coronavirus infections. I am not going to assign a specific region or state or whether you choose hospitalizations or infections since I want everyone to create a unique dataviz. I will not grade you on your selection of region, but instead the quality of the dataviz.
 
 **Solution:**
 The complete solution to the above problem is in the notebook:
 
 **Link(s) to work** [Data Visualization of Covid-19 Data](https://github.com/SirMore/Data-Visualization/blob/main/Home_Work_4/first_visualization/Data%20Visualization%20of%20Covid-19%20Data.ipynb) 
 
 **Data Importation and Data Wrangling**

- The dataset for this project is [Data on COVID-19 (coronavirus) by Our World in Data](https://github.com/owid/covid-19-data/tree/master/public/data). Which is a  complete COVID-19 dataset collection of the COVID-19 data maintained by -Our World in Data](https://ourworldindata.org/coronavirus). The data is updated daily throughout the duration of the COVID-19 pandemic.

- For the purpose of this project, I concentrated on the Covid-19 information on the United States.

- And the following columns were selected for visualization purposes:
    - total_cases:	Total confirmed cases of COVID-19. Counts can include probable cases, where reported.
    - new_cases:	New confirmed cases of COVID-19. Counts can include probable cases, where reported. In rare cases where oursource reports a negative daily change due to a data correction, we set this metric to NA.
    - total_deaths	Total deaths attributed to COVID-19. Counts can include probable deaths, where reported.
    - new_deaths	New deaths attributed to COVID-19. Counts can include probable deaths, where reported. In rare cases where our source reports a negative daily change due to a data correction, we set this metric to NA.
    - icu_patients	Number of COVID-19 patients in intensive care units (ICUs) on a given day.
    - hosp_patients	Number of COVID-19 patients in hospital on a given day
    - total_tests	Total tests for COVID-19
    - new_tests	New tests for COVID-19 (only calculated for consecutive days)
    - total_vaccinations	Total number of COVID-19 vaccination doses administered
    - people_vaccinated	Total number of people who received at least one vaccine dose
    - people_fully_vaccinated	Total number of people who received all doses prescribed by the initial vaccination protocol
    

**Pre-processing**
- Because the main attributes for this project is the hospitalisation and ICU, rows with missing values in these two columns were deleted and the resulting data frame was saved and imported for the visualisation.


**Initial Plots**: 

We’ll be following the object-oriented method for plotting. The plot function takes two arguments that are X-axis values and Y-axis values plot. In this case, we will pass the ‘X’ variable which has ‘Dates’ and ‘Y’ variable which has ‘Daily Hospitalisation’ to plot.

![Alt Text](https://github.com/SirMore/Data-Visualization/blob/main/Home_Work_4/first_visualization/figures/initial_hosp.png)

![Alt Text](https://github.com/SirMore/Data-Visualization/blob/main/Home_Work_4/first_visualization/figures/intitial_icu.png)

**Thoughts**

The plots above gives the initial visualizations of the variables of interest in this project.  But these plots are not the best representation for large dataset values along the axes as you can see the ‘Dates’ are overlapping on X-axis. To overcome this challenge we will introduce some new functions to take more control over the aesthetics of the graph.

**Aesthetics**

As you can see, the above graphs are not telling a good story, mainly because all of the yearly data is being plotted together. In addition, you can’t see the test dates because there are far too many points. Therefore, the first steps I took were to clean the data.
To have control over the aesthetics of the graph such as labels, titles, color and size we shall apply more functions as shown below.

**Intermidiate plot**
![Alt Text](https://github.com/SirMore/Data-Visualization/blob/main/Home_Work_4/first_visualization/figures/intermediate_hosp.png)

**Remark:**
Still as we can see the dates are overlapping and the labels along axes are not clear enough. 
This is a little better, but it’s still messy, and it’s not giving me all the information I want. By this point, I decided that my goal would not be accomplished with matplotlib, so I moved onto plotly.

**Final**
![Alt Text](https://github.com/SirMore/Data-Visualization/blob/main/Home_Work_4/first_visualization/figures/final_hosp.png)
![Alt Text](https://github.com/SirMore/Data-Visualization/blob/main/Home_Work_4/first_visualization/figures/final_icu.png)

**Remark: Refer to [Data Visualization of Covid-19 Data](https://github.com/SirMore/Data-Visualization/blob/main/Home_Work_4/first_visualization/Data%20Visualization%20of%20Covid-19%20Data.ipynb) for complete visualization**

Now, this was more of the format I was looking for, but now it was time to combine my data. The code below allowed me to plot the all the columns of interest together for the US in the chosen time-frame.

To break it down, first I created subplots to allow for a dual y-axis. Then I plotted the COVID-19 data for USA. I added traces for each line that I wanted to add. Then I formatted the titles and added annotations. I wanted to highlight the date of the first COVID lockdown re-opening in the state of California, so I added that with the text annotations.

Finally, I created my dropdown filter with the updatemenus parameter. 

NB: It can't be displayed here because it is interractive.

**Fianlly: Grouped bar charts for years**

Next, to compare which months recoreded the highest number of patients hospitalized and admitted into ICUs, I visualized the grouped bar charts of the dataset.
![Alt Text](https://github.com/SirMore/Data-Visualization/blob/main/Home_Work_4/first_visualization/figures/final_month_hosp.png)

![Alt Text](https://github.com/SirMore/Data-Visualization/blob/main/Home_Work_4/first_visualization/figures/final_month_icu.png)


## ⚡⚡ Home Work 5
**Question:**

The data (serialdat.csv), contains information about gene variant transcriptions. There were three replications of the variant transcriptions and a final column where the three replications were averaged. The two categorial varialbes included are the SUMOver (which is classes of genes - S#V# format). Ignore the replication number that follows the S#V# groups (of which there are 6 groups). Try to visualize the distributions according to each group. You may also include visualizations across the replications to see if the transcription process introduced error overall..
 
 **Solution:**
 The complete solution to the above problem is in the notebook:
 
 **Link(s) to work** [Gene Variant Transcription]https://github.com/SirMore/Data-Visualization/blob/main/Home_Work_5/Home_Work_5.ipynb)) 
 
 **Data Importation and Data Wrangling**
    

**Pre-processing**
The data was pre-processed so that the replication numbers number that follows the $S_iV_j$ groups  were deleled.


**Initial Plots**: 

In order to get a fair idea of how each gene class is distributed, a bar plot of the cummulative "average replications" vs "gene  class" is plotted.

![Alt Text](https://github.com/SirMore/Data-Visualization/blob/main/Home_Work_5/figures/ini_1.png)

**Thoughts**

From the cluster/bar plot, it is evident that gene class $S_1V_1$ recorded the highest mean occurrences. With $S_2V_2$ recording the minimum.



In order a make this visualisation easily to grasp how each gene class is fairing, an order barplot is given below

![Alt Text](https://github.com/SirMore/Data-Visualization/blob/main/Home_Work_5/figures/ini_2.png)

**Distribution of gene variant transcription**

**Final plot**
![Alt Text](https://github.com/SirMore/Data-Visualization/blob/main/Home_Work_5/figures/ini_3.png)

**Reamrk**

Next, we visualized the gene transcriptions across the classes. Evidence of outliers in each of the classes can be observed from the figure above. In can be inferrted from the box plot that, each of the gene classes are left skewed, with $S_2V_1$ having a higher dispersion. Similarly, $S_1V_1$ has has the least dispersion. 

The range of values for the gene classes $S_2V_1, S_2V_2$ is widely spread out. With $S_1V_1, S_1V_2$ closely parked together.



**Replication Plots**

In order to visualizations across the replications, first the data was transformed, where all the replications were put into the same column. 

![Alt Text](https://github.com/SirMore/Data-Visualization/blob/main/Home_Work_5/figures/ini_4.png)

**Thought**

After the preprocessing, a joint boxplot of the three replications was visualized.  It can be observed that $S_2V_1$ has the highest dispersions across all the groups and $S_1V_1$ has the least dispersion, which confirms our earlier observations.

**Remark: Refer to [Gene Variant Transcription](https://github.com/SirMore/Data-Visualization/blob/main/Home_Work_5/Home_Work_5.ipynb) for complete visualization**

## 
