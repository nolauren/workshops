
## CartoDB Tutorial

CartoDB is a web-based tool for visalizing and analyzing
small to medium sized spatial datasets. While ostensibly open-source
software, it is quite difficult to compile yourself and much of
the nice UI is actually proprietary. Fortunately, they offer a
good free-tier of the service (no credit card needed; just an e-mail)
which should suffice for the purposes of this tutorial.

### Set-Up Account
Go to https://carto.com/signup/ and sign-up.
I suggest using your @institutionname.edu account. It will give you access to an 
education account, which comes with more options than a non-education account. 

### Getting Started
Go to Maps -> Your Datasets. On the right of the screen, click New Dataset.

We are going to work with [Klaverns](https://github.com/nolauren/cartodbTutorial/blob/master/data/klavern.csv).

To download, click on Raw. You'll see the data set. Then, right click and 
Save As a .csv file. For our purposes, let's name is klaverns.csv.


### Working with  data in CartoDB

Importing data to CartoDB is, in theory, very easy. Just drag
and drop the file you want into the dashboard and you're done!

In the Dataset view, go to New Dataset -> Browse -> Select "klaverns.csv".
Connect data.



The data view shows a tabular representation of the data we
loaded into CartoDB. The program has already detected which
columns correspond to latitude and longitude and has created
variables called `the_geom`. This is a special data types that 
tell CartoDB where each row should
be mapped. There is also a column called `cartodb_id` with a
unique identifier for each row; we will use this a bit in this
tutorial, but it is particularly useful when integrating with
PHP and Javascript. The data types for the columns from the csv
file have also been automatically detected. Take note of these
as they will be important later.

### Let's map.

Switching to the map view, we begin to see the benefits of using
a tool like CartoDB. A reasonably nice map has been constructed
out of the box from the data we imported. Zooming in and out,
you'll notice that the map has discrete zoom levels. That's because
the map is being created by a tile server, which serves rasterized
tiles to the browser. 

What's the difference between rastor and vector data?

vector data model: [data models] A representation of the world using 
points, lines, and polygons. Vector models are useful for storing data
that has discrete boundaries, such as country borders, land parcels,
and streets. - ESRI GIS Dictionary

In other words, it is the acutal shapes. It is stored as points (x,y). 

raster data model: [data models] A representation of the world as a 
surface divided into a regular grid of cells. Raster models are useful 
for storing data that varies continuously, as in an aerial photograph, 
a satellite image, a surface of chemical concentrations,
or an elevation surface. - ESRI GIS Dictionary

In other words, it is a picture. It is stored as pixels. 
(You can't do analytics on rastor data.)

### Visualizations

The wizard offers a nice set of options out of the box.
Let's walk through several options.

On the right side of the map is a set of tools. 
Select "wizards".

To adjust the size and outline of the dot, adjust the "Marker Fill" and "Marker Stroke".
You can also add a "Label". In our case, we probably won't do this because the map 
will look too cluttered.

Play around!

We can also pick different spatial visualizations.
Let's walk through them.

For example, let's look at Torque. We have an issue. What is it?

To solve this issue, we can use a SQL query!

Go to SQL and type:

```
SELECT * FROM klavern
WHERE year > 0
```
And select Apply.
Let's try torque again!

### Let's zoom in.

Wizard -> Simple

Let's zoom in on Virginia.

Change Labeltext to "nickname".

Let's get rid of the Not Named entries.

```
SELECT * FROM klavern
WHERE nickname != 'Not Named'
```

Adjust the basemap and details. 

Let's add some more details. 
Click on infowindow. Let's turn on nickname, notes and year.
You can also select Hover instead.

### Final 

To actually make this a map, you must save it. To do so, select "Visualize."

 


