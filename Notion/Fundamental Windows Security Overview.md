- Intro To windows Security
    - MBSA (Microsoft baseline security analyzer)
        
        verifies patch compliance
        
        No longer supported in current os’s
        
    - Windows Security Infrastructure
        
        Misconfigurations
        
        Files Shares
        
        Best Practices
        
        EMET
        
        Windows Defender
        
    - microsoft enhanced mitigation experience
        
        free
        
        works with any software
        
        works with all os’s (after vita
        
        - 12 specific mitigation techniques
            
            Prevents memory corruption
            
            data execution prevention
            
            mandatory address space layout randomization (makes it difficult to find the addresses of data in memory)
            
            structure exception handler override protection
            
            export address table access filtering
            
            anti-return or init programming
            
              
            
        - hardening windows OS
            
            upgrade to supported version
            
            Regularly patch
            
            scan for open shares
            
            follow best practices
            
        - windows defender
            
            windows 8+
            
            free
            
            real time protection
            
            signature with machine learning and behavior monitoring
            
- Windows Firewall
    
    First line of defense
    
    filters network traffic
    
    blocks harmful traffic
    
    acts like a typical firewall on host machines with basic features
    
    can see ports that protoccols are running on
    
    create own rules
    
      
    
- MBSA
    
    I got run through the install process
    
    can scan computer in network or local machine
    
    review scan report
    
    just scans for vulnerabilities
    
    tells you how to fix the issues that it does find
    
      
    
- EMET (enhanced mitigation experience toolkit)
    
    ran through the download and install
    
    protect third party apps in memory that cannot be patched
    
- IP security
    
    secure networking protocols and services
    
    Used in VPNs
    
    - Securing IIS
        
        Uninstall unneeded IIS modules
        
        Audit users and groups
        
        HTTP Request Filtering
        
        Dynamic IP restrictions
        
        Isolate web apps
        
        Patch!
        
    - Securing RDP
        
        Restrict user account access
        
        Patch!
        
        Restrict access using firewalls
        
        Enable NLA
        
        Set account lockout policy and password policy
        
        change default listening port
        
        disable where it’s not needed
        
        port: 3389