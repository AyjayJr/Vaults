## Tasks
1. be able to connect nodes on the graph ✅
	- edge doesn't follow the port positions (fixed in a hacky way, redraw edges every frame is always true)
	 ![[Pasted image 20221109044235.png]]

2. populating the correct types of nodes on the graph via the node menu ✅
	- Dr.Murray suggests that adding the baseInteractable will give more information from events generated by the raycast
	- he suggests to look at SlateDrawingExample for details

3. be able to have a functioning running graph ✅
	- DebugNode triggers a menu to spawn on execution, this shows we have some sort of functionality

4. implement FlowObjects that can be affected by the graph execution ✅
	- FlowObjectMonoBehaviour is a component that is attached to objects to allow for manipulation, possibly
	- if that is the case then hardcode the id of each object in FlowObjectMonoBehaviour component, attach to object in scene
	- profit???