- 2.1 Threat Modeling
    - threat modeling
        
        approach for analyzing the security of an application
        
        enables you to identify, quantify and address security risks with an app
        
        threat is NOT vulnerability - threats can exist even if there are no vulnerabilities
        
        - Abuse or misuse case
            
            Most requirements are presented in use cases
            
            use cases shows the expected functions of the system
            
            need to consider how functions can be misused or abused
            
            extend standard use case to show threats
            
            misuse case example someone trying to steal a car = Human/Deliberate
            
            misuse case example weather causes car to skid= Environmental/Uncontrolled
            
- 2.2 Threat Modeling Part 2
    
    - application threat model
        
        start with architecture design diagram
        
        identify the assets
        
        identify threats to assets
        
        threat factors (threat actor and vector they would come from)
        
        develop controls to mitigate threats
        
        ![[Untitled 3.png|Untitled 3.png]]
        
          
        
    - Operational threat model
        
        Big picture view. Prioritizes infrastructure risk management
        
        [http://mozilla.github.io/seasponge/#/](http://mozilla.github.io/seasponge/#/) ← threat model software
        
    - Data Flow Threat model
        
        [Threatdragon.org](http://Threatdragon.org) draw out threats on dataflow
        
    
    threat modeler tool
    
- 2.3 Threat Modeling Part 3
    
    - STRIDE model to categorize threats (More advanced is the MITRE attack framework)
        
        spoofing, tampering, repudiation (doing something without knowing who did it), information disclosure, DoS, Elevation of Privilege
        
    - DREAD is a threat prioritization model
        
        Damage Potential, Reproducibility, Exploitability (time and effort), Affected Users, Discoverability
        
    - Environmental threat modeling
        
        Used when deciding the new location of a data center
        
        risks are environmental
        
    - Social threat modeling
        
        Identify targets for social engineering attacks
        
        phishing and etc
        
        identify the goal, medium, social engineer, target, compliance principles and techniques
        
    - how to start
        
        get architecture artefacts from development team
        
        boundary diagram
        
        dataflow diagram
        
        OWASP threat modelling guide
        
        use the free tools suggested
        
    - threat model document
        
        basic info - name, owner
        
        Dependencies - any external system that is needed
        
        entry points - what pages, protocols, API’s, FTP?
        
        assets - what are you protecting
        
        countermeasures - mitigation
        
    
      
    
- 3.1 2 and 3 Enterprise Security Areas Part 1
    - Network Security
        
        most fundamental security area to address
        
        not just firewall
        
        policies to prevent DoS, misuse, modification and monitor unauthorized access
        
        about securing communication between endpoints
        
        - threats
            
            Wireless attacks are common
            
            weak protocols Telnet, HTTP, wiretapping, port scanning, traffic analysis and information gathering and etc
            
            MAC address spoofing
            
        - Tools
            
            firewalls, IPS, network access control, Netflow capture, packet capture, Logs, Logs analysis, Network Visibility tools
            
    - Application Security
        
        hardening of an application to prevent exploits
        
        not just code scanning
        
        also depends on platform security
        
        consider configuration security and logging
        
        - threats
            
            weak key management
            
            information disclosure
            
            plain text comms & storage of credentials
            
            cross-site scripting
            
            sql injection
            
            brute force attack
            
            man-in-the-middle
            
            session replay
            
        - tools
            
            white box scan
            
            peer review
            
            tracing function to requirements
            
            black box scan
            
            pen tests
            
            app firewalls
            
            load testing
            
            performance testing
            
            dependent systems
            
            DB activity monitoring
            
            Limit access channels
            
            config management isolation
            
            Cgroups
            
            Seccomp
            
            fuzz testing
            
    - Endpoint Security
        
        Covers end devices of a system
        
        usually concern with computers & servers
        
        most difficult area to control
        
        - threats
            
            virus
            
            ransomwares
            
            APT (Advanced persistent threat)
            
            Keyloggers
            
            phishing
            
        - tools
            
            Anti Virus
            
            app whitelisting
            
            device whitelisting
            
            Signature based EDR
            
            Data loss prevention
            
            Deep learning EDR
            
    - ID & Access management
        
          
        
        Covers authentication and authorization
        
        how we manage privileged users
        
        identify
        
        authenticate
        
        authorize
        
        audit
        
        ![[Untitled 1 3.png|Untitled 1 3.png]]
        
        ![[Untitled 2 3.png|Untitled 2 3.png]]
        
        - threats
            
            Spoofing
            
            Identity theft
            
            Keylogging
            
            escalation of privilege
            
            information leaked
            
        - Tools
            
            identity manager
            
            fraud analytics
            
            provisioning
            
            MFA
            
            single sign on
            
            Privileged access management
            
            behaviour analytics
            
            role based approach
            
    - Data Protection
        
        covers collection, storage and sharing of data
        
        consider regulations
        
        what can admins see
        
        who admins the admins
        
        what if admins account is compromised
        
        how to reduce or limit damage
        
        - threats
            
            Compliance to laws of location
            
            Data encryption
            
            Privileged user access
            
            right to erasure
            
            data portability
            
        - tools
            
            distributed ledger tech
            
            anonymizer
            
            standard encryption
            
            homomorphic encryption
            
            multi-party trust computation
            
            database monitoring and prevention
            
    - Vulnerability & Patch Management
        - Vulnerability Management
            
            is the “practice of identifying, classifying, remediating and mitigating vulnerabilities
            
            Includes VA (vulnerability assessment) testing
            
            includes “zero-day” or vulnerabilities found “in the wild”
            
        - Patch management
            
            covers reviewing and applying patches to systems
            
            Needs to cover assessment (of need), testing, deployment and roll-back
            
        - Threats
            
            Zero-Day
            
            Workarounds
            
            ---
            
            Testing
            
            Patch Failure
            
        - Tools & Techniques
            
            Intel Feeds
            
            Validation Environment
            
            Good Communication Plan
            
            ---
            
            Multiple Environment
            
            Realistic Test Data
            
            Roll Back Procedures
            
            Snapshot Technologies
            
            virtual patching
            
    - Availability
        - High Availability
            
            is the concern with uptime
            
            is usually within the same environment as primary system
            
            targets affects system design for patch management
            
        - Disaster Recovery
            
            is about business continuity
            
            is usually a secondary site
            
            affects design based on RTO/RPO
            
            Plans greatly dependant on network bandwidth
            
        - Threats
            
            Application crash
            
            Load Beyond capacity
            
            misconfiguration
            
            equipment failure
            
            ---
            
            site destroyed
            
            large scale and prolonged power outage
            
        - Tools & techniques
            
            Load Balancer
            
            Stateless design
            
            Reliable messaging
            
            Redundancy for everything
            
            ---
            
            Snapshots
            
            Log replay
            
            2 phase commit
            
    - Supply Chain Security
        
        Covers the upstream and downstream effects of components in a system (e.g. cpu vulnerability that intel cpu’s had that were on a hardware level and nothing an IT specialist could do would mitigate it except for migrating the whole business to a new chip manufacturer)
        
        is sometimes hard to manage in the current it landscape
        
        - threats
            
            Open Sourced libraries (OpenSSL)
            
            Hardware components (Meltdown/spectre)
            
            Shared library
            
            common tools
            
            compiler
            
        - tools & techniques
            
            alternative source
            
            update/upgrade plans
            
            plan for worst case IR
            
            Intel feeds
            
        
          
        
- 4.1 Other Enterprise Security Areas Part 1
    - Cloud security
        
        Not just technology
        
        Needs processes, controls and policies.
        
        needs configuration security and logging
        
        [Cloud Security | NIST](https://www.nist.gov/itl/smallbusinesscyber/guidance-topic/cloud-security)
        
        - Customer responsibilities
            
            Apps and data
            
            network config & security
            
            ID & Access management
            
            System and platform config
            
            Data Security
            
        - Provider responsibilities
            
            Virtualization Platform
            
            Network infrastructure
            
            Physical Infrastructure
            
        - Common issues
            
            still vendor specific security stack
            
            lack of control of tech
            
            misconfiguration issues
            
            contracts are not easy to fit into models
            
        - Threats
            
            insecure APIs
            
            Supply chain weakness
            
            DDoS (both ways)
            
            APT
            
            Data leaks
            
            Data contamination
            
            Unauthorized access
            
        - Tools and tech
            
            workout IR process with vendor
            
            Check and recheck
            
            config
            
            MFA
            
            Check vendor DR
            
            Cloud Access Security Broker
            
        - consider
            
            log frequency and timelines
            
            privileged user access
            
            secrets/keys management
            
        
          
        
- 4.2 Other Enterprise Security Areas Part 2
    - Mobile
        - Issues
            
            Too many variations of mobile devices
            
            app explosion
            
            mixed personal with business environment
            
            Many threats now focus on a mobile first appraoch
            
        - threats
            
            malware
            
            data theft
            
            identity theft
            
            eavesdropping
            
        - tools and tech
            
            mobile device management
            
            mobile app management
            
            sandboxing
            
            self-destruction of data
            
    - Data center
        - threats
            
            cable tapping
            
            power outage
            
            communication outage
            
            fire/humidity
            
            Unauthorized access
            
            social engineering
            
        - tools and tech
            
            location
            
            utilities
            
            fire suppression
            
            temperature and humidity
            
            multiple access gates
            
            MFA
            
            lights off operations
            
            secure walls and cables
            
            recorded stations
            
- 4.3 Other Enterprise Security Areas Part 3
    
    IoT security covers protection of sensors and tampering with its information
    
    - Threats
        
        Consumer centric
        
        Lack of security considerations in many products
        
        too much variance
        
        support for protocol not uniformed
        
    - tools and tech
        
        tech to sign devices (e.g. micro certificates)
        
        implementation checks (micro pen test)
        
        highly scalable vpn (e.g. cisco GETVPN)
        
        Securing transport like MQTT
        
    
    managed security services usually heavy on network and less on applications
    
    mostly covers perimeter
    
    contracts and SLA have to be managed carefully
    
    - threats
        
        scope of coverage
        
        conttractual obligations
        
        SLA management
        
        on site management
        
    - tools and tech
        
        technical internal 2nd level defense
        
        contractual protection - SLA, audits
        
        partnership - co-sourcing
        
- 5.1 Cybersecurity Process Part 1
    
    you cannot architect a solution without thinking of the people maintaining it
    
    beware of the process required to keep it running
    
    - incident response
        
        NIST
        
        CERT  
        ISACA  
        ISO/IEC 270035  
        
        incidents need to be managed
        
        systems must be designed to support orgs ability to respond to security incidents
        
        as an architect, do not forget to get the requirements from security operational team
        
        - considerations
            
            can the incident responder rebuild the steps up to the incident?
            
            can you provide all the necessary evidence for investigation?
            
            how would forensics image be taken
            
            is the log format easily parsed
            
            vmware image vs aws image
            
            syslog vs local log directory
            
            longevity of log retention
            
            time synchronized across all systems
            
            encryption/decryption points
            
    - Auditing & reporting
        
        every company has some audit and compliance team
        
        make sure their input is also collected when architecting a solution
        
        - considerations
            
            is there a corporate dashboard you have to pipe information to?
            
            are you in a highly regulated industry? what are the regulatory requirements
            
            what are the audit requirements for your org
            
            is it easy to pull ad-hoc for security events
            
            log retention period to meet audit requirements
            
            able to pipe metrics to dashboard
            
            ad-hoc reporting comparing to SOC
            
              
            
- 5.2 Cybersecurity Process Part 2
    - Risk management
        
        As with Audit & Compliance, Risk management is an important function
        
        Risk is never static
        
        an important part of this is knowing where the risks are
        
        Not to be a risk expert but to recognize that it is an important role in being the architect
        
        - RM Phases
            
            Risk Assessment - identify assets, threats, vulnerabilities
            
            Risk analysis - impact of risk to assets
            
            Risk mitigation - how to deal with risk
            
            risk monitoring - goes on forever
            
        - Risk Assessment
            
            Many frameworks: OCTAVE, FRAP, NIST 800-30, etc
            
            Qualitative & Quantitative risk analysis
            
            Get familiar with the standard in your organization
            
            Even the best secure system will have some residual risk
            
        - Classification of risk
            - Risk Control
                
                Administrative
                
                Technical
                
                Physical
                
            - Risk treatment
                
                Preventive
                
                Detective
                
                Corrective
                
                Compensating
                
        - Residual Risk & Mitigation
            
            Risks expected to remain after planned response of risk has been taken - acceptable risk (no reasonable response)
            
            - mitigation classification
                
                Reduce
                
                accept
                
                transfer
                
                avoidance
                
                rejection
                
- 6.1 Architecture Documentation Part 1
    
    - Why document
        
        Create architecture
        
        Evaluate the architecture
        
        refine, update and refactor
        
        use architecture to guide implementation
        
        Enforce architecture during implementation
        
    
    communicate reasons behind decision
    
    need to cover perspective for the difference in audience - Process, Operation, Data flow
    
    Helps in future re-engineering projects
    
    helps to catalogue assets that can be reused
    
    - Artefacts
        
        threat models
        
        test cases
        
        system design documents - Technical, Process, deployment
        
        decision documents
        
        compliance checklist
        
    - software example
        
        how is it structured as a set of code units? Module Views
        
        how is it structured as a set of elements that have a runtime presence? Runtime views
        
        how artifacts are organized in the file system and how is the system deployed to hardware? Deployment Views
        
        What is the structure of the data repository? Data Model
        
          
        
- 6.2 Architecture Documentation Part 2
    
    impact non-functional characteristics of a system. Architect needs to document why and how (Thought process on how) he came to they decision that they did.
    
    - decision document
        
        subject area - what is it related to
        
        design decision - what is the decision you have to make
        
        issue or problem statement - explain why a choice has to be made
        
        assumption - list assumptions made when making decision
        
        motivation - what drives the decision
        
        alternatives - list other options considered
        
        decision - what was the decision made
        
        justification - explain decision
        
        implication - explain any side effect
        
        related decision - list other decisions that are related
        
    - put it all together
        
        it is very difficult to managed all these on paper
        
        if you do, make sure you have a good indexing system
        
        invest in an architecture tool to help you manage artifacts and relationships
        
        use standard and formal notation to help communication
        
        create an asset catalog to help reuse - architecture gets easier to use when you have more reusable components
        
        open to feedback - no one knows everything
        
        living doc that must be updated with new info - new technologies, new threats, product obsolescence, etc
        
    - tools
        
        orbus iserver
        
        visual paradigm
        
        unicom