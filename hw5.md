---
layout: page
title: License Visualization
---

# License Data Visualization

## Plot 1: Distribution of License Types

<div id="vis1"></div>

## Plot 2: Interactive License Status Filter

<div id="vis2"></div>

<script src="https://cdn.jsdelivr.net/npm/vega@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-lite@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-embed@6"></script>

<script>
vegaEmbed("#vis1", "chart1.json");
vegaEmbed("#vis2", "chart2.json");
</script>

---

## Plot 1

This visualization shows the distribution of license types in the dataset. The x-axis represents License Type (nominal), and the y-axis represents the count of records (quantitative). A bar chart is used because it effectively displays categorical frequencies. Color is mapped to License Type to distinguish categories. The data transformation applied is aggregation using count() to summarize the number of records for each category.

---

## Plot 2

This visualization shows the distribution of license types filtered by License Status. The x-axis represents License Type (nominal), and the y-axis represents count (quantitative). Color is again mapped to License Type for consistency. A filtering transformation is applied using a selection parameter to dynamically subset the data based on the chosen License Status.

---

## Interactivity

Interactivity is implemented using a dropdown selection bound to the License Status field. When a user selects a status, the chart updates to display only the corresponding subset of data. This improves clarity by allowing users to explore differences across categories without overcrowding the visualization.

---

## Data

[The Data](https://github.com/UIUC-iSchool-DataViz/is445_data/raw/main/licenses_fall2022.csv)

---

## Analysis

[The Analysis](https://github.com/Bingqing-L/Bingqing-L.github.io/blob/main/Workbook.ipynb)
