# Digital History Toolbox 🛠️
American Historical Association 2018 |  Washington D.C.

This session is an all-encompassing look at incorporating entry-level tools for text mining, 
mapping and timelines into your teaching or research for the first time. 
We’ll use web-based tools such as Storymap.js, Voyant and Timeline.js and 
give you a common dataset to work from. Along the way, we’ll also give 
you a few tips on how to get your own data in shape. 

Preparation: Please bring an Internet-equipped laptop.

-------------------

## Introductions

-------------


## Timeline (Timeline.js) ⏰

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

Let's look at [an example](https://docs.google.com/spreadsheets/d/1ORRtnJBGXcMO7cbkLRz4abijVPNMYWdH6tqXrxDxnWg/edit?usp=sharing).
Here we see a timeline developed by students in my Documenting 1960s America Class. 

And we have some issues! Let's take a look at:
- 4: Blank
- 45: Vietnam War (Link/ Multiple Photos Issue)
- 46: The Other America (Link/ Google Images)
- 54: Tet Offensive (Link/ No Link)

Can view link: https://docs.google.com/spreadsheets/d/1ORRtnJBGXcMO7cbkLRz4abijVPNMYWdH6tqXrxDxnWg/edit?usp=sharing

*Strategies/ Challenges:*
- Spelling!
- Blanks means no data.
- Supported media includes: Twitter, Flickr, YouTube, Vimeo, Vine, Dailymotion, Google Maps, Wikipedia, SoundCloud, Document Cloud 
- Media must end in the proper file extension. For example, an image link must be "LINK.jpg"
- YouTube: Once a video is chosen, select "SHARE". A link will appear. "Copy" this link and paste into the spreadshhet. 
- New columns can be added at the end but they will not appear on the timline. 

Collaborate: If you want to collaborate, select "Share" on the top right of the spreadsheet. 

### Publish

Once you are finished, go to File -> Publish to the Web -> Publish. Next, copy the URL in the
browser. Go back to [Timeline.js - Make A Timline](https://timeline.knightlab.com/). Scroll
down to Step 3. Paste the google sheets URL.

![ ](https://github.com/nolauren/link/blob/master/timelinejs_step3.png)

Once copied, select Preview. 

![ ](https://github.com/nolauren/link/blob/master/timelinejs_preview.png)

Timelines can be embedded on a website or linked to directly. 

*Limits of Timeline.js*:
1. Have to pick a specific time (range). It doesn't deal with ambiguity. 
2. Can only use media that is supported by the tool. 
3. Only load one piece of media per entry.
4. Use a proprietary (Google) to make it work. Issues include privacy/ data.

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

There is an expansive set of approachs and tools for mapping. The fields of geography and cartography offer many important methods and critiques to draw on when engaging in spatial analysis and mapping. Richard White's work is an exciting and necessary [read](https://web.stanford.edu/group/spatialhistory/cgi-bin/site/pub.php?id=29) for historians. While by no means exhaustive, I find it helpful to think about this area of inquiry as charachterized by several broad categories:

1. Interactive Mapping: Flexible interactive visualizations served over the web. Platforms include [CARTO](https://carto.com/) and [MapBox](https://www.mapbox.com/).  DH Projects like [Photogrammar](http://photogrammar.yale.edu) (project) and [Mapping Inequality](https://dsl.richmond.edu/panorama/redlining/) use Carto.

2. Narrative Mapping: Maps used to tell a story. They tend to support primarily linear story telling.  Platforms include StoryMap.js, [Odysessy](https://cartodb.github.io/odyssey.js/), [ESRI Story Maps](https://storymaps.arcgis.com/en/). An exampls is [Renewing Inequality](http://dsl.richmond.edu/panorama/renewal/).

3. Classic Cartography and Geographical Data: The study and practice of making maps.  This often involves the use of rastor (set of pixels representing real world features such as an aerial photograph or land elevations) and vector (set of x,y coordinatates that create points, lines, polygons, which represent features such as county borders and streets ) data to create maps. This is often what people mean what they say they want a GIS system. They are often necessary for georectifying maps. The main platform is ESRI's ArcGIS and open source QGIS for Mac.


4. Spatial Analysis:  While this term is sometimes applied more broadly, it  commonly is used for computational analysis of spatial data. This most often is in the form of predictive modeling such as tracking population movement or the the spread of a disease across a community. Platforms such as ArcGIS have specialized in this area. Programming languages like R and python also allow for this. Web-based interactive mapping tools like Carto continue to build this kind of functionality. For an example, see [Forced Migration of Enslaved Peoples](https://dsl.richmond.edu/panorama/forcedmigration/).


Today, we are going to explore narrative mapping by focusing on another Knight Foundation tool called [StoryMap](https://storymap.knightlab.com/).  


### Getting Started

Like Timeline.js, this tool requires the use of Google. After logging in with Google, we are given two map options: Classic or Gigapixel. While the [Gigapixel](https://storymap.knightlab.com/gigapixel/) map is definitely worth exploring, it requires hosting a set of images on a web server.  It also needs relatively large files. For today, we will use Classic.  So, let's make a storymap!

The storymap is comprised of a series of slides with a spatial component. It words best when the number of slides doesn't exceed ~20 and the story is relatively contained.  Let's walk through the first slide and then an example.

1. Slide 1 - Title
- Headline: From Selma to Montgomery
- Text:  Held in 1965,  three marches were organized to highlight the continuation of racial injustice. The violence and murder commmited by white supremacists during the marches led to national outrage. Credited with leading to the passage of the Voting Rights Act of 1965, the events were a critical part of the long struggle for civil rights and the fight to racial oppression.
- Media: Holding Hands (Credit: Getty Images)
- Location: Selma

2. Slide 2 - Murder of Jimmie Lee Jackson
- Headline: February 26, 1965: Jimmie Lee Jackson murdered by James Fowler, an Alabama State Trooper. In response, James Bevel and fellow civil rights activists organize a march from Selma to Montgomery. 
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
- Headline: March 9, 1965: The second march resulted in a confrontation between marchers led by Martin Luther King and state law enforcement. While the march ended peacefully, white segregationists murdered James Reeb, a white civil rights activist, later that evening. The event further spurred national uproar.
- Media: Find a piece of your choice. 
- Location: Green St at Water Ave

6. Slide 6 - Pick an event. 


Now that we have several event on our map, we might decide we want to change the base map. We can do so by going to Options. StoryMap offers several base maps. However, you might want to add your own. 

Once you are ready to share your map, select the Share button on the top right corner. 


*Limits of StoryMap*:
1. Have to pick a specific location. 
2. Can only use media that is supported by the tool. 
3. Only load one piece of media per slide.
4. Best with visually rich media. 
5. The data is locked into the tool.


Others: [Neatline](http://neatline.org), [Odyssey](https://cartodb.github.io/odyssey.js/); [ESRI Story Maps](https://storymaps.arcgis.com/en/)


### Create Your Own!

----------


## Text Analysis with Voyant 

Let's define Text Analysis. Are you familiar with this method? How would you define it?

For our corpus, we will explore the State of the Union addresses.  The State of the Union is delivered by the President of the United States annualy to a joint session of Congress. 
It is often a space where the President reflects on current issues and outlines goals for the nation. 
Therefore, it is a key document for understanding the ways the executive branch understands the current position 
of the country and their priorities. While today it is delivered oraly by the President, 
the State of the Union was initially a written document submitted to congress. 
In this lab, we will use Voyant to identify issues and priorities.


We will be using [Voyant](https://voyant-tools.org/):  a web-based text reading and analysis environment.

According to the Voyant Website <sup>[1](#myfootnote1)</sup>, we can do the folllowing:

- Use it to learn how computers-assisted analysis works. Check out our examples that show you how to do real academic tasks with Voyant.
- Use it to study texts that you find on the web or texts that you have carefully edited and have on your computer.
- Use it to add functionality to your online collections, journals, blogs or web sites so others can see through your texts with analytical tools.
- Use it to add interactive evidence to your essays that you publish online. Add interactive panels right into your research essays (if they can be published online) so your readers can recapitulate your results.
- Use it to develop your own tools using our functionality and code. 


### 2016 SOTU Speech
We will start with Obama's final State of the Union address.  

To begin, we will load in our text from [here](http://programminghistorian.github.io/ph-submissions/assets/basic-text-processing-in-r/sotu_text/236.txt).

Let's take a look at the speech. 
- What kind of file is this?  
- What does the format of this file tell us about one way that Voyant needs text to be structured to process it?

We can load data into Voyant three ways. 

1. Use the URL
2. Copy and paste the text into the box. 
3. Upload a file.


Now let's take a look at the kinds of text analysis used by Voyant!

#### Cirrus -  Terms - Links 

Cirrus:  Provides a word cloud of the most frequent terms. You can hover over the word to see the number of times it is used. 

- Are these the words we expected?
- Are there any words we would have expected that aren't included? 
- Are there any words we think should be removed?


#### Stop Words 

Stop Words are a list of common words that are filtered out before or during text processing. You can use default stop word lists, like those included in Voyant, or create your own.   

Let's say we want to remove "mdash" and add it to our stop words. Go to the bottom left panel that says "Summary Documents Phrases". Next to the question mark is another set of options that only appear once you hover over the area. The first option to the left of the question mark allows us to adjust our stop words. 

Voyant's default setting auto-detects a stop word list. Select "None" and see what happens! 
- Is this helpful?

Let's go back and select "English". To adjust our list, select "Edit List." Let's add "mdash". 

 - Are there any other we want to add? 

Let's add: "that's" and "it's". 

(Tip: When I'm adjusting the stop word list, I like to make a text file with my additional stop words. You'll notice Voyant only allows you to adjust your stop words once. If you try to add more, it deletes your previous custom words.)



#### Cirrus -  Terms - Links

Cirrus: Now we have a new word cloud!

Terms: We see the raw count of words in a list. 

Links: Provides a collocates graph shows a network graph of higher frequency terms that appear in proximity. Keywords are shown in green and collocates (words in proximity) are showing in red. 

Let's click on "America." Let's take a look at the Reader in the panel to the right. 
- What changed?

Now let's take a look at Trends in the panel furthest to the right. The default is Raw Frequencies. 

Let's change to Relative Frequenices. (This isn't as helpful with one document but will be when we are analyzing more than one at a time.)

Now let's go back to Links and double click on "America". 

- What changed?

#### Contexts - Bubblelines 

Contexts: Puts a term in context.

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


[Download the corpus](https://drive.google.com/open?id=0B6zkbDdW8bzIQnpQX2NQbVFYQjg) to your Downloads Folder. 

Unzip the file.

Go to [Voyant](https://voyant-tools.org/) and select "Upload".  
The speechs are named according to year. 
Make sure the files are in numerical order for this determines how Voyant loads them in.  Now, let's explore!

To begin, take a look at Cirrus. 
- Do we want to remove any stop words? If so, why?

Let's remove them. 

##### Summary - Documents - Phrases

- Can we learn anything from this? Document Length? Vocabulary Density? 

We also have a new option - Distinctive Words. 
Voyant uses Term Frequency-Inverse Document Frequency to weigh how important a word is in the document or corpus. 
Let's take a look at the terms used by Washington and Obama. 

- Are there any themes we can see in these speeches? By presidency? 

- Do we see particular phrases? 


##### Explore!

Interested in looking at all of the State of the Union addresses? Here you [go](https://programminghistorian.org/assets/basic-text-processing-in-r/sotu_text.zip)! 

If you are interested in how to work with the State of the Union addressed with the R programming language, see [my tutorial](https://programminghistorian.org/lessons/basic-text-processing-in-r) with Taylor Arnold on Programming Historian. 


PS: A quick note about lemmatization is necessary. Lemmatization may be important for your study. For example, if we are interested in how common the corpus talks talks about "states" then we need to search "state" and "states". By lemmatizing, all instances of "states" becomes "state". This can make a huge difference when calculating word frequencies for instance. We can then take this a step further. What if I use the term once to mean the political boundaries  (ex. the state of Virginia) and as second time to mean a condition once was in (ex. in a state of happiness) We could then use Natural Language Processing (NLP) to distinguish between these two kinds.  Tools for lemmatization and NLP include [CleanNLP](https://cran.r-project.org/web/packages/cleanNLP/index.html) (for R) and [Lexos](https://cran.r-project.org/web/packages/cleanNLP/index.html) (command line). 


