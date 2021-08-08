# Citibike Strategic Analysis Dashboard in Tableau

<p align="center">
<img src="https://github.com/kennethcandersen/Citibike-Strategic-Analysis-Tableau/blob/main/citibike_dashboard_tour.gif" width="900"/>
</p>

## Project summary 

### Project Goal
Create a dashboard in Tableau for New York City's Citibike stakeholders that demonstrates the evolution of the system and strategic trends for future develoment.

### How to View the Visualization 
Options:
1. Download the "Citibike Analysis.twbx" file and open in Tableau. 
2. View the visualizaiton online at [Tableau's website](https://public.tableau.com/views/CitibikeDashboard_16283828004620/TheStory?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link).

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
<div class='tableauPlaceholder' id='viz1628383085444' style='position: relative'><noscript><a href='#'><img alt='Usage Trends ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Ci&#47;CitibikeDashboard_16283828004620&#47;TheStory&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='CitibikeDashboard_16283828004620&#47;TheStory' /><param name='tabs' value='no' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Ci&#47;CitibikeDashboard_16283828004620&#47;TheStory&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='en-US' /><param name='filter' value='publish=yes' /></object></div>                <script type='text/javascript'>                    var divElement = document.getElementById('viz1628383085444');                    var vizElement = divElement.getElementsByTagName('object')[0];                    vizElement.style.width='100%';vizElement.style.height=(divElement.offsetWidth*0.75)+'px';                    var scriptElement = document.createElement('script');                    scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';                    vizElement.parentNode.insertBefore(scriptElement, vizElement);                </script>
