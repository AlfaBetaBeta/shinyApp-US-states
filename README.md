## Shiny app - US states basic spatial analysis

This repository showcases a basic usage of a leaflet based shiny app embedded in RMarkdown. The app is based on the `spData::us_states` dataset. 

For further information about this library and its datasets for spatial analysis, please refer to [the official library site](https://nowosad.github.io/spData/).

The `us_states` dataset comprises the following features for all 48 *continental* states of the US and the District of Columbia, whereby the term *continental* is loosely defined here as referring to all states in mainland America between Canada and Mexico, hence excluding Hawaii and Alaska:

* `GEOID`: character vector of geographic identifiers
* `NAME`: character vector of state names
* `REGION`: character vector of region names
* `AREA`: area in square kilometers of units class
* `total_pop_10`: numerical vector of total population in 2010
* `total_pop_15`: numerical vector of total population in 2015
* `geometry`: sfc_MULTIPOLYGON


### App functionality 1: Aggregation by state/region

The most basic subset of the reference dataset is by state `NAME` and `REGION`. In the interactive maps available, you can select your state of interest (tab `NAME`) and its relevant features for display in the `data.table` header. Alternatively, click on the highlighted state to have its summarised features pop up.

<img src="https://github.com/AlfaBetaBeta/shinyApp-US-states/blob/master/img/AppF1-Name.png" width=100% height=100%>

Additionally, you can select your region of interest (tab `REGION`) for it to be highlighted in the map and its cumulative and average features per state summarised in the `data.table` header. Hovering over the states in the highlighted region enables the display of their name.

<img src="https://github.com/AlfaBetaBeta/shinyApp-US-states/blob/master/img/AppF1-Region.png" width=100% height=100%>


### App functionality 2: Evolution of population 2010-2015

The only demographic features available in the `us_states` dataset are the total population values in years 2010 and 2015. With these, you can inspect the relative change in population over the timespan or, combined with each state `AREA`, the population density for either year. You can focus on a specific `REGION` or on the entire country from the dropdown menus. Hovering over the active `REGION` enables the display of its state `NAME`s, and clicking on any state activates a popup with the demographic metric of interest.

<img src="https://github.com/AlfaBetaBeta/shinyApp-US-states/blob/master/img/AppF2.png" width=100% height=100%>