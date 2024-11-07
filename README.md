# Spatial_Analysis-PTV_Coverage

## Overview
This project provides a detailed spatial analysis of public transportation accessibility and coverage within Melbourne's metropolitan area, focusing on **Statistical Area Level 2 (SA2)** and **Statistical Area Level 4 (SA4)** regions. By analyzing the distribution of train, tram, and bus stops across Melbourne, this project aims to identify areas with high accessibility, regions with multi-modal options, and gaps in coverage. The results are designed to inform urban planning and policy decisions, with a specific emphasis on improving transport accessibility and connectivity for Melbourne’s growing population.

## Datasets Used
1. **PTV/GTFS Dataset (March 2023):**
   - Provides data on stops, routes, and schedules for Melbourne’s public transportation network, including trains, trams, and buses. This dataset is essential for assessing coverage and multi-modal connectivity.
2. **Australian Boundary Data (ASGS):**
   - Supplied by the Australian Bureau of Statistics, this dataset includes statistical area boundaries at SA2 and SA4 levels. The boundaries allow for spatial aggregation of public transportation data, supporting in-depth regional analysis.

## Methodology
The analysis uses **PostgreSQL** with **PostGIS** for spatial processing, and **QGIS** for visualization. Key steps include:
1. **Data Restoration:** Importing GTFS data and ASGS boundary shapefiles into PostgreSQL.
2. **Data Preprocessing:** Filtering data to the Melbourne Metropolitan area, defining boundary polygons, adding geometry to stops, and creating consolidated tables for multi-modal analysis.
3. **Regional Aggregation:** Creating SA2 and SA4 boundary tables to enable a detailed spatial analysis across different levels.
4. **Catchment Analysis:** Calculating accessibility zones around train stations to identify areas lacking nearby transport options, enhancing understanding of multi-modal connectivity.

## Analysis and Key Findings
- **Overall Transport Coverage:** 
  - Buses cover 99.7% of SA2 regions, providing local accessibility. Trains cover 43%, mainly along commuter corridors, while trams cover 25%, concentrated around the CBD.
- **Gaps in Accessibility:** 
  - Outer areas, such as Melbourne's southeast and Mornington Peninsula, show limited transport access, with some train stations lacking bus stops within a 0.5 km radius.
- **Top Areas by Stop Count:** 
  - SA2 regions like **Wantirna South** and **Oakleigh - Huntingdale** feature high stop densities, primarily driven by bus coverage.
- **Catchment Zones:** 
  - Catchment analysis reveals that 92% of train station areas have nearby bus stops, facilitating commuter transfers, while 7% lack such integration, highlighting areas for improvement.

## Visualizations
The project includes a series of visualizations:
- **Heat Maps** for tram, train, and bus stops across SA4 and SA2 areas to show density and highlight gaps.
- **Catchment Maps** for 5 km and 7 km train station zones to assess accessibility.
- **Comparison Charts** of stop counts across modes for top SA2 regions, showing the extent of multi-modal options.

## Project Structure
- **SQL Scripts:** Contain data restoration, preprocessing, and spatial analysis steps.
- **Visualizations:** Maps and charts demonstrating findings for each transport mode.
- **Documentation:** Detailed report summarizing methodology, analysis, results, and recommendations.

## How to Run
1. Import datasets into PostgreSQL with PostGIS enabled.
2. Run SQL scripts to preprocess data and perform spatial analysis.
3. Use QGIS or a similar GIS tool to generate visualizations based on analysis results.

## Conclusion
This spatial analysis highlights the strengths and weaknesses of Melbourne’s public transport network. While buses provide widespread coverage, trains and trams have targeted reach, leaving certain areas underserved. This project underscores the need for enhanced multi-modal integration to better serve Melbourne’s diverse communities and support future growth.
