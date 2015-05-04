#### Goal 6
##### Work related to Summary of chapter 5 from book  pages <434 - 500>.

* Nodes: hosts, routers, switches, and WiFi access points.
* Links: communication paths.
* Network links:
	- point-to-point links
	- broadcast links.
	
* Link layer services:
	- Framing.
	- Link access (MAC).
	- Reliable delivery.
	- Error detection and correction.
	
* Link layer implemented in network adapter (network interface card - NIC).

* **Error detection and correction techniques:**
	- Parity checks:
		1. Even parity check -> d (data bits) + 1.
		2. Odd parity check -> 1 - valued bits from even parity.
		3. Two-dimensional parity check -> i (rows) + j (columns) + 1 (parity check). / Method used for detection only.
		4. forward error correction (FEC) -> used for detection and correction.
		
	- Checksumming methods
		1. the result of the sum of k-bit (d bits of data) integers will be the error-detection bits.
		2. Internet checksum.
		3. If result of sum = 0 then error detected.
		
	- Cyclic redundancy checks 
		1. Known also as polynomial codes.
		2. `d + r received bits by G`. If result <> 0 error has occurred; otherwise the data is accepted as being correct.
		3. 	CRC calculation is done by XOR.
		
* **Multiple Access Links and Protocols:**
	- multiple access protocols:
		1. channel partitioning protocols
			* TDM divides time into time frames then divides each time frame into N time slots.
			* FDM.
			* code division multiple access (CDMA).
			
		2. random access protocols
			* transmitting node always transmits at the full rate of the channel.
			* slotted ALOHA protocol.
			* pure ALOHA protocol.
			* Carrier Sense Multiple Access (CSMA) and with collision detection (CSMA/CD).
			
		3. taking-turns protocols.
			* polling protocol (master node. examples: 802.15 protocol and Bluetooth protocol) -> eliminates the collisions, achieves more efficiency.
			* token-passing protocol (no master node. examples: fiber distributed data interface (FDDI) protocol [Jain 1994] and the IEEE 802.5 token ring protocol).
	
* **Switched Local Area Networks**
	* Link-Layer Addressing and ARP.
		- MAC address -> 6 bytes long (Addresses represented in hexadecimal notation), giving 2^48 possible MAC addresses.
		- Address Resolution protocol or ARP: translates IP addresses to link-layer addresses.
	* Ethernet
		- Prevalent wired technology.
		- Evolution thru the years. Still the best option.
		- Example of Ethernet technologies: 10BASE-T, 10BASE-2, 100BASE-T, 1000BASE-LX.
	* Link-Layer Switches
		- Receive incoming frames and forward them onto outgoing links.
		- Switch tables -> contains **MAC address, Interface to be sent to, time for posting in table**
			* Filtering: determines whether a frame should be forwarded to some interface or dropped. 
			* Forwarding: determines the interfaces to which a frame should be directed and moves it to it.
		- Self-Learning.
		- Switches are plug-and-play devices.
		- Switches services:
			* Elimination of collisions.
			* Heterogeneous links.
			* Management and security.
	* Virtual Local Area Networks (VLANs)
		- isolate traffic.
		- Switch can be divided by groups or areas avoiding the use of more devices.
		- Management.
		- VLAN trunking.
* **Link Virtualization: A Network as a Link Layer**
	* Multiprotocol Label Switching (MPLS)
		- Referred as `label-switched router`: forwards an MPLS frame by looking up the MPLS label in its forwarding table and then passing the datagram to the correct output interface.
		- virtual private networks (VPNs) = tunnel / security.
* **Data Center Networking**
	* Used to store a huge amount of information.
	* Border routers used to control the flow and traffic between hosts (Internal or external).
	* load balancer: distributes requests to the hosts	making a balance of the load of the hosts.
	* data center network usually work with hierarchical arquitecet.
