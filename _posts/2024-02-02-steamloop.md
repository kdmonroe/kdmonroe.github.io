---
layout: post
title: "Streamlit Folium Map of Philadelphia's Steamloop"
date:   2024-02-02 00:01:20 +0000
categories: 
  - project
  - python
  - data-viz
permalink: /streamlit_steamloop/
thumbnail: /assets/thumbnails/streamlit_steamloop.png
app_url: "https://phl-steamloop.up.railway.app"
github_url: "https://github.com/kdmonroe/phl_steamloop_streamlit"
excerpt_separator: <!-- excerpt-end -->
---

This data visualization uses Streamlit Folium to generate a sophisticated mapping dashboard.
It includes an analysis of nearby buildings and neighborhoods, 
and background research on combined heat and power (CHP) energy infrastructure.

[Check out the app here, hosted on Railway.](https://phl-steamloop.up.railway.app) 

<!-- excerpt-end -->

# Map of Philadelphia Steamloop Boundaries (Estimated)
![Streamlit Folium](/assets/thumbnails/streamlit_steamloop.png)


# Streamlit App 

<iframe src="https://phl-steamloop.up.railway.app/" width="700" height="700"></iframe>

The above map embedded from the Streamlit application 
hosted on [Railway](https://railway.app/). 
It is embedded here by IFrame in the Markdown. 

I georeferenced public maps of the Philadelphia steamloop to get the linear boundaries shown in the map above. 
The Folium map also includes red markers to identify the two cogeneration plants of the system, and 
data layers for Philadelphia neighborhoods and buildings.

# Motivation
I was motivated to created this map because of my volunteer work with [Citizens Climate Lobby](https://citizensclimatelobby.org/) here in Philadelphia.
I am continuing to learn more about my city's energy infrastructure, and ways we can hasten decarbonization goals.
If you are interested in learning more about CCL Philadelphia, [check out their Instagram page here](https://www.instagram.com/ccl_philly/).

The steam loop was georeferenced from two main sources: 
- [Vicinity Energy (Informational Brochure)](https://www.vicinityenergy.us/brochures/delivering-reliable-green-energy-to-philadelphia) 
- [Old Trigen Steam Distribution Map](https://hiddencityphila.org/2012/02/all-steamed-up/)


# More about the Steam Loop
  -  [Vicinity Energy (Current Owner)](https://www.vicinityenergy.us/locations/philadelphia)
  -  [How A Combined Cycle Power Plant Works -Gas Power Generation](https://www.youtube.com/watch?v=KVjtFXWe9Eo&t=12s)
  -  [Could Philly’s steam system provide a climate solution? PGW says no - WHYY article](https://whyy.org/articles/philadelphia-pgw-vicinity-customers-gas-steam-loop-climate-change/) 
  -  [Willow Street Steam Generation Plant - Abandoned America](https://www.abandonedamerica.us/willow-street-steam-plant)
  -  [Center City steam loop a ‘diamond in the rough,’ - Philadelphia Inquirer article](https://www.inquirer.com/business/philadelphia-steam-plant-vicinity-veolia-dicroce-20200204.html)

### Building Footprints + Neighborhoods Data
- [Building Footprints, 2021 Microsoft](https://github.com/Microsoft/USBuildingFootprints)
- [Philadelphia Neighborhoods, Azavea](https://github.com/azavea/geo-data/blob/master/Neighborhoods_Philadelphia/Neighborhoods_Philadelphia.geojson)

### Limitations
Buildings were filtered to only include those in Philadelphia County and within 1000 meters of the steam loop and counts are estimated (see Disclaimer). It is unknown to what specific extent or general area buildings could connect to the system. 1000 meters is a generalized estimate. According to a <a href="https://www.inquirer.com/business/philadelphia-steam-plant-vicinity-veolia-dicroce-20200204.html" target="_blank">2020 Inquirer article</a>, 
The Center City district heating system produces steam at a central power plant and delivers it by underground pipes to about 500 buildings.

The steam loop's current energy capacity is unknown. Whether additional buildings are connected, or could be connected in the future, is also unknown. 
    
## Software
- [GeoPandas](https://geopandas.org/)
- [Folium](https://python-visualization.github.io/folium/)
- [Streamlit](https://streamlit.io/)
- [Streamlit-Folium](https://github.com/randyzwitch/streamlit-folium)
- [QGIS](https://qgis.org/en/site/)