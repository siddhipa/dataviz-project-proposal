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
![image](https://user-images.githubusercontent.com/49468721/134425401-6324e9fc-367b-41c5-9c50-964ac1cd0b48.png)

The top left plot shows the distribution of all Nike manufacturing factories across the world. Here, the size of circles represents the number of factories located within a country and its luminance indicates the percentage of migrant workers employed. Zooming in helps users to see cities where factories are actually situated. Clicking on circles allows users to check factory type distribution within the selected country shown by the pie chart on the top right corner. The percentage of female workers across factories manufacturing different types of products is shown by the bottom right chart. And, the bottom left bar chart displays the number of total workers across different countries allowing users to know about the factory/country that employed the highest number of workers.

## Open Questions

I am unsure about how user interactivity can be incorporated with these charts using d3.
