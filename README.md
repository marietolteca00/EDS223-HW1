-   Author: Marie Tolteca, Student at Bren School of Environmental Science and Management, Masters in Environmental Data Science

Data Source: EJScreen: Environmental Justice Screening and Mapping Tool to grab dataset to map Ventura County. The Ventura County GIS data was used to add labels to the map to better identify the cities. A polygon was added to better identify the cities using Ventura County GIS.

Dataset: <https://drive.google.com/file/d/1nG6Nj1bXfzQFOVMO8Km3eNy4SWu1YcIQ/view>

Dataset Citation:

-   United States Environmental Protection Agency. 2015. EJSCREEN. Retrieved:\
    www.epa.gov/ejscreen

-   United States Environmental Protection Agency. 2015. EJSCREEN. Retrieved:\
    <https://pedp-ejscreen.azurewebsites.net/> For Ventura County City Labels and Boundaries

-   County of Ventura ITSD GIS Division. April 23, 2024. <https://venturacountydatadownloads-vcitsgis.hub.arcgis.com/datasets/city-boundary/explore>

-   **Objectives:**

-   Find an environmental issue, build a map.

-   Practice manipulating vector and raster data to build multi-layer maps.

-   Practice making maps in R, specifically using a package called 'tmap'.

This project explores an **environmental justice issue** in Ventura County, California, using data from **EJSCREEN (2023)**. The focus is on the relationship between **low-income populations** and **air pollution (Particulate Matter 2.5)** levels.\
The goal is to visualize and interpret patterns that may indicate environmental inequities in exposure to air pollution.

## Overview

This project explores an **environmental justice issue** in Ventura County, California, using data from **EJSCREEN (2015)**. The focus is on the relationship between **low-income populations** and **air pollution (Particulate Matter 2.5)** levels.\
The goal is to visualize and interpret patterns that may indicate environmental injustice in exposure to air pollution.

------------------------------------------------------------------------

## Workflow

1.  **Required Packages for this Project**
    -   Load `tidyverse`, `sf`, `tmap`, `here`, and `dplyr` for data manipulation, spatial analysis, and map visualization.
2.  **Load Data**
    -   Read in EJSCREEN data (`EJSCREEN_2023_BG_StatePct_with_AS_CNMI_GU_VI.gdb`) and city boundary shapefiles(`City_Boundary.shp`).
3.  **Filter to Region of Interest**
    -   Filter the EJSCREEN dataset to **California** and further subset to **Ventura County**.
4.  **Select Variables**
    -   `P_LOWINCPCT`: Percentile of low-income population\
    -   `PM25`: Average concentration of fine particulate matter (air pollution)
    -   Use `EJSCREEN_2023_BG_Columns.xlsx` to view the acronyms of each variable
5.  **Maps using `tmap`**
    -   **ventura_low:** Visualizes low-income populations across Ventura County. I
    -   **ventura_pm25:** Visualizes PM2.5 concentrations in the same area.\
    -   **CA_lowincome:** Visualizes low-income percentile across California and Air quality risk of cancer. For each map there is an interpretation underneath.
6.  **Saving Figures**
    -   Export maps as `.jpeg` files into the `figs`.
7.  **Interpret Results**
    -   Comparing both maps `ventura_low` and `vnetura_pm25` (e.g., North Oxnard, Santa Paula) with both high low-income populations and higher PM2.5 levels, highlighting potential **environmental justice concerns**.
8.  **For Fun- Visualization**
    -   Created a statewide map showing low-income populations and air toxic cancer risk across California for broader context.

------------------------------------------------------------------------

## Outputs

-   `ventura_low.jpeg`: Map of low-income population in Ventura County
-   `ventura_pm25.jpeg`: Map of PM2.5 air pollution in Ventura County
-   `CA_lowincome.jpeg`: Bonus statewide comparison map

------------------------------------------------------------------------

## Interpretation of Both Maps

The maps reveal that lower-income communities in Ventura County—particularly around Oxnard and Santa Paula are more exposed to fine particulate matter (PM2.5). This spatial overlap suggests an ongoing **environmental justice issue**, where socioeconomic disadvantage coincides with poorer air quality. The visualization provides evidence that supports further research or policy attention to address air pollution inequities in the region.

------------------------------------------------------------------------

## Reproducibility

All analysis was conducted in **R studio** using the **tmap** package for visualization. Code is contained in the `EDS223-HW1.qmd` file, and outputs are saved in the `figs` directory.
