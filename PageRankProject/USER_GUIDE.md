# How to use the WebCrawler Application

This application is a kind of [web crawler](https://en.wikipedia.org/wiki/Web_crawler) that traverses HTML and scrapes links from webpages, then systemmatically explores other webpages
based on the initial target page it's given. You can specify how far out you want it to search (how many neighbors it should visit). Once it's done visiting webpages, it will
generate a graphical visual representation (found in the "Graph View" tab) that you can interact with to view the connections formed between web pages. There is a textual representation of the breakdown of the graph
in the "Logs / Tree View" that shows a "dump" of all the links on the left, and a tree-view on the right that you can expand out.

You can use the different parameters in the checkboxes to enable or disable certain search criteria. A brief description of what each checkbox does is given in the application.
There are two types of parameters a user can set:

# Search Trimming Parameters: 
*These types of parameters actually reduce/trim the search space of the application. The application will not visit some webpages based on whether or not these settings are enabled. Since these parameters do affect the search space, they also affect the runtime of the application by making it run a lot faster since there are less nodes and edges to traverse, and graphically generate.*

- Suffix stripping (Decreases runtime)
- Exclude local pages (Decreases runtime)
- Allow multiple edges (Significantly increases runtime)

Non-search trimming parameters (Aesthetic effect only):
- Prefix trimming (Little to no effect on runtime)

# Step-by-Step Using the App
1. Type in a URL into the top-left textbox. You must include the full URL/URI path including its prefix (e.g "http://", "https://")
2. Specfiy a neighbor-discovering distance (zero by default). 0 is suggested for the first search since it's fast.
3. Enable or disable the aforementioned checkboxes to your liking.
4. Press the search button or press enter to let the application begin searching the webpages. While it is loading, you will be able to make changes to the parameters or interact with the program. You can however watch the "Logs / Tree View" tab populate the links to see what links it's currently traversing.
5. Once the program finishes generating the links and the graph, feel free to explore the tree viewer or the graph viewer.

# Logs

Here you can see a dump of all the files that were crawled from the page.

# Tree Viewer

Every root webpage has "children" webpages that it has an outgoing link to. If you click the plus signs, you can unfold these children and explore the tree that way.

# Graph Viewer

The framework used in this application (Microsoft Automatic Graph Layout) has a built-in graph viewer. This is accessed in the "Graph Viewer" tab whenever a graph is generated
after a search. You can do several things with this graph viewer. You may do any of the following when interacting with the viewer menu bar at the top:

1. Zoom in and zoom out with the mouse wheel or icons in the menu bar.
2. Press home to return to the original view.
3. Use the hand/grabber tool to pan around the graph.
4. Use the default select tool to move edges and nodes around.
5. Forward and backward arrows to return to previous view ports.
6. Floppy disk icon to save images of the graph in several common image formats, .svg, or .msagl format.
7. Open another .msagl file.
8. Print the graph.
9. Change the layout algorithms of the nodes/edges.
10. Add a new edge/node into the graph using the icon that looks like an arrow.
