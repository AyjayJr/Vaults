# Where we left off

From what i remember we left off with the basic object manipulation working perfectly over the network, we got a couple nodes on the whiteboard, but we need more functionality and ideally we would have that functionality working over the network so the peers can manipulate and run each other's nodes and have the results of the graph appear for both clients.

At some point we must also address the issue of building the project. How can we do it if our scripts rely on editor scripts?

# Next steps:
---
## Default VR interactions

As of right now most default VR interactions are taken care of with the exceptions of the following:

### Manipulation of nodes on the whiteboard

Currently our nodes will spawn where we are aiming on the whiteboard but they will remain in that static position. It's our job to figure out how to freely move those nodes around the board.

*Steps towards implementation:*
- This one I can't think off the top of my head how to handle it. I'm sure it will require an understanding of MRTK interactables and interaction events such as OnSelect(). The MRTK Base Interactable handles much of this and thus, it may be as easy as adding that script to the node prefabs and adjust the interaction events.

---
## Visual scripting tasks

Get better game object manipulation through the graph, here are a few ideas i have of how we can acheive this:

### 1. Dynamically add game object node to objects in the scene

Right now we have GameObjectNode.cs that recieves a string name and if an object with that name is found in the scene then a node is initialized. Right now the string is hardcoded to "Cube(Clone)". We want to be able to point at an object in the scene and pass the name of that object to GameObjectNode.cs.

*Steps towards implementation:*
- Get the raycast select event from an interactable script (baseInteractable, object manipulator, etc.) that should be applied to all scene objects
- On Select create a copy of the name of that object and store it in some temporary storage variable
- On Release place that name at the point of the raycast if it is pointed at a GameObjectNode.cs, otherwise discard the name

### 2. Add more nodes

As of right now we have about 4 nodes that can actually cause some sort of effect in the scene. We need to create more helper nodes that can alter the output of these nodes.

For example, GameObjectManipulation node takes a color and a conditional statement. We need to make those color and conditional nodes in order to have more variance in what we are able to achieve with the game object manipulation node.

*Steps towards implementation:*
- Make nodes that stores user input values such as int and string (this will give us versatility)
- Test all nodes to identify it they are properly passing their values to the other nodes 
- Create counter node that increments values
	- this node should not have and world presence
	- it's ouput can be displayed by other nodes such as the modal node
- Some sort of toggle node, this can be use in a lightswitch type demo
	- this node would spawn an mrtk toggle button
	- toggle on turns on light game object
	- toggle off turns off
	- this would require us to add a light prefab to the objects library
	- would probably also require some control flow

### Stretch goals:
- node that can detect collisions of game objects
- set up basketball demo

---
## Multiplayer functions

### 1. Node/Whiteboard networking

The most important aspect of multiplayer left to implement currently is the networking of the VRWhiteboard and the nodes.

**Steps towards implementation:**
- adjust networked object script to work well with nodes
- fix bugs currently involved in the networking of the whiteboard


### 2. Sending results of graph events over network

In theory we would want to calculate the results of running the graph on one client and send the results of those calculations over to the other client.

For example, we can currently make a cube in the game world turn black through nodes on the graph but that result will not show for anyone other than the owner.

*Steps towards implementation:*
- this one is so far off and i'm so braindead rn idk how we would tackle this
- will definitely require knowledge of how the ubiq framework operates

---
## Database storage

We would love to store all the information in some database but unfortunately it seems it may be outside the scope of this semester.

Here's what we would need to do:
- create database
- have this db be able to interact with ubiq server and get updated when something about the room changes e.g. new node spawn, new object, object positions
- store this instance of the room in some serialized format including:
	- saved graphs
	- object positions
	- object status
---