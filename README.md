# Geo Mining
![AA_ee_black_2](https://user-images.githubusercontent.com/50297074/151965110-faf885a2-d8ff-412b-ac33-0ac9422a9a40.jpg)

This repository collects a computational pipeline to mine geospatial data through Google Earth Engine in Grasshopper 3D, via its most recent Hops component. To read more about case studies and applications refer to [I.Neri, Expanding Digital Design Workflows with Geospatial Analytics](https://doi.org/10.14627/537740047)

## Requirements
- [Rhinoceros 7](https://www.rhino3d.com/download/) (Win) & Hops (tested with 0.16)
- [Python 3](https://www.python.org/downloads/release/python-380/) (tested with 3.8.0)

## REMOTE : using Flask-ngrok and Colab
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/neriiacopo/GeoMining-EE-Hops/blob/main_v2/GeoMining_EE_Hops.ipynb)

## LOCAL : to live connect to Earth Engine
## Installation
1. **[clone the repository](https://help.github.com/en/github/creating-cloning-and-archiving-repositories/cloning-a-repository)**
  - open a Terminal (mac) or run PowerShell (win)
  - change directory to your desidered path `example: cd /Users/xxx/Desktop/`
  - git clone https://github.com/neriiacopo/GeoMining-EE-Hops.git

2. **[virtual environment](https://docs.python.org/3/tutorial/venv.html)**
  - enter the repository `cd GeoMining-EE-Hops`
  - create the virtual environment `python -m venv env_GeoMining`
  - win: `.\env_GeoMining\Scripts\activate`
3. **install dependencies**
  - `pip install -r requirements.txt`

## Usage
- Change directory in the Terminal/PowerShell to repository folder
- Activate your virtual environment (as explained above)
- Connect Grasshopper to Earth Engine via Hops `python import_ee.py`
- On the first run, follow the instructions in the console to authenticate your machine to Google Earth Engine

## Troubleshooting
- if `.\env_GeoMining\Scripts\activate` fails to run in Windows
  - make sure you run Powershell as Administrator 
  - `Set-ExecutionPolicy RemoteSigned`
  - `y`
  - `.\env_GeoMining\Scripts\activate`

- if any of the Python scripts fails to run 
  - check if you Python2 installed as well and make sure to call Python3
  - `python3 -m venv env_GeoMining`
  - `python3 import_ee.py`

- if `import_ee.py` fails due to Authentication
  - make sure to have a registered account to GEE
  - go at this **[link](https://signup.earthengine.google.com/)** and fill up the form
  
- if `import_ee.py` fails due to AttributeError: module 'collections' has no attribute 'Callable'
  - make sure to run Python < 3.10
 
  
## Citation
Neri, Iacopo. 2023. Expanding Digital Design Workflows with Geospatial Analytics: Linking Grasshopper3D with Google Earth Engine. DE: Wichmann Verlag. https://doi.org/10.14627/537740047.
