---
title: Categorical-Year-Group
slug: categorical-year-group
---
## Example (Line, bar and pie charts)
{{< flourish "visualisation/27591085" >}}
### Data Structure
| Year | Categorical Variable | Group 1 | ... | Group n |
| ---- | -------------------- | ------- | --- | ------- |
| t1   | cat 1                | pct.    |     |         |
| t1   | cat 2                |         |     |         |
| t1   | cat 3                |         |     |         |
| t2   | cat 1                |         |     |         |
| t2   | cat 2                |         |     |         |
| t2   | cat 3                |         |     |         |
| ...  | ...                  |         |     |         |
- labels/time is the focused categorical variable. 
- row filter is year.
### Notes 
1. The number in raw data could be either percentage or proportion. Flourish could adjust that 
2. To apply color scheme used in YJI, **Custom overriders** under **Colors** should be used. 
3. Do not hide overlapping labels
