## ⚡⚡ Home Work 4
**Question:**

 Use the provided data at the [website](https://ourworldindata.org/coronavirus/country/united-states?country=~USA) or All of Us data to complete the following visualization of amounts. Choose at least two continuous scale variables and a categorical variable for grouping. Then,  display the association in some manner that allows the viewer to see if association between the continuous variables differs across the categorical groups
 **Solution:**
 The complete solution to the above problem is in the notebook:
 
 **Link(s) to work** [Data Visualization of Covid-19 Data]() 
 
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
