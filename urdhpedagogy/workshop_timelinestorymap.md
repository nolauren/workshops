# Timeline.js and Storymap.js

-------------

## Ground Rules
- Plesae drive your own computer.
- Please remain on the same step as the workshop leader.
- Plesae place a sticky note on our computer if you need assistance.
- Questions? Please ask!

------------------

## Timeline (Timeline.js) ⏰

A tool for collaboratively building an interactive timeline that supports media (i.e photos, moving images, sound, etc). 

### Set Up

Because the tool uses Google products, a [gmail account](https://accounts.google.com/SignUp?hl=en) is required. 
Institutional email using gmail will work even if it ends with "@NAMEOFINSTITUTION.edu". To set up a timeline
on Timeline.js, following these steps:

1. Go to: [Timeline.js](https://timeline.knightlab.com/)
2. Select "Make A Timeline".  
3. Select "Use this template".

### Data

Now we all see a google sheet with a set data structure. 
This is the structure that this tool requires in order to work.   
The tool also only supports certain [media types](https://timeline.knightlab.com/docs/media-types.html). 


### Example

Let's look at [an example](https://docs.google.com/spreadsheets/d/1ORRtnJBGXcMO7cbkLRz4abijVPNMYWdH6tqXrxDxnWg/edit?usp=sharing).
Here we see a timeline developed by students in First Year Seminar: Documenting 1960s America. 
I developed the collaborative assignment to help students identify and keep track of the major events of the 1960s. 

Now let's take a look at the timeline! 

Does this look right?

We have some issues.  Let's take a look at:
- 4: Blank (Empty Cell/ Need to remove)
- 45: Vietnam War (Link/ Multiple Photos Issue)
- 46: The Other America (Link/ Google Images)
- 54: Tet Offensive (Link/ No Link)


*Strategies/ Challenges:*
- Spelling!
- Blanks means no data.
- Limited by supported media platforms. 
- Media must end in the proper file extension. For example, an image link must be "LINK.jpg"
- YouTube: Once a video is chosen, select "SHARE". A link will appear. "Copy" this link and paste into the spreadsheet. 
- New columns can be added at the end but they will not appear on the timline. 

Collaborate: If you want to collaborate, select "Share" on the top right of the spreadsheet. 

### Publish

Once you are finished, go to File -> Publish to the Web -> Publish. Next, copy the URL in the
browser. Go back to [Timeline.js - Make A Timline](https://timeline.knightlab.com/). Scroll
down to Step 3. Paste the google sheets URL.

![ ](https://github.com/nolauren/workshops/blob/master/img/timelinejs_step3.png)

Once copied, select Preview. 

![ ](https://github.com/nolauren/workshops/blob/master/img/timelinejs_preview.png)

Timelines can be embedded on a website or linked to directly. 

*Limits of Timeline.js*:
1. Have to pick a specific time (range). It doesn't deal with ambiguity. 
2. Can only use media that is supported by the tool. 
3. Only load one piece of media per entry.
4. Use a proprietary (Google) to make it work. Issues include privacy/ data.

### Teaching
- I build out a lab like this one and make it avaiable to the class. 
- Usually spend about 20 minutes introducing the tool and then let them start contributing.
- Next class: I pull up the timeline and usually something doesn't work! I show a few common errors and then ask them to troublshoot in groups.

### Reflection
- Why might you want to use a timeline in your classes?
- What might an assignment built around this tool look like?
 
 
### Try it out! 

If you are looking for other events to add to the timeline, here are links to
build a quick timeline about the New Deal:

- New Deal Events: http://xroads.virginia.edu/~MA02/volpe/newdeal/timeline_text.html

- FDR 1932 Democratic Convention: https://www.youtube.com/watch?v=6Ht6cJqgC6o

- FDR Election: http://depts.washington.edu/depress/images/fdr_1932_seattle_420.jpg

- Fireside Chat: https://www.youtube.com/watch?v=z9CBpbuV3ok

- CCC Poster: https://upload.wikimedia.org/wikipedia/commons/b/b2/CCC-poster-1935.jpg

- TVA Logo: http://www.sourcewatch.org/images/thumb/c/cf/TVA.jpg/170px-TVA.jpg (Timeline.js doesn't support .svg)

Feel free to add other events as well.

------------


## Mapping (Storymap.js) 🗺️

There is an expansive set of approachs and tools for mapping. 
The fields of geography and cartography offer many important methods and critiques to draw on when 
engaging in spatial analysis and mapping. Richard White's work is an exciting and 
necessary [read](https://web.stanford.edu/group/spatialhistory/cgi-bin/site/pub.php?id=29) for historians. 
While by no means exhaustive, I find it helpful to think about this area of inquiry as charachterized by 
several broad categories:

1. Interactive Mapping: Flexible interactive visualizations served over the web. 
Platforms include [CARTO](https://carto.com/) and [MapBox](https://www.mapbox.com/).  
DH Projects like [Photogrammar](http://photogrammar.yale.edu) (project) 
and [Mapping Inequality](https://dsl.richmond.edu/panorama/redlining/) use Carto.

2. Narrative Mapping: Maps used to tell a story. They tend to support primarily linear story telling.  
Platforms include StoryMap.js, [Odysessy](https://cartodb.github.io/odyssey.js/), 
[ESRI Story Maps](https://storymaps.arcgis.com/en/). An example 
is [Renewing Inequality](http://dsl.richmond.edu/panorama/renewal/).

3. Classic Cartography and Geographical Data: The study and practice of making maps.  
This often involves the use of rastor (set of pixels representing real world features 
such as an aerial photograph or land elevations) and vector (set of x,y coordinatates 
that create points, lines, polygons, which represent features such as county borders and streets) 
data to create maps. This is often what people mean what they say they want a GIS system. 
They are often necessary for georectifying maps. The main platform is ESRI's ArcGIS and open source QGIS for Mac.


4. Spatial Analysis:  While this term is sometimes applied more broadly, it commonly is used 
for computational analysis of spatial data. This most often is in the form of predictive 
modeling such as tracking population movement or the the spread of a disease across a community. 
Platforms such as ArcGIS have specialized in this area. Programming languages like R and python also 
allow for this. Web-based interactive mapping tools like Carto continue to build this kind of functionality. 
For an example, see [Forced Migration of Enslaved Peoples](https://dsl.richmond.edu/panorama/forcedmigration/).



Today, we are going to explore narrative mapping by focusing on another 
Knight Foundation tool called [StoryMap](https://storymap.knightlab.com/).  


### Getting Started

Like Timeline.js, this tool requires the use of Google. After logging in with Google, 
we are given two map options: Classic or Gigapixel. While the [Gigapixel](https://storymap.knightlab.com/gigapixel/) map 
is definitely worth exploring, it requires hosting a set of images on a web server.  It also needs relatively large files. 
For today, we will use Classic.  So, let's make a storymap!

The storymap is comprised of a series of slides with a spatial component. 
It words best when the number of slides doesn't exceed ~20 and the story is relatively contained. 
Let's walk through the first slide and then an example.


1. Slide 1 - Title
- Headline: From Selma to Montgomery
- Text:  Held in 1965,  three marches were organized to highlight the continuation of racial injustice. 
The violence and murder commmited by white supremacists during the marches led to national outrage.
Credited with leading to the passage of the Voting Rights Act of 1965, the events were a critical part of the long 
struggle for civil rights and the fight to racial oppression.
- Media: Holding Hands (Credit: Getty Images)
- Location: Selma

2. Slide 2 - Murder of Jimmie Lee Jackson
- Headline: February 26, 1965: Jimmie Lee Jackson murdered by James Fowler, an Alabama State Trooper. 
In response, James Bevel and fellow civil rights activists organize a march from Selma to Montgomery. 
- Media: (Image of Funeral)[http://assets.nydailynews.com/polopoly_fs/1.2099215.1422767566!/img/httpImage/image.jpg_gen/derivatives/article_750/cold-cases.jpg] (Credit: NY Daily News)
- Marion, Alabama

3. Slide 3 - Bloody Sunday
- Headline: March 7, 1965: The first march turned quickly violent when state troopers attacked the unarmed marchers. The day became known as Bloody Sunday.
- Media: https://www.youtube.com/watch?v=BFhcR362RyE
- Location: Right across the bridge 

4. Slide 4 - A Photo Elicits National Outrage
- Headline: March 7, 1965: The event received national attention spurred by a photo of Amelia Boynton's unconscious body. 
- Media: https://library.duke.edu/digitalcollections/snccdigitalgateway/selma6.jpg (Credit: SNCC Digital)
- Location: Edmund Pettus Bridge

5. Slide 5 - Turn Around Tuesday
- Headline: March 9, 1965: The second march resulted in a confrontation between marchers 
led by Martin Luther King and state law enforcement. While the march ended peacefully, 
white segregationists murdered James Reeb, a white civil rights activist, later that evening. T
he event further spurred national uproar.
- Media: Find a piece of your choice. 
- Location: Green St at Water Ave

6. Slide 6 - Pick an event. 


Now that we have several event on our map, we might decide we want to change the base map. 
We can do so by going to Options. StoryMap offers several base maps. However, you might want to add your own. 

Once you are ready to share your map, select the Share button on the top right corner. 


*Limits of StoryMap*:
1. Have to pick a specific location. 
2. Can only use media that is supported by the tool. 
3. Only load one piece of media per slide.
4. Best with visually rich media. 
5. The data is locked into the tool.


Note: [Gigapixel](https://storymap.knightlab.com/gigapixel/) is great for working with images. 

### Teaching
- I use this as the form of scholarly communication for assignments. 
- I build out a lab like this one and make it avaiable to the class. 
- Usually spend about 20 minutes introducing the tool and then let them start building their own. 
- Example [assignment here](https://github.com/nolauren/workshops/blob/master/urdhpedagogy/files/fys100assignment.md) 
and [example of student project](https://uploads.knightlab.com/storymapjs/3e541f8fc468eec97fe9f4715a3d8b31/fys-100-48-final-project/draft.html).


### Reflection
- Why might you want to use a timeline in your classes?
- What might an assignment built around this tool look like?

### Other Platforms
- [Neatline](http://neatline.org)
- [Odyssey](https://cartodb.github.io/odyssey.js/)
- [ESRI Story Maps](https://storymaps.arcgis.com/en/)


### Create Your Own!

