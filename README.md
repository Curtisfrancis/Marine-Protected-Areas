# Marine Protected Areas Analysis

## Overview
This project analyzes fishing vessel data in relation to Marine Protected Areas (MPAs). It processes geospatial data and vessel tracking information to identify fishing vessel movements within specified geographical boundaries.

## Features
- Reads and processes shapefile data for Marine Protected Areas
- Analyzes CSV files containing fishing vessel tracking data
- Calculates vessel speeds and positions
- Identifies vessels operating within defined geographical boundaries
- Computes average, minimum, and maximum speeds across multiple vessel datasets

## Requirements
- Python 3.0.1 and later versions
- Libraries:
  - geopandas
  - pandas
  - matplotlib
  - earthpy
  - numpy

## Installation
1. Clone this repository
2. Install required libraries:
   ```
   pip install geopandas pandas matplotlib earthpy numpy
   ```

## Data Structure
The project expects the following data structure:
- Shapefile for MPA boundaries: `/path/to/JOBcir.-line.shp`
- CSV files for vessel data: `/path/to/20160801_FishingVessels/*.csv`

Ensure your data follows this structure or update the file paths in the script accordingly.

## Usage
1. Update the file paths in the script to match your data locations:
   - MPA shapefile: `file = gpd.read_file('/path/to/JOBcir.-line.shp')`
   - Vessel data: `df = pd.read_csv('/path/to/20160801_FishingVessels/204235000.csv')`
2. Run the script to process the data and generate results.

## Key Functions
- `Speed(path)`: Calculates average, minimum, and maximum speeds across all vessel CSV files in the specified directory.

## Output
The script provides:
- A list of fishing vessels (MMSI, vessel name, and timestamp) operating within the specified geographical boundaries and speed range.
- Average, minimum, and maximum speeds across all processed vessel data.

## Contributing
Contributions to improve the analysis or extend the project are welcome. Please fork the repository and submit a pull request with your proposed changes.



<p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/"><a property="dct:title" rel="cc:attributionURL" href="https://github.com/Curtisfrancis/Marine-Protected-Areas">Marine-Protected-Areas</a> by <a rel="cc:attributionURL dct:creator" property="cc:attributionName" href="https://github.com/Curtisfrancis">Curtis Akapini Apegwine</a> is licensed under <a href="https://creativecommons.org/licenses/by/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">CC BY 4.0<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1" alt=""><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1" alt=""></a></p>
