# Introduction

ArcGIS is an advanced software platform for creating maps and conducting GIS research.  We are going to use its ability to create StoryMaps for the purposes of this tutorial.  StoryMaps is an additional application meant to work *on top of* already existing maps created in or imported to ArcGIS.  The University of Richmond allows students to login using their netid and passwords to create maps, but please make sure that you use the U of R login [available here](https://urichmond.maps.arcgis.com/).  This will allow you to login using your U of R Login or an ArcGIS account if you have one.  


Please Note: This tutorial is heavily adapted from the [ArcGIS Official Story Map Journal Tutorial](https://learn.arcgis.com/en/projects/get-started-with-story-maps/lessons/create-a-story-map-journal.htm) with only a few modifications to reflect the particularities of the University of Richmond.

# Creating a Story Map Journal

Once you have logged in, you should see projects that have already been completed here at U of R.  At the top, you should  see a square made up of 9 smaller squares.  Click the square and choose the "Story Maps" option. Next, you should see any previous story maps that you created, and an option to "Create Story."  After you click "Create Story," you can choose which type of story map you are interested in making.  For the purposes of this tutorial, we are going to create a "Story Map Journal."  

The pop up dialogue asks us if we would like a side panel or a floating panel.  We are going to leave it at the default side panel, which will show our navigation display on the left side.  Next, we need to enter in a title for our map.  In this case, we are going to type in "Welcome to San Diego."  The first section of our story map is the "Home Section."  This will introduce our visitors to our map.  We also have the option of choosing Map, Image, Video, or Web Page as the main content for our webpage.  We are going to use a nice image for our section that we have uploaded on Flickr.  Click the Flickr icon and for the username type in "ESRI Story Maps Demo."  After you click Load Albums, we can choose which image we want.  For the purposes of this tutorial, we are going to use the "View Over San Diego Bay" image and choose the "fill" option. 

We are now going to go add the text for this section next, so click on the "Side Panel" tab and enter the following:

> San Diego offers a near-perfect "endless summer" climate, great beaches, a lively downtown, cool neighborhoods, and a generally laid-back feel.
 
> Plus there are miles of coastline, mountains, and a desert to explore.
 
> Let us introduce you to the city and help you discover some cool places along the way that you may enjoy.

Click Save.  As you can see, we now already have a basis for our StoryMap.  Next thing that we are going to do is click "Add Section."  This will provide us the same dialogue that we saw when we created our home section.  For the title, insert "San Diego: The Second Largest City in California."  In this new section, we are going to show a map as our content.  Next to text that reads My Content, we can choose a map available on ArcGIS Online.  In the dropdown menu, click ArcGIS Online and find the map labeled "CreateMJSanDiego."  

We want to now adjust the zoom level to focus in on the area we are interested in.  Next to the word "Location", click on "Custom Configuration."   Zoom into San Diego and click "Save Map Location."  When our users go through our story map, this zoom level is what they will see.  In the Side Panel tab, type in the following:

> San Diego is located on the Pacific coast, 120 miles south of Los Angeles and 20 miles north of Tijuana.

We are going to add one final section on Downtown San Diego.  In the Main Stage, title this section "Downtown San Diego."  Where it says location, click "Custom configuration" and zoom into the downtown area.  Hit the button that says "Save Map Location."  Next, we will adjust what points are available.  Next to content, click "Custom Configuration."  This will provide us a popup with different location layers.  Let's go ahead and uncheck the "Ferry Routes" and add the "Food" points. Finally, click "Save Map Location."  In the side panel, type in the following information:

> Start your visit to San Diego in the lively downtown. Here, next to San Diego Bay, you'll find the Convention Center, Marina, the baseball stadium, and lots of things to do.

> The Gaslamp Quarter is the big evening destination with restaurants, bars, and shops along Fifth Avenue and the surrounding streets.

> Little Italy is another popular neighborhood, combining its Italian roots with some cool modern design.

> Click the green points to discover some fun places, or blue points to learn more about some great places to get food.

We are going to add a Story Map action to our content now.  Story Map actions allow interactivity to text.  We want it so that when users click on the text “Gaslamp Quarter” that they are presented a map zoomed into the Gaslamp Quarter area of San Francisco.  Highlight the words “Gaslamp Quarter” in our side panel text, and you should now have the option to click on what kind of interactivity you want.  Next to the small “i” icon, click on the section to “Change the Main Stage Content.”  A new popup will now appear that allows you to click “Custom Configuration."  Click it and zoom into the Gaslamp Quarter neighborhood.  Finally, click “Save Map Location.”  Now, if a user clicks on the text, the map will zoom in on the neighborhood.

# Conclusion

The flexibility of ArcGIS may make it an advanced software, but as you can see from this tutorial, getting a basic story map does not have to be complicated.  If you are interested in exploring story maps further, a quick Google or YouTube search should pull up plenty of options.  In addition, U of R has access to numerous tutorials through [Lynda.com](http://lynda.richmond.edu).  Finally, the official ArcGIS site also has [great tutorials](https://learn.arcgis.com/en/gallery/) .
