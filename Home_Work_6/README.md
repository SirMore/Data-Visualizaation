## ⚡⚡ Home Work 6
**Question:**

 Use the provided data at the [website](https://ourworldindata.org/coronavirus/country/united-states?country=~USA) or All of Us data to complete the following visualization of amounts. Choose at least two continuous scale variables and a categorical variable for grouping. Then,  display the association in some manner that allows the viewer to see if association between the continuous variables differs across the categorical groups
 **Solution:**
 The complete solution to the above problem is in the notebook:
 
 **Link(s) to work** [Data Visualization of Covid-19 Data]([https://github.com/SirMore/Data-Visualization/blob/main/Home_Work_6/HW_6.ipynb](https://github.com/SirMore/Data-Visualization/blob/main/Home_Work_6/HW_6-new.ipynb)) 
 
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



