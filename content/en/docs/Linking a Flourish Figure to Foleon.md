---
title: Linking a Flourish Figure to Foleon
slug: linking-a-flourish-figure-to-foleon
---

In the current [Demographics session](https://university-at-albany-youth-justice-institute.foleon.com/yji/youth-in-new-york-state-2024/demographics) in [Youth Snapshots](https://university-at-albany-youth-justice-institute.foleon.com/yji/youth-in-new-york-state-2024/), the map is not interactive. The audience needs to access the interactive version through a link to [tableau](https://public.tableau.com/app/profile/nys.youth.justice.institute/viz/TotalYouthinNewYorkStatebyCounty/Dashboard1). 

![[Screenshot 2026-05-12 131617.png]]

By linking the Flourish figure directly to Foleon, the map can become interactive within the page and better match the Y-FACTS [color schema](/docs/color-schema/). An example can be found in this [preview](https://viewer.foleon.com/preview/oqqy32ap3jk/demographics).

![[Screenshot 2026-05-12 131713.png]]

To add the interactive figure in Foleon, go to **Elements → Embed**.

When exporting and publishing a figure from Flourish, Flourish provides an HTML embed code, such as:
```
<div class="flourish-embed flourish-map" data-src="visualisation/28192604?1765335"><script src="https://public.flourish.studio/resources/embed.js"></script><noscript><img src="https://public.flourish.studio/visualisation/28192604/thumbnail" width="100%" alt="map visualization" /></noscript></div>
```
However, Foleon requires a URL rather than HTML code. In this case, we can use the following URL:
```
https://flo.uri.sh/visualisation/28192604/embed
```
The figure ID, `28192604`, comes from the `data-src` field in the Flourish HTML code: 
```
data-src="visualisation/28192604?1765335"
```
So the general format is:
```
https://flo.uri.sh/visualisation/[figure ID]/embed
```






