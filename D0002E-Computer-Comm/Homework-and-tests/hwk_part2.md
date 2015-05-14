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
##### 5. Prefix notation
##### 6. True or False 
