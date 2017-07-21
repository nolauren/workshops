# Digital History Toolbox
American Historical Association 2017 |  Colorado Convention Center Room 205  

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
## Mapping (Storymap.js)

Several broad categories of mapping (not exhaustive by any means!):

1. Flexible interactive visualizations served over the web. Ex. CARTO (tool), [Photogrammar] (photogrammar.yale.edu) (project), and [Mapping Inequality](https://dsl.richmond.edu/panorama/redlining/) (project)

2. Narrative mapping. Ex StoryMap.js and Odysessy (https://cartodb.github.io/odyssey.js/)

3. Classic Cartography and Geographical Data (proprietary databases (vector and raster), georectifying, and geolocation) Ex. ArcGIS 

4. Spatial Analysis such as building models of spatial processeslike the spread of diseases movement of people. Ex. python/r , ArcGIS


Today, we are going to look at narrative mapping:  https://storymap.knightlab.com/


### Getting Started

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


Others: [Neatline](http://neatline.org), [Odyssey](https://cartodb.github.io/odyssey.js/)


### Customize Map


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


