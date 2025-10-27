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

![orca interactions heatmap](https://github.com/HaleyEgan/Iberian-Peninsula-Orca-Interactions/blob/main/Images/orca%20interaction%20heatmap.png)

![sst v interactions](https://github.com/HaleyEgan/Iberian-Peninsula-Orca-Interactions/blob/main/Images/sst%20v%20orca%20interactions.png)

![sss v interactions](https://github.com/HaleyEgan/Iberian-Peninsula-Orca-Interactions/blob/main/Images/sss%20v%20orca%20interactions.png)

![shore distance v interactions](https://github.com/HaleyEgan/Iberian-Peninsula-Orca-Interactions/blob/main/Images/shore%20distance%20v%20orca%20interactions.png)

![bathymetry](https://github.com/HaleyEgan/Iberian-Peninsula-Orca-Interactions/blob/main/Images/bathymetry%20v%20orca%20interactions.png)

![correlation matrix](https://github.com/HaleyEgan/Iberian-Peninsula-Orca-Interactions/blob/main/Images/correlation%20matrix.png)

