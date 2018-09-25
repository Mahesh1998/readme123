## Map:
The 2.5D map is created to find the shortest path between source and destination so that the buildings and other obstacles in the outdoor environment can be visualized.
## Data collection:
Data is collected from OSM (Open Street Map) to create a 2.5D map.
## Data processing:
With the help of QGIS and python code, data processing is done that has been fetched from OSM.
## Shortest path:
<ol>
<li> All the possible paths are traced with the help of Voronoi Diagram. </li>
<li>The shortest path has been found with the help of A* algorithm.</li>
</ol>

## API: 
URL-  http://10.44.27.77:5000/source/destination<br>
By providing the source and destination given in the form of addresses, hit the above-mentioned URL.<br>
The 3 maps are:
<ol>
<li>The first map generated contains data for 2.5D.<br>
<img src="Outdoor_Pics/first_map.png"></li>
<li>The second map contains all the possible paths marked with source and destination.<br>
<img src="Outdoor_Pics/second_map.png"></li>
<li>The third map contains the shortest path.<br>
<img src="Outdoor_Pics/third_map.png"></li>
</ol>
&nbsp; All the maps generated are visualized with the help of MATPLOTLIB( python).