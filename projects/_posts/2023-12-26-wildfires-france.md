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
<h1><center> Wildfires in France between 2012 and 2022 </center></h1>



## Introduction
 

Welcome to my first project published on my portfolio website! To inaugurate, I decided to use my skills in data analysis to learn more about a topic that is important to me: wildfires in France over the last decade.

As a French national, I grew up in the North-East part of France, where the climate was pretty close to the one in the UK. I was in the lucky position to have family to visit every years in the South of France, and more precisely in what is now known as the Occitanie region.
 

![Occitanie region](/myportfolio/assets/wildfire_france/Occitanie_in_France_2016.png)

Occitanie region in France. Source: [Wikipedia](https://en.wikipedia.org/wiki/Occitania_(administrative_region))
{:.figcaption}
 

As a child, I remember that wildfires were a fairly common occurence. A topic which I could hear on TV during the news, but not one I could directly oberserve very often.

As an adult however, every time I visit the South of France, I am struck by the number of wilfires occuring and by the scarred landscape of burnt woods and bushlands.

I have the gut feeling that the frequency of wildfires is increasing over the year and that wildfires are now more frequent that they used to. However, I could not exclude the potential explanations that what differed was my percetion between my childhood and adult stages, or that I became more sensitive to those issues due to my awareness of climate change.

To check if my instinct is correct, I decided to look at unbiased raw data across the mainland French territories.

 


## Data preparation
 

### Source of the data
 

**Wildfires database**
The database about wildfires in France between 2012 and 2022 was collected from the gouvernmental website from [bdiff.agriculture.fr](https://bdiff.agriculture.gouv.fr/incendies) and was consulted on 2023-12-20.

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
 

{% include img-right-box.html path="/myportfolio/assets/wildfire_france/number_wildfires_2012_2022.png" alt="Number of wildfires between 2012 and 2022" 
title="Number of wildfires in France between 2012 and 2022" 
description="The dataset excluded the department 'Marne'" %}
 



{% include img-left-box.html path="/myportfolio/assets/wildfire_france/List-of-London-Boroughs_w600.png" alt="Greater London" 
title="The total surface burnt was 1,502 square km2" 
description="This is almost equivalent to the surface of Greater London (1,572 square km)" %}
 



{% include img-right-box.html path="/myportfolio/assets/wildfire_france/france_wildfires_yearly_w600.png" alt="annual trend of wildfires" 
title="Number of wildfires per years between 2012-2022" 
description="Over 10 years, the average number of wildfires per year has doubled from 1,500 to 3,000" %}
 


{% include img-left-box.html path="/myportfolio/assets/wildfire_france/france_wildfires_monthly_w600.png" alt="monthly trend" 
title="Average number of wildfires per month" 
description="Wildfires are more likely to happen over the summer and March" %}
 


{% include img-right-box.html path="/myportfolio/assets/wildfire_france/folium_map.PNG" alt="map French departments with most wildfires" 
title="Distribution of wildfires across French departments" 
description="Wildfires in France were largely concentrated in the departments near the Mediterranean Sea, and the center West coast" %}
 


{% include img-left-box.html path="/myportfolio/assets/wildfire_france/folium_map_artigues.jpg" alt="monthly trend" 
title="Most impacted municipality" 
description="The most impacted municipality was Artigues, in the South-East, wuth 17.04 square km. This is equivalent to 2,387 footbal fields" %}
 


{% include img-right-box.html path="/myportfolio/assets/wildfire_france/surfaces_burnt_types.png" alt="types of surfaces burnt" 
title="Types of surfaces burnt" 
description="Wildfires affected wood areas the most. However, the shrublands are disproportionaly affected compared to their share of the French surface (<5%)" %}
 


## Conclusions
 
We have seen that the number of wildfires has been steadily increasing over between 2012 and 2022. The fires were also mostly located in the South of France, and as expected, in the Occitanie region. The reason why those areas were more affected than others is likely due to the fact that they contain most of the shrublands in France. This type of dry vegetation is particularly sensitive to wildfires and seems prone to burnt easily in summer and at the end of Winter, before the Spring rain showers.


