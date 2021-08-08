# Citibike Strategic Analysis Dashboard in Tableau

<p align="center">
<img src="https://github.com/kennethcandersen/Citibike-Strategic-Analysis-Tableau/blob/main/citibike_dashboard_tour.gif" width="900"/>
</p>

## Project summary 

### Project Goal
Create a dashboard in Tableau for New York City's Citibike stakeholders that demonstrates the evolution of the system and strategic trends for future develoment.

### How to View the Visualization 
Options:
1. Download the ["Citibike Dashboard.twbx"](https://github.com/kennethcandersen/Citibike-Strategic-Analysis-Tableau/blob/main/Citibike%20Dashboard.twbx) file and open in Tableau. 
2. View the visualizaiton online at [Tableau's website](https://public.tableau.com/views/CitibikeDashboard_16283828004620/TheStory?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link).

## Executive Summary
<p align="center">
<img src="https://github.com/kennethcandersen/Citibike-Strategic-Analysis-Tableau/blob/main/executive_summary.png" width="900"/>
</p>

#### Conclusions
1. **Overall ridership was growing until the pandemic,** although the growth rate YoY has been decreasing since 2016. 
2. **The average number of rides per station remained relatively stable,** despite the aggressive expansion in stations.
3. **Women remain underrepresented among ridership.** But there is progress: in 2020 women represented 28.4% of riders, versus 20% in 2013.  In peak months it reaches over 30%.
4. **The percentage of Short-Term Customers has been increasing the last few years to over 25% of the overall user base.** Short-Term Customer use is highly seasonal, likely representing summer time tourism.
5. **The average rider age is now 41 years old, versius 38 in 2013.** The 2 age groups that increased in overall rider percentage are from ages 50- 59 and 60-69. This could be good news (the program is attracting a diversity of ages) or potentially bad news (the user base is aging and the program is failing to attract younger riders). More evaluation is needed. 
6. **Rider intensity is greatest in Central to Southern Manhattan.** All top-20 stations are located there. Although the system has grown substantially over the years, Manhattan remains the main hub of ridership. 

## ETL process 
#### Extract
- Raw CSV data files were downloaded from Citibike's open data website at https://www.citibikenyc.com/system-data. Usage data was available by month. 
#### Transform
- All of the monthly CSV files were cleaned and concatenated (merged) using Python and Pandas in Jupyter Notebook in order to export one master data file. It had 122 million rows and weighed 22GB. 
- Given the size of the dataset, I created a subset of one in hundred, resulting in a sample of 1.2 million data points and weighed 250MB.
- That file is still too large to store in GitHub. You can view a "one in thousand" dataset just to see how the data was structured, although this file was not used for the visualization. 
- 
#### Load
- Data was loaded into Tableau as one master CSV file and the dashboard was created. 

## Languages & Tools Used
- Python, Pandas and Jupyter Notebook for the data extraction & cleanup 
- Tableau Public for the visualization
