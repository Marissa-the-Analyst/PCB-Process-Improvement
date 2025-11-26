# PCB-Process-Improvement
My final SNHU project explores the fictional problem that many businesses would hate to find themselves in. Not only is there an increase in demand, but there's also an increase in defects! Tasked to address these issues with raw defect data from a quality assurance team, I identify problem areas and provide actionable next steps based on the exploratory analysis.

### The Scenario ###
There has been an unacceptable rise in welding defects on the electronic boards associated with Thru-Hole placement and soldering from the Manual Finish area. These defects fail industry standard acceptability requirements, and the associated cost of rectifying the defects post-production is not sustainable. To bring production within standard and meet production goals, a 20% reduction in defects and a 20% capacity increase are necessary. <br>

### Data Source ### 
This dataset was provided by the school but it should be like the data I used in this [ANOVA Test Comparison](https://www.kaggle.com/code/marissan/dat-475-anova-comparison).<br>
Here's a sample below:
<img width="873" height="250" alt="image" src="https://github.com/user-attachments/assets/6a46970f-7c36-434d-b327-10fb7fe51992" />

### Programs Used ###
- Excel for data collection and cleaning 
- Python for ARIMA testing 
- Powerbi for dashboard

### Scope of Work ###
**Deliverables**
- Fishbone Chart
- Pareto Chart
- Correlation Heatmap
- Process Improvement Dashboard

### Goals ###
I wanted to use a variety of data techniques to help narrow down the issue causing a large spike in defects. This involved identifying which models are experiencing higher defects, exploring trends among common defects, and overall narrowing the project's scope to something actionable. <br> 

A lot of this work was compiled into presentation slides; I will be using those to reflect on what I did. <br> 

### Fishbone Chart RCA ###
<img width="745" height="418" alt="image" src="https://github.com/user-attachments/assets/5444453e-8ffb-4e56-99ca-ee38ce0033d6" /> <br>

This is a fishbone style chart. Considered one of the Seven basic quality tools, it is used to identify all possible causes for a problem and works as an exercise to sort these issues into categories (What is a fishbone diagram? Ishikawa Cause & Effect Diagram | ASQ 2025). After doing research on PCB machines, I was able to identify common points of failure in broader categories such as machine, alignment, solder, and components. After unpacking all of that though, I was able to narrow it down even further by highlighting the broader areas of interest such as the wave soldering machine itself and component placement on the board and conveyor.  

### Pareto Charts ###
<img width="795" height="426" alt="image" src="https://github.com/user-attachments/assets/404cdb19-205d-4781-a2de-3f8418c705e8" /> <br>
Pareto charts are useful for identifying the categories that have the most impact overall. For instance, if you’re trying to reduce spending, you’d want to see the biggest impacts on said spending. For our scenario, we can see that there are about 7 categories of defects that have the largest impact on our overall defect rate. I chose to focus on the top 4 for this project. I also created similar Pareto charts for defecting models and broke those down into model specific defects. <br>

### Anova — Top 3 Model Defects ###
Another assignment using the same dataset had us compare the top three models to see if there were any significant statistical differences between them. This process is usually conducted with numerical data. Given the dataset, I only had categorical and had to operate using defect counts. This process is detailed in my [ANOVA Kaggle Workbook](https://www.kaggle.com/code/marissan/dat-475-anova-comparison).
<br>

<img width="800" height="349" alt="image" src="https://github.com/user-attachments/assets/e8496cfc-3a77-4ea7-9ced-9e34a3a72090" /> <br>
Here is a snip of those results indicating that there are no statistically significant differences between the counts of the models. 

### Heatmap ###
<img width="798" height="408" alt="image" src="https://github.com/user-attachments/assets/9951ec92-c465-4d5c-9ca6-24fd2817c2c0" /> <br>
Because we were unable to narrow the scope to one specific model out of the top 3, I created this heat map in python. This heatmap allows us to identify any overlapping defects across models as well as which models have the highest defects. I highlighted these areas in blue so the stakeholders can see that Model0-195 has the largest contribution, but to target the other two models as well, it’d be easy to focus on the “reversed component” defect.  <br>

### Process Improvement Dashboard ###
The scenario now suggests that the stakeholders are on board and would like a comprehensive dashboard visualizing these findings. I took inspiration from the PowerBI dashboards I’ve seen at my supply chain job. A lot of those centers around: 
- Where are we in relation to our goal? 
- What are we pacing? 
- Are we making progress? <br>
I took that to heart here. The Top 3 Defecting Models and Total Defects versus Goal reflect immediate easy to understand metrics. Considering the manager would also want to know if any shifts are performing better/worse in relation to defects, I added a bar chart with a goal reference line. If each shift hits that goal, we’d meet the overall defect goal for the building. In the bottom left, I was certain we’d want to continue monitoring which defect types were having the biggest impact, especially as we implement preventative interventions. These are listed here in a bar chart as well. With a helpful legend that breaks those bars into model types. Finally, using inspection weeks, we are able to see if these interventions continue with a downward trend in defects or if our implementations aren’t effective.   

### Overall Recommendations ###
<img width="805" height="435" alt="image" src="https://github.com/user-attachments/assets/ababaedc-cde1-49e7-8de5-2ca596d151d9" /> <br>
In conclusion, given the analysis, I recommended proceeding with a thorough investigation of the component alignment and solder tank configuration settings for our top three defecting production models. I’ve provided detailed areas of interest below each significant area. These recommendations target areas that will have the biggest impact on production defect rates. After resolution implementation, utilizing the dashboard provided will continue to provide actionable insights for many years to come. Using this dashboard shines a light on future opportunities in a way everyone from production line workers to executive level stakeholders can understand. These recommendations and tools will give us a clear roadmap to reducing our defect rate by 20% and even increasing our production rate by 20% to meet the demand of our customers. 

### Opportunities & Reflection ###
Frankly, the data for this project sucked haha. The data did not change based on each change in scenario and if I could’ve dug into more specific data on the defects or even have more details on each defect itself, I would’ve been able to provide a better analysis. However, there are a few opportunities for improvement here. I didn’t fully understand the PCB wave soldering process. I did a lot of external research, and I believe in a few areas I mixed basic soldering and wave soldering up. In a real-world setting, I’d have more direct access to people who are familiar with the process and could ask questions. Additionally, the dataset was generated by quality assurance team members. Having a dictionary of their descriptions of defects would have been very helpful to ferret out exactly what each defect meant. What on earth does “no property assembled” mean? I wasn’t even provided a diagram of the pcb board that was manufactured.  I also didn’t account for z factors where a different defect could be causing the one I’m looking at. These challenges emphasized the importance of understanding the subject matter. <br>
Data visualization wise though, I enjoyed many parts of this project. Creating a dashboard from scratch using the provided data required me to be creative. I thoroughly enjoyed working on this project! <br>

### References ###
What is a fishbone diagram? Ishikawa Cause & Effect Diagram | ASQ. asq. (2025). https://asq.org/quality-resources/fishbone 



 
