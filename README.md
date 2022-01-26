# cmb_assignment2_group_1

## Installation Notes: 

The following python libraries need to be installed before running the jupyter notebook:
- pandas
- geopandas
- matplotlib
- numpy
- seaborn
- requests

### Instructions
```
conda create --name cmb-assignment2-group1 python=3.9
conda activate cmb-assignment2-group1
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



There is the variable `new_read` in the first code cell, which is set to `False` by default and uses the cache file in order to immediately start the analysis. 

In order to create the cache file from the member's csv files (placed in the dumps folder), the variable can be set to `True` and then it runs through all steps of the notebook (including filtering local traffic and creating new columns for analysis purposes). These additional steps might run for approximately 30 minutes.