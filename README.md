# COVID-19 in Africa (2020): Geospatial Analysis Notebook

This Jupyter Notebook demonstrates how to process, analyze, and export COVID-19 case data for Africa in 2020 using geospatial techniques. The workflow leverages Python libraries such as `pandas` and `geopandas` to manipulate spatial and tabular data.

## Prerequisites

- Python 3.x
- Jupyter Notebook or Google Colab
- Required Python packages:
  - geopandas
  - pandas
  - (Optional) Google Drive mounted if running in Colab

Install dependencies (if needed):
```python
!pip install geopandas -q
```

## Data Sources

- **African GADM Shapefile:** Administrative boundaries for Africa.
- **World COVID-19 Shapefile:** Global COVID-19 case data with spatial attributes.

Update the file paths as needed for your environment.

## Notebook Workflow

### 1. Load Data

- Load African administrative boundaries and world COVID-19 data as GeoDataFrames.
- Print the first few rows to verify successful loading.

### 2. Spatial Clip

- Reproject the world COVID-19 data to match Africa's coordinate reference system (CRS).
- Clip the global COVID-19 data to Africa's boundaries, keeping only African records.

### 3. Save Clipped Data

- Save the clipped African COVID-19 data as a new shapefile for future use.

### 4. Date Processing

- Convert the `date` column to datetime objects.
- Extract the `year` and `month` for temporal analysis.

### 5. Data Exploration

- Display available columns for reference.

### 6. Monthly Aggregation (2020)

- Filter data for the year 2020.
- Aggregate cumulative COVID-19 cases by country and month.
- For each country and month, keep the last (most recent) record to represent cumulative cases.

### 7. Save Aggregated Data

- Save the monthly aggregated COVID-19 data for Africa in 2020 as a shapefile.

## Output

- `africa-covid-19.shp`: Clipped COVID-19 data for Africa.
- `africa-covid-19-monthly-2020.shp`: Monthly cumulative COVID-19 cases for African countries in 2020.

## Data Sources

- **African GADM Shapefile:** Administrative boundaries for Africa.  
  [Download from Google Drive](https://drive.google.com/drive/folders/1OOdPCx0acSUwSGvD9z9SDvZked_h_dqN?usp=drive_link)
- **World COVID-19 Shapefile:** Global COVID-19 case data with spatial attributes.
- **Africa COVID-19 Data 2020:**  
  [Download from Google Drive](https://drive.google.com/drive/folders/1xAT4t0tMGDV41jQiOdpHJHtxBfBr-zw3?usp=drive_link)


## Notes

- Adjust file paths if running outside Google Colab.
- Ensure all dependencies are installed before running the notebook.
- The notebook can be extended for visualization or further analysis.

---
**Author:**  
*Olamide SHOGBAMU*