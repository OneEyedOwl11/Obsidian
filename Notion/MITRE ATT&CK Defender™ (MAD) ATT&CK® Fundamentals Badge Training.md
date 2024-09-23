**Adversarial Tactics, Techniques, and Common Knowledge**

- 1.1 Introduction to ATT&CK
    
    What will they do after they get into our network
    
    ability to observe and adapt to threats
    
    - ATT&CK
        
        knowledge base of adversary behaviours
        
        based on real-world observations
        
        free, open, and globally accessible
        
        community contribution driven
        
    - Summiting the pyramid
        
        TTP’s - tough
        
        tools - challenging
        
        network/host artifacts - annoying
        
        domain names - simple
        
        IP - addresses - easy
        
        hash values - trivial
        
    - TTP
        
        tactics
        
        techniques
        
        sub-techniques
        
        procedures
        
- 1.3 Tactics
    
    objectives of the attacker
    
    look at the ID of the tactic in lesson above
    
- 1.2 Matrices and Platforms
    
    |   |   |   |
    |---|---|---|
    |ID|Name|Description|
    |[TA0043](https://attack.mitre.org/tactics/TA0043)|[Reconnaissance](https://attack.mitre.org/tactics/TA0043)|The adversary is trying to gather information they can use to plan future operations.|
    |[TA0042](https://attack.mitre.org/tactics/TA0042)|[Resource Development](https://attack.mitre.org/tactics/TA0042)|The adversary is trying to establish resources they can use to support operations.|
    |[TA0001](https://attack.mitre.org/tactics/TA0001)|[Initial Access](https://attack.mitre.org/tactics/TA0001)|The adversary is trying to get into your network.|
    |[TA0002](https://attack.mitre.org/tactics/TA0002)|[Execution](https://attack.mitre.org/tactics/TA0002)|The adversary is trying to run malicious code.|
    |[TA0003](https://attack.mitre.org/tactics/TA0003)|[Persistence](https://attack.mitre.org/tactics/TA0003)|The adversary is trying to maintain their foothold.|
    |[TA0004](https://attack.mitre.org/tactics/TA0004)|[Privilege Escalation](https://attack.mitre.org/tactics/TA0004)|The adversary is trying to gain higher-level permissions.|
    |[TA0005](https://attack.mitre.org/tactics/TA0005)|[Defense Evasion](https://attack.mitre.org/tactics/TA0005)|The adversary is trying to avoid being detected.|
    |[TA0006](https://attack.mitre.org/tactics/TA0006)|[Credential Access](https://attack.mitre.org/tactics/TA0006)|The adversary is trying to steal account names and passwords.|
    |[TA0007](https://attack.mitre.org/tactics/TA0007)|[Discovery](https://attack.mitre.org/tactics/TA0007)|The adversary is trying to figure out your environment.|
    |[TA0008](https://attack.mitre.org/tactics/TA0008)|[Lateral Movement](https://attack.mitre.org/tactics/TA0008)|The adversary is trying to move through your environment.|
    |[TA0009](https://attack.mitre.org/tactics/TA0009)|[Collection](https://attack.mitre.org/tactics/TA0009)|The adversary is trying to gather data of interest to their goal.|
    |[TA0011](https://attack.mitre.org/tactics/TA0011)|[Command and Control](https://attack.mitre.org/tactics/TA0011)|The adversary is trying to communicate with compromised systems to control them.|
    |[TA0010](https://attack.mitre.org/tactics/TA0010)|[Exfiltration](https://attack.mitre.org/tactics/TA0010)|The adversary is trying to steal data.|
    |[TA0040](https://attack.mitre.org/tactics/TA0040)|[Impact](https://attack.mitre.org/tactics/TA0040)|The adversary is trying to manipulate, interrupt, or destroy your systems and data.|
    
    overlap and redundancies exist between matrices
    
    adversaries may execute hybrid breaches
    
- 1.4 techniques and sub-techniques
    - techniques
        
        means by which adversaries achieve their tactical goals
        
        how an adversary performs their actions
        
        list of techniques may differ across platforms, but may grow and evolve over time
        
        has unique identifiers
        
        technique T####
        
    - sub-techniques
        
        more specific description of the adversarial behavior used to achieve a goal
        
        describe behavior at a lower level than a technique
        
        sub-techniques have a single technique parent
        
        not always, but often platform specific
        
        designed to help reduce changes to techniques as new variations and platforms are added
        
        sub-technique T####.###(must be under a technique)
        
- 1.5 Mitigations
    
    configurations, tools or processes that we can use to prevent a technique from working or having the desired outcome for an adversary.
    
    intended to allow you to take an action such as changing a policy or deploying a tool
    
    mitigations to techniques are shown next to the techniques on the mitre site and can be further delved into
    
- 1.6 Data sources & detections
    - data sources
        
        source of information collected by a sensor or logging system
        
        used to collect information relevant to identifying adversary actions
        
        where to collect data
        
        data sources also include data components to further define data requirements
        
    - detections
        
        high level analytic process, sensors, data, and detection strategies
        
        useful to identify a technique has been used by an aversary
        
        how to interpret data collection
        
          
        
- 1.7 groups & software
    - Procedures
        
        specific implementation the adversary uses for techniques or subtechniques
        
        populated on a technique page as well as Groups/Software
        
        Describe the group or software entity with a brief description of how the technique is used
        
    - groups
        
        related intrusion activity that are tracked by a common name
        
        some groups have multiple names associated with similar activities
        
    - software
        
        tools or malware used by an adversary during intrusions
        
        some entries have multiple names
        
- 1.8 How ATT&CK grows and evolves
    
    adversaries, malware and their behaviors evolve everyday
    
    techniques, groups, software, etc are designed to be added, deleted and/or enhanced as needed
    
    process for vetting and modifying content
    
    you can access pervious versions of ATT&CK
    
- 2.1 Community Perspective
    
    ATT&CK contributed by global community
    
    MITRE ATT&CK team curates and maintains this knowledge
    
      
    
      
    
- 2.2 Common Language
    
    critical for consistently sharing ideas about adversary behaviours
    
    language is abstracted to an operations-level
    
    common usage: connecting adversary perspective to defensive countermeasures
    
      
    
      
    
- 2.3 Quantitative scorecard
    
    not easy to quantify
    
    vital to track progress and growth
    
    ATT&CK can be used to set up a scorecard
    
    Document priorities
    
    Identify Gaps
    
      
    
- 2.4 ATT&CK Navigator
    
    designed to provide basic navigation of ATT&CK matrices
    
    visualize your defensive coverage, your red/blue team planning, the frequency of detected techniques or anything else you want to do.
    
    manipulate the cells in the matrix (color coding, adding a comment, assigning a numerical value)
    
    - Navigation Layers
        
        Custom Views of the ATT&CK matrix
        
        can be created interactively with Navigator or generated programmatically (JSON)
        
        Layers can also be exported and shared
        
    
    [ATT&CK® Navigator (mitre-attack.github.io)](https://mitre-attack.github.io/attack-navigator/)
    
      
    
- 3.1 Cyber Threat Intelligence
    
    CTI - is about knowing what your adversaries do
    
    critical for improving decision making
    
    ATT&CK is a great starting point
    
- 3.2 Detection & Analytics
    
    Detection software and other Methods can help detect that an attack has become E.g monitoring unexpected processes interacting with LSASS.exe such as mimikatz (Credential Dumping)
    
    Provide defensive suggestions used for detections
    
    highlight variances in how adversaries have executed the target behaviours
    
    explain the technical details of the target behaviour
    
- 3.3 Threat Emulation
    
    Red team mimicking known threats
    
    allows us to operationalize intelligence, scope and prioritize what threats and behaviours we test
    
    observe and evaluate our defenses from the perspective of our adversaries
    
    - Threat-Informed Assessments
        
        github.com/mitre-attack/attack-arsenal
        
        provides measures on how to deal with threats
        
- 3.4 Assessment and Engineering
    
    what risks are most critical to address
    
    what risks can/must we tolerate
    
    building one piece, or informed decision, at a time
    
    assessments using threats will lead us towards necessary enhancements
    
    cumulative, iterative process that never stops
    
    inform us of prioritize and relevant opportunities to improve defensive capabilities
    
- 3.5 Putting it all together into threat-informed defense
    
    Easier when we coordinate, communicate, and work together
    
    Understand and consider our threats in every action or decision
    
    a quantifiable way of understanding, tracking, communicating, and addressing what our threats are doing
    
    we can use this knowledge to gain strategic and operational advantages