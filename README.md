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

The interactive donut chart below shows the number of manufacturing factories available for each product type all over the world. Hovering over the chart shows details and top dropdown allows user to filter factories based on countries.[![image](https://user-images.githubusercontent.com/49468721/137227761-e5a19564-291e-42bf-9850-8e44f8488c13.png)](https://vizhub.com/siddhipa/dfc92cac6f174a4289ec8ae05d40c4d8)

To get a better sense of the top countries and their breakdown of factories in terms of different types of products they manufacture, the stacked bar chart is used. The chart has tooltips for each bar portion and highlighting effect when hovered over legend.[![image](https://user-images.githubusercontent.com/49468721/141050559-d90b4fc2-3146-4a76-84b5-e22242698aac.png)](https://vizhub.com/siddhipa/360db8e242da4cdf9bfb9a042d3ae9e6)

The bubble world map visualizes total number of Nike Factories by country using circles on a map allowing users to pan & zoom and hover over each country to get its details. In coming weeks, this map will have animation effects/interaction for users. [![image](https://user-images.githubusercontent.com/49468721/139173222-636df8fe-e5ed-4128-b311-378a03bdd7b2.png)](https://vizhub.com/siddhipa/5faede5e67704af7a368c3905781b673)

The bar chart visualizes the top 15 Nike factories in terms of the total number of workers employed. It also uses colors to indicate types of products manufactured by factories. The country menu at the top allows filtering of factories. Hovering over highlights the bar and shows tooltips with details such as factory name, its country, and total workers.[![image](https://user-images.githubusercontent.com/49468721/141049790-cfe5d165-3858-4e35-8074-c40a0adec976.png)](https://vizhub.com/siddhipa/e3fb0093f5394a2eb79105498400f1e6)

The column chart displays countries where Nike factories are situated and the average percentage of either females or migrants among employed workers based on the selection of menu at the top. Hovering over bars shows tooltips and highlights the respective bar.[![image](https://user-images.githubusercontent.com/49468721/141050260-b7847b7f-edf8-44e6-be23-6b220451a765.png)](https://vizhub.com/siddhipa/bd1bc58d07de43aeab6335429e313109)


## Questions & Tasks

The following tasks and questions will drive the visualization and interaction decisions for this project:

 * Around the world, where are the manufacturing factories of Nike are located (country-wise/city-wise)? Which country has a greater number of factories?
 * Which types of products are more common?
 * How the number of workers is distributed all over factories?
 * How is the distribution of female and migrant workers across factories around the world? Which country has the highest female and migrant workers percentage? 
 

## Sketches

The following sketch shows an initial draft of the visualization imagined for the given dataset.
![image](https://user-images.githubusercontent.com/49468721/136826714-958d8d1f-b9a6-4d43-bfa9-e5062d8748ad.png)

The top left plot shows the distribution of all Nike manufacturing factories across the world and will help users to know the country with the highest number of factories. Here, the size of circles represents the number of factories located within a country. Zooming in the world map will help users to see cities where factories are actually situated i.e. zooming a country will split the bigger circle into smaller circles representing cities of factories whereas zooming out shows the bigger circle whose size represents the number of factories. All data points will have tooltips indicating details about factories.

The bottom left donut chart displays the distribution of factories based on product types they manufacture. It will help users to know which product type factories are more common and which are few in number. The color legend will have a different color palette making sure colors are distinguishable even to color-blind users. The country dropdown at the top will allow selecting countries and types of factories situated there. Thus, users can select either 'All' or a specific country to see factory type distribution. Changing the country will update the donut chart based on the number of factories situated there. Also, parts/sections of donut charts will have labels showing the number of factories for each product type. 

The top right bar chart shows the total number of workers employed in all factories. Hovering on bars will show tooltips with the number of workers. Two dropdowns at the top will allow users to filter bars based on country and product type that factories manufacture. Both will have an 'All' option to select in order to display all factories and their workers. Changing selections for country and product type will have animation of changing bars in the plot.

The bottom right bar chart shows the female percent workers employed by all countries. In this plot, users will have the option to choose the y-axis with either percent of female workers or with percent of migrant workers. Hovering over the bars will show the exact value for that bar. This plot will help to understand how Nike factories have diverse employees in terms of female/migrant workers all over the world.



## Schedule of Deliverables

1.	Interactive Donut chart	  	
   - Create donut chart	(10/11-10/13)
     - Grouping data by countries & product types  
     - Counting number of factories for each group
  	  - Add legend and labels
   - Add interaction for filtering based on country selection	(10/13-10/17)
     - Populating dropdown with countries and handling click events
     - Update donut chart and legend
   - Improvements based on feedback/suggestions	(10/17-10/19)
   
2.	Interactive Map
   - Create a world map and add circles with different radius (10/19-10/21)
     - Grouping data by countries & counting number of factories
     - Add legend indicating circle size and values
   - Zoom in & out of map allowing to countries and cities	(10/21-10/27)
   - Animation that breaks one bigger circle (for a country) into smaller circles (for cities) on zooming in and vice versa	(10/21-10/27)
   - Add tooltips on hovering	(10/21-10/27)
   - Improvements based on feedback/suggestions (10/27-10/29)
   
3.	Interactive Bar chart (filtering data)
   - Create bar chart	(10/29-10/30)
     - Handle empty/0 number of workers
   - Highlighting the bar and showing tooltip on hovering	(10/30-10/31)
   - Add interaction for conuntry-based filtering (10/31-11/5)
     -	Populating dropdown with countries and handling click events
     - Update X & Y axes
     - Include hovering effect
   -	Add interaction for product type-based filtering (10/31-11/5)
   -	Improvements based on feedback/suggestions (11/5-11/7)
   
4.	Interactive Bar chart (changing axis)						
   - Create bar chart (11/7-11/8)
     - Grouping data by countries
     - Handling 0 or empty percent values
     - Averaging over percent migrant workers and percent female workers
   - Highlighting the bar and showing tooltip on hovering	(11/8-11/9)
   - Add interaction to change Y-axis (11/9-11/11)
     - Populating dropdown and handling click events
   - Improvements based on feedback/suggestions		(11/11-11/13)
