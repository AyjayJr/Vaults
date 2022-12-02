
## Useful Scripts

RealityFlowGraphScript.cs is the main script for the canvas
Command palette is junk, it was trying to undo/redo but didn't work

Scripts are scattered

- [RealityFlowNodes](https://github.com/many-realities-studio/realityflow-new/tree/main/Unity/Assets/Scripts/RealityFlow/NodeGraphProcessor/RealityFlowNodes)/ has the graph nodes that inherit from ngp
- [GraphScripts](https://github.com/many-realities-studio/realityflow-new/tree/main/Unity/Assets/Scripts/RealityFlow/GraphScripts)/ contains the visual functionality for the graphs

## Where is the functionality??? the core logic?
- within ngp (https://alelievr.github.io/NodeGraphProcessor/api/index.html)
- what changes did they make?
	- added visual representation of the nodes

## Todo
- whiteboard synchronization over network
- get node to populate on the whiteboard
	- do the same for multiple useful nodes e.g. transform manipulation, counter, display 
- make connections between nodes
- run a completed graph that has some affect on an object

