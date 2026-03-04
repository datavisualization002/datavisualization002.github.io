---
title: Data Explorer
slug: data-explorer
---
Data explorer could be used for more complicated data structure. This tool could be used to present both univariate distribution by map and relationship between multiple variables by both x-axis, y-axis, color, size. In addition, it includes an aggregation and filter. 
With aggregation, flourish will ask you to select from max(), min(), sum(), mean() of the raw values. You need to select the appropriate value based on the feature of variable and the variable setting up the group in aggregation. For example, percentage should be be added. 
Here are two examples, the first one is more clear and easy to understood. The second has more complicated data structure and not very straightforward. However, the second one is more informative and allows user to get more information. 
However, personally, I do not think this is a very good visualization since the audience of these figures are usually not very familiar with the data structure. 
## Example 1
{{< flourish "visualisation/27778153?1765335" >}}
### Data Structure
#### Data 

| ID         | GEOID | County | Group | Var 1 | Var 2 | Var ... |
| ---------- | ----- | ------ | ----- | ----- | ----- | ------- |
| $county_1$ |       |        |       |       |       |         |
| ...        |       |        |       |       |       |         |
| $county_n$ |       |        |       |       |       |         |

In the data part, ID is individual ID created by Flourish.
GEOID is the ID used to link geo information, and the GEOID is also the id for the unit of analysis in this figure. 
County is the name label.
Group is the group variable used to aggregate our analysis sample. For example whether the county belong to NYC. 
Var 1 to Var ... are continuous variables we are interested in. 
#### geographic file (Regions geometry)
This will be same structure as the one used in [Custom Map](/docs/custom-map/).

## Example 2
{{< flourish "visualisation/27699972?1765335" >}}
### Data Structure

| ID         | GEOID | year | County | Group | Var 1 | Var 2 | Var ... |
| ---------- | ----- | ---- | ------ | ----- | ----- | ----- | ------- |
| $county_1$ |       | t1   |        |       |       |       |         |
| ...        |       | t1   |        |       |       |       |         |
| $county_n$ |       | t1   |        |       |       |       |         |
| $county_1$ |       | t2   |        |       |       |       |         |
| ...        |       | t2   |        |       |       |       |         |
| $county_n$ |       | t2   |        |       |       |       |         |
| ...        |       | ...  |        |       |       |       |         |
| $county_1$ |       | tn   |        |       |       |       |         |
| ...        |       | tn   |        |       |       |       |         |
| $county_n$ |       | tn   |        |       |       |       |         |

In the data part, ID is individual ID created by Flourish.
GEOID is the ID used to link geo information, and the GEOID is also the id for the unit of analysis in this figure. 
In this figure, each row is a unique county-time pair. 
#### geographic file (Regions geometry)
This will be same structure as the one used in [Custom Map](/docs/custom-map/).

### Notes 
1. Key benefits of Data explorer:
	1. providing both map and charts.
	2. showing relationship between two variables, or even among three variables, based on audience's interests.
2. When the dataset is too big, Flourish handle it with small glitch.

