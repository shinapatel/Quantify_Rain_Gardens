# Quantify_Rain_Gardens
UROP 2023-2024 Digital Water Lab Research Project

The goal of this project is to determine the variation in rain garden efficiency over time as modeled on a first order exponential decay function.

## Background
Highly dense, hard impervious surfaces prevent stormwater absorption into the ground. This causes excess stormwater (run-off) to drain into nearby bodies of water, picking up pollutants along the way. This form of water pollution can be resolved using rain gardens--a form of green infrastructure (GI) intended to solve urban water systems. To track rain garden efficiency, the Digital Water Lab has deployed +30 GI sensors within different rain gardens in the Detroit area. Each GI sensor reports the water drawdown rates (water depth over time) following a storm, whose efficiency is quantifiable using a first-order exponential decay function to estimate the exponential decay coefficient, α.

## Methods
# Removing Erreoneous Data
To clean the data receieved from GI sensor's, a multistep algorithm was implemented. Any minor negative water depth (m) values attributed to sensor drift and outliers in the data that exceed 2 standard deviations of the mean are removed.

# Storm Segmentation
