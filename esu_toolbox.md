# Digital Humanities Toolbox
ESU 2017   

This session is an all-encompassing look at incorporating entry-level tools 
for text mining, mapping and timelines into your teaching or research for the first time. 
We’ll use three web-based tools (Storymap.js, Voyant and Timeline.js) and give you a common
dataset to work from. Along the way, we’ll also give you a few tips on how to get your own
data in shape. Preparation: Please bring an Internet-equipped laptop.

----------


## Introductions

----------


## Timeline (Timeline.js)

https://timeline.knightlab.com/


Select "Make A Timeline". It uses Google Docs and will require authentication.

Once on the google spreadsheet, select "Use this template".

If you want to collaborate, select "Share" on the top right of the spreadsheet. 

Once you are finished, go to File -> Publish to the Web -> Publish 
Then, take the URL and go back to https://timeline.knightlab.com/ and scroll down to Step 3.
Once copied, select Preview. 

Limits of Timeline.js:
1. Have to pick a specific time. It doesn't deal with ambiguity. 
2. Can only use media that is supported by the tool. 
3. Only load one piece of media per entry.

Note: The structure of the data is helpful for moving to another tool.

### Sample Data 

New Deal Events: http://xroads.virginia.edu/~MA02/volpe/newdeal/timeline_text.html

FDR 1932 Democratic Convention: https://www.youtube.com/watch?v=6Ht6cJqgC6o

FDR Election: http://depts.washington.edu/depress/images/fdr_1932_seattle_420.jpg

Fireside Chat: https://www.youtube.com/watch?v=z9CBpbuV3ok

CCC Poster: https://upload.wikimedia.org/wikipedia/commons/b/b2/CCC-poster-1935.jpg

TVA Logo: http://www.sourcewatch.org/images/thumb/c/cf/TVA.jpg/170px-TVA.jpg (Timeline.js doesn't support .svg)

Others: [TikiToki](http://www.tiki-toki.com/) 


------------
Time Mapper (http://timemapper.okfnlabs.org/)

Like with Timeline.js, a specific template is needed. 

Here is an example to use as a guide: [Template](https://docs.google.com/spreadsheet/ccc?key=0Al6mO9_3Hr2PdGZnRjEwUWxOekhreTNNZEFEMWRZbkE)

Once on the google spreadsheet, adjust according to your data.

If you want to collaborate, select "Share" on the top right of the spreadsheet. 

Once you are finished, go to File -> Publish to the Web -> Publish 
Then, take the URL and go back to  http://timemapper.okfnlabs.org/create  to add your url in Step 2. 

Now you have choices:
1. Timemap
2. Timeline
3. Map


 

----------------


----------

## Text Analysis with Voyant 

Let's define Text Analysis. Are you familiar with this method? How would you define it?

For our corpus, we will explore the State of the Union addresses.  The State of the Union is delivered by the President of the United States annualy to a joint session of Congress. It is often a space where the President reflects on current issues and outlines goals for the nation. Therefore, it is a key document for understanding the ways the executive branch understands the current position of the country and their priorities. While today it is delivered oraly by the President, the State of the Union was initially a written document submitted to congress. In this workshop, we will use Voyant to identify issues and priorities.


We will be using Voyant:  a web-based text reading and analysis environment.

According to the Voyant Website <sup>[1](#myfootnote1)</sup>, we can do the folllowing:

- Use it to learn how computers-assisted analysis works. Check out our examples that show you how to do real academic tasks with Voyant.
- Use it to study texts that you find on the web or texts that you have carefully edited and have on your computer.
- Use it to add functionality to your online collections, journals, blogs or web sites so others can see through your texts with analytical tools.
- Use it to add interactive evidence to your essays that you publish online. Add interactive panels right into your research essays (if they can be published online) so your readers can recapitulate your results.
- Use it to develop your own tools using our functionality and code. 


### 2016 SOTU Speech
We will start with Obama's final State of the Union address.  

To begin, we will load in our text from a URL: http://programminghistorian.github.io/ph-submissions/assets/basic-text-processing-in-r/sotu_text/236.txt

Now let's take a look at the kinds of text analysis used by Voyant!

#### Cirrus -  Terms - Links Part 1

Cirrus:  Provides a word cloud of the most frequence terms. You can hover over the word to see the number of times it is used. 

-  Is this what you expected? Are there any words you would have expected that aren't included? Any words you think should be removed?


#### Stop Words 

Stop Words are a list of common words that are filtered out before or during text processing. You can use default stop word lists, like those included in Voyant, or create your own.   

Let's say we want to remove "mdash" and add it to our stop words. Go to the bottom left panel that says "Summary Documents Phrases". Next to the question mark is another set of options that only appear once you hover over the area. The first option to the left of the question mark allows us to adjust our stop words. 

Voyant's default setting auto-detects a stop word list. Select "None" and see what happens! 
- Is this helpful?

Let's go back and select "English". To adjust our list, select "Edit List." Let's add "mdash". 

 - Are there any other we want to add? 

Let's add: "that's" and "it's". 

(Tip: When I'm adjusting the stop word list, I like to make a text file with my additional stop words. You'll notice Voyant only allows you to adjust your stop words once. If you try to add more, it deletes your previous custom words.)



#### Cirrus -  Terms - Links Part 2

Cirrus: Now we have a new word cloud!

Terms: We see the raw count of words in a list. 

Links: Provides a collocates graph shows a network graph of higher frequency terms that appear in proximity. Keywords are shown in green and collocates (words in proximity) are showing in red. 

Let's click on "America." Let's take a look at the Reader in the panel to the right. 
- What changed?

Now let's take a look at Trends in the panel furthest to the right. The default is Raw Frequencies. Let's change to Relative Frequenices. This isn't as helpful with one document but will be when we are analyzing more than one at a time. 

Now let's go back Links and double click on "America". 

- What changed?

#### Contexts - Bubblelines 

Contexts: Puts a term in context. ;)

Bubblelines: A visualization of the term frequency in the document. 


#### Summary - Documents - Phrases
 
Summary: Overview of the document.  To increase the number of frequence words, adjust the items slider on the bottom left. 

Documents: We only have one document, but it will be helpful when we look at multiple at once.

Phrases: Provides a table of repreating phrases. 

Let's sort by the most common phrases. (Tip: If Voyant won't let you reset and see all the phraes, reload.)

Pair up and take a few minutes to explore. 
- Interesting insights? 


### Washington vs Obama

Let's now take a look at George Washington vs President Obama's SOTU addressess.


Download the corpus to your Downloads Folder: https://drive.google.com/open?id=0B6zkbDdW8bzIQnpQX2NQbVFYQjg

Unzip the file.

Go to https://voyant-tools.org/ and select "Upload".  The speechs are named according to year. Make sure the files are in numerical order for this determines how Voyant loads them in.  Now, let's explore!

To begin, take a look at Cirrus. 
- Do we want to remove any stop words? If so, why?

Let's remove them. 

##### Summary - Documents - Phrases

- Can we learn anything from this? Document Length? Vocabulary Density? 

We also have a new option - Distinctive Words. Voyant uses Term Frequency-Inverse Document Frequency to weigh how important a word is in the document or corpus. Let's take a look at the terms used by Washington and Obama. 

- Are there any themes we can see in these speeches? By presidency? 

- Do we see particular phrases? 

##### Explore!


### Resources

- Programming Historian: http://programminghistorian.org/
- Historian Macroscope: http://www.themacroscope.org/2.0/
- Humanites Data in R: http://www.humanitiesdata.org


<a name="myfootnote1">1</a>: See https://voyant-tools.org/docs/#!/guide/about


-------------------

## Mallet

For the tutorial, visit [here](https://programminghistorian.org/lessons/topic-modeling-and-mallet) and [here](https://docs.google.com/document/d/1GzrdJ_q7HH8_OpXFCIkGo8vPKBc_OrOx-Ifh88vBx_8/edit?usp=sharing). (A special thank you to Peter Leonard, Yale University, for sharing his tutorial.)

For the data, visit here: 

For the following issues,  visit [here](https://github.com/nolauren/TopicModeling_Mallet):
- Not Enough Memory
- Adjust Stopwords


Programming Historian for Mac:
```
bin/mallet import-dir --input sample-data/web/en --output tutorial.mallet --keep-sequence --remove-stopwords

bin/mallet import-dir --input amstudiestxt --output tutorial.mallet --keep-sequence --remove-stopwords

./bin/mallet import-dir --input /users/username/database/ --output tutorial.mallet --keep-sequence --remove-stopwords

bin/mallet train-topics  --input  

./bin/mallet import-dir --input  amstudiestxt --output tutorial.mallet --keep-sequence --remove-stopwords

bin/mallet train-topics  --input tutorial.mallet

bin/mallet train-topics  --input tutorial.mallet --num-topics 20 --output-state topic-state.gz --output-topic-keys tutorial_keys.txt --output-doc-topics tutorial_compostion.txt 
```

------------

## Networks - Using Gephi

### Install with PC
Follow the instructions on the [Gephi Install page.] (http://gephi.github.io/users/install/)

### Install with MAC
Go to Terminal.

Type

```
java -version
```

If you have Java 6, great!

If you have Java 7 or higher, we need Java 6 to run Gephi 0.8.2. In December, a new version of [Gephi 0.9](https://gephi.wordpress.com/2015/11/02/announcing-gephi-0-9-release-date/) will be available that works with Java 8. Until then, we need to do a work around. We need to delete/ disable your current version of Java. 

For deleting newer versions of Java, go to the terminal (if you're on a Mac) and type:

```
cd /Library/Java/JavaVirtualMachines/
ls
```
You need to delete every version of Java in here!

Note: Make sure to change where it says "version" to the version's of java on your machine.

```
cd /Library/Java/JavaVirtualMachines/
sudo rm -rf /Library/Java/JavaVirtualMachines/jdk<version>.jdk
```

For example:
```
sudo rm -rf /Library/Java/JavaVirtualMachines/jdk1.8.0_60.jdk
```

```
sudo rm -rf /Library/Java/JavaVirtualMachines/jdk1.8.0_51.jdk/
```

```
sudo rm -rf /Library/Java/JavaVirtualMachines/jdk1.8.0_05.jdk/
```

Download [Java 6](https://support.apple.com/kb/DL1572?locale=en_US).



Download [Gephi](http://gephi.github.io/). 

Open the .dmg file. Drag Gephi into Applications. Launch Gephi.


If it doesn't open: Right click and select "Show Package Contents". Go to Contents -> Resources -> gephi -> etc -> gephi.conf

Open gephi.conf with a text editor.

Edit the #jdkhome line so that it points to Java6.  Most likely:

jdkhome="/SystFem/Library/Frameworks/JavaVM.framework/Versions/1.6.0/Home/"



(Special thank you to [Evan Van Ness](http://www.evanvanness.com/post/71491924768/how-to-run-gephi-in-mac-os-x) for this work around.)



### Exercise 2
Download [20050.zip](http://amst23101s2015.coursepress.yale.edu/wp-content/uploads/sites/165/2015/03/20050.zip). Download [Supreme Court Zip Files](http://amst23101s2015.coursepress.yale.edu/wp-content/uploads/sites/165/2015/03/ussc-31.zip).

[Code Book](http://scdb.wustl.edu/documentation.php?s=2c)

File -> Open -> 20050.csv


ust an Edge List:
In order to import, Gephi requires the data to be structured with certain labels. The edge list needs "Source" and "Target". By default, the data will be imported as directed. If we want the data to be undirected, add "Type" and use "Undirected". Save the list as a .csv.  
Back in Gephi, go to Data Table > Import Spreadsheet. Choose your .csv. It will import as an edge list. 
Go to Data Table > Edges. We see our data.
Go to Data Table > Nodes. We need to create our labels. Go to "Copy Data to other column" and duplicated "ID" to "Label". 
Save! Save! Save! 

But what if we want to scale up? Our data changes? 
We need to make an edge list and node list.
For our edge list, we need "Source" , "Target", edge "ID", and "Type".
For our node list, we need node "ID" and "Label".
When we import the data, add the node list first!  Then, add the edge list. 




Here you must choose whether your graph is directed or undirected. The decision depends on your data.

Note: If the proper screen doesn't seem to be appearing, you can always to go Window in the menu bar. For example, I often find myself having to go to Window-> Graph to get my network to appear. (As you'll see, Gephi is fickle!) To move the graph, select Command and then move your graph. You can zoom in and out with your mouse.

[Overview of Gephi Panel](http://www.clementlevallois.net/gephi/tuto/en/gephi_cheat%20sheets_en.pdf) by Clement Levallois.



### Data
To see the data, select Data Laboratory. (If the tables don't appear, go to Window -> Data Table)

It separates your data into a node list and edge list.  You can adjust the data within Gephi. If you do so, make sure to export it!

Let's take a quick look at the graph. How does it look? Look good? 
Let's add labels.


### Layout
You can choose your layout. Let's take a look at two:



Layout -> Fruchterman Reingold -> Run -> Stop

It is based on graph drawing. The idea is that the edges want to stay together but the nodes want to move apart.
It is comes out of physics and mimicks the movement of charged particles.  



Layout -> Forced Atlas2 -> Run -> Stop

Designed for Gephi and popular for visualizations.



The first time you select a layout, options will appear. Some adjustments you might consider are  Gravity, Prevent Overlap and Scaling. To return to this screen, go to Data Laboratory -> Layout. Select the layout you want to adjust and the options screen will appear.



#Labels
In the graph view, select the T in the bottom menu. The labels will appear. Their are several options next to the T that allow you to adjust text font and size. Play around!



### Statistics
Statistics -> Modularity -> Run

Modularity is an algorithm designed to help identify groups or communities in a network (i.e. community detection). It measures the nodes, so to visualize it, we want to look at how this calculation impacts the nodes. Go toward the top left of your screen  and select Partition -> Refresh (icon with two arrows) -> Nodes ->  Choose a partition parameter  -> Modularity Class

Now we have groups of cases. Let's say I want to know which cases are the most important. So, let's count the number of edges using Degree.

Statistics -> Average Degree -> Run

Ranking (next to Partition) -> Select the Diamond -> Degree -> Min/Max -> Apply

Now you can adjust the Min / Max. The nodes with the least amount of edges are adjusted through Min size: and the nodes with the most amount of edges are adjusted by Max size:.  After you hit apply, the nodes sizes should adjust accordingly.

Let's also check out In-Degree and Out-Degree.

The other options are excellent as well and worth exploring!

For example, betweenness and and closeness centrality are popular because they both measure which nodes are central to the network. You can access these calculations by selecting Avg. Path Length.  After you do that, go to the "Ranking" screen in the top left column. Make sure "Edges" is selected, click on "Betweenness Centrality," and then click on the red diamond symbol. Adjust the "Max size" to whatever number makes the important nodes distinguishable to you (we set ours to 50). Then, click "Apply." The nodes that have a high betweenness centrality, which means they are often on the shortest path to other nodes, should look larger. In our case, it isn't a surprise that 347 US 483 Brown v Board of Education is central to cases on school desegregation.



### Outliers(?)
So, let's say there are some outliers that I am not interested in. (This is particularly important if you have a lot of data.) We might consider removing certain nodes. For example, let's say one case has only been cited by one other case. We might decide this case isn't important to our network for we want to know which cases are the most influential.

Window -> Filters -> Topology -> Degree Range

A slider will appear. Adjust accordingly.  Select Filter to apply.

 
#Final
Select Preview. There are many options. Play around and make sure to hit refresh in order to see them. To Export, go to File -> Export





### Assignment
You can use your data or visualize a theme from the Supreme Court Data. In the response, explain the theme chosen, the decisions made in Gephi and any conclusions we can draw from the network.  More broadly, comment on the the possibilities and limits of network analysis and Gephi. Make sure to include the network in your blog post. Add “Network Analysis″ from Categories. 

1. Use the  [Code Book](http://scdb.wustl.edu/documentation.php?s=2c) to pick a topic. (Ex. 20050  - Desegregation)

2. Download the [ussc](http://amst23101s2015.coursepress.yale.edu/wp-content/uploads/sites/165/2015/03/ussc-31.zip).  Once you have downloaded, unzip and select your topic.

3. Load your data into Gephi.  Adjust as you deem fit!


### Related Readings

Cordell, Ryan, “Uncovering Reprinting Networks in Nineteenth-Century American Periodicals.” Am Lit Hist (Fall 2015) 27 (3): 417–445. [Viral Texts Project at Northeastern] (http://viraltexts.org/) and [Networks of Viral Texts](http://networks.viraltexts.org/)

Edward Arriaga, Fernando Caparini and Juan Luis Suarez, [“Modeling Afro-Latin American Artistic Representations in Topic Maps: Cuba’s Prominence in Latin American Discourse.”](http://www.digitalhumanities.org/dhq/vol/7/1/000145/000145.html).

Meeks, Elijah and Scott Weingart. [An Introduction to Networks Analysis and Representatin.] (http://emeeks.github.io/networks/)

Moretti, Franco. [Network Theory, Plot Analysis.](https://litlab.stanford.edu/LiteraryLabPamphlet2.pdf)

Weingart, Scott. [“Topic Modeling and Network Analysis.”](http://www.scottbot.net/HIAL/?p=221) The scottbot irregular.

Weingart, Scott. [“Contextualizing networks with maps.”](http://www.scottbot.net/HIAL/?p=1942) The scottbot irregular.









------------
 
## Mapping

### Getting Started

Several broad categories of mapping (not exhaustive by any means!):

1. Flexible interactive visualizations served over the web. Ex. CARTO (tool), [Photogrammar] (photogrammar.yale.edu) (project), and [Mapping Inequality](https://dsl.richmond.edu/panorama/redlining/) (project)

2. Narrative mapping. Ex StoryMap.js and Odysessy (https://cartodb.github.io/odyssey.js/)

3. Spatial Analysis such as building models of spatial processes like the spread of diseases based on the movement of people. Ex. python/r , ArcGIS

They rely on Geographical Data (proprietary databases (vector and raster), georectifying, and geolocation) Ex. ArcGIS 



#### (Storymap.js)

Today, we are going to look at narrative mapping:  https://storymap.knightlab.com/


We have two options: Classic or Gigapixel. We will use Classic. 

So, let's make a storymap!

Note: I always like to stop to think about the implications of using Google, particularly when working with students.


To change the map, go to Options.

To share your map, select the Share button on the top right corner. 

Example StoryMap: https://uploads.knightlab.com/storymapjs/00d95891f556eb378e1fb8a1f6ec48ec/fwp/draft.html


Limits of StoryMap:
1. Have to pick a specific location. 
2. Can only use media that is supported by the tool. 
3. Only load one piece of media per slide.
4. Best with visually rich media. 
5. The data is locked into the tool.


Others: [Neatline](http://neatline.org), [Odyssey](https://cartodb.github.io/odyssey.js/), [StoryMap](https://storymaps.arcgis.com/en/)


### CartoDB Tutorial

CartoDB is a web-based tool for visalizing and analyzing
small to medium sized spatial datasets. While ostensibly open-source
software, it is quite difficult to compile yourself and much of
the nice UI is actually proprietary. Fortunately, they offer a
good free-tier of the service (no credit card needed; just an e-mail)
which should suffice for the purposes of this tutorial.

#### Set-Up Account
Go to https://carto.com/signup/ and sign-up.
I suggest using your @institutionname.edu account. It will give you access to an 
education account, which comes with more options than a non-education account. 

#### Getting Started

Importing data to CartoDB is, in theory, very easy. Just drag
and drop the file you want into the dashboard and you're done!

Go to Maps -> Your Datasets. We can drag and drop in our data. 

Let's work with [our movies](https://docs.google.com/spreadsheets/d/19-UEPA-_0iU42nfhK5cpuZyZwXgwpm_FqNhBsSaI0sU/edit?usp=sharing).

Save As a .csv file.  


#### Working with data in CartoDB

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

#### Let's map.

We will immediately see we have a problem signaled by the "!".

What's the isssue?


#### Georeferencing

The new Carto builder now includes a georeferencer.

Go to Analysis.
- Input: Source is our .csv
- Type: Countries
- Parameters: Need to tell Carto which column in our spreadsheet to talk to.
 
If you want to use a different georeferencer:

Geoferecing tutorials:
- [New York Public Library Map Warper](http://maps.nypl.org/warper/) (allows access to NYPL open digital map library, but only georeferencing their maps) 
- [Map Warper](http://Mapwarper.net) (web-based application that allows you to upload public domain maps and serve XYZ layers to Carto)
- [British Library Georeferencer](http://www.bl.uk/georeferencer/georeferencingmap.html)  (can visualize in OSM, side by side, Google Earth; can get an account and do your georeferencing here)

Now we have our locations!

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

#### Data Analysis and Visualizations

Builder provides "widgets" to subset and search  data geographically.

Carto suggests widgets as well as let's your build them.

Let's make a genre widget.

Let's also make a widgit for budget. 

Let's change our basemap.

Add a legend.


#### Final 

To actually make this a map, you must save it. To do so, select "Share."

 




