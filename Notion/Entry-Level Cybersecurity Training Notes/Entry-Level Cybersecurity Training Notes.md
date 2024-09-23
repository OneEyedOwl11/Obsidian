- Lesson notes for 2.1 Network Terminology & The CIA Triad
    - **Authentication** - Verifying a user is who they say they are
    - **Authorization** - Validating that an identity being  
        claimed by the user is known to the system and verifying what that user  
        should have access to.  
        
    - **Availability** - _This is part of the CIA Triad._ Availability means ensuring timely and reliable access to and use of information.
    - **Bit** - A binary digit having a value of 0 or 1.
    - **Byte** - A group of eight bits that is treated either as a single entity or as an array of 8 individual bits.
    - **Confidentiality** - Another part of the CIA Triad,  
        confidentiality means preserving authorized restrictions on information  
        access and disclosure, including means for protecting personal privacy  
        and proprietary information.  
        
    - **Identification** - asserting an identity and having it confirmed
    - **Integrity** - The last part of the CIA Triad,  
        integrity means guarding against improper information modification or  
        destruction and includes ensuring information non-repudiation and  
        authenticity.  
        
    - **Defense-in-Depth** - An information security strategy that integrates people, technology, and operations capabilities to  
        establish variable barriers across multiple layers and missions of the  
        organization.  
        _Note: We will talk more about this concept in later  
        lessons, but it’s good to start thinking about it now. A lot of what we  
        are talking about here is how to defend our networks at every level. In  
        the early days of network security, network administrators only  
        concerned themselves with protecting the network at the perimeter or  
        outward-facing edge of the network. As information security has evolved, it has become clear that we need to protect networks from the inside  
        out, at each connection level in order to truly defend them.  
        _
    - **Network** - A system implemented with a collection of interconnected components. Such components may include routers, hubs,  
        cabling, telecommunications controllers, key distribution centers, and  
        technical control devices.  
        _(Jenn's simpler definition: Two or more computers that are connected and share information and resources.)_
    - **Non-Repudiation** - Not being able to deny you did  
        something. In the context of network communications, non-repudiation  
        refers to the proof of who the sender of a message was. In this way, the sender cannot deny that they sent it.  
        
    - **Software** - Computer programs and associated data that can be dynamically written and modified during execution.
    - **Threat Actor** - An individual or a group posing a threat.
- Lesson notes for 2.2 Network Models Part 1
    
    a switch is only concerned about sending traffic between computers on the same network
    
    A router routes data between networks
    
    - Network Terms
        
        **Hub** - a node that broadcasts data to every computer or Ethernet-based device connected to it. _Remember that unlike a switch, a hub broadcasts to all nodes and cannot direct traffic to specific nodes._
        
        **Switch** - A device that connects multiple nodes on the same network. _Remember  
        that it is more sophisticated than a hub because it can direct traffic  
        to only certain nodes instead of broadcasting to all nodes.  
        _
        
        **Router** - A device that connects and routes traffic between networks
        
        **Endpoint** - Typically, an end-user device like a desktop, laptop, printer, mobile phone, etc.
        
        **Server** - A computer that is dedicated to providing a particular service, like a mail server or print server.
        
        **Firewall** - A device that filters traffic going between networks for the purposes of protecting the network.
        
    - Types of networks
        
        LAN Local area network
        
        WAN Wide area network
        
        WLAN Wireless WAN
        
        VPN Virtual Private Network
        
    - OSI Model (Open Systems Interconnection Model)
        
          
        
        Describes how network communication occurs
        
        What is happening with data as it moves from one stage to another
        
        ![[Untitled.png]]
        
        ![[Untitled 1.png]]
        
        - Data Encapsulation
            
            How data is encapsulated and de-encapsulated as it moves through the layers of the model (encapsulation occurs when data is transmitted whether through TCP [these pieces of data would be called segments] or UDP [these pieces of data would be called Datagrams] e.g. when the data is broken up to be sent through the transportation layer. A header would be added and that layer would contain source port, destination port, sequence number, etc. )
            
- Lesson notes for 2.3 Network Models Part 2
    
    - The OSI Model is not something you’ll work with day to day but it is information you’ll need when when conversing about higher level activities like:
        
        An applications programmer may need to understand about network communications in order to design their software securely
        
        An architect may need to ask a network engineer about what is already existing in the network in order to design a new part of the network
        
    - The TCP/IP Model uses 4 layers to represent the same ideas that the OSI model does (This is considered to be more practical)
        
        [https://images.ctfassets.net/kvf8rpi09wgk/7AJtllqS49Mdv38fx1CAiY/e5a64065e9a36fd06c356a0e99258dfe/TCP-IP-Model_Part_2.png](https://images.ctfassets.net/kvf8rpi09wgk/7AJtllqS49Mdv38fx1CAiY/e5a64065e9a36fd06c356a0e99258dfe/TCP-IP-Model_Part_2.png)
        
    
    The two models TCP/IP and OSI Model is beneficial because It can help you take an inventory of your network. This is one way to apply the Defense-In-Depth method as this method takes a look at all aspects of your network and how to defend it
    
    - OSI Layers
        - Physical layer 1:
            
            Address Type: N/A
            
            Devices: Cables, Network cards & Hubs.
            
            Data type: Bits
            
        - Data Link Layer 2:
            
            Address Type: MAC Address
            
            Devices: Switches/Bridges
            
            Data type: Ethernet Frame
            
            Ethernet Frame = Ethernet Header, IP Header, TCP Header, Data Payload & Ethernet Trailer
            
        - Network Layer 3:
            
            Address Type: IP Address
            
            Devices: Routers, Firewalls
            
            Data type: Packet
            
            Packet = IP header, TCP header & Data Payload
            
        - Transport Layer 4:
            
            Address Type: Ports
            
            Devices: Routers, Firewalls
            
            Data type: Segments
            
            Segment = TCP header & Data payload
            
        - Session Layer 5:
            
            Managing data in sessions and end-user applications
            
            E.g. When logging into your bank app the app makes sure you have the correct authentication and authorization. Also managing when the logged in session starts and ends
            
        - Presentation Layer 6:
            
            Translating data ,formatting, encryption & compression
            
        - Application Layer 7:
            
            This has to do with how the data shows up in the user interface and user inputs back into the application
            
    - TCP/IP Model
        
        Transmission control and internet protocol
        
        Predates OSI Model
        
        Only has 4 layers
        
- Lesson notes for 2.4 Common Ports and Protocols
    
    Port: is an entry point (Like a doorway). Can be opened or closed and these ports can have designated functionality
    
    Protocol: A set of rules for communication to work. Each protocol has it’s own purpose
    
    - Common Protocols:
        
        IP - Internet Protocol - Getting the address to which to send data
        
        TCP - Transmission Control Protocol - enables application programs and computing devices to exchange messages
        
        UDP - User Datagram Protocol - enables communications with low latency and loss tolerance. No acknowledgement needed before transmission. E.g. streaming
        
    - Generally non-secure ports and Protocols:
        
        21 - FTP
        
        23 - Telnet
        
        25 - SMTP
        
        143 - IMAP
        
        37 - Time
        
        53 - DNS
        
        80 - HTTP
        
        161/162 - SNMP
        
        389 - LDAP
        
    - Generally secure ports and Protocols:
        
        22* - SFTP
        
        22* - SSH
        
        587 - SMTP
        
        993 - IMAP
        
        123 - NTP
        
        853 - DoT (DNS over TLS)
        
        443 - HTTPS
        
        161/162 - SNMP v3
        
        636 - LDAPS
        
    
    Shell - shell is a computer program that allows you to control a computer from a command-line interface (Therefore you do not have a GUI)
    
    SSH - Secure shell. Is a network protocol that allows you to operate network services securely over an unsecured network. Most notable application is remote login and command-line execution. SSH uses a public key cryptography. Obtaining SSH credentials is really important for hackers so it should only be accessible through authorized admins
    
    Web Shell - Nefarious script that a hacker will use to access and control a web server remotely
    
- Lesson notes for 2.5 Network Threats and Attacks
    
    Lockheed Martin’s Cyber Kill Chain - Basic steps taken out when conducting a cyber attack
    
    - Cyber Kill Chain Steps
        1. **Reconnaissance** - obtain information about the target
        2. **Weaponization** - create the malware to use against the victim
        3. **Delivery** - infiltrate the victim's network to deliver the malware
        4. **Exploitation** - once in the victim network, take steps to achieve goals
        5. **Installation** - install malware, backdoors, and other cyber weapons
        6. **Command and Control (C2)** - communicate with the malware once installed
        7. **Actions on Objectives** - carry out the final objective, such as stealing information or disrupting services
    - MITRE ATT&CK Framework Steps (Adversarial Tactics, Techniques, & Common Knowledge.)
        1. **Reconnaissance** - gather info about the victim from the outside
        2. **Resource Development** - establish resources to use
        3. **Initial Access** - gain access to the victim network
        4. **Execution** - run malicious code
        5. **Persistence** - maintain one's foothold
        6. **Privilege Escalation** - gain higher-level privileges
        7. **Defense Evasion** - avoid being detected
        8. **Credential Access** - steal account credentials
        9. **Discovery** - learn more about the victim's network environment
        10. **Lateral Movement** - move around in the network
        11. **Collection** - gather data of interest for achieving one's goal
        12. **Command and Control (C2)** - communicate from within compromised systems and control them
        13. **Exfiltration** - steal data
        14. **Impact** - manipulate, interrupt, or destroy systems and data
    
    What is a threat - Any circumstance or event with the potential to adversely impact an organization/individual
    
    Vulnerability - Weakness in a piece of software or system
    
    CVE - Common vulnerabilities and exposures
    
    - Types of threats
        
        Spoofing - Impersonating another entity in order to obtain information/access that you are not supposed to have
        
        Phishing - Social engineering attack to get the recipient to do something (usually uses spoofing to achieve phishing)
        
        Man-in-the-middle - Intercepting traffic in order to obtain information. E.g. a keylogger
        
        - DoS/DDoS (Distributed Denial of Service) - Attack that overloads a server with requests therefore denying people who do have authorization to not be able to access the server.
            - Fragment attacks:
                
                Fragment data is transmitted in such a way that the system is not able to put the data fragments back together again
                
                Fragmentation is a normal process in which data is broken down into smaller parts in order to be transmitted over a network
                
                A threat actor can interfere with this process and make it so it can make it impossible for a system to assemble the packets therefor being part of a DDoS attack
                
            - Oversized Packet attacks
                
                Sends a packet that is too large for the system to handle and overwhelm it therefore making the system unavailable
                
        - Remote Code Execution:
            
            Remotely executing Malware on a target system
            
            Threat actor gaining access to a target machine through phishing for example. and will then launch malware remotely
            
            Attackers can also take advantage of software already on the system. This is called living off the land
            
        - SQL injection
            
            Exploits web forms
            
            If the site does not enforce formatting, code can be injected through the forms and the database can be altered in nefarious ways
            
        - Privilege escalation
            
            Bug or flaw that allows higher permission than one should have
            
        
        Virus - malicious software that requires a human to activate it
        
        Worm - Malicious code that can replicate itself
        
        Trojan - Something left behind that can provide future access for an attacker
        
        living off the land - Uses components on a targeted network to their advantage E.g. using an already hacked machine to orchestrate a DDoS attack on another system
        
        Side-Channel Attack - attacker gains information network like measuring eminations from supply current or execution time for something to run
        
- Lesson notes for 2.6 Network Security Infrastructure
    - Tools used to protect networks
        - **IDS** (Intrusion Detection System) - A device or  
            software solution that monitors a network for activity that is known or  
            suspected to be malicious and alerts network defenders about the  
            activity. It does not take any action to respond or prevent the  
            activity. Variations are NIDS (Network IDS) and HIDS (Host IDS).  
            
        - **IPS** (Intrusion Protection System) - A device or  
            software solution that monitors a network for suspected or known  
            malicious activity and actually takes action to prevent it or stop it.  
            This feature of taking action to prevent the activity is what  
            differentiates an IPS from an IDS. Variations are NIPS (Network IPS) and HIPS (Host IPS).  
            
        - **SIEM** (Security Information and Event Management) - A tool used to combine security information and event management in a way that allows analysts and network managers to more easily monitor it and make sense of it. A SIEM typically centralizes logs or pulls in already centralized logs from many sources so that they are consolidated and  
            searchable for network defenders to visualize and analyze.  
            
        - **EDR** (Endpoint Detection & Response) - A  
            solution that monitors end-user devices for malware and responds to  
            prevent or stop it. We've talked a few times about endpoint devices and  
            how they can be especially vulnerable. This solution is meant to help  
            mitigate endpoint security issues.  
            
        - **SOAR** (Security Orchestration Automation &  
            Response) - A solution that is typically made up of a collection of  
            tools that automatically handle security operation tasks, like scanning  
            for vulnerabilities and responding to incidents. This type of tool  
            automates tasks that network defenders might normally do in response to a threat or incident. With automation of this sort, network defenders can be freed up to do other work and more quickly respond to incidents that get past normal defenses.  
            
        - **Honeypot** - A system (e.g., a web server) or system  
            resource (e.g., a file on a server) that is designed to be attractive to potential hackers and intruders, like honey is attractive to bears.  
            _The idea is to put a honeypot out to attract an adversary and confirm  
            whether that adversary is trying to target you. It can also provide  
            valuable intelligence about how that adversary behaves in relation to  
            the target.  
            _
    - How to build a secure network infrastructure
        
        Take inventory of your network
        
        - Defense-in-depth:
            
            Multiple authentication points
            
            Zero Trust: trust no one, verify everyone
            
        - Segmentation: break network into segments that are easier to secure
            
            E.g. A DMZ usually consists of a web server and a mail server which has a firewall to connect to the enterprise LAN
            
            and a firewall to connect to the internet
            
              
            
        
        VLAN - a logical subset of a physical LAN that designates certain nodes within that LAN to be on their own separate VLAN
        
        VPN - Encrypts your internet traffic and provides a more secure environment.
        
          
        
        - Cloud Service Models
            
            SaaS - Software as a Service - the provider provides almost all aspects of the infrastructure and applications
            
            PaaS - Platform as a Service - The provider provides infrastructure and the OS
            
            IaaS - Infrastructure as a Service - The provider only provides the infrastructure
            
              
            
- Lesson notes for 3.1 What is Security Control
    - What is a security control?
        
        A Control = something that affects the outcome
        
        Security controls - protect the C-I-A of a system
        
        reduce risk
        
        cost vs. impact
        
        Detective, corrective or preventive
        
        control frameworks help us ensure we’re following best practices
        
    - types of controls
        - physical - locks, physical barriers
            
            physical barriers e.g. fences and etc.
            
            Guards
            
            CCTV
            
            Alarm systems
            
            Crime prevention through elemental design
            
        - Logical/Technical - passwords, firewalls
            
            Passwords and password policy enforcement
            
            endpoint security; vulnerability scanning
            
            can affect performance and slow things down
            
            assess these controls at least annually
            
        - Administrative - directives, regulations and even training
            
            Control behaviour
            
            policies - what and why
            
            procedures - How
            
            guidlines - recommendations
            
            standards- Must do
            
        - SETA - Securty Education, Training and Awareness
            
            everyone is responsible for security.
            
            clean desk policy is good because it prevents visitors from seeing sensitive information that may just be laying on the desk.
            
            propper procedure when disposing of information e.g. shredding documents
            
            Strong passwords and changing passwords regularly
            
            proper rules for attachments in emails and how to encrypt said attachments
            
            beware of suspicious emails/texts
            
              
            
              
            
        - More Security Control Terminoligies
            
            Principle of least privilege - give the end user minimum resources and authorizations for them to perform their functions
            
            the need to know - give the recipient access only to the information that they need in order for them to function
            
            segregation of duties - requiring more than one person to complete a task ensures that it is more difficult for there to be fraudulent activities because now there is accountability
            
            Dual Controls - Similar to above where two or more people are required to perform an action
            
            Man trap - physical control requires people to pass through two doors with only one being open at a time
            
- Lesson notes for 3.2 Access Management
    
    User provisioning - allowing a user to access what they need and not more than that e.g., there is no reason a cashier would need to install software on a computer and etc.
    
    - Key Access Concepts
        
        Identification - asserting an identity and having it confirmed.
        
        Authentication - Verifying a user is who they say they are.
        
        Authorization - validating the identity being claimed by the user is known to the system and verifying what the user has access to.
        
    - Ways of managing access control
        
        MFA
        
        Non-Repudiation
        
        PII (Personal Identifiable Information)
        
    - Access Control Modules
        
        DAC - Discretionary Access Control
        
        MAC - Mandatory Access Control
        
        RBAC - Role-based Access Control
        
        Access Control Lists - Text file that list who is allowed or denied
        
    
    - **User Life Cycle Management** - This concept is associated with all the practices related to creating, maintaining, disabling, and deleting a user account. When a new employee joins an organization, administrators will create the account and onboard the new user. They may use a "baseline account" to set the user up and then apply any changes to that user's access that are commensurate with the user's role. If the user changes to a new position, the administrator may need to modify the account and its access. If the user takes a temporary leave of access, the admin will likely need to temporarily disable the account. And, finally, when the user has a separation of employment, the admin will need to delete and "offboard" the account. Administrators have a lot of responsibility when it comes to ensure that this life cycle is handled in the most secure and meticulous way.
    - **User Life Cycle Risks** - Risks associated with not managing the user life cycle properly include inadvertently allowing for privilege creep, such as if a user required greater privileges for one role, but then transfers to another role, and the admin fails to remove those privileges. Another risk could be that the administrator fails to deprovision a user when that user goes on a temporary leave or separates from the organization.
    - **Privileged Access Management (PAM)** - Properly managing privileged access is another major responsibility for administrators. Privileged users require admin-level accounts that need to be highly protected; however, with PAM, the need to use those privileges can be limited so that administrators only use them when needed. This process reduces risk and reduces the chances that a threat actor will be able to obtain privileged access. This is also known as "reducing the attack surface" by limiting the opportunities a threat actor has to exploit the system and gain greater access.
    - **Insider Threat** - The threat that an insider will use her/his authorized access, wittingly or unwittingly, to do harm to the security of organizational operations and assets, individuals, other organizations, and the Nation. _This is an important threat to keep in mind when performing access management and one that is often overlooked._
- Lesson notes for 3.3 Control Frameworks
    - What is a control framework
        
        A set of standards and guidelines
        
        Shows your clients that your systems and processes are secure
        
        some are mandated in particular industries
        
        orgs get certified through an audit process
        
    - Control Frameworks
        
        ISO27001 - International Standards Organization
        
        COBIT (and RISK IT) - Control Objectives in IT
        
        NIST SP 800-53 - National institute for Science and Technology
        
- Lesson notes for 4.1 Data handling practices
    
    Indicators of Compromise (IOCs)
    
    - SIEM Tools
        - Splunk - This is probably one of the most popular SIEM tools available. It can also be expensive, but as of early 2022, they offer a free trial version for a limited time, if you want to check it out.
        - Elastik (EKL Stack) - Elastic offers a free version of its SIEM tool, which is also commonly referred to as the ELK Stack, as it is made up of three components: Elastic, Logstash, and Kibana. Cybrary features this SIEM tool in the labs for its Threat Actor Campaign series of courses.
        - Sumo Logic - This SIEM tool was ranked as a "visionary" in Gartner Research's 2021 "Magic Quadrant for Security Information Event Management (SIEM)" report. It also has a free version that you can try out.
        - LogRhythm - This SIEM tool has been ranked as a "leader" in the aforementioned Gartner Research report. As of mid-2022, it did not appear to have a free trial version available.
    - information is an asset that needs to be protected. To do that we must categorize and classify it. It has its own life cycle from created to used to stored.
        - classification
            
            Enables admins to grant access based on classification lvl and need to know
            
            reflects value and handling rules for the data
            
            involves labeling things appropriately
            
            must be consistent
            
            Should suit needs of org
            
        - Data retention and destruction
            - should have policies on data retention
                
                how to store? encrypted?
                
                How long to retain?
                
                How to properly destroy it?
                
            - may be driven by regulations
                
                geography - do you need to account for general data protection regulation
                
                health do you need to account for health insurance portability and accountability act
                
                privacy
                
                financial - do you need to account for PCI DSS (how we protect credit card info)
                
            - Logging - huge in CyberSecurity
                
                What to log
                
                storage needed
                
                how to keep logs
                
                how long before logs get overwritten
                
                do not rely on defaults
                
                centralized logging has benefits like making storage, protection and destruction easier to manage
                
                Logs need to be monitored
                
                Centralized
                
                - Automated monitoring e.g. a SIEM - Security information and event management
                    
                    Correlated logs and identifies anomalies
                    
                    helps seen the signal through the noise
                    
                
                  
                
- Lesson notes for 4.2 Encryption and Cryptography
    
    - Cryptography - The discipline that embodies the principles, means, and methods for the transformation of data in order to hide their semantic content, prevent their unauthorized use, or prevent their undetected modification.
    - Plaintext - Intelligible data that has meaning and can be understood without the application of decryption. _In other words, this is typically the original message without any encryption applied to it._
    - Ciphertext - Encrypted (enciphered) data. _In other words, this is the message after encryption has been applied to it._
    - Encryption - Any procedure used in cryptography to convert plaintext into ciphertext to prevent anyone but the intended recipient from reading that data.
    
    - Encryption Today
        
        Data encryption standard (DES) = 56bit key
        
        Advanced Encryption Standard (AES current standard) = 128, 192 and 256-bit keys
        
        - Symmetric Encryption
            
            Same key used for encryption and decryption
            
            Pro: it’s fast
            
            Con: hard to securely share key, not scalable
            
            AES is a form of this
            
        - Asymmetric Encryption
            
            Two keys: public & private
            
            One person uses a public key to encrypt and another uses a private key to decrypt
            
            Private key is not shared
            
            public & private keys are mathematically linked
            
            Overcomes key distro problems
            
            scalable
            
            pub keys are shared via directories and certificates
            
            E.g. algorithms: RSA (Rivest, Shamir and adleman), Diffie Hellman
            
        - PKI (Public Key Infrastructure)
            
            Provides system for sharing keys
            
            Involves use of digital certificates and certificate authorities - which issue the certificates. Secure sites will have certs
            
            PKI facilities secure transfer of info when rigorous proof is needed to identify parties involved
            
              
            
        - Hashing
            
            numeric representation of a file
            
            like a fingerprint for a file
            
            input is the file
            
            output is unique, fixed-length representation called a “diggest”
            
            input will always have the same output if using the same hashing algorithm
            
            seemingly random
            
            nonreversible
            
            when you want to ensure the file you have is the file you expected
            
            when you want to make sure the file is the same without opening it
            
              
            
        - CIA Triad implication
            
            Encryption protects CONFIDENTIALITY
            
            Hashing protects INTEGRITY and CONFIDENTIALITY
            
            since it’s a one way operation. if someone gets you hash they have no way to decrypt it
            
            When you protect data at the highest level you’ll want to encrypt it with symmetric encryption and encrypt at res, in storage and in transit
            
              
            
        
        To provide for this validation, there is a whole system involved with  
        the issuance of a person's (or entity's) public key. Something called a  
        **Certificate Authority**  
        (CA) is trusted to issue public keys to people or entities that are  
        referred to in this case as "subscribers." The keys are issued as part  
        of what is called a  
        **Digital Certificate**. The Digital  
        Certificate contains the identity of the issuing authority (the CA), the  
        identity of the subscriber, the period during which the certificate is  
        valid, and the subscriber's public key. As I suggested, these  
        certificates are not only issued to people, but also to entities like  
        applications and devices. Networks can use the digital certificates  
        issued to applications or devices to ensure that only trusted entities  
        connect to the network. Certain web sites also require digital  
        certificates in order for you to interact with them.  
        
- Lesson notes for 5.1 Incident response
    
    Incident Response (IR), Business Continuity (BC), and Disaster Recovery (DR)
    
    - IT terms
        
        Incident - when C-I-A of a system is jeopardized
        
        Response - incident has occurred, how you react according to response plan
        
        Vulnerability - weakness in system that can be exploited
        
        Zero Day - vulnerability that is exploited that has not been previously recognized or registered; we are likely unprepared for it
        
        Threat Actor - someone is trying to cause disruption, destruction or theft
        
    - CIRT
        
        Senior Manager
        
        Incident Manager > Incident Responders
        
        Technical Leads
        
        Security Team
        
        Comms/PR Team
        
        Legal/HR
        
    - Incident response life-cycle
        
        prepare
        
        detect/analyze
        
        contain/recover
        
        post-incident activity → prepare
        
    - IR Comms
        
        Single stream of info
        
        Internal comms - very direct
        
        external comms - driven by PR
        
        - must consider
            
            Customers
            
            Supply chain
            
            shareholders
            
            regulators
            
        
        Must continue to give updates - even if nothing is new
        
          
        
    - IR Plan
        
        Training must occur
        
        table top exercises are inexpensive and effective
        
        Links to BC & DR
        
        need to know when to invoke plan and when to escalate > when to call CEO in the middle of the night
        
- Lesson notes for 5.2 Business Continuity
    
    Business impact analysis > recover strategies > Plan Development > testing and exercises
    
    - Types of Events - What types of events would most  
        disrupt the business? Consider damage to facilities, supply chain  
        disruptions, system outages, loss of personnel, etc.  
        
    - Types of Impact - Given the various event  
        scenarios, what would be the impact? How would the organization be  
        affected financially? What would be the effect on the organization's  
        reputation? What are the regulatory implications?  
        
    - Timing and Duration - What would be the worst time  
        and/or length of time for an event to occur and how would that impact  
        the business? For example, a retail store would be severely affected if  
        an event were to coincide with a major holiday shopping period. Or, for  
        an airline, the temporary grounding of an aircraft type will have a  
        greater impact the longer the aircraft are not able to fly.  
        Organizations should consider the worst-case scenario and determine how  
        they would react. Would they be ready to react?  
        
    
    - Why is BC so important?
        
        BC is about continuing to run the business after an incident is dealt with
        
        - Vital elements
            
            Legal
            
            IT
            
            Security
            
        
        If in a highly regulated industry - you probably have special concerns to follow up on
        
        orgs ability to continue during incident may make or break the business
        
        - What is a BC Plan?
            
            Steps needed to sustain the business during an incident
            
            - Describes
                
                Who is involved
                
                What needs protecting
                
                When to invoke the plan
                
            
            It should invoke the Business Impact Analyses (BIAs)
            
            it should specify how back-ups are created
            
            it should be tested so everyone knows what to do in a real-life situation
            
        - What happens when you invoke the plan
            
            Comms across the business - what needs to happen
            
            specify alternate sites
            
            specify means of communication
            
            ensure vpn and other security measures are available
            
            provide updates even if nothing has changed
            
        
        the infrastructure and processes to back up critical data and fail-over  
        to another system if one system goes down should be in place  
        _before_ an incident occurs.
        
- Lesson notes for 5.3 Disaster Recovery
    
    - Recovery Time Objective (RTO) - This is the maximum amount of time that the organization has assessed that it can afford to wait for IT systems to come back online after a disaster strikes.  
        Another way of looking at this is that it is the amount of time in which you need to restore systems after a disaster in order to avoid an  
        unacceptable situation for the business.  
        
    - Recovery Point Objective (RPO) - This is the  
        maximum amount of data that the organization can afford to lose in a  
        disaster before it becomes severely damaging to the business. Another  
        way of looking at this is that it relates to how often you should create backups of your data because if a disaster should hit between backups,  
        this would be the amount of data you would lose. Perhaps your backups  
        are created every five hours. If you were to lose five hours of data,  
        would that be acceptable for your business or would that be too great of a loss? When you are planning for a disaster, you need to assess this  
        and make changes to your backup processes accordingly.  
        
    
    - How is DR different
        
        the other two are immediate reactions
        
        DR happens when a disruption causes long-term effects and serious damage and you have to totally rebuild or replace some part of your system or business
        
    - what is a DR plan
        
        Similar to a BC plan
        
        - describes
            
            Who is involved
            
            what needs to be done
            
            when to invoke the plan
            
        
        Information about how systems are built and should be re-built if needed
        
        if backups are available - how do you access
        
        it should be tested - so everyone knows what to do in real-life situations
        
          
        
    - Types of Events
        
        Cyber Incident - Ransomware
        
        Hurricane/Earthquake
        
        9/11-type attack; planes grounded; people stranded
        
        pandemic
        
    - what happens when you invoke the plan
        
        Alternate communications
        
        alternate sites
        
        alternate power sources and backups
        
        might need to house people and transport
        
        provide updates even if nothing has changed
        
    
    basic tool that can be critical for a DR Plan is a call tree. This is a  
    list of whom to contact, and in what order, when a disaster occurs.  
    
- Lesson notes for 6.1 Governance
    
    This is a whole sub-field within the field of cybersecurity. If you think you would enjoy defining, reviewing, and implementing security policies or delving into the expansive area of risk management, or auditing organizations to see if they are in compliance with standards, policies, and regulations.
    
    legal or legislation - where we must abide by the law
    
    corporate governance - where we must abide by our industry's standards and policies
    
    - Governance - How the organization manages, protects and makes decisions about information security.
        
        Standards - the quality and assurance criteria we strive for
        
        Policies - the what and why - dictated by leadership
        
        Procedures - the how - dictated by business laws
        
        Regulations - the rules dictated by laws
        
    - Governance, risk management and compliance are all intertwined
- Lesson notes for 6.2 Risk Management
    
    An organization faces many risks, such as disruptions to productivity, loss of revenue, a data breach, or damage to one's reputation. With so much of our business happening in a digital context today, cybersecurity risks have become a major focus in risk management.
    
    - Risk management Terms
        
        Risk appetite/tolerance - The amount of risk you’re willing to take
        
        Residual Risk - the risk left over after you apply controls
        
        - Risk Assessment - You evaluate your assets and determine their worth relative to the risks that might affect them.
            
            How much should you invest in protecting them?
            
            there are various formulas that are used in risk management to assess risk and the likelihood of risk
            
              
            
        - Risk Responses
            
            Accept
            
            Avoid
            
            Reduce/mitigate > Firewalls, IDS, IPS, SOC
            
            Share/Transfer > Insurance, Cloud architecture
            
- Lesson notes for 6.3 Compliance
    
    Compliance is a fairly involved concept in my mind. On  
    the surface, it is just about an organization's adherence to the various  
    laws, standards, regulations, and policies it is required to follow. On  
    the other hand, it also invokes the ideas of being transparent about  
    whether you follow these things, as well as proving that you follow  
    these things  
    
    - Some laws I need to be familiar with
        - Family Educational Rights and Privacy Act (FERPA) - This act regulates the handling and privacy of student education records.
        - General Data Protection Regulation (GDPR) - This  
            regulation governs data protection and privacy for people in the  
            European Union (EU). Importantly, it applies to any company that handles the protected data of people who are in the EU, even if the company  
            itself is not located in the EU.  
            
        - Gramm-Leach-Bliley Act (GLBA) - This act applies to financial institutions and regulates the privacy of customer financial information.
        - Health Insurance Portability and Accountability Act (HIPAA) - This act regulates the handling and privacy of protected health information.
        - ISO/IEC 27001 - This standard specifies how organizations should manage information security.
        - Payment Card Industry Data Security Standard (PCI DSS) - This standard applies to any organization that handles branded credit cards. If you use credit cards, you benefit from the protection this  
            standard provides to ensure your cardholder data is securely processed,  
            stored, and transmitted by retailers and other merchants.  
            
        - Sarbanes-Oxley Act (SOX) - This act applies to any publicly traded company and regulates the financial reporting activities of such companies.
    - What is compliance
        
        Adhering to standards
        
        Follow rules & the law
        
        Working within regulations
        
        Enforcing policies
        
        Being transparent
        
        Proving that you are compliant
        
    - Roles & Certs in Compliance
        
        - Main Roles
            
            Auditor
            
            Compliance Officer/advisor
            
            Compliance project manager
            
        
        Certified Information Systems Auditor (CISA)
        
        Certified in Risk and Information Systems Control (CRISC)
        
        Certified Information Privacy Professional (CIPP)
        
        Certified in the Governance of Enterprise IT (CGEIT)