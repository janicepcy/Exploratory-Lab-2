# Vancouver Park Accessibility

**GEOS 472 – Exploratory Lab 2: Interactive Mapping**

## Project Overview

This interactive map explores the distribution and accessibility of public parks across Vancouver, British Columbia. Using a 500-metre radius, users can select any location on the map to examine how many park polygons are located within the surrounding area and compare their sizes.

The map was developed using MapLibre GL JS and Turf.js, combining geographic visualization with spatial analysis to help users explore differences in park accessibility across Vancouver.

## Interactive Map

**Live Map:** [Vancouver Park Accessibility](https://janicepcy.github.io/Exploratory-Lab-2/)

**Screenshot:**

*Insert a screenshot of the map showing the 500 m buffer, highlighted parks, and accessibility results panel.*

## Map Features and Interactivity

The map includes several interactive features:

- **Location selection:** Users can click anywhere on the map to select a location and generate a 500-metre buffer.
- **Spatial analysis:** Turf.js identifies park polygons that intersect the buffer and calculates the total number.
- **Park size comparison:** The results panel displays the number of small (under 1 ha), medium (1–5 ha), and large (5+ ha) park polygons intersecting the buffer.
- **Pulsing animation:** Intersecting park polygons are highlighted with a subtle pulsing effect while retaining their original green classification.
- **Park information:** Clicking a park displays a popup containing its name, area, size category, and classification.
- **Navigation:** Users can zoom and pan across Vancouver to compare different locations.

These features allow users to explore spatial relationships that would be difficult to examine through a single static map.

## Data Sources and Tools

**Data:** Vancouver Parks and Green Spaces, City of Vancouver Open Data Portal.

The dataset contains park polygon boundaries and associated attributes, including park names and areas. Park polygons were classified into three size categories to communicate differences in park size.

**Tools and libraries:**

- **MapLibre GL JS** – Interactive map display, geographic layers, and popups.
- **Turf.js** – 500-metre buffer creation and polygon intersection analysis.
- **Maputnik** – Customization of the basemap's visual style.
- **HTML, CSS, and JavaScript** – Map layout, interface design, and interactive functionality.
- **GitHub Pages** – Hosting and publishing the interactive map.

## Reflective Analysis

### Design Decisions and Intended Insights

My main objective was to explore how access to public parks varies across Vancouver, particularly in terms of both the number and size of nearby parks. I designed the map for people interested in understanding the distribution of urban green spaces, including residents and students exploring different neighbourhoods. Rather than presenting park locations alone, I wanted users to investigate how the surrounding park environment changes depending on where they select a location. The 500-metre buffer provides a consistent distance for comparing locations, while the three green shades distinguish small, medium, and large parks. I retained the relatively simple basemap from my previous lab to keep the park polygons visually prominent and reduce unnecessary visual distractions.

### Development Process and Interactivity

I began with the park map developed for Exploratory Lab 1, then added Turf.js to generate a 500-metre buffer around a user-selected point. The next step was to identify park polygons intersecting that buffer and display the results. I subsequently added a breakdown by park size because the total number of parks alone does not necessarily indicate the amount or type of nearby green space. The pulsing animation was another addition intended to make the intersecting parks easier to identify without replacing their original size classifications. This interaction allows users to compare different parts of Vancouver by repeatedly selecting locations and observing how the buffer, highlighted parks, and numerical results change. Unlike a static map, the visualization allows users to explore their own questions about nearby parks.

### Limitations and Possible Improvements

One important limitation is that the 500-metre buffer represents straight-line distance rather than actual walking accessibility. Roads, barriers, park entrances, and pedestrian routes are not considered. In addition, the analysis counts park polygons that intersect the buffer, even when only a small portion of a park falls within it. Therefore, the results should not be interpreted as the number of parks fully contained within walking distance. The map also does not account for park facilities, quality, or public accessibility differences. A possible improvement would be to incorporate a pedestrian network and calculate walking-distance service areas instead of circular buffers. Adding population data could also help investigate whether neighbourhoods with different population densities have similar access to green spaces. Despite these limitations, the map demonstrates how interactive spatial analysis can reveal differences in the distribution of nearby parks that are less apparent from a static visualization.

## References and Resources

- [City of Vancouver Open Data Portal](https://opendata.vancouver.ca/)
- [MapLibre GL JS Documentation](https://maplibre.org/maplibre-gl-js/docs/)
- [Turf.js Documentation](https://turfjs.org/)
- [Maputnik Map Style Editor](https://maputnik.github.io/)
- [OpenFreeMap](https://openfreemap.org/)
- [OpenStreetMap](https://www.openstreetmap.org/)
