
Network Analysis Workshop by Scott Weingart

## Workshop I

### Introductions

### nodexl.codeplex.com

Download.


### Who are you?
Name
Where you're from.
What is your interest in networks?

### Google

Poor results. Thought of the internert as a network.
Based on citation network.


### What is a network?

ex. London Underground
ex. Facebook / Food Web/ Citation Network / Electrical Grid

All have particular properties. 
Ex. Electrical Grid going down in US in 2000s. Spread to power outage throughout the northeast. 
Image of aerial view.

graph/network used interchangably

Network science independently created by a lot of different disciplines.

### Edge Attributes

Directed/ Asymmetric or Undirected/ Symmetric  (ex. Twitter -> Follow or not Follow vs Facebook)
Weighted or Unweighted (Amount of time two actors share together)
Types (Different kinds of connections)

### Node Attributes
Gender/Location/  Start and End Time / Age/ Title/ Salary/ etc

### Dyads and Triads
Building blocks of networks.

###Transitivity & Triadic Closure
If A is conect to be and B is connected to C, likely C will connect to A.

### Isolates

### Bipartite Networks

Nodes of different sorts conencted to each other.  People and Organizations connected. 
Unlikely to have isolate because fundamentally interested in relationships.

### K - Partite Networks 
Ex. Author - Title - Publisher 
Nodes of different sorts conencted to each other.

### Parallel Edges & Self-Loops
Gephi can't handle Parallel Edges. You can turn it into a weight in Gephi though. Ex. I call Scott, Scott calls me.
If different types of edges, need to analyze seperate them into different networks.
More recent work is helping with this. Not in the tools.

Network algorithms aren't great with self-loops.

### Huamanities Networks
- Moretti - Network Plot Analysis Article
- Russian River Network - Moscow had highest betweeness centrality.
- Florentine Families (Padgett & Ansell 1993) (Read!) No math. Just visualization.
- Charachter Network (Graham Sack 2012) - charachter co-occurance networks. Literary trends.
- Body in Folklore (Weingart & Jorgensen 2013 - "Representations of Gender and the Body in European Folktales") 

## Network Data and Decision Making / Part 2

### Data vs Capta
- Data (n) - Neuter past participle of dare (latin)/ what which is given
- Capta (n) -Neuter past participle pf capere (latin)/ "That which is taken"

Teach: Have students redo Moretti's network. Rarely do!

### Choosing Varibles
- spectrum of subjectivity
- subjective process of variable choice
- all that data -> bottom of the iceberg

### Network Data

Flows -  Potentiona <--> Actual (Helpful slide he has)

### Generating Data
- image of dining room... how to make the network? What decisions will we make?
Ex. charachter interactions 

Scott fan of doing mulitple networks and the results agree, then can trust the result.
Not a fan of one graph, see!, walk away.

### The Matrix
graph theory -> linear algebra (not happy with self loops, particulary in gephi)

### Adjacency/ Edge List 
Prefered mode. (Relational database -> a join table)
Not for underlying representation. Need this as a data structure.

### Node & Edge Lists 
Makes it easier to add attributes.


### NodeXL
Way to structure networks in Excel.

### Diary of Samual Pepys
http://www.pepysdiary.com/
- Make your own network.
- Use Pepy's diary - two days. 
- Launch NodeXL
- Walking through NodeXL. (Ex. Use Width in Edges to represent weight.)
- Provided a few ideas.
- Now go!


### Moving from NodeXL to Gephi
- Source/ Target/ Type / Kind / Weight in regular excel

### Gephi


----------------


## Workshop II

### Dyads adn Triads
Can ask how many in your network?

### Dyads & Global Reciprocity
How reciprocal? How like to write back for example?
Helps us look at power dynamics in a network for example. Loca and global reciprocity. 

### Transitivity
What's the likelinhood two nodes will become conneted? In other words, two nodes become friends?
Will see local densities get more dense.

### Global Triadic Closure
What is the global tridic closure? Likelihood triangles will close?
How easily are networks created within a company? Lower triadic closure means they aren't making friends.

### Degree Centralization
Nodes can have metrics. Edges can. Networks can.
How many edges are a node connected to. 
Social network: Popularity
Centrality measurement a treat of each node and can make it global. 
One node have very high while others are low? Medium centralization? Low centralization?
Showing topology of the network -> ie the shape of the network

### Degree Distribution

### Matthew Effect
Some are bell curves.
Some are power law distribution. (most nodes have 1 or 2 degrees and very few have 9 or 10)
Every network has a power law distriubtion. This isn't new and you shouldn't report it. Every network has it. 

### Matthew Effect
Social networks tend to grow in triangles.  Nodes already have lots of links are more likely to get more links. 
Rich get richer.  More connected are more like to get more connected. This is called "Preferential Attachment".

### Preferential Attachment
Twitter very little ceiling. 
Dunbar's Number - most people don't interact with more than 150 people. Cognitivie upper limit.
Depends on the medium how far this scales.

### Examples
- movie-stars
- co-authorship 
- web links
- airline networks

### Network Topologies
Ring, Linke, Tree, Ring?
ex. disease control.. hard with a lattice vs a ring

### Network Path

#### Shortest Path

#### Network Diameter
The longest shortest path.
Longest of the most efficient paths

#### Path Length

### Closeness Centrality
How does it take to get from A to any other node in the network.
sum of the shortest paths to all nodes/ total nubmer of nodes -1
how central is a node relative to all the other nodes
ex. who is the most impt to remove from the network? such as disease
Isolates? Hve to define if you want it on a single component or all the components.
Don't it across two different networks. If include isolates, it will be undefined. 
Centrality on a particular node... it's a local metric on ONE NODE.

### Average Path Length
Global version of closeness centrality
Avg distance from one node to another 

This is Kevin Bacon example. Six Degrees of Kevin Bacon?  
Airdish number.
Six degree is your average to another person in the world. Six Degrees of Seperation.

### Between Centrality
local metric
= number of shortest paths a node sits between
How likely you are to be a transportation hub

### Closeness Centrality
How likely you are to get to somebody


### Density
Global metric
How many edges from one node to another compared to how many possible nodes 
Can tell you whether doing network analysis is a good idea? Density of 0  or 100  ... don't do networks!
Does my network get more dense over time?

### When I get new data (Network EDA)
Number of Nodes? Edges? Possible edges?  Density? Diameter? Avg. Path Length?


Q/A: Are their discrete types of networks we are working with? What is the topology? Power Log Network - Ring Network - etc? Once we know the categories of these topologies, then helps determine what to do next/ type of analysis/ what we can learn.
Small World and Power Law -> tend to be the ones humanities people work with.


### The Strength of Weak Ties
People who you are least well connected to are more likely to help/ give you the info/ connect you to another area.
(Granovetter 1973)
Weak Tie vs Strong Tie
What edge is a bridge? Which one isn't? Need to understand the communities. 

### Broker
Structural holes in the network (Burt 1992)
The broker is filling the structural hole.
The people who fill structural holes are the most likely to have good idea. - Burt

### Six Degrees of Seperation 
Milgram 1950s

### Small Worlds
clusters of groups with small bridges between
different kind of topology -  high clustering coefficient, low average path length
easy to get from one person to another despite being large
a kind of topology
ex. studying academics.. often will be small worlds
use it to find people, connections that are integral,  looking over time... example: still a small world but in late stages getting lower average pathlinks because instiutioanalization of science, no longer need a big personality, there is a bureaucratic infrastructure ...     how are the properties of these small world changing? compared against another small world?

### Clustering Coefficient
local metric
measurement of if nodes tend to cluster
amount of my neighbors who are neighbors with each other
pretty much a very local density measurement

make it global by doing an avg of this measurement - "Global Clustering Coefficient"

### Connected Components
connected into different components (a component can be me one/ isolate)
Gephi will give you one. We need to know you can't do that. Needs to all be connected!  Can't be seperate networks (seperate components).  

### Community Detection
What are the communities being formed? 
- Divisive (Top-Down) - (1) cuts on weak ties/ local bridges (2) Edge Betwenness - repear calculation each time
- Modularity Method -  This is what Gephi does.  By saying... I have a local community where all the nodes know each other and are less likely to know the nodes in the other communities.  Looking for small chunks of nodes that cluster together.  Network of a million nodes and look with this method.  
- Agglormerative (Bottom-Up)


 
### Visualizations

#### Force-Directed Layouts
We have an idea that eucleadian distance matters. So closer together this must mean they are closer. 
NOT true in networks. 
This visualizations are a little random. Distance does not similarity. 




