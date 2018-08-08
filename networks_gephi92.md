## Gephi

### Install with PC
Follow the instructions on the [Gephi Install page.](http://gephi.github.io/users/install/)

### Install with MAC

Download [Gephi](http://gephi.github.io/). 

Open the .dmg file. Drag Gephi into Applications. Launch Gephi.

### Data

We will be using Supreme Court data.  We will be working with school discrimination cases. 

Code book: http://scdb.wustl.edu/documentation.php?s=1

Edges: https://github.com/introdh2016/labs/blob/master/20050_edges.csv

Source | Target
--- | ---  
333US147 | 332US631
333US147 | 339US629
332US631 | 339US629
332US631 | 339US637

For example, 333US147 Fisher v Hurst (1948) is cited by 333US631 Sipuel v. Board of Regents (1948)

Nodes: https://github.com/introdh2016/labs/blob/master/20050_nodes.csv


Id | term | chief | name | issue | issue_description |liberal_flag
--- | --- | --- | --- | --- | --- | --- 
332US631 | 1947 | Vinson | SIPUEL v. BOARD OF REGENTS OF THE UNIVERSITY OF OKLAHOMA et al. | 20050 | "desegregation, schools" | 1
333US147 | 1947 | Vinson | "FISHER v. HURST, CHIEF JUSTICE, ET AL." | 20050 | "desegregation, schools" | 0
339US629 | 1949 | Vinson | SWEATT v. PAINTER et al. | 20050 | "desegregation, schools" | 1


All Supreme Court Edges: https://github.com/introdh2016/response3_network/blob/master/ussc-31.zip

All Supreme Court Nodes: https://github.com/introdh2016/labs/blob/master/scotus_nodes.csv


There are a couple of very important things about this structure that make it work smoothly (and in some cases, at all) in Gephi.

- Edge: **source** and **target** are the necessary column names for the edge list to be read by Gephi.
- Node: **id** is a column header that Gephi looks for in both the node and edge list. It should be a unique identifier for each node that will appear on the graph. If this id isn't written then same as the `source` or `target` in the edges list, this won't work.
- Node: **label** is another term that Gephi looks for. This will be the label that you can toggle on and off on your graph.


 
### Import data

Open up Gephi and go to the Data Laboratory. 
File > Import Spreadsheet, and choose `20050_nodes.csv`
on your computer. Make sure you select Nodes Table as the table type. 
Leave all of the defaults except you'll want to select append to existing workspace instead of create new workspace. 


Back in Gephi, go to Data Table > Import Spreadsheet. Choose `20050_edges.csv`. It should now
import as an edge list, but we can make sure by checking the 'Import As' option. By default, the data will be imported as directed. (If we want the data to be undirected, we can change "Type" to "Undirected".)  

Go to Data Table > Edges. We see our data. Now, go to Data Table > Nodes. Make sure the column 
that corresponds to your Edge list is labeled Id. Now, click on Overview on the top bar. What do you see?

### Labels

To make our graph more readable, we can add labels to the points in the graph. Go back to the
data laboratory and click on "Copy Data to other column" and select "name". Copy this
value to "Label".  Click back on overview, and select the capital "T" on the bottom toolbar.  What do you think?

This isn't great data viz, so let's go back change the Label to ID.

Click back on overview, and select the capital "T" on the bottom toolbar. You
can play around with the bottom toolbar to make the graph more readable. Take a minute to do
so!


### Layout
You can choose an algorithm to help construct a better layout for the graph. Let's take a look at two:

```
Layout -> Fruchterman Reingold -> Run -> Stop
```

It is based on graph drawing. The idea is that the edges want to stay together but the nodes want to
move apart. It is comes out of physics and mimics the movement of charged particles.  We can also
try:

```
Layout -> Forced Atlas2 -> Run -> Stop
```

This particular layout is designed for Gephi and popular for visualizations in DH.


The first time you select a layout, options will appear. Some adjustments you might consider are
Gravity, Prevent Overlap and Scaling. To return to this screen, go to Data Laboratory -> Layout
Select the layout you want to adjust and the options screen will appear. Take a moment to experiment
around a couple of different layouts until you find one that makes it easier to interpret the network.


### Nodes and Degree
Let's say I want to know which cases are central to our network. We can visualize this using the
degree of a node:

```
Appearance -> Nodes -> Ranking -> Degree
```

We can then look at which cases are citing more cases in our network. These will tend to be later cases because they are relying on the case law of previous cases. 

```
Appearance -> Nodes -> Ranking -> In-Degree
```

However, what we are probably most interested in is which cases are being cited. This gives us information about the most prominent cases in our network. We can do this by looking at the out-degree of each node.

```
Appearance -> Nodes -> Ranking -> Out-Degree
```

This is interesting but we can visualize this is an even more exciting way! While still in the Nodes - Partition section, we can actually visualize the node itself by selecting the circles icon. 

```
Appearance -> Nodes -> Circles Icon -> Ranking -> Out-Degree
```
Let's adjust the max size to see it better. Let's try Max. size: 100

We can then highlight our nodes in a different way. Let's say we are interested in communicating which Chief Justices had a large impact on our network. We can do this by:

```
Appearance -> Nodes -> Art Pallete Icon -> Partition -> Chief
```


### Statistics

On the right side of the interface, under the ‘Statistics’ tab, you’ll find a Network Overview menu with a number of metrics listed. These metrics are helpful for analyzing the graph, and for visualizing the graph in different ways.

Click ‘Run’ next to a metric to generate a data report window. The measurement for the entire graph will appear in the Network Overview, and the measurement for each node will be also be added to the Data Laboratory.

- Average Degree - The average number of edges connected to a node
- Avg. Weighted Degree - The average sum of the weights of edges connected to a node
- Network Diameter - The longest shortest path between nodes within the graph
- Graph Density - Measures how close the graph is to complete
- HITS - Computes two values for each node; How valuable information stored at that node is & the quality of the nodes links
- Modularity - Community detection algorithm
- PageRank - Ranks nodes “pages” according to how often a user following links will non-randomly reach the node “page”
- Connected Components - Determines the number of connected components in the network
- Avg. Clustering Coefficient - Averages how nodes are embedded in their neighborhood
- Eigenvector Centrality - A measure of node importance in a network based on a node’s connections; the sum of the centrality measures of all nodes connected to a node
- Avg. Path Length - The average number of steps to get from one randomly selected node to another

Let's try one!


Modularity is an algorithm designed to help identify groups or communities in a network (i.e.
community detection). We can run it using:

```
Statistics -> Modularity -> Run
```

You'll see a single pop up that gives us several options. In our case, we don't have edge weights. To visualize the results of the algorithm, select:

```
Appearance -> Nodes -> Make sure the palette is selected -> Ranking -> Modularity Class
```

Now we have groups of cases but the size of our nodes is not helping communicate this. So,
let's adjust the nodes.

```
Appearance -> Nodes -> Select the Circles -> Ranking -> Liberal Flag
```
Let's change the Max size: 25 and let's make our communities more obvious. Let's go back and change the color. We can do this by selecting the very hard to see color menu to the right of the color ramp. I like ramps with more variance when highlighting communities.  

### Subsetting the graph

Finally, let's consider the case where our data has some outliers that we are not particularly
interested in. This is extra important if you have a lot of data. We might consider removing
certain nodes.

```
Window -> Filters -> Library (double click) -> Topology -> Degree Range
```

A slider will appear. Adjust accordingly.  Select "Filter" to apply. Now, try it with the Ego
Network:

```
Window -> Filters -> Library (double click) -> Topology -> Ego Network
```

This allows us to see the local neighborhood of a given node. Type in `347US483` to select
the neighborhood of Brown vs Board of Education. You can modify the visualization by choosing how many
degrees of seperation (Depth) to include, and whether you want to add the case directly to
the graphic (With Self).

### Presenting

Select 'Preview' and a series of setting will appear on the left side. If you don't see a graph, click 'Refresh' at the bottom of the menu. There a lot of options to explore! 


#Related Readings

Cordell, Ryan, “Uncovering Reprinting Networks in Nineteenth-Century American Periodicals.” Am Lit Hist (Fall 2015) 27 (3): 417–445. [Viral Texts Project at Northeastern] (http://viraltexts.org/) and [Networks of Viral Texts](http://networks.viraltexts.org/)

Edward Arriaga, Fernando Caparini and Juan Luis Suarez, [“Modeling Afro-Latin American Artistic Representations in Topic Maps: Cuba’s Prominence in Latin American Discourse.”](http://www.digitalhumanities.org/dhq/vol/7/1/000145/000145.html).

Meeks, Elijah and Scott Weingart. [An Introduction to Networks Analysis and Representatin.] (http://emeeks.github.io/networks/)

Moretti, Franco. [Network Theory, Plot Analysis.](https://litlab.stanford.edu/LiteraryLabPamphlet2.pdf)

Weingart, Scott. [“Topic Modeling and Network Analysis.”](http://www.scottbot.net/HIAL/?p=221) The scottbot irregular.

Weingart, Scott. [“Contextualizing networks with maps.”](http://www.scottbot.net/HIAL/?p=1942) The scottbot irregular.
