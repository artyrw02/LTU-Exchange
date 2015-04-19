#### Goal 4
##### Work related to Summary of chapter 4 from book  Part 1.

* **Network layer services**:
	- Guaranteed delivery.	
	- Guaranteed delivery with bounded delay.
	- Arrival in-order packet delivery.
	- Guaranteed minimal bandwidth.
	- Guaranteed maximum jitter.
	- Security services.
	
* **ATM service models**: constant bit rate and available bit rate service.

* **Virtual-Circuit networks** = connection service at the network layer.  
	1. path from source to destination.
	2. VC numbers, one number for each link along path.
	3. entries in forwarding tables in routers along path.
	
	* Routers maintain connection state information for the ongoing connections.
		- VC setup.
		- Data transfer.
		- VC teardown.
		
	* Signaling messages: messages that the end systems or routerss send into the network to initiate, terminate or set up a VC.
	
* **Datagram networks** = connectionless service at the network layer.
	- **Datagram** = network-layer packet.
	- Packet's paths may vary depending on the router (analyzes and selects the best path and sometimes may vary).
	- Routing tables:
		* Used to determine which path will be used to forward the packet.
		* The use of **prefixes** allow routing tables to avoid storing unnecessary number of IP addresses.
		
* Router Architecture		
	- **Routers** = forward datagrams from input links to output links.
		* Forwarding = action to move datagrams from one link to another. 
		* Routing = determs the paths that the datagram will follow in order to move from end-to-end by using protocols like RIP, OSPF, BGP.
	- Physical components:
		* Input ports.
		* Switching fabric.
			- Packets are forwarded.
			- Switching techniques: Memory, Crossbar, Bus.
			- Packets can be forwarded one at a time.
		* Output ports.
		* buffering size = B = RTT * C/√N
			where: 	amount of buffering (B) 
					round-trip time (RTT) 
					link capacity (C).
	* Routing processor & memory (executes routing protocols, controls routing tables).			
			- The forwarding table is computed and updated by the routing processor.
* Components of network layer:
		- IP protocol = IPv4 / IPv6.
		- Routing protocols = path selection with RIP, OSPF or BGP.
		- ICMP protocol = error reporting and router “signaling”.
			
	* maximum transmission unit (MTU).		
	* Framentation = break one IP datagram into more IP datagrams.
	* Interfaces = provide network connectivity to the host / router.
	* Router can have multiple interfaces.
	* IP address v4 has 32 bits long.
	* Subnet is a logical division of an IP network.
	* Classless Interdomain Routing (CIDR) =  method for allocating IP addresses and routing IP packets.
	* To assign an IP addresses to any host:
		- Manually by system administrator.
		- By using a DHCP server (provides an IP address).
	* NAT = Network Address Translation.
	* Universal Plug and Play (UPnP) = protocol that allows a host to discover and configure a nearby NAT.
	* ICMP protocol	is used to test the communication between hosts.
	* IPv6 = protocol that will take place over IPv4 as it is running out of space for new IP addresses.
		- has 128 bits long.
		- anycast addresses.
		- dual-stack approach.
		- Tunneling as an alternative of dual-stack approach.
	* IP security = Virtual Private Networks (VPNs).
