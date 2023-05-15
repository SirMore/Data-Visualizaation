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

---------------------------------------------------------------------------------
-----------------------------------------------------------------------------

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

--------------------------------------
---------------------------------------------
## ⚡⚡ Home Work 6
**Question:**

 Use the provided data at the [website](https://ourworldindata.org/coronavirus/country/united-states?country=~USA) or All of Us data to complete the following visualization of amounts. Choose at least two continuous scale variables and a categorical variable for grouping. Then,  display the association in some manner that allows the viewer to see if association between the continuous variables differs across the categorical groups
 **Solution:**
 The complete solution to the above problem is in the notebook:
 
 **Link(s) to work** [Data Visualization of Covid-19 Data](https://github.com/SirMore/Data-Visualization/blob/main/Home_Work_6/HW_6.ipynb) 
 
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


 
![Alt Text](https://github.com/SirMore/Data-Visualization/blob/main/Home_Work_6/Main/figures/continent_1.png)

In the entire dataset it can be observed that the continents with the highest to least number of countries are:
Africa, Asia, Europe, North America, Oceania, South America.


**Visualisations**:

In order to better understand if any the association between continuous outcomes, we focused on exploring the continous variables:
 - Median Age and 
 - Life Expectancy
 And categorical variable
 - Continents


![Alt Text](https://github.com/SirMore/Data-Visualization/blob/main/Home_Work_6/Main/figures/conti.png)



**Thoughts**

- From the plot above, it can be observed that, the continent with the highest median age is Europe with their median age of over 40 years, closely followed by the North American continent with a median age very close to 35 years.

- Africa has the least median age of slightly above 20 years.

- From these values, it is quite clear as to why more people in Europe and North America were affected with the covid-19
- And very less records of these cases for the African continent.
As you can see, the above graphs are not telling a good story, mainly because all of the yearly data is being plotted together. In addition, you can’t see the test dates because there are far too many points. Therefore, the first steps I took were to clean the data.
To have control over the aesthetics of the graph such as labels, titles, color and size we shall apply more functions as shown below.

![Alt Text](https://github.com/SirMore/Data-Visualization/blob/main/Home_Work_6/Main/figures/median.png)

**Thoughts**

From the plot above, it is observed that, the most/modal "median age" of:
- The worls is 33 years
- Asia is 31 years
- North America is 27 years
- Africa is 18 - 19
- Europe is 35, 39 - 42
- South America is very uniform across all the age groups
- Oceania is 37 - 38


**Intermidiate plot**
![Alt Text](https://github.com/SirMore/Data-Visualization/blob/main/Home_Work_6/Main/figures/expectancy.png)



**Thoughts**

To better understand the distribution of the median age, we used a side-by-side box plot to visualise the median age across the different continents.

From the plot above, it can be observed that:
- The median age of the people of the Asian continent is slightly left skewed with the presence of an outlier
- Regards to Europe and North America, we can observe that they are kinda symmetrical, with no presence of any outliers, implying that the proportions of the young and old is almost the same. (Which to me is a little stange because I though that Europe had a higher older generation)
- Africa is very much skewed to the right with the presence of several outliers. It can be observed that, the maximum age of Africans is less than the median ages of people from thye Asian and North American continents.
- Finally, Oceania on the other hand is extremely right skewed.
- The North American and the Oceania continents, have median ages which are very widely spread out unlike their counterparts in Europe, African and South America, whose median ages are very much close together with less variability.


**Life Expectancy plot**
![Alt Text](https://github.com/SirMore/Data-Visualization/blob/main/Home_Work_6/Main/figures/LIFE.png)

![Alt Text](https://github.com/SirMore/Data-Visualization/blob/main/Home_Work_6/Main/figures/LIFE2.png)

**Thoughts**

We finally plotted the life expectancy across various continents.
- As per the median age, it can be seen that the continent with the highest life expectancy, is Europe with a median value of over 80 years and minimum and maximum values of 72 and 87 years respectively.
- North America has a median life expectancy of 77 years with 72 and 84years being the minimum and maximum values respectively.
- Africa as usual, has the least life expectancy, with a median value of 64, minimum value of 53 and maximum life expectancy of 77
- It can be observed that the life expectancy of Europe and South America is very much skewed to the left.
- While that of Asia, Africa and North America is slightly symmetirc.
- Oceania had the highest variability in Life Expectancy.







------------------------------------------------------------------
-----------------------------------------------------------------
## 
## ⚡⚡ FINAL PROJECT
**Question:**

Using a data on food aand housing security of the students at **----** recoreded since 2019 and continues to today, this visualisation seeks to answer thr following questions: 
1) How is use of government federal aid/assistance associated with food insecurity as measured by the USDA index or categories?
2) Does food insecurity (as measured by USDA index or categories) have a relationship with the items pertaining to concentration on school and degree progress/completion?
3) Are there gender or ethnicity differences in the items pertaining to concentration on school and degree progress/completion?
---------
 
 **Solution:**
 The complete solution to the above problem is in the notebook:
 
 **Link(s) to work** [FINAL PROJECT](https://github.com/SirMore/Data-Visualization/blob/main/Final_Project/Final_Project.ipynb)
 ------------
 **Data Importation and Data Wrangling**

- The data set for this project consist of the main data and an extra data which contains important information of the respondents. 
![image](https://github.com/SirMore/Data-Visualization/assets/10974475/6806e659-bb89-401d-9892-ed443cd5065c)

- In order to merge the data, the key "RespondentId" is used since it is the only common variable between the two data sets master and extra. Allow the columns conating the questions in the extra data was not included in the merged data.
- The master data comprised of 11763 variables/columns and 59 observations, while the extra data has 1743 columns and 57 obervations. In all the merged data has 1743 variables and 73 observations.
    

**Pre-processing**
-  **Pre-processing the variable college**
The column variable was casted back unto the original character values using the table below as a key

| Old Key| 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | multi-option |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| New Key | Business | Education | Engineering | Liberal Arts | Health Sciences | Nursing | Science | Pharmacy | Other | multi-option |

- **Processing the variable Ethnicity**

The ethnicity of the responders was transformed back unto the original character values using the table below as a key quide

| Old Key| 1 | 2 | 3 | 4 | 5 | 6 | 7 | multi-option |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| New Key | Hispanic | American Indian/Alaska native | Asian | African American | Native Hawaiian | White/Caucasian | Other  | Mixed |

- **Processing the variable Gender**

The gender variable was also transformed using the following key:

| Old Key| 1 | 2 | 3 | 4 | 5 | 6 | 0 | multi-option |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| New Key | Female | Male | Transgender | Gender variant | Other | Other | Other  | Transgender|



-----------------------------
## Section 1: Effects of government aids on food insecurity

**Question: How is use of government federal aid/assistance associated with food insecurity as measured by
the USDA index or categories?**

**1.1 Federal Aid and Academic Level Relationship**
![Alt Text](https://github.com/SirMore/Data-Visualization/blob/main/Final_Project/Figures/1_1.png)

![Alt Text](https://github.com/SirMore/Data-Visualization/blob/main/Final_Project/Figures/1_1b.png)

**Remark:**

The above (upper figure) is a cluster plot of the educational levels vs the type of federal aid received by the respondents. After which, we built a category scatter plot to display the respondents for the classification-to-fedaid categorical values intersect. 

On top of the population cluster plot above, we can draw the follow conclusions:

- Work-study is predominate in all the different levels of education
- As the repondents climbs the academic levels, their reliance on loans decreases
- Very few respondents benefitted from the UTEP's COVID CARE Act fund
- The respondents hardly took the Emergency Loan
- Finally, the respondents with professional certificates did not really enrol on any of the federal aid programs

**1.2 Federal Aid and USDA Index Relationship**

From the cluster plot above, it can be observed that: 

- Students within the high/marginal food security, either work/study, take loans or take grants.
- Similarly, across the different USDA index, it can be observed that work-study, take loans or grants dominate the levels.
![Alt Text](https://github.com/SirMore/Data-Visualization/blob/main/Final_Project/Figures/1_2b.png)

![Alt Text](https://github.com/SirMore/Data-Visualization/blob/main/Final_Project/Figures/1_2b.png)

**Thoughts**

- It can be observed that respondents who work-study exxperienced the highest levels of food insecurities across all the USDA index, with the higest been marginal food security. 
- Very few students received emergency loans across the USDA category. it is also very evident that most of the students either work and study or take loands and grants.
- This observation was very evident in all the analysis performed. Refer to the notebook at .............. for a complete analysis.

----------------------------------------------------------------
**Question: Does food insecurity (as measured by USDA index or categories) have a relationship with the items pertaining to concentration on school and degree progress/completion?**

In order to answer this question,  we performed another set of visualisations, which not everythin will be reported here. 
![Alt Text](https://github.com/SirMore/Data-Visualization/blob/main/Final_Project/Figures/2b.png)
 
 As can be seen from the above most of the numerous students were female hispanics among the survey respondents are within the following clusters below:
 
 - Most of the senior students are in Health Sciences, followed by Engineering and Business.
 - Very few seniors are in Pharmacy and Sciences.
 - Similarly, the top 3 colleges for Juniors are: Health Sciences, Engineering and Business respectively in order.
 - And the bottom 3 colleges among the respondents are: Science, Education and Pharmacy.
 - Similar observation can be made about students in Sophomore year.
 - The bottom three colleges in this instance are: Science, Liberal Arts and Pharmacy
 - Among the freshmen, the most populous colleges were Health Sciences, Engineering and Nursing. And the least populous colleges are Science, ducation and Pharmacy
 - Interestingly, among the masters students, the most populous college is Education and Health Sciences.
 - Finally, for Doctoral students, most respondents were in Nursing and Engineering.
 - Among all the cluster of colleges, it can be observed that the distribution of federal aids is very similar as we would expect from the results and visualisations from the previous section.


----------------------------------------------------------------
**Question: Are there gender or ethnicity differences in the items pertaining to concentration on school and
degree progress/completion?**

- Since the data has records across different years, we visualized the distribution of federal aids the years. It can be oberved that most students benefitted from the federal aids for 2020, which is probably duee to the COVID 19 pandemics.
- Students across the differrent years, work and study followed by loans.
![Alt Text](https://github.com/SirMore/Data-Visualization/blob/main/Final_Project/Figures/year.png)

Following the visualisation above, we performed analysis of the Food Insecurity as defined by the USDA index across the different years. 

- It can be clearly seen that most food insecurities was observed in 2020. The amount of values recorded for 2020 is more that of the remaining years. With high/marginal food security been the most dominated category or index.
- Surprisingly, the number of students within the categories dropped significantly in 2021, with very little records for marginal/high food security.


![Alt Text](https://github.com/SirMore/Data-Visualization/blob/main/Final_Project/Figures/year2.png)



From the visualisation (below) of the ethnicity (**upper-left plot**), we observed that Hispanics dominated the entire survey. But to better understand distribution for the different races with regard to USDA index and federal aids, we performed individual separate visualisations for the distinct ethnicities (See below).

<p float="left">
  <img src="https://github.com/SirMore/Data-Visualization/blob/main/Final_Project/Figures/hispanic1.png" width="500" title = "good" /> 
  <img src="https://github.com/SirMore/Data-Visualization/blob/main/Final_Project/Figures/his.png" width="500" /> 
  <img src="https://github.com/SirMore/Data-Visualization/blob/main/Final_Project/Figures/asian.png" width="500" />
 <img src="https://github.com/SirMore/Data-Visualization/blob/main/Final_Project/Figures/black.png" width="500" />
</p>

From the plot above (upper-left to bottom left):
- upper-left: Category plot of gender vs Federal Aid
- upper-right: Category plot of Hispanics for Federal Aid vs USDA Index
- bottom-left: Category plot of Blacks for Federal Aid vs USDA Index
- bottom-right: Category plot of Asians for Federal Aid vs USDA Index

- From the distributions above, it can be observed that eventhough there is a disproportional ethnicity distribution, the individual plots of the various races with regards to Federal Aids and USDA categories/Index are all very similar or the same with the same proportions for the various ethnicities.  

From the visualisation of the ethnicity, we observed that Hispanics dominated the entire survey. But to better understand distribution for the different races with regard to USDA index and federal aids, we performed individual separate visualisations for the distinct ethnicities.

----------------------------------------------------------------
**ALLUVIAL PLOTS**:
In order to determine whether the differences in gender and  ethnicity affects the the concentration on school and degree progress/completion,  the alluvial plots for both males and females was used

![Alt Text](https://github.com/SirMore/Data-Visualization/blob/main/Final_Project/Figures/race_female.png)
![Alt Text](https://github.com/SirMore/Data-Visualization/blob/main/Final_Project/Figures/race_male.png)


After reviewing both of the alluvial diagrams above, we can see that most of the male students are Hispanic (kinda expected) are in the Health Sciences college, in their senior year and they are msotly in the marginal/high food security category and they usually work and study.


**Final**


**Remark: Refer to [FINAL PROJECT](https://github.com/SirMore/Data-Visualization/blob/main/Final_Project/Final_Project.ipynb) for complete visualization**


