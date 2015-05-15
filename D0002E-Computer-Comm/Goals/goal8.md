#### Goal 8
##### Work related to Summary of chapter 8 from book  pages <671 - 742>.

* Secure communication properties.
	- Confidentiality (encryption).
	- Message integrity.
	- End-point authentication.
	- Operational security (firewalls).

* Cryptography
	- plaintext or cleartext: message without encryption.
	- ciphertext: message using encryption algorithm.
	- keys are used in the algorithms in order to decrypt the messages.
	- symmetric key:
		- substituting one thing for another.
		- monoalphabetic cipher:
			- substitutes one letter of the alphabet with another letter of the alphabet.
			- breaking encryption scenarios:
				* Ciphertext-only attack.
				* Known-plaintext attack.
				* Chosen-plaintext attack.
		- polyalphabetic encryption.	
			- use multiple monoalphabetic ciphers.
		- symmetric encryption techniques:
			* stream ciphers.
			* block ciphers (DES, 3DES, and AES):
				+ Cipher Block Chaining (CBC).
	- Public Key Encryption:
		* public key: known by everyone.
		* private key: known only by user that will decrypt data.
		* RSA algorithm.
* Message Integrity and Digital Signatures
	* Message Integrity and Digital Signatures.
	* shared secret or authentication key is used for message integrity.
	* digital signature is a cryptographic technique.
	* public key certification.
	* Certification Authority (CA).
* End-point authentication
	- process that provides its identity to another entity over a computer network.
	- authentication protocol:
		+ run before the two communicating parties run some other protocol.
		+ four different versions. Each one with improvements.
			* ap1.0: exchange of messages.
			* ap2.0: exchange of messages by using IP address.
			* ap3.0: exchange of messages by using authentication (password).
			* ap3.1: exchange of messages by using authentication (encrypted password).
			* ap4.0: exchange of messages by using nonce and symmetric key cryptography forms.
* Securing E-Mail:
	* confidentiality.
	* authentication of sender and receiver.
	* Message integrity.
	* Pretty Good Privacy (PGP) uses:
		- MD5 or SHA for calculating the message digest.
		- CAST, triple-DES, or IDEA for symmetric key encryption.
		- RSA for the public key encryption.
* SSL
	- Secure Sockets Layer (SSL) -> Transport Layer Security (TLS).
	- used to provide security to transactions that take place over HTTP. (secures TCP or any app that runs over it).
	- Almost-SSL (and SSL) three phases: handshake, key derivation, and data transfer.
* IPsec and Virtual Private Networks
	+ provides security at the network layer.
	+ secures IP datagrams.
	+ create virtual private networks (VPNs).
	+ the Authentication Header (AH) protocol:
		- source authentication and data integrity but does not provide confidentiality. 
	+ Encapsulation Security Payload (ESP) protocol.
		- provides source authentication, data integrity, and confidentiality.
	+ are used for private networks.
	+ VPns are created over public network.
	+ IPsec Datagram:
		- tunnel mode
		- transport mode
	+ Internet Key Exchange (IKE) protocol:
		- Similar to the handshake in SSL.
* Securing Wireless LANs
	- Wired Equivalent Privacy (WEP):
		* secret 40-bit symmetric key.
		* Weak encryption standard.
	- IEEE 802.11i:
		* stronger forms of encryption.
		* four phases:
			+ Discovery and advertisement.
			+ Mutual authentication and Master Key (MK) generation -> Extensible Authentication Protocol (EAP).
			+ Pairwise Master Key (PMK) generation.
			+ Temporal Key (TK) generation.
		* AES-based encryption scheme.	
* Operational Security: Firewalls and Intrusion Detection Systems
	- firewall:
		+ used isolates an organization’s internal network from the Internet allowing some packets to pass and blocking others.
		+ three categories:
			* traditional packet filters (router -> packet filtering with access control lists).
			* stateful filters (track TCP connections to make filtering decisions).
			* application gateways (DMZ).


		
	
