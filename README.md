# HackHours
We will use the notebook here to explore NODD data using holoviz, then create a virtual dataset using Virtualizarr, and then run an embarrassingly parallel job (construction of references for each file) using Dask, and then also use Dask for parallel data access in Xarray.  

### Setup:
#### For running Dask with Coiled
Login to the [NMFS OpenSpaces 2i2c JuptyerHub](https://nmfs-openscapes.2i2c.cloud/) with the default environment, but choosing 7.4GB RAM for the "Resource Allocation". 

You will need to create an account at https://coiled.io to use Coiled.  After creating an account, open a terminal and type "coiled login", a one-time step that will allow you to launch Coiled from your server.  I created the named coiled environment by creating a [conda environ file](hackhours_coiled_env.yml) that matched the package versions in the JupyterHub default environment, as of 2025-03-21, via this command:

```
coiled env create --name hackhours-arm --workspace esip-lab --conda hackhours_coiled_env.yml --architecture aarch64
```
Clone this repo by opening a terminal and typing:
```
git clone https://github.com/OpenScienceComputing/HackHours.git
```
Then run the demo notebook, making sure `cluster_type='Coiled'` is set, not `cluster_type='Gateway'`. 

#### For running Dask with Dask Gateway
Login to the [NMFS OpenSpaces 2i2c JuptyerHub](https://nmfs-openscapes.2i2c.cloud/) choosing "Other" for the environment, and enter "openscapes/python:07980b9". Choose 7.4GB RAM for the "Resource Allocation". 

Clone this repo by opening a terminal and typing:
```
git clone https://github.com/OpenScienceComputing/HackHours.git
```
Then run the demo notebook, making sure `cluster_type='Gateway'` is set, not `cluster_type='Coiled'`. 
