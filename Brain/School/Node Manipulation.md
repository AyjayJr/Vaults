How to be able to make the node stick to the cursor

I feel like i would be able to repurpose the TrackCursor script to do this

On Select, track cursor, on exit, don't track

---

# 11/13

Added a close button to the nodes but the problem is that it only visually deletes the node it doesn't actually remove it from the graph that is going to cause a lot of problems if i don't fix it now. 

TODO:

- Make close button remove instance from graph
	- Look into how clear graph works and apply it to the close button on the nodes.
- Remove edges when the nodes are removed
- I think the edges issue may inherently be solved if i can figure out how to remove the nodes from the base graph 


