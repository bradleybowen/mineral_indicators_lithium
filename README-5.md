# Predicting Lithium Presence From Surrounding Geological Features (Updated Nov 5)

## Kara Bivens and Bradley Bowen

The goal of our project is to build a model that uses the prevalence of specific minerals to predict the presence of lithium in a given region.


### Research questions: 

- Which minerals are the best indicators for the presence of lithium?
- Are there geographic/geological patterns that are indicative of where lithium is extracted?
- What is the best method to quantify the distance between lithium and other mineral deposits?
- Are there location-specific features that influence prediction methods?

### Data

Our data originates from the [USGS](https://mrdata.usgs.gov/mrds/map-commodity.html#home) from their mineral resources data system. This includes mineral deposit location filtered by type of mineral and mine activity. 

### Python Libraries 


- os
- glob
- matplotlib
- numpy
- itertools
- PIL
- sklearn
- tensorflow
- pandas
- geopandas
- rasterio
  


### Initial Methods

We will first determine which minerals have a preexisting geochemical analysis (from existing research papers) that links key indicators to lithium. Next, we will explore the data and make initial visual insights. The following portion of the analysis will include determining an effective and interpretable distance metric for quantify the distance between lithium and neighboring mineral deposits. This distance metric be used as a predictor of lithium presence along with indicator variables for which type minerals are nearby. After developing a model, we will work to refine the model through optimization strategies. Additional statistical methods may be used to develop additional predictors and uncertainty quantification such as confusion matrices, test statistics, etc. 

### Expected Outcomes

According to the research paper (found below), other minerals can serve as effective predictors of lithium presence. We believe this result is likely to occur in our analysis. It is also expected that the model will perform well in a limited geographic space, with constrained generalizations. Our presentation will likely include visualizations, models, and analysis of statistical techniques. 



#### Additional Information

Lithium is often extracted from spodumene rock. From prior knowledge, there are spodumene belts that are located in North Carolina outside of Charlotte. Also, from NC mining, there appear to be locations of tin, feldspar, and quartz that are extracted from nearby sites. 


#### References


[1][Columbite-tantalite and cassiterite as indicator minerals for lithium pegmatites: implications from geospatial and mineralogical analyses of stream sediments in southeast Ireland](https://link.springer.com/article/10.1007/s00126-025-01366-8)
