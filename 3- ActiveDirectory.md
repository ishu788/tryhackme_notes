Active Directory - Domain Controller.

comes with default groups and 2 users - Admin and guest


4 types of user
- Domain admin - big boss (only one to have domain access)
- Service accounts - to attach to services
- local admin - control of local machines
- domain users - daily users can access which they are authorized


2 types of group 
- Security groups
- Distribution groups


### Domain Trust

- Directional - The direction of the trust flows from a trusting domain to a trusted domain
- Transitive - The trust relationship expands beyond just two domains to include other trusted domains

The type of trusts put in place determines how the domains and trees in a forest are able to communicate and send data to and from each other when attacking an Active Directory environment you can sometimes abuse these trusts in order to move laterally throughout the network. 


- LDAP - Lightweight Directory Access Protocol; provides communication between applications and directory services
- Certificate Services - allows the domain controller to create, validate, and revoke public key certificates
- DNS, LLMNR, NBT-NS - Domain Name Services for identifying IP hostnames


The most important part of Active Directory -- as well as the most vulnerable part of Active Directory -- is the authentication protocols set in place. 


- Kerberos : The default authentication service for Active Directory uses ticket-granting tickets and service tickets to authenticate users and give users access to other resources across the domain.
- NTLM: default Windows authentication protocol uses an encrypted challenge/response protocol