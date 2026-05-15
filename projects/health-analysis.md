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
vegaEmbed('#chart1', '/projects/health-analysis/chart1_map.json');
</script>

The choropleth map reveals a strong geographic pattern in health outcomes across U.S. counties. When switching between obesity, diabetes, and hypertension, counties in the southern region, particularly Mississippi, Alabama, Louisiana, and West Virginia, consistently appear in the darkest shades, indicating prevalence rates often exceeding 35–45%. 

In contrast, counties in the West and Northeast generally appear in lighter colors, with many regions showing prevalence levels closer to 20–30%. This pattern remains stable across multiple health indicators, suggesting that the differences are not driven by a single condition but reflect broader regional health disparities.

Overall, the map highlights a clear geographic divide: the southern United States experiences significantly worse health outcomes compared to other regions, pointing to systemic regional inequalities in public health.

---

## Context 1: State-Level Differences

<div id="chart2"></div>

<script>
vegaEmbed('#chart2', '/projects/health-analysis/chart2_state_obesity.json');
</script>

The state-level comparison highlights the magnitude of differences in obesity rates across the United States. States such as Mississippi (~43%), Louisiana (~42%), and Alabama (~41%) rank among the highest, while states like Colorado and the District of Columbia have rates closer to 20–25%.

This means that the average obesity rate in the highest-ranking states is nearly double that of the lowest-ranking states. Additionally, the top 10 states with the highest obesity rates are concentrated in the South and parts of the Midwest, whereas the lowest 10 are primarily located in the Northeast and West.

This contrast shows that health disparities are not only visible at the county level but are also deeply embedded at the state level, reinforcing the idea that geography plays a critical role in shaping health outcomes.

---

## Context 2: Behavior and Health Outcomes

<div id="chart3"></div>

<script>
vegaEmbed('#chart3', '/projects/health-analysis/chart3_scatter.json');
</script>

The scatter plot demonstrates a strong positive relationship between physical inactivity and diabetes rates across U.S. counties. As the percentage of adults with no leisure-time physical activity increases from around 15% to over 40%, diabetes rates also rise from approximately 6% to above 20%.

Regional patterns further reinforce this relationship. Counties in the South are concentrated in the upper-right portion of the plot, indicating both high inactivity and high diabetes prevalence. In contrast, counties in the West are clustered in the lower-left region, reflecting lower inactivity and lower diabetes rates.

This consistent upward trend suggests that physical inactivity is a strong predictor of diabetes outcomes, and that behavioral risk factors contribute significantly to the regional health disparities observed in the United States.

---

## Conclusion

Across all three visualizations, a consistent pattern emerges: geography and behavior are strongly linked to health outcomes. Southern regions consistently experience higher rates of obesity, diabetes, and related conditions, while western and northeastern regions tend to perform better. These findings highlight the importance of addressing both regional inequalities and behavioral risk factors in improving public health outcomes.

---

## Data and Code

**Health Data:**  
CDC PLACES: Local Data for Better Health  
https://data.cdc.gov/resource/swc5-untb.csv  

**Geographic Boundary Data:**  
U.S. county boundary shapefiles provided by the us-atlas project  
https://cdn.jsdelivr.net/npm/us-atlas@3/counties-10m.json   

**Python Analysis Notebook:**  
The full analysis, including data cleaning, transformation, and visualization code, is available here:  
https://github.com/YOUR_USERNAME/YOUR_REPO/blob/main/YOUR_NOTEBOOK.ipynb  

---

## Visualization Sources

All visualizations in this project were created by the author using Python and the Altair visualization library. 

The choropleth map, bar chart, and scatter plot were generated from the CDC PLACES dataset as part of the analysis workflow. The code used to generate these visualizations is included in the Python notebook linked above.

No external visualizations were used; all figures are original and reproducible from the provided code.
