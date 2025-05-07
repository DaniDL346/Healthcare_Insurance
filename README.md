# Health Insurance   

**Health Insurance** is a comprehensive data analysis tool designed to analyse healthcare metrics for streamlining data exploration and visualisation. The tool supports multiple data formats and provides an intuitive interface for both novice and expert data scientists.

<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTqWlDP88eXtH5ivaYVlz5x6qn925dQe3VKew&s" width="100" height="100" /> 



## Dataset Content
* The Dataset was taken from the [Kaggel Health Insurance link](https://www.kaggle.com/datasets/willianoliveiragibin/healthcare-insurance). It is the Healthcare Insurance dataset, the location is USA and the shape of the dataset is 1338 rows by 7 columns. The size of the "insurance.csv" file is 55.63 kB. 


## Business Requirements
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

1. Our assumption is that because the age is increases, the BMI and charges increase.

2. The insurance charges are likely to increase based on sex, smoker status and region. The regions of Northeast and Southeast the charges are higher because they are located along the coastline and harsh weather conditions.


3. Predictive Analysis
    - Descriptive Analysis:
        - Average of age by BMI_range (plot 1)
        - Average of charges by age (plot 2)
        - Average of charges by age and region (plot 3)
        - Average of charges by sex, smoker and region (plot 4) - stacked bar chart

4. Correlation Analysis: 
Scatterplot Between sex and bmi vs charges and trendline plotted.


## Project Plan
* Outline the high-level steps taken for the analysis.
* How was the data managed throughout the collection, processing, analysis and interpretation steps?
* Why did you choose the research methodologies you used?

## The rationale to map the business requirements to the Data Visualisations
* List your business requirements and a rationale to map them to the Data Visualisations

## Analysis techniques used
* List the data analysis methods used and explain limitations or alternative approaches.
* How did you structure the data analysis techniques. Justify your response.
* Did the data limit you, and did you use an alternative approach to meet these challenges?
* How did you use generative AI tools to help with ideation, design thinking and code optimisation?

## Ethical considerations
* Were there any data privacy, bias or fairness issues with the data?
* How did you overcome any legal or societal issues?

## Dashboard Design
* List all dashboard pages and their content, either blocks of information or widgets, like buttons, checkboxes, images, or any other item that your dashboard library supports.
* Later, during the project development, you may revisit your dashboard plan to update a given feature (for example, at the beginning of the project you were confident you would use a given plot to display an insight but subsequently you used another plot type).
* How were data insights communicated to technical and non-technical audiences?
* Explain how the dashboard was designed to communicate complex data insights to different audiences. 

## Unfixed Bugs
* Please mention unfixed bugs and why they were not fixed. This section should include shortcomings of the frameworks or technologies used. Although time can be a significant variable to consider, paucity of time and difficulty understanding implementation are not valid reasons to leave bugs unfixed.
* Did you recognise gaps in your knowledge, and how did you address them?
* If applicable, include evidence of feedback received (from peers or instructors) and how it improved your approach or understanding.

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
    -   There is a slight difference in cost, but it is not significant. There is a high range between low and high cost of the same age So it is hard to tell the difference in cost..

- Are there differences in the impact of BMI on costs between genders? 
     -   The trend line for the cost per BMI fluctuates more with females compared to males. Females are paying more.




## Main Data Analysis Libraries
* Here you should list the libraries you used in the project and provide an example(s) of how you used these libraries.


## Credits 

* In this section, you need to reference where you got your content, media and extra help from. It is common practice to use code from other repositories and tutorials, however, it is important to be very specific about these sources to avoid plagiarism. 
* You can break the credits section up into Content and Media, depending on what you have included in your project. 

### Content 

- The text for the Home page was taken from Wikipedia Article A
- Instructions on how to implement form validation on the Sign-Up page was taken from [Specific YouTube Tutorial](https://www.youtube.com/)
- The icons in the footer were taken from [Font Awesome](https://fontawesome.com/)

### Media

- The photos used on the home and sign-up page are from This Open-Source site
- The images used for the gallery page were taken from this other open-source site



## Acknowledgements (optional)
* Thank the people who provided support through this project.