<h1 align="center"> USA Fatal Crashes Report (2015-2022) </h1>
<div align="center">
	<img src="/images/conversion.png">
</div>

## Topic
This project focuses on analyzing and visualizing fatal crash data in the USA from 2015 to 2022 using Power BI.
The report provides insights through various visualizations, including maps, pie charts, line charts, and summary cards.

## Background
The data for this report was obtained from the National Highway Traffic Safety Administration (NHTSA) API, 
which provides detailed crash information. The project aims to give a clear picture of crash trends across different states and over time,
helping to identify patterns and factors contributing to fatal crashes. The report includes a comparison of crash data across years and visual breakdowns of the data based on various metrics.

## Techniques & Technology Used
- **Python (Data Retrieval and Preprocessing):**
    - [Downloaded data from the NHTSA Crash API:](https://crashviewer.nhtsa.dot.gov/CrashAPI)
      - Endpoint used: `/crashes/GetCaseList?states=1,1&fromYear=""&toYear=""&minNumOfVehicles=1&maxNumOfVehicles=6&format=json`
	    - Parameters:
		  - states : [Specify the state numbers for multiple States]("/Resources/USAStates.csv")
		  - FromYear and ToYear: Mention the FromYear and ToYear to include the multiple crash years data.
		  - minNumOfVehicles and maxNumOfVehicles: Specify the number of vehicle effected by changing minNumOfVehicles and maxNumOfVehicles parameter
		  
    - A separate CSV file containing the states of the USA was used to facilitate the API loop.
    - Cleaned the data by:
        - Formatting date fields
        - Removing unwanted columns
        - Renaming columns for consistency
		
- **Power BI (Data Visualization):**
    - **Map Visual:** To display fatal crash locations across the USA.
    - **Pie Chart:** To show the distribution of fatal crashes across various factors.
    - **Line Chart:** To compare the number of fatal crashes year-over-year.
    - **Card Visuals:** For summarizing key metrics, such as the total number of fatal crashes.
    
## Summary
This Power BI report provides a comprehensive analysis of fatal crashes in the USA from 2015 to 2022. 
By utilizing both Python for data collection and cleaning, and Power BI for visualization, the report highlights key trends in fatal crashes across different states. The visual insights presented in this report can help in understanding the factors contributing to road safety issues and the year-over-year trends in fatal crashes.


## Folder Structure and Description 
- Root : Contains the USAVehicalCrashes.pbix
- Resources: This flooder contains the csv files which are used in the PowerBI report.
- JupyterNotebooks: Contains the jupyter notebook that is used to download the data from the API site.
- images : Contain the images used in the report and README.md file.


