**UK Road Safety Data Analysis Dashboard
Project Overview**
This project is a Power BI-based analysis of Great Britain’s 2021 road casualty data (STATS19) released by the Department for Transport. It provides an interactive, multi-view dashboard to help policymakers, and the public understand factors affecting road safety. The dashboard uses over 100,000 reported accident records with attributes like location (latitude/longitude), time, severity (fatal/serious/slight), road type, weather, and light conditions. The goal is to clean and transform the raw data, create DAX measures (e.g. total and fatal accidents), and visualize patterns to inform safety decisions.

**Features**
•	Interactive Slicers and Filters: Users can slice the data by road type, date, or other fields. For example, a road-type slicer lets users filter all visualizations by selected road type, making the analysis context-specific.
•	Data Cards: Prominent KPIs (cards) show total collisions and total fatalities for 2021, providing at-a-glance severity metrics.
•	Stacked Bar Chart: Displays total accidents by road type and severity. This reveals that single carriageways had the most incidents while slip roads had the fewestfile-danhsxypl4yvxsdaddrzjk.
•	Clustered Bar Chart (Weekday Trends): Shows number of accidents by day of week. The analysis found most accidents occurred on Saturdays and least on Sundaysfile-danhsxypl4yvxsdaddrzjk.
•	Stacked Column Chart (By Police Force): Ranks the top 10 police forces by number of accidents, broken down by severity. This highlights regional hotspots of severe collisions.
•	Scatter Plot (Light vs Speed): Plots accident counts against speed limits, colored by light conditions. This visualization shows how poor light increases accident frequency, suggesting that better lighting correlates with safer roadsfile-danhsxypl4yvxsdaddrzjk.
•	Line Chart (Casualties by Day): Tracks total casualties (injuries) across days of the week, which can guide emergency response planning (peaking on weekends).
•	Geographic Map (Hotspot Map): A heatmap overlay (e.g. focused on Greater Manchester) identifies collision hotspots by latitude/longitudefile-danhsxypl4yvxsdaddrzjk. This helps prioritize locations for safety interventions.
•	Interactivity: All visuals are linked. Selecting an item in one chart (e.g. clicking a bar or map point) filters the others, allowing drill-down analysis and hypothesis testing. For example, selecting “Night” in the Light Condition filter updates all charts to show only night-time accidents.

**Installation and Setup Instructions**
1.	Get Power BI Desktop: Download and install Power BI Desktop (free) from Microsoft for Windows.
2.	Clone Repository: Clone or download this repository to your local machine.
3.	Data Files: Ensure the dft-road-casualty-statistics-collision-2021.csv file (collision data) is in the same folder as the Power BI .pbix file or update the data source path in Power BI. The CSV and code-list are provided by DfT.
4.	Open the Dashboard: Launch Power BI Desktop and open the file RoadSafetyDashboard.pbix (included in this repo). On first load, refresh the data if prompted. The report will load all visuals and data models.
5.	Enable Map Data (if needed): If the map visuals do not render, ensure Power BI can access internet maps (Bing) or update to “Shape map” settings and supply location fields.
6.	No Additional Libraries: All analysis is built-in to Power BI; no external programming environment is required.

**Example Usage**
To use the dashboard, simply interact with the visuals:
•	At the top, data cards display the grand totals (e.g. Total Accidents and Fatal Accidents).
•	Use the Road Type slicer (on the left) to filter all charts by the selected road category. For example, filtering to “Motorway” will update every visual to show only motorway data. This allows focused insights (e.g. comparing motorway vs urban road accidents).
•	Hovering over map points or bars will show detailed tooltips. Clicking on a bar or slice (for day, police force, etc.) will cross-filter the other charts. For instance, clicking on Saturday in the weekday bar chart will refresh the casualty line chart and map to only Saturday crashes. This interactivity helps answer questions like “Where do most night-time accidents occur?” or “How did weather conditions affect accidents?”.
 


**Dataset and Metadata Description**
The data come from the UK government’s STATS19 open dataset (DfT) for year 2021. It contains records of all reported personal-injury collisions on public roads, as recorded by the police. Key fields include: date, time, longitude/latitude (for mapping), accident_severity (fatal/serious/slight), number_of_casualties, road_type, weather_conditions, light_conditions, and police_force, among others. All variables are coded; the data guide (included Excel) provides code lists for translating values. This structure allows detailed filtering – for example, light_conditions is coded so the dashboard can distinguish accidents at night vs day. Because the dataset is large (~100k rows), Power BI’s data model and DAX measures are used to aggregate quickly.

**Contribution Guidelines**
Contributions are welcome! Feel free to submit bug reports or feature requests via GitHub Issues. If you wish to extend or improve the dashboard (e.g. add new visuals, update for future years, or refine calculations), please fork the repository and open a Pull Request. Ensure that data privacy and government open-data policies are respected.

