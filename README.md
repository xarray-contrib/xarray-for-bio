# Data Branch

This branch contains small datasets for the xarray-for-biology tutorials and examples.

## Purpose

This branch is used to store small example datasets that are used in the main documentation and tutorials. By keeping data separate from the main code, we can:

- Keep the main branch lightweight
- Version control data separately
- Make it easy to download specific datasets

## Usage

To access datasets from this branch in your code:

```python
import pandas as pd
import xarray as xr

# Example loading data from raw GitHub URLs
data_url = "https://raw.githubusercontent.com/your-username/xarray-for-biology/data/path/to/dataset.csv"
df = pd.read_csv(data_url)
```

## Contributing Data

When adding new datasets:
1. Keep files small (< 10MB preferred, < 25MB maximum)
2. Use efficient formats (Parquet, Feather, or compressed CSV)
3. Include a description in this README
4. Document the data source and any processing steps

## Available Datasets

(Datasets will be listed here as they are added)