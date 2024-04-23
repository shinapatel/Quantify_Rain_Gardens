# Quantify_Rain_Gardens
UROP 2023-2024 Digital Water Lab Research Project

The goal of this project is to determine the variation in rain garden efficiency over time as modeled on a first order exponential decay function.

## Abstract
Rapid urbanization and climate change are driving urban flooding and sewer overflows in cities around the world. Concrete, asphalt, and other impervious surfaces prevent rainfall from absorbing into the ground, resulting in stormwater runoff. In order to manage stormwater, green infrastructure (GI) such as rain gardens are implemented to capture runoff. To determine the efficiency of rain gardens over time, the Digital Water Lab has deployed 33 GI sensors in the Detroit metro area to measure water drawdown rate (water depth over time) following storms. In this project, we initially model GI drawdown with a first-order exponential decay function, which is directly quantified by an exponential decay coefficient, α. Then, through hyperparameter tuning, we determine the best model fit for each sensor and examine how rain garden efficiency varies over time. Quantifying rain garden efficiency will support the further implementation of green infrastructure to improve urban stormwater management and reduce flooding.

## Background
Impervious surfaces prevent stormwater absorption into the ground, causing excess stormwater (runoff) to accumulate. Such runoff collects pollutants as it drains into nearby bodies of water. This water pollution can be resolved using rain gardens–a type of green infrastructure (GI) to improve urban water systems. To track rain garden efficiency, the Digital Water Lab (DWL) deployed 33 GI sensors within different rain gardens in the Detroit area. Each GI sensor reports the water drawdown rates (water  depth over time) after a storm. Rain garden efficiency is quantifiable using a first-order exponential decay function to estimate the exponential decay coefficient, α. 

## Methods
### Removing Erroneous Data
To clean the data receieved from GI sensor's, a multistep algorithm was implemented. Any minor negative water depth (m) values attributed to sensor drift and outliers in the data that exceed 2 standard deviations of the mean are removed.

![Clean time series data](https://github.com/shinapatel/Quantify_Rain_Gardens/blob/main/overlay_clean_data.png)
Here, the erroneous data (blue) are removed, resulting in the clean time series plot (orange).

### Storm Segmentation
To identify a distinct storm event, I modeled the drawdown rate to a first-order exponential decay. Drawdown rate indicates how the rate of stormwater absorption over time changes, quantifying a rain garden’s performance. 

## Results