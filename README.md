# Homenetwork Analysis

This repository is a walk-trough over a home network analysis, that was performed in the beginning of 2022 by [geitner-max](https://github.com/geitner-max), [sven0311](https://github.com/sven0311) and [fabianh001](https://github.com/fabianh001).
We first wanted to understand general information about our networks, namely the used protocols, DNS servers, encryption distribution and ethertypes. Further, the sources and destinations of our requests were analysed and which devices sent the most data. Lastly, a closer look was taken onto suspicious network traffic.

## Installation Notes 

The following python libraries need to be installed before running the jupyter notebook:
- pandas
- geopandas
- matplotlib
- numpy
- seaborn
- requests

### Instructions
The easiest way for setup is to use conda and create a conda environment.

```
conda create --name net-analysis python=3.9
conda activate net-analysis
conda install --file requirements.txt
```

## Run the Jupyter Notebook

You need to have jupyter installed.
In order to run the notebook analysis, only the notebook `cmb2.ipynb` and the cache file `df.csv` are required. Please place the files in the following file structure:

```
Root Folder
├── dumps                   # Contains csv files from team members
├──────  advanced-dumps-sven.csv
├──────  allPorts_fabian.csv
├──────  allPorts_maxi_v3.csv
└── README.md
└── df.csv
```



There is the variable `new_read` in the first code cell, which is set to `False` by default and uses the cached `df.csv` file to immediately start the analysis. 

In order to create the cache file from the member's .csv files (placed in the dumps folder), the variable can be set to `True`. The notebook then runs through all steps, including data preprocessing. These additional steps take very long and might run for approximately 30 minutes.
