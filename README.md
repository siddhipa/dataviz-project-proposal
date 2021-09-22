# Data Visualization Project

## Data

The data I propose to visualize for my project is [Nike Global Manufacturing Data Export (February 2021)](http://manufacturingmap.nikeinc.com/). It consists of details of Nike manufacturing factories across the world – their locations, factory types, number of workers, female workers, and migrant workers, etc. 

Description of Attributes –

Factory Name – Name of Factory

Factory Type – Type of factories such as Materials or Finished Goods

Product Type – Type of products it manufactures such as Apparel, Equipment, Footwear, or Materials.

"Nike, Inc. Brand(s)" – Brands included such as Nike or Converse or both

Supplier Group – Name of supplier

City – Name of the city where the factory is situated

State – Name of the state where the factory is situated

Postal Code – Postal code

Country/Region – Name of the country where the factory is situated

Region – Region Name

Total Workers – Number of workers employed in the factory

Line Workers – Number of line workers

% Female Workers – Percent of female workers

% Migrant Workers – Percent of migrant workers

You can find the dataset and description [here](https://gist.github.com/siddhipa/3357f23f4ecd08f3737215f16026269e).


## Prototypes

I’ve created a proof of concept visualization of this data. It's a basic scatter plot and it shows the total number of workers employed in factories vs the number of line workers. The relation seems to be linear stating the obvious that with a number of increase in line workers there will be an increase in the number of total workers. Most factories are average-scale factories employing around 3000-4000 employees.
[![image](https://user-images.githubusercontent.com/49468721/134425996-5a91e0b1-b058-41a0-b1d0-9432479456dc.png)](https://vizhub.com/siddhipa/e75567ad58d44564b91fa851ad9e6f3e)


## Questions & Tasks

The following tasks and questions will drive the visualization and interaction decisions for this project:

 * Around the world, where are the manufacturing factories of Nike are located? Which country has a greater number of factories?
 * Which factory has the highest number of workers?
 * How is the distribution of female and migrant workers across factories around the world?
 * Which types of factories and products are more common and where these are located?

## Sketches

The following sketch shows an initial draft of the visualization imagined for the given dataset.
![image](https://user-images.githubusercontent.com/49468721/134425401-6324e9fc-367b-41c5-9c50-964ac1cd0b48.png)

The top left plot shows the distribution of all Nike manufacturing factories across the world. Here, the size of circles represents the number of factories located within a country and its luminance indicates the percentage of migrant workers employed. Zooming in helps users to see cities where factories are actually situated. Clicking on circles allows users to check factory type distribution within the selected country shown by the pie chart on the top right corner. The percentage of female workers across factories manufacturing different types of products is shown by the bottom right chart. And, the bottom left bar chart displays the number of total workers across different countries allowing users to know about the factory/country that employed the highest number of workers.

## Open Questions

I am unsure about how user interactivity can be incorporated with these charts using d3.
