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
##### 3. Fragmentation
##### 4. IP overhead 
##### 5. Prefix notation
##### 6. True or False 
