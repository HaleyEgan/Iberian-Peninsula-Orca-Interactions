# Iberian Peninsula Orca Interactions, 2022-2024
## Overview
This project began out of personal interest and passion. Living in the Puget Sound, we often have Transient and Resident Orcas nearby, and it's not uncommon to see them from shore using updates from Orca Network for tracking. During the summer of 2025, I was lucky enough to walk the Camino Portugese Litoral, walking 200 miles from Porto, Portugal to Santiago de Compostela, Spain along the coast. Learning about the Iberian coast and their local orca population inspired me to dig into the orca and vessel interactions that have been occurring in that area over the past few years. Even while I was on the Camino, two orca-vessel interactions occurred near Lisbon, resulting in the capsizing of one vessel (no one was hurt). 

## Data
This project explores a public dataset provided by the [Ocean Biodiversity Information System (OBIS)](https://obis.org/dataset/178820dc-ead7-497b-b2a2-2c8ea4d5a084), which documented 107 orca interactions entered into the [AnvaNet system](https://ipt.vliz.be/eurobis/resource?r=anavnet_orcas), from 2022-2024. The dataset contains 107 rows, one for each orca interaction, and 64 columns of variables. A full list of the dataset columns is documented in [DataCurration_Nb1.ipynb](https://github.com/HaleyEgan/Iberian-Peninsula-Orca-Interactions/blob/main/DatasetCurration_Nb1.ipynb). I decided to only use 15 columns for my data exploration and visualizations, including dates, sst, sss, latitude, longitude, bathymetry, and shore distance. 

## Notebooks
- [DatasetCurration_Nb1.ipynb](https://github.com/HaleyEgan/Iberian-Peninsula-Orca-Interactions/blob/main/DatasetCurration_Nb1.ipynb) - in this notebook I examine each column to understand the importance of each variable, and whether or not to keep it in my final dataset.
- [DataExploration_Nb2.ipynb](https://github.com/HaleyEgan/Iberian-Peninsula-Orca-Interactions/blob/main/DataExploration_Nb2.ipynb) - in this notebook I perform in-depth data exploration and try to unearth trends/patterns in the data.
- [MapVisualization_Nb3.ipynb](https://github.com/HaleyEgan/Iberian-Peninsula-Orca-Interactions/blob/main/MapVisualization_Nb3.ipynb) - in this notebook I use plotly to plot orca interactions and the associated data on a map for better visualization and exploration.

## Data Exploration
![month v year](https://github.com/HaleyEgan/Iberian-Peninsula-Orca-Interactions/blob/main/Images/Interactions%20by%20Month%20and%20Year.png)

<br>

![orca interactions heatmap](https://github.com/HaleyEgan/Iberian-Peninsula-Orca-Interactions/blob/main/Images/orca%20interaction%20heatmap.png)

I was surprised to see orca and human interactions off the Iberian peninsula throughout the entire year, because the orcas tend to be around the Iberian peninsula in spring and summer, and then move further away during the winter months. The only month that consistantly sees no orca interactions (with this dataset) is January. Though summer months are the most common months for an interaction, from June-September being the most common. In 2022, most interactions were in the latter half of the year, from July-December, while in 2024 interaction were common in the earlier part of the year from February-September. Most interactions occurred in 2023, and were steady throughout the entire year except for January, May, and September.

<br>

![sst v interactions](https://github.com/HaleyEgan/Iberian-Peninsula-Orca-Interactions/blob/main/Images/sst%20v%20orca%20interactions.png)
![sss v interactions](https://github.com/HaleyEgan/Iberian-Peninsula-Orca-Interactions/blob/main/Images/sss%20v%20orca%20interactions.png)

The drop in temperature and salinity in September is likely due to seasonal upwelling. There also doesn't appear to be any obvious link between sea temperature/salinity and orca interactions.

<br>

![bathymetry](https://github.com/HaleyEgan/Iberian-Peninsula-Orca-Interactions/blob/main/Images/bathymetry%20v%20orca%20interactions.png)
There doesn't appear to be an obvious pattern between water depth and orca interactions. If orcas preferred to interact with vessels at a particular depth, the red plotted line would be more linear. Some months see a high number of interaction at low depths, while other at high depths. There's also no clear pattern from month to month and months across the years.

<br>

![shore distance v interactions](https://github.com/HaleyEgan/Iberian-Peninsula-Orca-Interactions/blob/main/Images/shore%20distance%20v%20orca%20interactions.png)
Again, there's no obvious pattern between orca interactions and shore distance. However, one interesting trend in 2023 was most interactions during the summer months occurring between 15000 and 20000 meters from shore.

<br>

![correlation matrix](https://github.com/HaleyEgan/Iberian-Peninsula-Orca-Interactions/blob/main/Images/correlation%20matrix.png)

The main variables the show a strong correlation are 'sst' and 'sss' vs 'decimalLatitude'. The correlation is negative, suggesting that as latitude increases, sst and sss would decrease, and visa versa. Interestingly, 'sst' and 'decimalLongitude' appear to be highly correlated. 'sss' and 'sst' also have a very strong positive correlation. The correlation coefficients also indicate that there's no clear correlation between the different metrics we have in our data, and orca interactions.

It's quite possible that orca interaction relate to other variables that are not in this dataset, such as blue-fin tuna abundance/location, quantity of vessels in the water, type of vessels in the water, age of orcas or specific pods, weather events, etc. There is data and exploration on some of these topics (such as age and individual orcas involved), but not in this dataset. It would be interesting to add this data to our dataset if it can be aquired.

<br>

