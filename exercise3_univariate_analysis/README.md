# Exercise 3 – Univariate Analysis

Course: Analysis and Visualization of Complex Agro-Environmental Data

## Objective
Analyze the distribution of Annual Mean Temperature (`temp_ann`) across the four catchments with the largest number of fish sampling sites.

## Dataset
EFI+ Mediterranean dataset.

## Visualizations
The following univariate plots were created:

- Strip plots
- Histograms
- Boxplots

Each visualization compares temperature distributions among the selected catchments.

## Additional Analysis
A simulation was performed using random sampling with replacement to explore how the mean temperature estimate stabilizes with increasing sample size.

Sample sizes tested:
10, 50, 100, 150, 200, 250, 300, 500, 1000

1000 samples were generated for each sample size.

## Tools Used
Python libraries:

- pandas
- numpy
- matplotlib
- seaborn