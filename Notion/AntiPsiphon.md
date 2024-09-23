- Commands to know on windows cmd
    
    netstat
    
    netview
    
    net use
    
    net session
    
    wmic process get name,parentprocessid,processid
    
    tasklist /svc
    
    tasklist /m
    
    tasklist /ntll.dll
    
    tasklist /m /fi “pid eq [proc_id]”
    
    netstat
    
    - netstat -naob
        
        a: displays all active TCP connections and the TCP and UDP ports that are listening
        
        n: Displays active TCP connections, addresses & port numbers displayed numerically
        
        o: displays active TCP connections and includes process ID
        
        b: displays executable involved in creating each connection or listening port
        
        f: tries to do name resolution
        
    
    netstat -f
    
- commands with linux
    
    - ps aux = `report a snapshot of the current processes`
        - a = Select all processes except both session leaders (see getsid(2)) and processes not associated with a terminal.
        - u = userlist  
            Select by effective user ID (EUID) or name.  
            This selects the processes whose effective user name or ID is in userlist. The effective user ID describes the user whose file access permissions are used by the process (see geteuid(2)). Identical to U and --user.  
            
        - x = Lift the BSD-style "must have a tty" restriction, which is imposed upon the set of all processes when some BSD-style (without "-") options are used or when the ps personality setting is BSD-like. The set of processes selected in this manner is in addition to the set of processes selected by other means. An alternate description is that this option causes ps to list all processes owned by you (same EUID as ps), or to list all processes when used together with the a option.
    
    htop = `display Linux tasks`
    
    mtr = `a network diagnostic tool`traceroute
    
    lsof -i -P = `list open files`
    
    strings = `print the strings of printable characters in files`
    
      
    
- Tools to look at
    
    Wazuh  
    Elastic  
    OPENEDR  
    
    sysmon with swift on security-config.xml
    
    sysmon modular
    
    Security Onion
    
    ZAP - zed attack proxy
    
    W3AF - Automatic web security scanner
    
    Nikto - free web scanner
    
    Burp Pro - crawls a website
    
    Kismet - Wireless Cracking tool
    
    Aircrack ng -
    
    fail2ban
    

AuditScripts - compliance rules

www.auditscripts.com