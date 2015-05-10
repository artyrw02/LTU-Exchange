#### Goal 7
##### Work related to Summary of chapter 6 from book  pages <513 - 578>.

* Elements in a wireless network:
	- Wireless hosts: end-system devices running applications.
	- Wireless links.
	- Base station: responsible for sending and receiving data.
	- Network infrastructure.
	
* Wireless networks	classification:
	- Single-hop, infrastructure-based.
	- Single-hop, infrastructure-less.
	- Multi-hop, infrastructure-based.
	- Multi-hop, infrastructure-less.
	
* Wireless Links and its characteristics
	- signal-to-noise ratio(SNR): measurement of the strength of received signals.
	- hidden terminal problem: physical obstructions in the enviroment.		
	- CDMA used in wireless LANs.
	- WiFi uses CSMA/CA (colission avoidance).

* WiFi: 802.11 Wireless LANs
	- 802.11 standarts like 802.11b, 802.11a, and 802.11g.
	- The 802.11 Architecture:
		* basic service set (BSS) with one or more wireless stations and a central base station (access point - AP).
		* infrastructure wireless LANs.
		* To install an AP, administrator must configure:
			+ Service Set Identifier (SSID).
			+ channel number.
		* AP periodically send beacon frames that includes SSID and MAC address.
		* passive scanning and active scanning are used to scan channels and listen beacon frames.
	- Short Inter-frame Spacing (SIFS).
	- Distributed Inter-frame Space (DIFS).
	- Request to Send (RTS) control frame and Clear to Send (CTS) control frame are used to reserve access to the channels.
	- The IEEE 802.11 Frame:
		+ Payload (IP datagram or an ARP packet).
		+ CRC Fields (used to detect bit errors).
		+ Address Fields (6-byte MAC address).
		+ Sequence Number, Duration, and Frame Control Fields.
	- Bluetooth for shorter distances.
		+ frequency-hopping spread spectrum (FHSS).
		+ Bluetooth piconet.
	- Zigbee for longer distances.
		+ lowerpowered, lower-data-rate, lower-duty-cycle applications.
* Cellular Internet Access
	- Global System for Mobile Communications (GSM) standards.
	- base transceiver station (BTS) transmits signals to and receives signals.
	- 2G cellular systems uses combined FDM/TDM (radio).
	- 3G cellular system
		* 3G standards:
			+ Serving GPRS Support Nodes (SGSNs).
			+ Gateway GPRS Support Nodes (GGSNs).
		* Radio Network Controller (RNC).
	- 4G: LTE
		* Evolved Packet Core (EPC).
		* LTE Radio Access Network.
* Mobility Management: Principles 
	- Addressing
		- A foreign agent create a so-called care-of address (COA) for the mobile node.
		- two addresses associated with a mobile node:
			* permanent address.
			* COA or foreign address.
		- Foreign agent also inform the home agent that the mobile node is resident in its network.
	- Routing
		* indirect routing
			+ triangle routing problem.
		* direct routing
			+ cost of additional complexity.
* Mobile IP
	- Agent discovery.
		+ agent advertisement.
		+ agent solicitation.
	- Registration with the home agent.
	- Indirect routing of datagrams.
	- Security.
* Managing Mobility
	* home public land mobile network (home PLMN).
		- Has a database named home location register (HLR).
	* visited PLMN
		- Has a database named visitor location register (VLR).
		
	
	
