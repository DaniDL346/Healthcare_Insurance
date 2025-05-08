# Health Insurance 

**Health Insurance** is a comprehensive data analysis tool designed to analyse healthcare metrics for streamlining data exploration and visualisation. The tool supports multiple data formats and provides an intuitive interface for both novice and expert data scientists.


This [Dashboard](https://app.powerbi.com/groups/me/reports/97735ba6-f5c4-4b1c-a415-73a7d9d1dce1/324ed4c8b8ee7eaeb894?experience=power-bi) shows relationships in an interactive way between the lifestyle measures that affect the cost of insurance.
The dataset consists of lifestyle measure like age, sex, smoking status, total children, regions which can influence the insurance charges.
Some of these features are more significant to the costs than others.

For further analysis click on separate pages on left side of dashboard. The pages include general statistics, correlation, predictive model and cost insights

<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTqWlDP88eXtH5ivaYVlz5x6qn925dQe3VKew&s" width="100" height="100" /> 


## Dataset Content
* The Dataset was taken from the [Kaggel Health Insurance link](https://www.kaggle.com/datasets/willianoliveiragibin/healthcare-insurance). It is the Healthcare Insurance dataset, the location is USA and the shape of the dataset is 1338 rows by 7 columns. The size of the "insurance.csv" file is 55.63 kB. 


## Business Requirements

We were asked to investigate a health insurance dataset and create an interactive Dashboard for our client - Insurance Company, where the business executives can make decisions for insurance revenue costs.
These are the investigation questions below:

1. Personal attributes and Insurance cost   
    - How does age influence insurance charges?
    - How does smoking status affect insurance charges?
    - Does BMI correlate with higher insurance costs? Is there a threshold BMI where costs spike?
    - How does family size (no. of dependents) impact insurance costs?

2. Geographic Influence
    - Do people living in different regions (e.g., northeast, southeast, southwest, northwest) pay different average insurance premiums?
    - Are there geographic regions where smoking or high BMI is more common, thereby influencing costs?

3. Interaction Effects
    - Does the combination of being a smoker and having a high BMI lead to disproportionately higher charges compared to either factor alone?
    - Are older smokers charged even more than younger smokers, indicating an age-smoking interaction?
    - Are there differences in the impact of BMI on costs between genders?

4. Predictive Modeling
    - Can we predict insurance charges accurately based on a person’s age, gender, BMI, number of children, smoking status, and region?
    - Which features are the strongest predictors of insurance charges?

5. Cost Optimization Insights
    - What lifestyle changes (e.g., reducing BMI, quitting smoking) could significantly lower insurance costs according to the model?
    - Can we identify "high-risk" profiles where costs are extremely high? What are their characteristics?

6. What is the expected insurance cost for a non-smoking male in his 30s with a normal BMI across different regions?

7. How much more does a smoker pay compared to a non-smoker on average?

8. How much could insurance companies save by promoting smoking cessation programs?  


## Hypothesis and how to validate?
* List here your project hypothesis(es) and how you envision validating it (them)

1. Our assumption is that because the age increases, the BMI and charges increase.
   - In dashboard overview, line chart shows the relation between age, BMI and insuarance costs. The chart is interactive and clearly shows with increase in age and BMI, the insurance costs increase.
   - There are also bar charts to validate this hypothesis in 
   GenStatsPart1 and GenStatsPart2 pages.


2. The insurance charges are likely to increase based on sex, smoking status and region. The regions of Northeast and Southeast the charges are higher because they are located along the coastline and harsh weather conditions.

   - In Jupyter notebook, we created a geographical map to indicate if the location affects the insurance charges.  There are statistical tests comparing the distribution for sex, smoking status and regions. For example, Mann–Whitney U test,Kruskal–Wallis Test,t-test,Chi-square test. In the Dashboard, we have general statistics with line and bar graphs to understand the relationship of sex and smoking status.


3. Predictive Analysis
    - Descriptive Analysis:
        - Average charges by sex and smoker
        - Average charges by children
        - Average charges by age
        - Average age by BMI_Range
        - Average age by smoker and charges

4. Correlation Analysis: 

    - In Dashboard, we created a Scatterplot between sex and bmi vs count of charges and trendline plotted.

    - We created a heatmap in Jupyter notebook to determine the correlation between the variables sex, BMI and charges, and pasted in dashboard in Correlation Statistics page.

    - Heatmap in jupytper notebook clearly shows correlation coefficients are higher among variables between BMI_Range, age and smoking status


## Project Plan
* Outline the high-level steps taken for the analysis.

  - Initially we started with ETL in Jupyter notebook, once the dataset was cleaned we did some initial visualisations to understand realtions between variables and performed statistical tests. Then we loaded the clean dataset into Power BI, to continue to perform interactive visualisations.
* How was the data managed throughout the collection, processing, analysis and interpretation steps?
  - The data was downloaded from kaggle and initially checked for datatypes, columns sex, smoker and regions were encoded to numerical types and added as new columns. Duplicate row was removed. The cleaned data was then saved to csv file which then was opened in PowerBI for further analysis and interpretation.
* Why did you choose the research methodologies you used?
   - We chose the statistical tests to compare the distributions to indicate if charges varied between smoker(yes/no), sex (male vs female) and regions( northwest, northeast, southwest, southeast).


## Analysis techniques used
* List the data analysis methods used and explain limitations or alternative approaches.

    - Geographical analysis: We used plotly mapbox function to create a map of USA for all the regions(northwest, northeast, southeast and southwest) and the average charge per region. Unfortunately PowerBI could not produce a map due to basic version of PowerBI. 

    - Personal attributes and Insurance cost: We used a combination of data analysis tools in Jupyter notebook for plotting bar
    bar charts, scatterplots, line plots and correlation heatmap to understand the personal attribute and insurance costs. Statistical testing such as Mann–Whitney U test,Kruskal–Wallis Test,t-test,Chi-square test, also provided us with more insight of the distributions when comparing the variables sex, regions and smoking status. Power BI Dashboard was also used for computing bar charts, line charts, number cards, slicers and pie charts.

    - Interaction Effects: In PowerBI we used the visualisation tools on our dataset, when we select a value from our dropdown box, it allows all the visualisations to update and change which makes the experience for the user interactive.

    - Predictive Modeling: In PowerBI, we used the predictive modelling tool to produce what the next year’s forecast would be in charges for each of the variables. We also produced a visualisation of each variable output sex, age, BMI, children, smoking status and region
    - Cost Optimisation insights: We used PowerBI to created visualisations to understand cost optimisations

* Did the data limit you, and did you use an alternative approach to meet these challenges?
    - the data was already somewhat cleaned and had less datapoints for better analysis. We would need more informtion and more columns. There needed to be more null values and feature engineering to be done.
* How did you use generative AI tools to help with ideation, design thinking and code optimisation?
   -We used chatGPT, Copilot, Perplexity and Google to understand the data and its features properly and for code optimisation.

## Ethical considerations
* Were there any data privacy, bias or fairness issues with the data?

    - Were there any data privacy, bias or fairness issues with the data?
    yes, the version controlling was done with git and merging rights was with admin. the secure https was used for dashbord URL and also for the geographical map representation. There was no Bias in the data and the data was handled with absolute fairness
    * How did you overcome any legal or societal issues?
    - we followed the standard approach to dashboarding. No   person is affected with this project.

   

## Dashboard Design
* List all dashboard pages and their content, either blocks of information or widgets, like buttons, checkboxes, images, or any other item that your dashboard library supports.

   - User can navigate through 6 pages through front dashboard.

    The first page is overview where interactive dashboard is located.
    - At the middle of first page is the name of dashboard next to it's image, with little description underneath about the dashboard..
    On top left of page there is doughnut chart with Total Revenue by Region. 
    - We have 3 cards on top right corner showing Number of customers, Total Revenue and Monthly Revenue. 
    - Under those 3 cards is a slider bar to select bmi range.
    - The first  graph is interactive line chart showing average charges by average bmi and age.
    - Under the line chart is a scatter plot showing BMI vs Charges by smoking status.
    - Next to scatter plot is Area plot showing average charges by age and region.
    - Next to line chart on right is a drop down box to select age.
    -Under the drop down box is checkbox for smoking status 
    - And the last one on right down corner is checked box for regions to be selected interactively.


    -  On GenStatsPart1 page, we focused on the General Statistics, there are 4 produced plots, 
    1st plot: “Average charges by sex and smoker”, this stacked column chart describes the mean charges separated by sex and then smoking status.
    2nd plot (top right), “Average charges by children”, this line chart indicates the mean charges versus amount of children one family has. A trend line was also added.
    3rd plot (bottom left), “Average charges by age”, this line and clustered column chart indicates the mean changes versus age. A trend line was also added.
    4th plot (bottom right), “Average age by BMI_Range”, is a stacked column chart indicating the mean charges per BMI.

    - On GenStatsPart2 Page we focused on the second part of General Statistics, there are 2 visualisation plots. 
    1st plot(top): “Average age by smoker and charges”, this scatter chart plots the mean age per charges, where the colour of the dots indicate the smoking status. Light blue dots for “no” and dark blue dots for “yes”. A trend line was also added which clearly shows a direct separation between non-smokers and smokers.
    2nd plot(bottom): “Average charges by region and bmi”, is a scatter plot of the mean charges per BMI, where the colour of the dots indicate the different regions. Light blue for “northeast”, dark blue for “northwest”, orange for “southeast” and purple for “southwest”.



    - On Correlation statistics page first is scatter plot showing Count of charges by BMI and Sex under there is also an interactive table.
    On the right is a Heatmap showing correlation coefficients between different variables.

    - On Pred-model page is interactive Predictive model shows a prediction of the insurance charges based on the measures - age, sex, BMI, children, smoker and region.

    - On cost insights page first is horizontal bar chart showing average charges by BMI_Category and underneath description.


Insurance costs are affected heavily by lifestyle changed which shows: Smokers pay 2–3× more than non-smokers.
People in Obese category pay significantly more than those in Normal BMI.
on the top right is bar chart sowing average charges by smoker and under there is a High Risk bar chart.
  
* How were data insights communicated to technical and non-technical audiences?

    - For Technical audiences- we used Jupyter Notebook to demonstrate more technical statistics. In Power BI, we targeted a non-technical audience with our visualisations.

* Explain how the dashboard was designed to communicate complex data insights to different audiences. 

    - For executive customers there are overview statistics indicating total revenue, for average customers, there are drop down tools for customers to check their monthly revenue based on sex, smoking status, age, range of BMI and region

## Unfixed Bugs
* Please mention unfixed bugs and why they were not fixed. This section should include shortcomings of the frameworks or technologies used. Although time can be a significant variable to consider, paucity of time and difficulty understanding implementation are not valid reasons to leave bugs unfixed.

    - We faced software glitches and limitations while using PowerBI desktop applications. The software requires more computing power
    - The Map visualisation was not working properly in PowerBI.

* Did you recognise gaps in your knowledge, and how did you address them?
    - We recognised gaps in knowledge which we addressed through team work and through research.
* If applicable, include evidence of feedback received (from peers or instructors) and how it improved your approach or understanding.
    - All the evidences are in Github.

## Development Roadmap
* What challenges did you face, and what strategies were used to overcome these challenges?
* What new skills or tools do you plan to learn next based on your project experience? 

## Answers to Investigation Questions:

1. Personal attributes and Insurance cost
 - How does age influence insurance charges?
    - Shows direct correlation between age and insurance cost. With increase in age likely to increase the cost of insurance.

- How does smoking status affect insurance charges?
    -   Smokers are charged higher insurance than non-smokers.
 
- Does BMI correlate with higher insurance costs? Is there a threshold BMI where costs spike?
    - The BMI doesn't have a direct correlation with higher insurance costs. The BMI is the measure of the person's body weight and height.

- How does family size (no. of dependents) impact insurance costs?
    - The insurance costs decrease in families with more than 3 children.
2. Geographic Influence
    - Do people living in different regions (e.g., northeast, southeast, southwest, northwest) pay different average insurance premiums? Are there geographic regions where smoking or high BMI is more common, thereby influencing costs?
    - There are more policy holders in the southeast region adding to more revenues.
    - For non-smokers, the charge is regular, the trend line is straight line. For smokers, as soon as the BMI is above 30, the charge increases rapidly from 20k to about 33k. The region with high BMI does not indicate the significant difference in  high or low insurance costs. 

3. Interaction Effects
    - Does the combination of being a smoker and having a high BMI lead to disproportionately higher charges compared to either factor alone?

    - People with higher BMI and being Smoker tend to pay higher charges than having one factor alone.

- Are older smokers charged even more than younger smokers, indicating an age-smoking interaction?
    - There is a slight difference in cost, but it is not significant. There is a high range between low and high cost of the same age So it is hard to tell the difference in cost..

- Are there differences in the impact of BMI on costs between genders? 
     - The trend line for the cost per BMI fluctuates more with females compared to males. Females are paying more.

4. Can we predict insurance charges accurately based on a person’s age, gender, BMI, number of children, smoking status, and region?

-   Model predicts insurance charges based on features - age, sex, BMI, children, smoker and region.

-   AGE : Shows direct correlation between age and insurance cost. With increase in age likely to increase the cost of insurance.
-   SEX : The trend line for the cost per BMI fluctuates more with females compared to males. Females are paying more.
-   BMI: The BMI doesn't have a direct correlation with higher insurance costs. The BMI is the measure of the person's body we
-   CHILDREN: The insurance costs are likely to decrease in families with more than 3 children.
-   SMOKING STATUS: Smokers are charged higher insurance than non-smokers.
-   REGION: The region with high BMI does not indicate the significant difference in  high or low insurance costs.


5. Which features are the strongest predictors of insurance charges?

-  Age, smoking status and BMI are the main features that affect the insurance costs.

6. Cost Optimization Insights: What lifestyle changes (e.g., reducing BMI, quitting smoking) could significantly lower insurance costs according to the model?

-  shows smokers pay 2–3× more than non-smokers.
-  People in Obese category pay significantly more than those in Normal BMI.

- Insight:
    "Quitting smoking" and "reducing BMI to Normal" are clearly associated with significant cost savings, visible in the charts.

    




## Main Data Analysis Libraries
* Libraries used: Numpy, Seaborn, Plotly, Matplotlib, Pandas, Scipy.stats

    - We have used python numpy and pandas library for data cleaning and ETL steps.
    For data visualization, we have used matplotlib, seaborn and plotly libraries.
    For Dashboard, we used Power BI.
    For transformation and encoding, the scikit learn was used.



## Credits 

    - code institute LMS material.
    stackoverflow.
    chatGPT, Perplexity AI, Copilot.
    google searches, Power BI.


### Content 

    - The ETL and data visualization in jupyter notebook were taken from the code institute LMS content.
    The dashboard data visualisation was done in Power BI.
    Stackoverflow.
    Used chatGPT, perplexity AI, Copilot in VS Code and Power BI for some predictions.


- The text for the Home page was taken from Wikipedia Article A
- Instructions on how to implement form validation on the Sign-Up page was taken from (https://www.youtube.com/watch?v=Dk25lwdTKow&t=2448s)

### Media

    - The health insurance logo from (https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTqWlDP88eXtH5ivaYVlz5x6qn925dQe3VKew&s).
    - github for version control - (https://github.com/DaniDL346/Healthcare_Insurance).

    - Health Insurance Dashboard (https://app.powerbi.com/groups/me/reports/97735ba6-f5c4-4b1c-a415-73a7d9d1dce1/324ed4c8b8ee7eaeb894?experience=power-bi)




## Acknowledgements (optional)
      We wish to thank my facilitator Vasi, technical head Niel, our data coach John for the support during the project development.
      We also wish to thank my class colleagues Dani, Raihan, Saoni, Mohammad , Jacob and Bruno for their support.
