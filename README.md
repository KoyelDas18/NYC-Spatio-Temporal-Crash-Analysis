# NYC-Spatio-Temporal-Crash-Analysis
This project analyzes NYC crash data across space and time using H3 hexagons, time-based summaries, and interactive maps. It identifies hotspots, highlights patterns by hour and weekday, and produces clear visuals and tables to support transportation safety decisions.
The notebook walks through the full workflow, from raw data to insights that can support decisions around transportation safety.

## What the notebook does ##

### 1. Cleans and prepares NYC crash data ###

* Loads raw crash records

* Handles missing fields and formats timestamps

* Converts crash locations into geometry for spatial analysis

### 2. Builds an H3 hexagonal grid ###

* Assigns each crash to a hex cell

* Aggregates counts per hex for different time windows (hour, weekday, month)

### 3. Creates spatiotemporal summaries ###

* Crash frequency by hour

* Crash frequency by weekday

* Monthly crash trends

* Rolling and cumulative crash patterns

### 4. Generates hotspot statistics ###

* Ranks hex cells with the highest crash density

* Produces tables of the top risky locations

* Breaks hotspots down by time period

### 5. Produces interactive maps ###

* H3 hex density map

* Time-filtered hotspot map

* Layered visualizations for exploring patterns spatially

### 6. Saves key outputs ###

* Processed datasets

* Hotspot tables

* Time-series summaries

* Exportable CSV files

## Why this matters ##

The project gives you a repeatable framework for understanding when and where crashes cluster in NYC. It can support:

* School bus routing safety checks

* Infrastructure planning

* Vision Zero evaluations

* Any analysis that needs both time and location to be considered together

## Requirements ##

Install the main libraries used in the notebook:
```python
pip install pandas numpy geopandas folium h3 matplotlib seaborn shapely
```
Depending on your Python setup, you may also need:
```python
pip install contextily pyproj plotly
```
### How to use ###

1. Clone the repository

2. Open the notebook:
```python
jupyter notebook NYC_Spatio_Temporal_Analysis.ipynb
```
3. Run the cells in order.

4. Review the generated tables, plots, and interactive maps.

5. Check the exported CSVs if you want to use the results in another workflow.

## Project structure ##
```python
NYC_Spatio_Temporal_Analysis.ipynb   # Full workflow
data/                                 # (optional) Place your raw crash files here
outputs/                              # Processed CSVs and saved results
maps/                                  # Auto-generated interactive maps
```
## Data sources ##

The workflow is designed for NYC Open Data crash records, but it can be adapted to any geocoded crash dataset with timestamps.

## Extending the project ##

The project can be extended by adding features such as:

* Seasonal decomposition

* Predictive modeling

* A weekly crash alarm system

* Street-level clustering

* Weather overlays
