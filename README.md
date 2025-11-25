# Predicting Lithium Presence From Surrounding Geological Data

## Kara Bivens and Bradley Bowen

The goal of our project is to build a model which uses the proportion of certain minerals within a given spatial radius as predictors for the nearby presence of lithium. If our model has strong predictive power, this project could assist the mining industry in determining where lithium, a valuable resource, can be found.

### Research questions: 
Objectives:

- Design a model that can predict the presence of lithium with high accuracy, precision, and recall across various states in the U.S.
- Incorporate geospatial distance metrics in creating the predictors for lithium presence, namely in finding the proportions of geochemically relevant minerals within a certain radius

Questions: 

- Which minerals are the best predictors for the presence of lithium? (This question will be resolved through literature review.)
- How effective are various optimization strategies and model alternatives at predicting lithium presence?
- How can we cluster our data so that we can predict lithium presence at a more granular level?

### Data

Our data originates from the [USGS](https://mrdata.usgs.gov/mrds/map-commodity.html#home) (the USGS Mineral Resources Data System). The data includes mineral deposit location with information about the type of mineral and mining activity. 

### Python Libraries 

- geopandas
- numpy
- zipfile
- os
- matplotlib
- sklearn
- pandas
- shapely
- scipy

### Initial Methods
We will first conduct a literature review to find which minerals are geochemically linked to lithium. We will then clean our data and check that the logic of our project is sound (that mines which contain lithium contain other minerals, that those mines are near mines that do not contain lithium, etc). We will use K-Means Clustering to form centroids and then create a radius around each centroid, ultimately calculating the proportion of each of the geochemically relevant minerals within that radius. We will use point geometry from the shapely package to help us define the radius. The proportions will be used as predictors in a logistic regression model, along with an additional predictor for the number of mining sites within that cluster. We will augment the data, run ensembling techniques, and test our predictive power on lithium presence in other states. As needed, we will develop alternative models in an attempt to improve predictive performance. 

### Expected Outcomes

According to the research paper cited below, geochemically linked minerals have previously served as effective predictors of lithium presence in international contexts. We believe this result is likely to occur in our United States analysis as well, so we think our model will have strong predictive power after augmentation. However, we recognize that our USGS data likely does not grant us access to every tectonic and geological variable that would help us predict most effectively, so our model might struggle to generalize across states. Our presentation will likely include visualizations, models, and analysis of statistical techniques. 

#### Additional Information

We knew previously that lithium is often extracted from spodumene rock. From prior knowledge, there are spodumene belts that are located in North Carolina outside of Charlotte. Also from our prior knowledge of NC mining, there appear to be locations of tin, feldspar, and quartz that are extracted from nearby sites. 

#### References

[1][Columbite-tantalite and cassiterite as indicator minerals for lithium pegmatites: implications from geospatial and mineralogical analyses of stream sediments in southeast Ireland](https://link.springer.com/article/10.1007/s00126-025-01366-8)
