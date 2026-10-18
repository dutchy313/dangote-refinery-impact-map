# Dangote Refinery Impact Map

An interactive geospatial analysis of countries whose refined petroleum export revenues to Nigeria may be exposed as domestic refining capacity expands following the start of production at the Dangote Petroleum Refinery.


## About the Project

Nigeria has historically imported significant volumes of refined petroleum products from countries across Europe, Asia, Africa, and other regions.

The Dangote Petroleum Refinery began production following the receipt of its first crude oil in December 2023. This created the potential for Nigeria to increasingly substitute domestically refined petroleum products for imports.

This project uses Nigeria's **2022 refined petroleum import data** as a pre-refinery baseline to visualize countries with potential exposure to a reduction in Nigerian import demand.

The visualization should be interpreted as a **map of trade exposure**, not as an estimate of realized post-refinery revenue losses.

## What the Map Shows

The interactive map combines:

- A choropleth showing 2022 refined petroleum exports to Nigeria by country
- Proportional circle markers representing the relative value of exports
- Interactive tooltips showing country-level values
- Labels for selected countries with the highest exposure
- An OpenStreetMap basemap
- A layer control for exploring the visualization

Larger circles indicate countries with greater pre-refinery petroleum export exposure to the Nigerian market.

## Data

The analysis uses **2022 refined petroleum import data for Nigeria** obtained from the Observatory of Economic Complexity (OEC).

**Source:**  
https://oec.world/en/profile/country/nga

Values are expressed in **millions of US dollars**.

## Key Interpretation

Countries with higher 2022 refined petroleum export values to Nigeria had greater exposure to any future reduction in Nigerian import demand.

The analysis does **not** claim that these countries have already lost the corresponding amount of revenue.

Measuring actual post-refinery impact would require newer trade data and a before-and-after analysis comparing import patterns before and after the Dangote Refinery became operational.

## Repository Files

- `dangote_refinery_impact_map.ipynb` — Main analysis and visualization notebook
- `petroleum.csv` — Source trade dataset
- `petroleum.html` — Exported interactive map
- `README.md` — Project documentation
- `map-preview.png` — Optional preview image for the repository README

## Requirements

- Python 3.x
- pandas
- folium

Install the required packages with:

```bash
pip install pandas folium
```

## Running the Project

1. Clone or download this repository.
2. Ensure `petroleum.csv` is in the same directory as the notebook.
3. Open `dangote_refinery_impact_map.ipynb`.
4. Run all notebook cells.
5. The notebook generates `petroleum.html`.
6. Open `petroleum.html` in a web browser to explore the interactive map.

## Method

The notebook:

1. Loads and cleans the petroleum trade data.
2. Standardizes country names for geographic matching.
3. Uses a fixed country coordinate reference to avoid dependency on live geocoding services.
4. Creates a choropleth layer based on 2022 refined petroleum export value to Nigeria.
5. Adds proportional circle markers for countries with positive export values.
6. Adds tooltips for country-level interpretation.
7. Exports the final interactive visualization as an HTML file.

## Why This Matters

The Dangote Petroleum Refinery represents a major change in Nigeria's downstream petroleum market.

If Nigeria progressively substitutes imported refined petroleum products with domestic production, the effects may extend beyond Nigeria. Countries that previously earned substantial export revenue from supplying the Nigerian market could experience varying levels of exposure.

This project uses data visualization to make that potential trade shift easier to explore.

## Limitations

This project is exploratory and descriptive.

It does not estimate causal effects, actual revenue losses, or changes in bilateral trade after refinery production began.

The 2022 dataset is used as a baseline because it represents a pre-refinery period. A more complete impact analysis would require post-2023 trade data and a formal before-and-after comparison.

## Technologies Used

- Python
- pandas
- Folium
- OpenStreetMap
- Jupyter Notebook

## Author

**Oludotun Babayemi**

Designed and developed in 2024 as a data storytelling and geospatial analysis project.

## License

This project is intended for educational, analytical, and portfolio purposes. Please review the terms of the underlying data source before reuse or redistribution.
