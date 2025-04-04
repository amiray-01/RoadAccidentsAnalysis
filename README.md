# Road Accidents Analysis (2021–2022)

## Overview
This project focuses on analyzing **French road accident data** for the years **2021 and 2022**, which is released as open data by the French Ministry of Transport. Specifically, it covers:

- **Data Retrieval**: Programmatic downloading of multiple CSV files (accidents, vehicles, users, roads) for each year.
- **Data Cleaning & Preparation**: Converting columns to the correct data types (including dates and categorical variables), handling missing or null values, and ensuring a reproducible data pipeline.
- **Data Merging**: Combining the individual datasets (accidents, vehicles, users, roads) into a single view, using common keys (e.g., Accident_Id).
- **Exploratory Analysis**:  
  - Generating descriptive statistics (mean, median, quartiles, standard deviation, skewness, kurtosis, etc.).  
  - Creating boxplots to visualize the distribution of numeric features (e.g., accident severity, road conditions).
  - Visualizing accident occurrences by day of the week, time of day, and month, helping identify potential patterns or peaks in accident frequency.
- **Focused Sub-Analyses**:  
  - Profiling specific groups of road users (e.g., motorists vs. pedestrians vs. cyclists).  
  - Identifying accidents that involved at least one pedestrian or cyclist, and comparing their characteristics (time, place, circumstances) to the overall dataset.
- **Advanced Data Handling**:  
  - Demonstrating use of Spark DataFrames (or Pandas on Spark) with more complex data structures (arrays, structs, etc.) for convenient storage and manipulation of nested data.
- **Data Export**: Saving the cleaned and merged dataset in **Parquet** format (with a chosen partitioning strategy) for efficient querying and archiving.

In short, this project not only showcases how to **collect and unify** multiple large CSV files but also provides a **comprehensive analysis** of road accidents, along with best practices for data cleaning, transformation, and visualization in a reproducible Python workflow.

## Technologies
- **Python 3.x**
- **PySpark** (version 3.0+ recommended)
- **requests** (for programmatic data download)
- **Pandas** and/or **Pandas on Spark**
- **Plotly** or **Altair** (for interactive visualizations)

## Installation
To install the core Python libraries:
```bash
pip install pyspark requests plotly altair pandas
```

## Usage

### Download the accident data
- By default, the notebook fetches the CSV files (2021, 2022) using the `requests` library, saving them to a `data/` folder.
- Alternatively, you can manually place the downloaded CSV files in `data/`.

### Open and run the notebook
1. **Launch** Jupyter Notebook or JupyterLab.  
2. **Open** `accidents_analysis.ipynb`.  
3. **Run** each cell in order to:  
   - Download/Load the data.  
   - Clean and merge accident tables (accidents, vehicles, users, roads).  
   - Perform exploratory data analysis (descriptive stats, visualizations, filtering).  
   - Export the cleaned dataset to Parquet.
