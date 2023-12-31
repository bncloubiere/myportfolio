---
layout: post
title: Wildfires in France 2012-2022
image:
  path: /assets/wildfire_france/wildfire_image.jpg
  scrset:
    800w: /assets/wildfire_france/wildfire_image_w800.jpg
    400w: /assets/wildfire_france/wildfire_image_w400.jpg
    200w: /assets/wildfire_france/wildfire_image_w200.jpg
description: >
  This is a small project that looked at some data about wildfires in France between 2012 and 2022
  Credit: Thibaud Moritz/AFP via Getty Images
sitemap: false
hide_last_modified: true
---

## Introduction
Welcome to my first project published on my portfolio website! To inaugurate, I decided to use my skills in data analysis to learn more about a topic that is important to me: wildfires in France over the last decade.

As a French national, I grew up in the North-East part of France, where the climate was pretty close to the one in the UK. I was in the lucky position to have family to visit every years in the South of France, and more precisely in what is now known as the Occitanie region.

Even when I was a child, I remember that wildfires were a fairly common occurence. A topic which I could hear on TV during the news, but not one I could directly oberserve very often.

As an adult however, every time I visit the South of France, I am struck by the number of wilfires occuring and by the scarred landscape of burnt woods and bushlands.

I have the gut feeling that the frequency of wildfires is increasing over the year and that wildfires are now more frequent that they used to. However, I could not exclude the potential explanations that what differed was my percetion between my childhood and adult stages, or that I became more sensitive to those issues due to my awareness of climate change.

To check if my instinct is correct, I decided to look at unbiased raw data across the mainland French territories.

## Data preparation

### Source of the data

**Wildfires database**
The database about wildfires in France between 2012 and 2022 was collected from the gouvernmental website from bdiff.agriculture.fr and was consulted on 2023-11-20.

**Cities localisation datbase**
The databse about French cities, their INSEE code and spatial coordinates was collected as cities.csv from the related [governmental website](https://www.data.gouv.fr/fr/datasets/villes-de-france/).

**Map of French departments for folium**
The polygons needed for the geospatial localisations of departments in France, and their boundaries, were created by Gregoire David and are accessible on his [website](https://france-geojson.gregoiredavid.fr/). The data was collected as a geojson file renamed departments.geojson on 2023-11-21.

Note: the two French territories in Corsica (2A and 2B) were manually removed from the geojson in order to focus on the French mainland only.

### Data

The various steps taken to clean the data and prepare it for analysis are presented in the Jupyter Notebook [here]. \
This includes: loading and manipulating dataframes with pandas, data cleaning, automatic translation with Google Translae API.

The data analysis itself and SQL queries raised are referenced in the following [notebook].\
This includes: SQL queries, data visualisation (Matplotlib, seasborn), geospatial analysis with folium.

## Results and Observations

{% include img-right-box.html path="/myportfolio/assets/wildfire_france/wildfire_image_w800.jpg" alt="test image" 
title="Number of wildfires per year 800" 
description="Based on trendline, the number of wildfires in France has doubled in 2022 compared to 2012" %}

{% include img-right-box.html path="/myportfolio/assets/wildfire_france/wildfire_image_w600.jpg" alt="test image" 
title="Number of wildfires per year 600" 
description="Based on trendline, the number of wildfires in France has doubled in 2022 compared to 2012" %}

some text to test

{% include img-left-test.html path="/myportfolio/assets/wildfire_france/wildfire_image_w600.jpg" alt="test 2"
title="This is the title on right" 
description="Some more text that will appear to the right of the image number 2." %}
