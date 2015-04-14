#### Summary Chapter 3 - part 2
##### From book pages <230 - 282>
##### Connection-Oriented Transport: TCP


* **TCP (Transmission Control Protocol) basic characteristics**:
	* Connected-oriented.
	* Reliable data transfer.
	* Flow control. 
	* Acknowledgments. 
	* Timers (timeout/retransmit mechanism) to recover from lost segments.
	* Data follows a sequence and arrive in a specific order.
	* Congestion Control.
	* Used for multimedia applications along with UDP.
	* Provides full-duplex service.
	* Point-to-point.
	

	* **Structure of TCP Segment**:

	* **Timers**:
		* Round-trip time (RTT),  the time from when a segment is sent until it is acknowledged.
		* The sample RTT (SampleRTT) amount of time between when the segment is sent (that is, passed to IP) and when an acknowledgment for the segment is received (Doesn't work with retransmitted segments).
		* Average of the SampleRTT values: `EstimatedRTT = (1 – alpha) • EstimatedRTT +alpha • SampleRTT' where the recommended value is ' alpha = 0.125`.
		* Derivation from SampleRTT formula: ` DevRTT = (1 – β) • DevRTT + β •| SampleRTT – EstimatedRTT | ` The recommended value of β is 0.25.
		* The timeout interval should not be too much larger than EstimatedRTT; otherwise, delays can be caused because TCP won't retransmit fast.
		* TCP’s method for determining the retransmission timeout interval: `TimeoutInterval = EstimatedRTT + 4 • DevRTT`. An initial TimeoutInterval value of 1 second is recommended.

	* **Reliable data transfer**:
		* Events related to data transmission and retransmission in the TCP sender:
			1. Data received from application above.
				* Create TCP segment with sequence number.
				* If timer currently not running then TCP starts the timer.
				* Expiration interval for timer is the TimeoutInterval.
				
			2. Timer timeout.
				* Retransmits the segment that caused the timeout event. 
				* TCP then restarts the timer.
				
			3. ACK receipt.
				* Compares ACK value with its variable SendBase.
				* Update SendBase with ACK value.
				* Restarts the timer if there currently are any not-yet-acknowledged segments.
			
		* Fast retransmit is a method used to retransmit the missing segment before the segment’s timer expires.

	* **Flow Control**: 
		* Eliminates the possibility of the sender overflowing the receiver’s buffer.		
		* Receive window (rwnd) used to define how much free buffer space aprox is available at the receiver from the sender side.
		* rwnd is set to the amount of spare room in the buffer: 'rwnd = RcvBuffer – [LastByteRcvd – LastByteRead]'.

	* **TCP Connection Management**
		* **Establish a connection between client - server.**
			*Three-way shaking*
			1. Client opens the connection by sending a 'SYN' specifing random sequence number.
			2. Server receives packet and sends 'SYN + ACK'.
			3. Client receives the 'SYN + ACK' and replies with an 'ACK'.
			
		* **Closing a connection between client - server.**
			Two states:
			1. Client sends a segment 'FIN'. Server replies with an 'ACK'.
			2. Server sends a segment 'FIN'. Client replies with an 'ACK' waits an amount of time between '30sec to 2 mins' and then connection is closed.
			
* **Principles of Congestion Control**:
	* Causes:
		- Occurs when a link is carrying so much data than the capacity of the network can handle.
	* Effects:
		- Queueing delay, packet loss or the blocking of new connections.		
	* Congestion and flow control are not the same.
	* Congestion-control approaches:
		- end-end congestion control
		- network-assisted congestion control
	* Slow Start:
		- When a TCP connection begins, cwnd = small value of 1 MSS  and increases by 1 MSS every time a transmitted segment is first acknowledged.
	* Fairness:
		- Used to determine whether end systems or applications are receiving a fair share of system resources. 
		- Used to avoid congestion collapse.
		
	
	
	
	
