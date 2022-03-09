# **Gage Guesser**

Theo Ross and Ian Van Dusen

**Intro:**

The goal of this project is to estimate river discharge levels based on several climatic factors occurring in the hydrosheds. We looked at a river gage located on the Nisqually River in Washington and set out to understand what the most influencial climate factors are for determining discharge levels in the study region. We collected climate data from three different sources (SNOTEL site, interpolated weather data, and satellite data), and trained a machine learning model for each dataset to predict discharge levels.

**Research Question:** 

1. Based on several climate factors can we train a model to estimate discharge in a specific hyrdobasin?

2. To what extent does a glacier influence river discharge levels?

3. Can global data collection methods (such as satellites) provide sufficiently detailed, daily data to predict discharge levels?  

**Datasets:**

USGS Gage Data --  [Dataretrieval](https://github.com/USGS-python/dataretrieval)
Site number - 12082500

USDA SNOTEL Data -- [Rainier Weather](https://wcc.sc.egov.usda.gov/reportGenerator/edit/customMultiTimeSeriesGroupByStationReport/daily/start_of_period/679:WA:SNTL%7Cid=%22%22%7Cname/2013-01-01,2022-02-01/PREC::value,PRCPMTD::value,TAVG::value,TMIN::value,TMAX::value,SMS:-2:value,SMS:-4:value,SMS:-8:value,SMS:-20:value,SNDN::value,WTEQ::value,SNWD::value,SNRR::value?fitToScreen=false)

Satellite data (MODIS & GPM) -- [Google Earth Engine](https://code.earthengine.google.com/b317a307847ff930a41fa60d5942bfdf?noload=true)


**Tools and Packages:**

* python 3.8
* matplotlib
* numpy
* pandas
* geopandas
* jupyter
* shapely
* rioxarray
* scikit-learn
* dataretrieval
* folium

**Planned Methodology and approach:**

1. Identify the hydroshed and draw a shapefile signifying its borders
2. Collect SNOTEL data at the Paradise site location within the hydroshed (#679)
3. Collect interpolated weather data from Daymet
4. Clip MODIS and GPM satellite data to ROI and export data from Google Earth Engine
5. Build machine learning model for each dataset
6. Evaluate results of models

**Expected Outcomes**

We anticipate discharge to be particularly correlated with climatic factors such as precipitation and temperature, given that the study area includes glaciers that influence discharge levels. Additionally, we expect that glacial influence on discharge will be heightened during warmer, drier months as main snow melt has already occurred. When comparing machine learning models, we expect the SNOTEL site to perform the best as it provides the most detailed daily information on site.

![Mt Rainier](doc/MtRainier.jpeg)

