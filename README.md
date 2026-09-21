# dtp-managed-roads-asset-analysis
Geospatial analysis and Power BI dashboard using publicly available DTP Managed Roads GeoJSON data.



This project uses publicly available DTP Managed Roads GeoJSON data downloaded from the Transport Victoria Open Data portal. 
The dataset describes Victorian freeways and arterial roads managed by the Department of Transport and Planning.
The analysis is an independent portfolio project and is not an official DTP analysis.


## Data Source

This project uses the publicly available **DTP Managed Roads** GeoJSON
dataset from the Transport Victoria Open Data Portal.

The source dataset contains 90,797 road-segment features represented as
LineString geometries with associated road, classification, management
and locality attributes.

The raw and generated Bronze, Silver and Gold datasets are not stored
in this repository due to file size and because they can be reproduced
using the supplied notebooks.

### Reproducing the data pipeline

1. Download the DTP Managed Roads GeoJSON from the Transport Victoria
   Open Data Portal.
2. Upload the GeoJSON to a Databricks Unity Catalog Volume.
3. Run the notebooks in numerical order:
   - `01_ingest_roads_geojson.ipynb`
   - `02_transform_roads_silver.ipynb`
   - `03_gold_build_asset_intelligence.ipynb`
   - `04_sql_asset_intelligence_analysis.ipynb`
4. The pipeline produces reporting-ready Gold Delta tables for Power BI.


