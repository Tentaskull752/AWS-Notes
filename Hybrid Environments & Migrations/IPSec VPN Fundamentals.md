
## Personal Summary

- Group of protocols that create a secure private channel of connection for networks across an insecure environment
- Set up between two peers, or their Routers specifically
- Provides authentication and encryption
- Interesting Traffic: traffic that matches certain rules, if data matches any of those rules, IT CLASSIFIES and is carried to it's pre-determined destination

 - Symmetric Encryption - Fast, exchanging keys is a CHALLENGE
 - Asymmetric Encryption is slow, BUT CAN EXCHANGED PUBLIC KEYS (Public key is used to encrypt and the corresponding private key is used to encrypt.)


 - IPSEC TWO PHASES:
	 - IKE Phase 1 (Slow & Heavy): where you initially authenticate using a pre-shared key; Using Asymmetric encryption to agree on, and create a shared Symmetric key
	 - IKE SA Created (phase 1 tunnel)

	- IKE Phase 2 (Fast and Agile)
	- Use keys agreed in phase 1
	- Agree encryption method, and keys used for bulk data transfer
	- Create IPSEC SA...phase 2 tunnel (architecturally running over phase 1)

 - 1. Certificate or pre-shared key authentication 
 - 2. Each side creates a DH Private Key
 - 3. And derives a public key
 - 4. Public Keys are exchanged over the public internet
 - 5. Each side takes their private key, and remote peers public key - independently generates the "same" shared Diffie-Hellman Key
 - 6. Using DH Key - exchanges key material and agreements
 - 7. Each side generates a Symmetrical key(Used to encrypt anything passing through the Phase 1 Tunnel/IKE Security Association) - using DH key and exchanged material

 PHASE 2

- 1. Symmetrical key is used to encrypt and decrypt agreements and pass more key material
- 2. "Best" "shared" encryption and integrity methods communicated and agreed
- 3. DH Key and Exchanged Key Material is used to created Symmetrical IPSEC Key
- 4. IPSEC Key is used for bulk encryption and decryption of interesting traffic


 - Policy-Based VPN: 
	 - rules sets match traffic -> a pair of SAs
	 - different rules/security settings
	 - allows more flexibility and more routes for different types of traffic.
	 - Could have tracks for financial, managerial, or other topic of interesting traffic.
- Route-Based VPN:
	 - target matching (prefix)
	 - matches a single pair of SAs