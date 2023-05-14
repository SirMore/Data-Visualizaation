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


