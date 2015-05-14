### Homework 5	

##### 1. Aloha
Suppose three active nodes - nodes A, B, and C- are competing for access to a channel using slotted Aloha. Assume each node has an infinite number of packets to send. Each nodeattempts to transmit in each slot with probability p. The first slot is numbered slot 1, the second slot is numbered slot 2, and so on. Answer the following questions. For the correct answer you get 10 points, for the incorrect -10 points and for "I am not sure" 0 points.

1. What is the probability P1 that node A succeeds for the first time in slot 4?
2. What is the probability P2 that some node (either A, B or C) succeeds in slot 2?
3. What is the efficiency E of this three-node system (all nodes suceed)?

**ANSWERS MISSING PART 2-------------------------------------------------------------------------------------------**
	1. Probability P1:
		- Formula: **p(1 - p)^(N - 1)** & **p -> probability that A succeeds** 
		- p*(1 - p)^(3 - 1) -> p*(1 - p)^2:
			* When A transmits -> p
			* When B and C don't -> (1 - p)
		- A succeeds for the first time in slot 4:
			* p(1 - p)^(4-1)
			* **`p(1 - p)^2* (1 - p(1 - p)^2)^3`**
	2. 	Probability P2:
		- 3 nodes -> Np(1 - p)^(N - 1)
		- 3p(1 - p)^2
	3. 	Efficiency E:
		
##### 2. Broadcast channel
Consider a broadcast channel with N nodes and a transmission rate of R b/s. Suppose the broadcast channel uses polling  (with an aditional polling node) for multiple access. Suppose the amount of time from when a node completes transmission until the subsequent node is permitted to transmit (that is the polling delay) is d_poll. Suppose that within a polling round, a given node is allowed to transmitt at most Q bits. What is the maximum throughput of this broadcast channel?

**ANSWERS----------------------------------------------------------------------------------------------**

broadcast channel with	->	N nodes
transmission rate of 	->	R bps
amount of time for node	-> 	d_poll	to complete transmission
bits allowed to transmit->	Q bits

- Maximum throughput of this broadcast channel:
	length of polling round -> 	N(Q/R + d_poll)
-Number of bits transmit in a polling round NQ
	- (NQ)/[N(Q/R + d_poll)] **DESPEJAR
		**`= Q(R/[1 + (R*d_poll)/Q])`**

	
##### 3. CSMA/CD
Suppose two nodes, A and B, are attached to opposite ends of a 900 m cable, and that they each have one frame of 1000 bits (including all headers and preambles) to send to each other. Both nodes attempt to transmit at time t0. Suppose there are four repeaters between A and B, each inserting a 20-bit delay. Assume the transmission rate is 10 Mb/s, and CSMA/CD with backoff intervals of multiples of 512 bits is used. After the first collision, A draws K=0 and B draws K=1 in the exponential backoff protocol. Ignore the jam and the 96-bit time delay. Answer the following questions.
1. What is the one way propagation delay (including repeaters delays) between A and B in seconds? Assume the signal propagation speed is 2*10^8 m/s
2. At what time in seconds is A's packet completely delivered at B?

**ANSWERS----------------------------------------------------------------------------------------------**

2 nodes (A and B)
transmit time		-> t0
4 repeaters (rept) inserting -> 20 bit delay
transmission rate -> R = 10 Mbps -> 10*10e6 or 10e7
CSMA/CD with 512 bits
distance between nodes d = 900 m
prop_speed -> 2*10^8 m/s
Length of frame -> L = 1000 bits

1. What is the one way propagation delay between nodes:
	* formula -> (d / prop_speed) + rept *(rept_delay / R)
				  propagation	+ transmission
	* (900 / 2*10^8) + 4(20/10e7) = 0.0000125 seconds -> 12.5microsecs
2. 	A's packet completely delivered at B:
	* A detects collision at t0 = 12.5microsecs
	* A retransmits at t = 25 microsecs + t0 -> t2 = 37.5 microsecs bit arrives to B
	* t = 37.5 + L/R
		= 37.5 + 1000/10e7 = 0.0001375 -> 137.5microsecs

##### 4.  Spanning Tree
Consider a network depicted in the figure above. In the figure you see a bridged network consisted of two hosts (A, B) and eight transparent bridges. Answer the following questions. The correct answer gives you 10 points, the incorrect one -10 points, the "I am not sure" - 0 points.

1. Does transparent bridge store a packet before sending it to next hop?
2. Does the Spanning Tree Protocol calculate a shortest path between any 2 devices in a local area network?
3. What would be the root bridge for the Spanning Tree Protocol in the topology above?
4. Using the Spanning Tree Protocol for bridges determine root, designated and blocked ports for each bridge: What status (root - r, blocked - b or designated -d ) have ports 1,2, and 3 of bridge A24?

**ANSWERS----------------------------------------------------------------------------------------------**

##### 5. True or False 

1.	**[FALSE]** If all the links in the Internet were to provide reliable delivery service the TCP reliable delivery service will be redundant			
2.	**[FALSE]** The structure of the frame for 10BASE-T, 100BASE-T and Gigabit Ethernet is the same			
3.	**[FALSE]** A transparent bridge may be configured with an IP address			
4.	**[TRUE]** The efficiency of Slotted Aloha is almost 2 times higher than that of the un slotted variant			
5.	**[TRUE]** A 10 Mb/s Ethernet network can be arbitrary long.			
6.	**[TRUE]** The Gigabit Ethernet is built using CSMA/CD technique			
7.	**[TRUE]** Ethernet adresses are hierarchically structured			
8.	**[FALSE]** ARP protocol is used to find out an IP address of the first router			
9.	**[TRUE]** The nodes connected to different ports of a learning switch belong to the same collision domain			
10.	**[TRUE]** A spanning tree protocol is invented to avoid loops in LANs
