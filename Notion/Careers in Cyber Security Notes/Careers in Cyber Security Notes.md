- Most common type of attack
    
    Password attack. It is easy to do and can be automated and done on various systems at a time
    
    - How to find and prevent this type of attack:
        
        Review log files to find the authentication records
        
        ![[Untitled 4.png|Untitled 4.png]]
        
        1. The date and time of the event
        2. The hostname of the system that recorded the event, in this case the system named “SSH-Server-2”.
        3. Descriptive text stating that the user “jsmith” failed to authenticate because they entered the wrong password.
        4. Descriptive text stating that the source of the failed authentication attempt is the system 172.47.30.1.
        
        Multi-factor Authentication
        
- One of the tasks of a security engineer is to oversee the installation of new apps/extensions in a work environment. For extensions such a way to do this would be to:
    
    Read the privacy practices of the company offering the extension
    
    Read reviews of the extension (Both good and bad)
    
    Check the developer reputation
    
    Use [https://crxcavator.io/](https://crxcavator.io/) or an alternative to see the risk score of the extension and any vulnerabilities to look out for when using it
    
      
    
- Key terms when it comes to risk assessment that Cyber Security Managers/Analysts do when conducting an audit. These terms help to express the level risk and loss that occurs when safeguards are not in place
    
    **Asset Value (AV)**- This means the monetary value an asset is worth.
    
    **Exposure Factor (EF)**- This means the percentage of the assets value that would be lost if a breach or attack happened.
    
    **Single Loss Expectancy (SLE)**- This means the loss from a single incident. (AV x EF)
    
    **Annual Rate of Occurrence (ARO)**- This means the number of times an incident is expected to occur in a year.
    
    **Annual Loss Expectancy (ALE)**- This means the loss that is expected to happen within a year. (SLE x ARO)
    
    **Safeguard Value (SV)**- This means the cost of a control  
    that will be used to mitigate risk. SV is (ALE before implementing safe  
    guard) - (ALE after implementing safeguard) - (Annual cost of  
    safeguard) = Value of safeguard to company.  
    

An example of this would be a company that issues laptops to their employees. Losing a single laptop is and SLE. An aggregation of all laptops lost in one year is ALO. ALE = ALO x SLE.

SV would be the amount of money used to reduce the ALE

Password cracking can be done via obtaining the hash file of credentials and then finding out the hash method used to create said hash and finally using a hash cracker to figure out the password