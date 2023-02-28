# Data-Visualization
The following are my personal projects, mostly school-related projects in data visualizations will be hosted here.

## ⚡⚡ Home Work 4
**Question:**

 Use the provided data at the [website](https://ourworldindata.org/coronavirus/country/united-states?country=~USA) or All of Us data to complete the following visualization of amounts. Choose a state or region in the US and display the amounts of either hospitalizations for COVID-19 or Coronavirus infections. I am not going to assign a specific region or state or whether you choose hospitalizations or infections since I want everyone to create a unique dataviz. I will not grade you on your selection of region, but instead the quality of the dataviz.
 
 **Solution:**
 The complete solution to the above problem is in the notebook: 
 **Link(s) to work** [Data Visualization of Covid-19 Data](https://github.com/SirMore/100-days-of-code-python/blob/master/Projects/Day_006/reeborg_maze.py) 
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


**Today's Progress**: Today I covered Python functions, code blocks and the While loop.

**Thoughts** I really enjoy the Reeborg Maze debugging cases. This was very challenging especially the random walls challenging.

**Link(s) to work** [Reeborg's Maze](https://github.com/SirMore/100-days-of-code-python/blob/master/Projects/Day_006/reeborg_maze.py) 

![Alt Text](https://github.com/SirMore/100-days-of-code-python/blob/master/Projects/Day_006/ezgif.com-video-to-gif.gif)
