# A-Bottom-Up-Citywide-Electrification-Impact-Study

“emissions from buildings — primarily for heat and hot water — account for more than a quarter of the nation’s emissions. In New York City, it’s roughly 70 percent, and under a 2019 city law, most large buildings have to drastically reduce their numbers starting in 2024. If they exceed their emissions limits, they will be fined” - An Oily Challenge: Evict Stinky Old Furnaces in Favor of Heat Pumps - The New York Times


This research proposal will address the Climate Leadership and Community Protection Act (CLCPA) mandate for a 40% reduction in greenhouse gas (GHG) emissions in New York City by 2030. Building emissions account for two-thirds of total GHG emissions in NYC, a large proportion of which are residential. There are a lot of unknowns when it comes to residential energy use in NYC, as it involves a large variety of building types leading to uncertainty in planning for energy transition at the local level. To address these challenges, this research proposal aims to integrate Building Energy Modeling and Spatial Analytics / Data science to develop a bottom-up approach for local area decarbonization planning to meet CLCPA goals. By analyzing energy consumption data in conjunction with information about building characteristics, we can gain insights into the design and operation of buildings and evaluate the energy efficiency of different types of buildings. We can also estimate the potential changes in emissions resulting from shifts in end-use profiles and the adoption of electric alternatives. The results of this study will help identify specific buildings that could play a key role in helping the city reach its GHG reduction goals and inform the development of a more sustainable and efficient energy transition strategy in New York City.

### Independent Study Description

This independent study will provide an energy transition roadmap for New York City buildings to contribute to city/state energy or emissions targets. The research will contribute to Groundwork Data's mission of using the latest tools in spatial data science, machine learning, and data visualization to power a clean, equitable, and resilient energy transition. We aim to create an interactive modeling and analytics tool that guides New York City's long-term energy policies and helps in meeting its carbon goals.

1. The Study will address the following Research Questions:
2. How can clustering algorithms be used in geospatial analysis to identify patterns in the end-use of natural gas in residential buildings in a specific region, and what are the implications for building energy efficiency and greenhouse gas emissions?
3. What are the key considerations and approaches for planning and implementing city-scale energy transitions?
4. What are some scalable interventions that can be implemented to decarbonize building emissions in New York City beyond electrification?
5. How can we use spatial data science to determine the most appropriate areas for transitioning their end uses?
6. How can data from NREL ResStock and ComStock datasets be used to estimate energy transition for NYC buildings?
7. How can NYC open data (parcel and energy use data) be used to profile New York City's building stock to help with citywide electrification?

### Data Collection and Preprocessing

1. The National Renewable Energy Laboratory's (NREL) Residential Stock Characterization (ResStock) database contains detailed information on the characteristics of residential buildings in the United States. The data in the ResStock database is self-reported by building owners and covers various building types, including single-family homes, multi-family homes, and manufactured homes. The database includes information on demographic characteristics (age, size, and location of the building), building envelope (type and age of the building's insulation, windows, doors, and roof), heating, and cooling systems, appliances and electronics, water heating, lighting, and other energy-related characteristics. Some preprocessing steps to prepare data for analysis will include:
- To visualize the spatial distribution of the buildings in the study area, we will geocode the location of each building using the building's address, city, state, and zip code. We will use the Google Maps API and ESRI ArcGIS geocoding services to convert the building's address into latitude and longitude coordinates and plot the building locations on a map
- The NREL ResStock dataset provides information about end-use load profiles in 15-minute intervals, allowing for a detailed analysis of energy use over time. To understand the peak daily energy demand, we will aggregate the energy consumption data for various end uses (such as heating, cooling, appliances, and lighting) and use this information to calculate the peak demand for each building in the database. This peak demand data will be critical for understanding the energy demands of the buildings and identifying opportunities for improving energy efficiency.
2. Local Law 84 (LL84) data is the ground truth energy and water consumption data for buildings over 25,000 Square Feet. In contrast, the NREL ResStock and CompStock data are modeled energy consumption data for all buildings, irrespective of size. We will check the accuracy of NREL ResStock data for buildings covered under LL84 to check the validity of energy modeling data used in stock
3. The MapPLUTO data set is a comprehensive collection of geographic and tax assessment data for properties in New York City. It includes information on the location, size, and use of each property, as well as data on the zoning, land value, and tax assessment of each property
4. To gain a more comprehensive understanding of energy consumption patterns and their potential impact on equity, we will collect data from both the US micro-census and satellite sources. Demographic information will be considered as we design strategies for energy transition, as some neighborhoods may be better equipped to handle investments in energy upgrades. Using a combination of these data sources, we aim to approach the issue of energy consumption from a nuanced and equitable perspective

### Study Design and Analysis

1. The NREL ResStock data set is a valuable resource for understanding energy consumption patterns in residential buildings, but the data can be difficult to interpret in its raw form. To improve the usability of the data set, we will create a user-friendly dashboard that allows users to easily access and explore the data. The dashboard will include data visualization and mapping tools, filtering and aggregation options, and comprehensive documentation. We will use Tableau to build interactive dashboards.
2. To study the patterns of natural gas end-use in NYC, we will use a contiguous clustering approach in ArcGIS. In addition to NREL ResStock data on natural gas consumption, building type, and location, we will use census data on equity, education, and minority population. Next, we will use contiguous clustering to group these buildings into clusters based on their natural gas consumption and proximity to one another. Finally, we will analyze the characteristics of each cluster to identify patterns to understand how building type, equity, and location contribute to natural gas consumption patterns in the city and to identify areas that may be candidates for targeted energy efficiency interventions
3. Spatial mapping, energy modeling, and analysis tool showing hyperlocal energy usage and building characteristics data at the land parcel level. For each land parcel, the tool will provide:
- Energy Upgrade recommendations, including cost and potential GHG Impact
- Google Street View showing building facade and roof to show potential for insulation upgrade and availability of space for equipment such as heat pump
- Filtering criteria showing the percentage of GHG emissions reduction at the city scale, building types, type of heating fuel, age, location, etc
The idea of the tool is to provide city officials and policymakers with multiple routes to achieve the CLCPA emissions goal. Additionally, community leaders and building owners can derive insights from the tool before investing in expensive building upgrades.
