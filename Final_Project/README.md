## ⚡⚡ FINAL PROJECT
**Question:**

Using a data on food aand housing security of the students at **----** recoreded since 2019 and continues to today, this visualisation seeks to answer thr following questions: 
1) How is use of government federal aid/assistance associated with food insecurity as measured by the USDA index or categories?
2) Does food insecurity (as measured by USDA index or categories) have a relationship with the items pertaining to concentration on school and degree progress/completion?
3) Are there gender or ethnicity differences in the items pertaining to concentration on school and degree progress/completion?
---------
 
 **Solution:**
 The complete solution to the above problem is in the notebook:
 
 **Link(s) to work** [Data Visualization of Covid-19 Data](https://github.com/SirMore/Data-Visualization/blob/main/Home_Work_4/first_visualization/Data%20Visualization%20of%20Covid-19%20Data.ipynb) 
 
 **Data Importation and Data Wrangling**

- The data set for this project consist of the main data and an extra data which contains important information of the respondents. 
- Variable	Meaning	Notes	Variable type
Enroll	Enrollment type at UTEP	1-‘Full-time’;  2-‘Part-time’	Factor with 2 levels
Employ	Are you employed?	1-‘Full-time’; 2-‘Part-time’; 3-‘No’	Factor with 3 levels
Working	Job on/off campus	1-‘On campus’; 2-‘Off campus’; 3-‘Both’	Factor with 3 levels
Hrs	Weekly hours worked	1-’19 hours or less’; 2-‘More than 19 hours’	Factor with 2 levels
Age	What is your age?	Numerical	Numeric; Range 0-75
Ethnicity	What is your ethnicity?	1-‘Hispanic’; 2-‘American Indian/Alaska native’; 3-‘Asian’; 4-‘African American’; 5-‘Native Hawaiian’; 5-‘White/Caucasian’; 6-‘Other’; 7-‘Prefer not to say’	Character; they were allowed to select multiple options, so there might be lists of responses
Income	2022 household income	1-‘Less than $10,000’; 2-‘$10,000 to $19,999’; 3-‘$20,000 to $29,999; 4-‘$30,000 to $39,999’; 5-‘$40,000 to $49,999’; 6-‘$50,000 to $59,999’; 7-‘$60,000 to $69,999’; 8-‘$70,000 to $79,999’; 9-‘$80,000 to $89,999’; 10-‘$90,000 to $99,999’; 11-‘$100,000 or more’	Factor with 11 levels
Classification	Academic level	1-‘Freshman’; 2-‘Sophomore’; 3-‘Junior’; 4-‘Senior’; 5-‘Graduate (Masters)’; 6-‘Doctoral’; 7-‘Special: Professional (Certificate Program)’	Factor with 7 levels
College	Which college are you a student of?	1-‘Business’; 2-‘Education’; 3-‘Engineering’; 4-‘Liberal Arts’; 5-‘Health Sciences’; 6-‘Nursing’; 7-‘Science’; 8-‘Pharmacy’; 9-‘Other’	Character; they were allowed to select multiple options, so there might be lists of responses
Commute	Way of transportation to school	1-‘Car (alone)’; 2-‘Car (someone drives to campus and picks you up)’; 3-‘Carpool’; 4-‘Bus/Public transportation’; 5-‘Bike’; 6-‘Trolley’; 7-‘Walk’; 8-‘Uber/Lyft’; 9-‘Other’; 10-‘Not applicable’	Factor with 11 levels
Alone	Do you live alone?	1-‘Yes’; 2-‘No’	Factor with 2 levels
Dependents	# of dependents	1-‘None’; 2-‘1’; 3-‘2’; 4-‘3’	Factor with 4 levels
HoH	Head of household	1-‘Yes'; 2-‘No’	Factor with 2 levels
Live	Current housing situation	1-‘On campus’; 2-‘Off campus with family’; 3-‘Off campus not with family’; 4-‘Other’; 5-‘Off campus with parents’; 6-‘Off campus with partner’; 7-‘Off campus with partner and kids’	Factor with 7 levels
FedAid	Federal Student Aid in the past 12 months	1-‘Grants’; 2-‘Work-study’; 3-‘Loans’; 4-‘Scholarship’; 5-‘Emergency Loan’; 6-‘UTEP’s COVID CARES Act Fund’; 7-‘Other’; 8-‘None’	Factor with 8 levels
PA	Permanent address in the past 12 months	1-‘Yes'; 2-‘No'	Factor with 2 levels
FreqNightElse	Frequency spending nights elsewhere due to lack of PA	1-‘Often’, 2-‘Sometimes’; 3-‘Rarely’	Factor with 3 levels
UTEPHomeless	Do you know any students experiencing homelessness?	1-‘Yes’; 2-‘No’	Factor with 2 levels
Year	Year of collecting the data	1-‘2019’; 2-‘2020’; 3-‘2021’; 4-‘2022’	Factor with 4 levels
HH3	The food did’t last and there were no more money left for more food	1-‘True’; 0-‘False’	Character
HH4	Couldn’t afford balanced meals	1-‘True’; 0-‘False’	Character
AD1	Cut size or skip meals because of lack of money	1-‘True’; 0-‘False’	Character
AD1a	How often did AD1 happen?	1-‘Almost every month/Some months’; 0-‘Only 1 or 2 months’	Character
AD2	Eat less because of lack of money	1-‘True’; 0-‘False’	Character
AD3	Hungry but didn’t eat because of lack of money	1-‘True’; 0-’False’	Character
Index	Food security stats/score	0,1,2,3,4,5,6	Character
Gender	Gender you identify with	1-‘Female’; 2-‘Male’; 3-‘Transgender’; 4-‘Gender variant’; 5-‘Other’; 6-‘Prefer not to say’	Character; they were allowed to select multiple options, so there might be lists of responses
USDAcat	Calculated Food Security levels	If Index %in% 0:1 then USDAcat-‘Marginal/High FS’; If Index %in% 2:4 then USDAcat-‘Low FS’; If Index %in% 5:6 then USDAcat-‘Very Low FS’	Character
YR_2019:YR_2022	Specific year; 4 separated columns	1-‘No’; 2-‘Yes’	Factor with 2 levels; if the variable ‘Year’ is equal with the year in the name, the entry will be ‘Yes’ and ‘No otherwise’
Ethn_Hisp:Ethn_Other	Specific ethnicity; 7 separated columns	1-‘No’; 2-‘Yes’	Factor with 2 levels; if the variable ‘Ethniciy’ is equal with the ethnicity in the name, the entry will be ‘Yes’ and ‘No otherwise’
Coll_BSN:Coll_NA	Specific college; 10 separated columns	1-‘No’; 2-‘Yes'	Factor with 2 levels; if the variable ‘College’ is equal with the college in the name, the entry will be ‘Yes’ and ‘No otherwise’
![image](https://github.com/SirMore/Data-Visualization/assets/10974475/6806e659-bb89-401d-9892-ed443cd5065c)



- 
- 
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
