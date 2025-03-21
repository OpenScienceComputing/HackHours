# HackHours
To use the token to run COILED, login to the [NMFS OpenSpaces 2i2c JuptyerHub](https://nmfs-openscapes.2i2c.cloud/) with the default environment, open a terminal and type:
```
coiled login --token af791b1a879e4c0b99a8b7bec850e9a1-1e7144a190114be06abf273052d98640b62cb5fa
```
This will give you access for 24 hours (2025-03-21) only.

I created the named coiled environment by creating a [conda environment file](hackhours_coiled_env.yml) that matched the package versions in the JupyterHub default environment, as of 2025-03-21, via this command:

```
coiled env create --name hackhours-arm --workspace esip-lab --conda hackhours_coiled_env.yml --architecture aarch64
