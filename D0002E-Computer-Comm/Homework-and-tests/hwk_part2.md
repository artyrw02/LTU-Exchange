### Homework 4	

##### 1. Address Planning 
Consider a network topology on the figure above. Do the address planning, assigng missing roles to network devices. Answer the following questions. The correct answer gives you 10 points, the incorrect one -10 points, the I am not sure gives you 0 points.

1. Consider a network of nodes [D:O]. As the network layout in the figure above indicates this subnetwork is assigned a network address 192.30.147.249/29. What is the network mask for nodes in this IP subnet?
2. Assume switches are not configured with an IP address. Can the assigned address space support all nodes in this network? 
3. If host A have an IP address as shown in the figure above, what functionality should be implemented in device B? 
4. How many simultaneous connections can device B support in principle? 

**ANSWERS----------------------------------------------------------------------------------------------**
  1. 192.30.147.249/29 -> 255.255.255._ _ _ _ (_) _ _ _ -> **`255.255.255.248`**
  2. /29 -> 255.255.255.1 1 1 1 1 1 [0 0 0] 3 available for hosts -> 2^3 - 2 = 6 ip availables so answer **` YES`**.
  3. **`NAT`**
  4. Class B -> 172.237.147.0  /16 -> **` 2^16 connections.`**

##### 2. Distance vector routing
Consider the network fragment  shown above. Router x has only two attached neighbors, w an y. Router w has a minimum-cost path to destination u  (not shown) of 5, and y has a minimum-cost path to u of 6. The complete paths from w and y to u (and between w and y) are not shown. All link costs in the networkhave strictly positive integer values. Answer the following questions. The correct answer will give you 10 points the incorrect one -10 points, the "I am not sure" gives you 0 points.

1. Give x's distance vector for destinations w, y, and u.

2. Give a link cost change for either c(x,w) or c(x,y) such that x will inform its neighbors of a new minimum cost path to u as a result of executing the distance-vector algorithm.

3. Give a link cost change for either c(x,w) or c(x,y) such that x will not inform its neighbors of a new minimum cost path to u as a result of executing the distance-vector algorithm.

**ANSWERS----------------------------------------------------------------------------------------------**

1. x's distance vector:
	**`- Dx(w) = 2`**
	**`- Dx(y) = 4`**
	**`- Dx(u) = 7`**	
2. cost change for either c(x,w) or c(x,y) will inform:
	- c(x,w) = 2
	- c(x,y) = 5	
	**`c(x,w) > 6 -> will  inform change**`	
3. cost change for either c(x,w) or c(x,y) will not inform:
	- c(x,w) = 2
	- c(x,y) = 5
	**`c(x,y) > 1 -> will not inform change**`
	
##### 3. Fragmentation
Consider sending a 3000 byte datagram into a link that has an MTU of 500 bytes. Suppose the original datagram is stamped with the identification number 422. Answer the following questions. The correct answer gives you 5 points, the incorrect one -5 points, the "I am not sure" gives you 0 points.

1. How many fragments are generated?  
2. What are their characteristics?

**ANSWERS----------------------------------------------------------------------------------------------**
3000 byte datagram -> (20 bytes of IP header + 2980 IP payload)
MTU = 500 bytes
Id num = 422
[datagram - IP_header]/[MTU - IP_header] = aprox fragments
[3000 - 20]/[500 - 20] = 6,20 ~ 7 fragments

8 bit chunk -> 480 / 80 -> increment of offset by 60.
|Number|Size   |ID   |Offset   |Flag   |
|---|---|---|---|---|
|1   |480 bits + 20   |422   | 0  | 1  |
|2  |480 bits + 20   | 422  |  60 | 1  |
|3   |480 bits + 20   | 422  |  120 | 1  |
|4   |480 bits + 20   |422   | 180  | 1  |
|5   |480 bits + 20   |422   | 240  | 1  |
|6   |480 bits + 20   |422   | 300  | 1  |
|7   |2980 - (480 * 6) = 100 + 20   | 422  | 360  | 0  |

##### 4. IP overhead 
Suppose an application generates chunks of 40 bytes data every 20 milliseconds, and each chunck gets encapsulated in a TCP segment and then an IP datagram. What percentage of each datagram will be overhead, and  what percentage will be application data?

**ANSWERS----------------------------------------------------------------------------------------------**

**`TCP header 20 bytes 	-> 50% overhead**`
**`IP header 20 bytes		-> 50% application**`

##### 5. Prefix notation
Suppose an ISP owns the block of addresses of the form 101.101.101.64/26. Suppose it wants to create four subnets from this block, with each block having the same number of IP addresses. What are the prefixes of the four subnets?

**ANSWERS----------------------------------------------------------------------------------------------**
`** wants to create ~~ four subnets ~~ **`
101.101.101.64/26 	-> 	255.255.255. 1 1 0 0 0 0 0 0

1. 2^4 = 16 subnets.
2. 255.255.255. [1 1 0 0] {0 0 0 0}   <- [ ]selecting 4 for the bits used ; {} remaining bits
				/ 28
				
3. Ips:
	- _._._.64 /28
	- _._._.64 + 16 = 101.101.101.80 /28
	- _._._.80 + 16 = 101.101.101.96 /28
	- _._._.96 + 16 = 101.101.101.112 /28

##### 6. True or False 

1.	[** TRUE**] The routers both in datagram networks and virtual-circuit networks use forwarding tables.			
2.	[** FALSE**] Internet Control Message Protocol is a protocol at the Transport layer.			
3.	[** FALSE**] When a host joins a multicast group, it must change its IP address to be that of the multicast group it is joining.			
4.	[** FALSE**] IPv6 uses 64 bits addresses.			
5.	[** FALSE**] With a help of ICMP protocol one can determine a minimum size MTU.			
6.	[** TRUE**] Link-state routing protocol OSPF implements Dijkstra routing algorithm.			
7.	[** TRUE**] The RIP routing protocol based on Bellman Ford algorithm may create loops in the topology.			
8.	[** TRUE**] The OSPF protocol consumes more network resources than RIP for its operations.			
9.	[** FALSE**] A router must be configured with only one IP address			
10.	[** TRUE**] The routing protocols for Inter-AS and Intra-AS are different			
11.	[** TRUE**] Head-of-line blocking occurs at the output port of a router			
12.	[** FALSE**] In a 2x2 switch to have no input port queuing, the switching fabric should operated at a speed at least 2 times the line speed.			
13.	[** TRUE**] /24 network is larger than /29 network			
14.	[** FALSE**] In a network with mask 255.255.255.252 there are maximum 8 IP enabled devices			
15.	[** FALSE**] Ethernet addresses are hierarchically structured while IP addresses are not
