#### Goal 5
##### Work related to Summary of chapter 4 from book  Part 2.

* **Routing Algorithms**
	- Graph: used to formulate routing problems (`G = (N,E)`).
		- For any edge (x,y) in E -> c(x,y) " the cost of the edge between nodes x and y".
		- Pair (x,y) that does not belong to E -> c(x,y) = ∞.
		- Node `y` is said to be a neighbor of node `x` if (x,y) belongs to E.
		- Path in a graph G =(N,E): sequence of nodes each of the pairs are edges in E.
		- Cost of a path: the sum of all the edge costs along the path, c(x_1,x_2) + c(x_2,x_3) + ...+ c(x_p-1,x_p).
			* Paths: 
				1. least-cost path.
				2. shortest path.
				
		* **Classification of Routing Algorithms:**			
			- **Global routing algorithm (link-state (LS) algorithms):** gathers information before calculating.
			- **Decentralized routing algorithm - distance-vector (DV) algorithm.**	
			- **Static routing algorithm.**
			- **Dinamic routing algorithm.**
			- **Load-sensitive algorithm.**
			- **Load-insensitive algorithm.**
						
	* **Link-state**
		- Dijsktraʼs Algorithm.
		- protocol example: OSPF and IS-IS.
	* **Distance Vector**
		- Bellman-Ford Equation
			d_x(y): cost of least-cost path from x to y.
			
			`d_x(y) = min_v{c(x,v) + d_v(y)}`
			
			min_v takes over all of x’s neighbors.
		- protocol example: RIP, BGP.		
	* **Hierarchical**
		- autonomous systems (ASs): 
			* alternative defined to solve some problems from the routing algorithms (Regions).
			* collection of routers under the same administrative and technical control (Region)
		- Routers within the same AS all run the same routing algorithm. `intraautonomous system routing protocol`
		- gateway router: forwards the packet on the one link that leads outside the AS.
		- inter-AS routing protocol:	
			1. Obtains reachability information from neighboring ASs.
			2. Propagates the reachability information to all routers internal to the AS.
		- hot potato routing.

* **Dinamic Routing Protocols (intra-AS routing protocols):**
	- Also known as **interior gateway protocols**.
	- **RIP (Routing Information Protocol)**:
		* distance-vector protocol.
		* `hop` number of subnets traversed along the shortest path.
		* maximum cost of a path = 15.
		* RIP routers exchange advertisements every 30 seconds.
		* routing tables.
		* two versions of RIP.
		* RIP runs over UDP to implement routing algorithms.
	- **OSPF**:
		- Actual version = 2.
		- link-state protocol.
		- Uses Dijkstra’s algorithm to determine shortest-path tree.
		- router broadcasts routing information to all other routers in the AS.
		- broadcasts link-state information every 30 minutes.
		- HELLO messages to evaluate functionality of links.
		- Advantages:
			1. Security
			2. allows multiple paths to be used.
			3. support for unicast and multicast routing
			4. Support for hierarchy within a single routing domain
		- OSPF is configured into areas.
	- **BGP**:
		- allows subnet to advertise its existence to rest of Internet.
		- BGP session: two BGP routers "peers" exchange BGP messages.
		- external BGP (eBGP) session: a BGP session with two ASs.
		- internal BGP (iBGP) session: BGP session between routers in the same AS.
		- BGP allows each AS to learn which destinations are reachable via its neighboring ASs.
		- destinations -> CIDRized prefixes.
		- BGP advertisements -> route = prefixes + BGP attributes.
		- BGP attributes:
			1. AS-PATH:
				* prevents looping advertisements.	
			2. NEXT-HOP.
				* "Is the router interface that begins the AS-PATH".
				* Used to configure forwarding tables.
				* gateway router -> import policy
				* BGP eliminates rules when there is more than one router with the same prefix.
					- Routing Policy.
					- Scale.
					- Performance.					
* **Broadcast and multicast**	
	- Broadcast routing: from a source node to all other nodes in the network.
		* flooding: send copy of a packet to all of its neighbors.
		* broadcast storm: multiplication of broadcast packets.
		* Use of sequence numbers to avoid broadcast storm and control flooding.
		* reverse path forwarding(RPF) or reverse path broadcast (RPB).
		* Spanning-Tree is used to avoid redundant Broadcast packets.
				
	- Multicast routing: single source node to send a copy of a packet to a subset of the other network nodes.
		* address indirection (single identifier is used for the group of receivers).		
		* multicast group.
		* Multicast in the Internet: IGMP and multicast routing protocols.
		* softstate protocol.
		* multicast routing tree.
			- source-based tree
			- group-shared tree.
			
		* Multicast routing protocols	
			* Distance-Vector Multicast Routing Protocol (DVMRP).	
			* Protocol-Independent Multicast (PIM).
			
