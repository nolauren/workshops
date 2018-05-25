
## Networks - Using Gephi

### Install with PC
Follow the instructions on the [Gephi Install page](http://gephi.github.io/users/install/).

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

Easley, David. [Networks, Crowds, and Markets: Reasoning About a Highly Connected World](http://www.cambridge.org/gb/academic/subjects/computer-science/algorithmics-complexity-computer-algebra-and-computational-g/networks-crowds-and-markets-reasoning-about-highly-connected-world?format=HB&isbn=9780521195331#27IcB9j9LJIJgyYm.97), 2010.

Meeks, Elijah and Scott Weingart. [An Introduction to Networks Analysis and Representatin.] (http://emeeks.github.io/networks/)

Newman, Mark. *[Networks: An Introduction.](https://global.oup.com/academic/product/networks-9780199206650?cc=us&lang=en&)*, 2010.   

Weingart, Scott. [“Demystifying Networks, Part I & II.” Journal of Digital Humanities. Vol 1 No. 1. Winter 2011.](http://journalofdigitalhumanities.org/1-1/demystifying-networks-by-scott-weingart)

Weingart, Scott. [“Topic Modeling and Network Analysis.”](http://www.scottbot.net/HIAL/?p=221) The scottbot irregular.

Weingart, Scott. [“Contextualizing networks with maps.”](http://www.scottbot.net/HIAL/?p=1942) The scottbot irregular.


Example Projects: [Linked Jazz](https://linkedjazz.org/),[Republic of Letters](http://republicofletters.stanford.edu/), [Signs at 40](http://signsat40.signsjournal.org/cocitation/), and  [Wikipedia](xefer.com/WIKIPEDIA)


