# Citibike Strategic Analysis Dashboard in Tableau

# Bikeshare Program Strategic Growth Analysis & Visualization

<p align="center">
<img src="https://github.com/kennethcandersen/Citibike-Strategic-Analysis-Tableau/blob/main/citibike_dashboard_tour.gif" width="900"/>
</p>

## Project summary 

### Project Goal
Create a dashboard in Tableau for New York City's Citibike stakeholders that demonstrates the evolution of the system and strategic trends for future develoment.

### How to View the Visualization 
Options:
1. Download the "Citibike Analysis.twbx" file and open in Tableau. 
2. View the visualizaiton online at [https://public.tableau.com/views/CitibikeDraft/TheStory?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link](https://public.tableau.com/views/CitibikeDraft/TheStory?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link).

## Executive Summary
<p align="center">
<img src="https://github.com/kennethcandersen/Citibike-Strategic-Analysis-Tableau/blob/main/executive_summary.png" width="900"/>
</p>

## Original data Sources 
The original data can be found in the following links: 
- [**Ecobici CSV**](https://www.ecobici.cdmx.gob.mx/es/informacion-del-servicio/open-data): ECOBICI trip information by month. Files can be downloaded as CSVs. 
- [**Ecobici API**](https://www.ecobici.cdmx.gob.mx/es/informacion-del-servicio/open-data): The ECOBICI API has information about the 480 stations ( station name, station id, location). 
- [**Open Data Mexico City: Colonias**](https://datos.cdmx.gob.mx/dataset/coloniascdmx): Information about the neighborhoods in Mexico City. We used the "coloniascdmx.csv" file to trace the Colonia boundaries on our map visualizations. 

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

## Preview 🚲
You can move freely around the webpage, so we invite you to explore the data! You can use the navbar, get different information to populate, graphs, tables and maps or whatever you prefer! Have fun!

![image](https://github.com/mgeffroy/P2-Ecobici_insights_and_recommendations/blob/main/static/Images/ecobici_tour_gif.gif)


## Conclusion summary 
- Most Ecobici users are men.
- Most users are in the 20-40 age range. 
- Some stations have traffic and in some areas some are underused. 
- Stations with more traffic are close to metro stations and supermarkets. 





Strategic data analysis and visualization of the Citibike's evolution and future growth in Tableau.
