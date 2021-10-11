# Data Visualization Project

## Data

The data I propose to visualize for my project is [Nike Global Manufacturing Data Export (February 2021)](http://manufacturingmap.nikeinc.com/). It consists of details of Nike manufacturing factories across the world – their locations, factory types, number of workers, female workers, and migrant workers, etc. The main goal of this data visualization project is to easily understand how Nike factories and their workers are distributed all over the world.

Details of Attributes –

|Attribute Name | Description | Type |
| --- | --- | --- |
| Factory Name | Name of Factory | Categorical |
| Factory Type | Type of factories such as Materials or Finished Goods | Categorical |
| Product Type | Type of products it manufactures such as Apparel, Equipment, Footwear, or Materials. | Categorical |
| "Nike, Inc. Brand(s)" | Brands included such as Nike or Converse or both | Categorical |
| Supplier Group | Name of supplier | Categorical |
| City | Name of the city where the factory is situated | Categorical |
| State | Name of the state where the factory is situated | Categorical |
| Postal Code | Postal code | Categorical |
| Country/Region | Name of the country where the factory is situated | Categorical |
| Region | Region Name | Categorical |
| Total Workers | Number of workers employed in the factory | Quantitative |
| Line Workers | Number of line workers | Quantitative |
| % Female Workers | Percent of female workers | Quantitative |
| % Migrant Workers | Percent of migrant workers | Quantitative |

You can find the given dataset and description [here](https://gist.github.com/siddhipa/3357f23f4ecd08f3737215f16026269e).


## Prototypes

I’ve created a proof of concept visualization of this data. It's a basic scatter plot and it shows the total number of workers employed in factories vs the number of line workers. The relation seems to be linear stating the obvious that with a number of increase in line workers there will be an increase in the number of total workers. Most factories are average-scale factories employing around 3000-4000 employees.
[![image](https://user-images.githubusercontent.com/49468721/134425996-5a91e0b1-b058-41a0-b1d0-9432479456dc.png)](https://vizhub.com/siddhipa/e75567ad58d44564b91fa851ad9e6f3e)

I improved the above scatter plot by including color channel to show factories with different product types. Hovering over product types in color legend highlights only those factories that belong to the chosen product type. Also, the circles in the plot have tooltips associted with them displaying factory names and countries.
[![image](https://user-images.githubusercontent.com/49468721/136814990-b097c9a6-3146-4643-bfd2-9cfca8e417ea.png)](https://vizhub.com/siddhipa/dec7ce1c8fa449e794385aef310be434)

To integrate interaction in the scatter plot, the below plot shows the availability of dropdown with countries that allows users to filter factories based on countries and to check proportion of line workers to number of workers and product types manufactured by them.[![image](https://user-images.githubusercontent.com/49468721/136815768-8edc046f-d09e-4c89-8920-aedb5845a905.png)](https://vizhub.com/siddhipa/374452615186417a921623c8a7b3010a)


## Questions & Tasks

The following tasks and questions will drive the visualization and interaction decisions for this project:

 * Around the world, where are the manufacturing factories of Nike are located (country-wise/city-wise)? Which country has a greater number of factories?
 * Which types of products are more common?
 * How the number of workers are distributed all over factories?
 * How is the distribution of female and migrant workers across factories around the world? Which country has the highest female and migrant workers percentage? 
 

## Sketches

The following sketch shows an initial draft of the visualization imagined for the given dataset.
![image](https://user-images.githubusercontent.com/49468721/136826714-958d8d1f-b9a6-4d43-bfa9-e5062d8748ad.png)

The top left plot shows the distribution of all Nike manufacturing factories across the world and will help users to know the country with the highest number of factories. Here, the size of circles represents the number of factories located within a country. Zooming in the world map will help users to see cities where factories are actually situated i.e. zooming a country will split the bigger circle into smaller circles repsenting cities of factories whereas zooming out shows the bigger circle whose size represents the number of factories. All data points will have toolotips indicating details about factories. 

The bottom left donut chart displays the distribution of factories based on product types they manufacture. It will help users to know which product type factories are more common and which are few in number. The color legend will have different color palette making sure colors are distinguishable even to color blind users. The country dropdown at the top will allow to select country and types of factories situated there. Thus, users can select either 'All' or a specific country to see factory type distribution. Changing the country will update the donut chart based on number of factories situated there. Also, parts/sections of donut charts will have labels showing number of factories for each product type. 

The top right bar chart shows total number of workers employed in all factories. Hovering on bars will show tooltips with number of workers. Two dropdowns at the top will allow users to filter bars based on country and product type that factories manufacture. Both will have 'All' option to select in order to display all factories and their workers. Changing selections for country and product type will have animation of changing bars in the plot. 

The bottom right bar chart shows the female percent workers employed by all countries. In this plot, users will have option to choose y-axis with either percent of female workers or with percent of migrant workers. Hovering over the bars will show the exact value for that bar. This plot will help to understand how Nike factories have diverse employees in terms of female/migrant workers all over the world.
