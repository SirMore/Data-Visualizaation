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


