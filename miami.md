# Mapping

## Getting Started

Several broad categories of mapping (not exhaustive by any means!):

1. Flexible interactive visualizations served over the web. Ex. CARTO (tool), [Photogrammar] (photogrammar.yale.edu) (project), and [Mapping Inequality](https://dsl.richmond.edu/panorama/redlining/) (project)

2. Narrative mapping. Ex StoryMap.js and Odysessy (https://cartodb.github.io/odyssey.js/)

3. Spatial Analysis such as building models of spatial processes like the spread of diseases based on the movement of people. Ex. python/r , ArcGIS

They rely on Geographical Data (proprietary databases (vector and raster), georectifying, and geolocation) Ex. ArcGIS 






## CartoDB Tutorial

CartoDB is a web-based tool for visalizing and analyzing
small to medium sized spatial datasets. While ostensibly open-source
software, it is quite difficult to compile yourself and much of
the nice UI is actually proprietary. Fortunately, they offer a
good free-tier of the service (no credit card needed; just an e-mail)
which should suffice for the purposes of this tutorial.

#### Set-Up Account
Go to https://carto.com/signup/ and sign-up.
I suggest using your @institutionname.edu account. You can then email Carto 
about access to free plans by going here: https://carto.com/community/ambassadors/#started. 
They review applications every month. 


### Data



Let's take a look at the data. Each row is a photo. Each column is an observation about the photo. Several aspects of this data:
- Make sure everything it types the same. For exampe, "Alfred T. Palmer" is always typed this way. 
- If we google a cnumber, it will correspond to the LOC call number.  When working with an archive/collection, consider keeping the collection's unique identifying information.   
- We used "NA" when we didn't know a value. Often people just keep the cell blank. We did this so we knew what we had checked. 

For mapping, the most important are the columns about location information. 
When we first had this state, we only had City, County, and State. 
So let's start by looking at how Carto can help us get the longitude and latitude. 



 

### Uploading Data

Importing data to CartoDB is, in theory, very easy. Just drag
and drop the file you want into the dashboard and you're done!

Go to New Map -> Add Datasets -> Connect Dataset.

We are going to upload the dataset: photo_dataset_all_raw.csv


Once the data is loaded, a pop-up will appear on the bottom left that will show you the data. This will only appear once. 
To get back to the data, go to the top left of the screen. There you will see the Carto logo, your username, and Maps. Click on Maps -> Your datasets. 


The screen will shift to a map interface. This is called "Carto Builder". 



### Carto Builder

There are two main ways CartoBuilder is organized: Layers and Widgets. Along with these options, 



Switching to the map view, we begin to see the benefits of using a tool like CartoDB. A reasonably nice map has been constructed out of the box from the data we imported. Zooming in and out, you'll notice that the map has discrete zoom levels. That's because the map is being created by a tile server, which serves rasterized tiles to the browser.

What's the difference between rastor and vector data?

vector data model: [data models] A representation of the world using points, lines, and polygons. Vector models are useful for storing data that has discrete boundaries, such as country borders, land parcels, and streets. - ESRI GIS Dictionary

In other words, it is the acutal shapes. It is stored as points (x,y).

raster data model: [data models] A representation of the world as a surface divided into a regular grid of cells. Raster models are useful for storing data that varies continuously, as in an aerial photograph, a satellite image, a surface of chemical concentrations, or an elevation surface. - ESRI GIS Dictionary

In other words, it is a picture. It is stored as pixels. (You can't do analytics on rastor data.)





#### Base Map

We can change the base map. Carto offers several options. The Voyager style offers several different colors and varying degrees of detail. For example, Positronh has city and state labels while Positron (LITE) does not. Voyager is a slighlty different color as well as includes major highways. The color will depend on the mood you are trying to convey.  Base map needs will also depend on the time period being mapped. Particularly for Photogrammar, we would not want to use the Here map collection. It would be ahistorical. Also, place names are not value neutral. For example, if one were mapping indigenous communities, which place names to use is a major issue to consider. If you want to add your own map, Mapbox is an option. This will require turning a map into raster data to then upload. One option is to use the open source [QGIS](https://www.qgistutorials.com/en/docs/georeferencing_basics.html). Programming Historian also offers [a tutorial](https://programminghistorian.org/lessons/geocoding-qgis). 



#### Layers - Visualizations/ Style

Click on Layers. By default, our data is the first layer. We will primarily work with this layer during the workshop. If we wanted to layer the map wtih additional data, all we would need to add a new layer. 

Let's explore our default layer. Click on "photo_dataset_all_raw" -> Style  


Points: They are great, but you need to be careful when the actual location isn't precise. Since we are looking at a national scale, this is less of an issue. However, if we zoom in, this becomes an issue as we don't have the exact location of many of the photos. Labels can be added. We have way too much data for "Labels", but it is worth noting. If you click on it, you can see the options. What we can do instead is add a Pop-Up. Select "Pop-Up" and select the metadata you want to apeear. In our case, I am going to select pname, year, and title. You can change the name of the title as it will appear in the pop-up here, which we want to do here instead of adjusting our original data.  If you select the final "Pop-Up Header with URL" and provide a full URL, an image will appear in the header. The url column needs to be called "photourl" and the first selected item. You can also select if you want a user to see the pop-up when they "hover" or "click". We picked click becasue of the density of points. 

 

Hexbin: They can be very helpful for this  with point data. It suggests the general area but doesn't visually suggest we know the exact location. It also helps show photo counts. One thing I don't like about Carto is their default color ramp suggests the lighter the color, the more photos there are.  Visually, we tend to associate darkness with a higher count, so I'd switch the ramp. We can do that by going to color. One thing to keep in mind those who may be color blind. I find [this tool](http://colorbrewer2.org/#type=sequential&scheme=BuGn&n=3) very helfpul. You will notice that this is the same color ramp we use for Photogrammar. Let's pick this green color ramp under Style in Carto.

- Heatmap: It can be great! Just not for this data set.


- Legend: You can add aspects as necessary for your project. To rename the Title, we have to reame the layer.


Let's make our map points with an appropriate pop-up. Then, we can add widgets! 


#### Widgets

Widgets are a way to add additional interactivity to the map.  Click on the pencil on the far left menu ("Edit Map"). Then select Widgets-> +Add New Widget.




#### Publish 






