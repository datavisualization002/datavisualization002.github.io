---
title: Custom Map
slug: custom-map
---
## Example (Projection map)
{{< flourish "visualisation/27572844" >}}

### Data Structure 
Feature tables and GeoJSON need to be separated files. 
#### data file (Regions)

| GEOID | Label | var 1 | var 2 | ... |
| ----- | ----- | ----- | ----- | --- |
|       |       |       |       |     |
#### geographic file (Regions geometry)

| geometry | GEOID |
| -------- | ----- |
|          |       |
### Notes
1. Flourish provide detailed [guidance](https://flourish.studio/blog/make-your-own-data-driven-maps/) on how to upload custom map. 
2. The file should be a GeoJSON data that sizes **up to 5 MB**
3. 




