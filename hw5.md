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

This visualization shows the distribution of license types in the dataset. The goal is to understand which types of licenses appear most frequently. The x-axis represents License Type, which is treated as a nominal variable (:N) because it consists of unordered categories. The y-axis represents the count of records, which is a quantitative aggregation showing how many entries fall into each category. A bar chart is used because it is an effective way to compare frequencies across categorical groups.

In terms of design choices, color is also encoded using License Type (:N). This helps visually distinguish different categories and improves readability, especially given the large number of license types present. Although color is not strictly necessary for a bar chart, it enhances the ability to differentiate categories quickly when scanning the chart.

The primary data transformation applied in this visualization is aggregation using count(), which summarizes the number of records per license type. No filtering or additional preprocessing was implemented beyond this aggregation, as the goal was to display the overall distribution of the full dataset.

---

## Plot 2

This visualization builds on the first plot by introducing a filtered view of license types based on license status. The purpose is to explore how the distribution of license types changes when focusing on a specific status category, such as ACTIVE or NOT RENEWED. Similar to the first plot, the x-axis encodes License Type (:N), and the y-axis represents the count of records (:Q), where a bar chart is used.

The design choices remain consistent with the first plot to maintain visual comparability. Color is again mapped to License Type (:N), ensuring that categories are easily distinguishable and consistent across both visualizations. Keeping the same encoding structure allows users to directly compare the filtered results with the overall distribution shown in Plot 1.

The primary data transformation applied in this visualization is aggregation using count(), which summarizes the number of records per license type. In addition, a key transformation in this plot is dynamic filtering based on user input. Instead of showing all records, the dataset is filtered using a selection parameter tied to the License Status field. This transformation reduces visual clutter and allows the chart to focus only on the subset of data relevant to the selected status.

---

## Interactivity

Interactivity is implemented using a dropdown selection bound to the License Status variable. Users can select a specific status from the dropdown menu, and the visualization dynamically updates to display only the records that match the selected value. This is achieved using a selection parameter combined with a transform_filter() operation.

This interactive feature improves the clarity and usefulness of the visualization. Without interactivity, comparing distributions across different license statuses would require multiple static charts, which can be overwhelming and inefficient. By allowing users to filter the data dynamically, the visualization becomes more flexible and user-driven, enabling targeted exploration of specific subsets of interest. This approach reduces visual clutter and helps highlight patterns that may not be immediately visible in the full dataset.

---

## Data

[The Data](https://github.com/UIUC-iSchool-DataViz/is445_data/raw/main/licenses_fall2022.csv)

---

## Analysis

[The Analysis](https://github.com/Bingqing-L/Bingqing-L.github.io/blob/main/Workbook (1).ipynb)
