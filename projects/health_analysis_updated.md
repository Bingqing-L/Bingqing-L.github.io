---
layout: default
title: "How Healthy Is Your County?"
---

# How Healthy Is Your County?
### By Yifeng Luo & Bingqing Li

---

<script src="https://cdn.jsdelivr.net/npm/vega@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-lite@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-embed@6"></script>

---

## Introduction

Health outcomes vary widely across the United States, and these differences are not random. Using county-level data from the CDC PLACES dataset, this project explores how geographic location and behavioral factors jointly shape public health outcomes such as obesity, diabetes, and physical inactivity.

---

## Main Visualization: Health Across the U.S.

<div id="chart1"></div>

<script>
vegaEmbed('#chart1', '/projects/chart1_map.json');
</script>

The choropleth map reveals a strong geographic pattern in health outcomes across U.S. counties. When switching between obesity, diabetes, and hypertension, counties in the southern region, particularly Mississippi, Alabama, Louisiana, and West Virginia, consistently appear in the darkest shades, indicating prevalence rates often exceeding 35–45%. 

In contrast, counties in the West and Northeast generally appear in lighter colors, with many regions showing prevalence levels closer to 20–30%. This pattern remains stable across multiple health indicators, suggesting that the differences are not driven by a single condition but reflect broader regional health disparities.

Overall, the map highlights a clear geographic divide: the southern United States experiences significantly worse health outcomes compared to other regions, pointing to systemic regional inequalities in public health.

---

## Context 1: State-Level Differences

<div id="chart2"></div>

<script>
vegaEmbed('#chart2', '/projects/chart2_state_obesity.json');
</script>

The state-level comparison highlights the magnitude of differences in obesity rates across the United States. States such as Mississippi (~43%), Louisiana (~42%), and Alabama (~41%) rank among the highest, while states like Colorado and the District of Columbia have rates closer to 25-27%.

This means that the average obesity rate in the highest-ranking states is nearly 70% higher than those in the lowest-ranking states. Additionally, the top 10 states with the highest obesity rates are concentrated in the South and parts of the Midwest, whereas the lowest 10 are primarily located in the Northeast and West.

This contrast shows that health disparities are not only visible at the county level but are also deeply embedded at the state level, reinforcing the idea that geography plays a critical role in shaping health outcomes.

---

## Context 2: Behavior and Health Outcomes

<div id="chart3"></div>

<script>
vegaEmbed('#chart3', '/projects/chart3_scatter.json');
</script>

The scatter plot demonstrates a strong positive relationship between physical inactivity and diabetes rates across U.S. counties. As the percentage of adults with no leisure-time physical activity increases from around 15% to over 40%, diabetes rates also rise from approximately 6% to above 20%.

Regional patterns further reinforce this relationship. Counties in the South are concentrated in the upper-right portion of the plot, indicating both high inactivity and high diabetes prevalence. In contrast, counties in the West are clustered in the lower-left region, reflecting lower inactivity and lower diabetes rates.

This consistent upward trend suggests that physical inactivity is a strong predictor of diabetes outcomes, and that behavioral risk factors contribute significantly to the regional health disparities observed in the United States.

---

## Context 3: Poverty and Health Inequality

<div id="chart4"></div>

<script>
vegaEmbed('#chart4', '/projects/chart4_poverty_obesity.json');
</script>

This scatter plot draws on a second dataset — the U.S. Census Bureau's Small Area Income and Poverty Estimates (SAIPE) for 2021 — to explore whether poverty helps explain the geographic health disparities seen in the main map. Each point represents one U.S. county, with poverty rate on the x-axis and obesity rate on the y-axis, colored by US region. 

A clear positive relationship appears: as poverty increases from about 5% to over 30%, obesity rates also rise from around 25% to above 45%. Counties with higher poverty rates almost always have higher obesity rates.

Regional patterns are also clear. Southern counties (red) are mostly in the upper-right corner, meaning they have both high poverty and high obesity. In contrast, counties in the West and Northeast cluster in the lower-left, with lower poverty and lower obesity.

This suggests that economic disadvantage is closely connected to poor health outcomes and may help explain why the South has worse health conditions than other regions.

---

## Conclusion

Across all four visualizations, a consistent pattern emerges: geography, behavior, and economic conditions are all strongly linked to health outcomes. Southern regions consistently experience higher rates of obesity, diabetes, and related conditions, while western and northeastern regions tend to perform better.

The analysis shows that behavioral factors such as physical inactivity are associated with worse health outcomes, but economic factors also play an important role. Counties with higher poverty rates tend to have higher obesity rates, suggesting that economic disadvantage may also be a key driver behind these regional disparities.

Overall, these findings suggest that improving public health outcomes may require not only changes in individual behavior, but also broader efforts to address economic inequality.

---
## Data

[CDC PLACES Dataset (Health Data)](https://data.cdc.gov/resource/swc5-untb.csv)

[U.S. County Boundary Data (us-atlas)](https://cdn.jsdelivr.net/npm/us-atlas@3/counties-10m.json)

[U.S. Census Bureau SAIPE (Poverty Data, 2021 – Documentation)](https://www.census.gov/programs-surveys/saipe.html)

[SAIPE 2021 County Poverty Data (Direct Download)](https://www2.census.gov/programs-surveys/saipe/datasets/2021/2021-state-and-county/est21all.xls)

---

## Analysis

[Main Analysis Notebook (Charts 1–3)](https://github.com/Bingqing-L/Bingqing-L.github.io/blob/main/projects/Workbook.ipynb)  

[Poverty Analysis Notebook (Chart 4)](https://github.com/Bingqing-L/Bingqing-L.github.io/blob/main/projects/Workbook1.ipynb)

---

## Visualization Sources

All visualizations in this project were created by the authors using Python and the Altair visualization library. 

Charts 1–3 (the choropleth map, state-level bar chart, and inactivity vs. diabetes scatter plot) were generated using the CDC PLACES dataset. The code used to create these visualizations is available in the main analysis notebook:  
https://github.com/Bingqing-L/Bingqing-L.github.io/blob/main/projects/Workbook.ipynb  

Chart 4 (poverty vs. obesity scatter plot) uses an additional dataset from the U.S. Census Bureau’s Small Area Income and Poverty Estimates (SAIPE), 2021. The code used to create this visualization is available in the poverty analysis notebook:  
https://github.com/Bingqing-L/Bingqing-L.github.io/blob/main/projects/Workbook1.ipynb  

All figures are original and fully reproducible from the provided code.
