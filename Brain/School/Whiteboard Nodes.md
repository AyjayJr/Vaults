- first a raycast is shot from the nodebrush and hits the whiteboard
- on hit the whiteboard is triggered to spawn the node

- for our implementation it would be better to select with a button and then use the controller raycast to select where on the whiteboard to spawn the node.
---
## Steps to implementation

### Task
- create buttons for nodes
	- similar implementation to the object spawning (SpawnObjectAtRay.cs)
### Issues
- the graph is not being initialized in reality flow graph view
- in the previous project, it was being intialized at runtime through new reality flow window
- our problem is just figuring out how to initiliazie a FlowVSGraph and BaseGraph
	- is there a way to just give a static reference of a graph???????
---

We are now able to initialize the flowvsgraphs but are running into server stuff.
Need to remove server logic.
The main scripts of focus are:
- FlowVSGraph.cs
- RealityFlowGraphView.cs
- SpawnNodeAtRay.cs

Seems like the nodes are being spawned on the graph but it isn't being represented visually.

Can the nodes be spawned without removing server logic for graphs? If so, do that first.
If not, remove server logic.