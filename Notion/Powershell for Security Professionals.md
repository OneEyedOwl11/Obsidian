- 1.1 Locate and run Cmdlets
    
    cmdlets allow code that’s bundled up to run making life easier.
    
    first command learned
    
    get-help show’s how to use the help function on any command and shows example
    
    get-process (alias “gps” ”ps”)
    
    gal “insert any letter here”* ( get all commands that start with a letter you insert into the quotations spot. Without quotations obviously
    
    pwd (shows current filepath)
    
      
    
- 1.2 Understanding Basic Scripts
    
    powershell scripts run as a .ps1 file
    
    you wont need to write your own scripts most of the time but it’s useful to understand how it works. the script will do around 80% of the job itself and the last 20% will need your input for your specific situation
    
    $ = variable (e.g $computerName)
    
    invoke-command (calls a command)
    
- 1.3 Functions in PowerShell
    
    Functions provide a way to make code that you’ve written reusable.  
    (Works like any other language eg  
    
    ```PowerShell
    function my-function {
    	$PSVerstionTable.PSVersion
    	Get-Location
    }
    
    my-function
    ```
    
    )
    
- 1.4 intro to git and version control
    
    I already know this
    
- 2.1 Create and Run a script
    
    Practical lesson on making a script and running it
    
    if you want to be able to run scripts you need to set “Set-ExecutionPolicy RemoteSigned” to yes but this will somewhat make that system more vulnerable
    
      
    
- 2.2 Installing visual studio code
    
    LOL
    
- 2.3 Add control flow to a script
    
    eg of for loop
    
    ```PowerShell
    $Websites = 'google.com','amazon.com','cybrary.it'
    
    foreach ($site in $Websites) {
    	ping $site
    }
    ```
    
    Do loop
    
    - Do Until
        
        ```PowerShell
        $number = Get-Random -Minimum 1 - Maximum 5
        do {
        		$guess = Read-Host -Prompt "Enter your guess"
        		if ($guess -lt $number) {
        			Write-Output 'Too low buddyPal'
        		}
        		elseif ($guess -gt $number) {
        			Write-Output 'Too high bucko'
        		}
        	}
        until ($guess -eq $number)
        ```
        
    - Do While
        
        ```PowerShell
        $number = Get-Random -Minimum 1 - Maximum 5
        while ($guess -ne $number) {
        do {
        		$guess = Read-Host -Prompt "Enter your guess"
        		if ($guess -lt $number) {
        			Write-Output 'Too low buddyPal'
        		}
        		elseif ($guess -gt $number) {
        			Write-Output 'Too high bucko'
        		}
        	}
        }
        ```
        
    
    Break, Continue, Return
    
    - break
        
        ```PowerShell
        for ($i = 1; $i -lt 5; $i++) {
        Write-Output "sleeping for $i seconds"
        Start-Sleep -Seconds $i
        break
        }
        ```
        
    - continue
        
        ```PowerShell
        while ($i - lt 5) {
        	$i += 1
        	if ($i -eq 3 {
        		continue
        	}
        	Write-Output $i
        }
        ```
        
    - return
        
        ```PowerShell
        $number = 1...10
        foreach ($n in $number) {
        	if ($n -ge 4) {
        		Return $n
        	}
        }
        ```
        
- 2.4 Script safeguards through error handling
    
    ```PowerShell
    try 
    {
    Write-Output
    }
    catch
    {
    	Write-Output "Something through out an exeption"
    	Write-Output $__
    }
    ```
    
    majority of powershell code is written in these blocks to try and catch errors
    
- 2.5 PowerShell Scripting Demo
    
    ```PowerShell
    for ($number = 0; $number -le 25; $number++) {
    		"$number is the number"
    }
    ```
    
    ```PowerShell
    for ($character = "" ; $character.length -le 15; $character = $character+"4") {
    		Write-Host $character
    		Start-Sleep -Milliseconds 15
    } 
    ```
    
- 3.1 User Roles and Features
    
    ```PowerShell
    \#Remotely remove roles
    Uninstall-WindowsFeature
    Install-WindowsFeature
    
    \#Change execution policies
    Set-ExecutionPolicy 
    
    \#Sign PowerShell Script
    Set-AuthenticationSignature
    
    \#constrained mode
    ```
    
- 3.2 Manage Specific Rules
    
    Group policy commandlets are important for managing your entire orgs group policy
    
    can quickly write a script to move users to a group if a vulnerability has been exploited
    
- 3.3 Execution Policies
    
    [https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_execution_policies?view=powershell-7.2](https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_execution_policies?view=powershell-7.2)
    
    ## PowerShell execution policies
    
    Enforcement of these policies only occurs on Windows platforms. The PowerShell  
    execution policies are as follows:  
    
    **AllSigned**
    
    - Scripts can run.
    - Requires that all scripts and configuration files be signed by a trusted  
        publisher, including scripts that you write on the local computer.  
        
    - Prompts you before running scripts from publishers that you haven't yet  
        classified as trusted or untrusted.  
        
    - Risks running signed, but malicious, scripts.
    
    **Bypass**
    
    - Nothing is blocked and there are no warnings or prompts.
    - This execution policy is designed for configurations in which a PowerShell  
        script is built in to a larger application or for configurations in which  
        PowerShell is the foundation for a program that has its own security model.  
        
    
    **Default**
    
    - Sets the default execution policy.
    - **Restricted** for Windows clients.
    - **RemoteSigned** for Windows servers.
    
    **RemoteSigned**
    
    - The default execution policy for Windows server computers.
    - Scripts can run.
    - Requires a digital signature from a trusted publisher on scripts and  
        configuration files that are downloaded from the internet which includes  
        email and instant messaging programs.  
        
    - Doesn't require digital signatures on scripts that are written on the local  
        computer and not downloaded from the internet.  
        
    - Runs scripts that are downloaded from the internet and not signed, if the  
        scripts are unblocked, such as by using the  
        `Unblock-File` cmdlet.
    - Risks running unsigned scripts from sources other than the internet and  
        signed scripts that could be malicious.  
        
    
    **Restricted**
    
    - The default execution policy for Windows client computers.
    - Permits individual commands, but does not allow scripts.
    - Prevents running of all script files, including formatting and configuration  
        files (  
        `.ps1xml`), module script files (`.psm1`), and PowerShell profiles  
        (  
        `.ps1`).
    
    **Undefined**
    
    - There is no execution policy set in the current scope.
    - If the execution policy in all scopes is **Undefined**, the effective  
        execution policy is  
        **Restricted** for Windows clients and  
          
        **RemoteSigned** for Windows Server.
    
    **Unrestricted**
    
    - The default execution policy for non-Windows computers and cannot be  
        changed.  
        
    - Unsigned scripts can run. There is a risk of running malicious scripts.
    - Warns the user before running scripts and configuration files that are  
        not from the local intranet zone.  
        
- 4.1 Using PowerShell to Exploit
    
    User > Cannot run code off the internet or their own scripts
    
    Admin > More privileges eg run scripts
    
    Root > more privileges than admin
    
    Kernel > Unchecked privileges
    
    To be able to run PowerShell scripts on a target device
    
    https://github.com/PowerShellMafia/PowerSploit
    
    https://github.com/EmpireProject/Empire
    
    Must be run on kali linux
    
- 4.2 Using PowerShell to deliver payloads
    1. Decide what you want your payload to do
    2. Use a combination of obfuscation techniques to make sure your payload goes undetected
    3. Choose the right memory/resource allocation
    4. Create your payload
    5. Deliver your payload using a prewritten framework.
- 4.3 exercise
- 5.1 Integrating the Power of API’s
    
    - four main
        
        Get - get info from api in form of json
        
        Put - edit existing record
        
        Post - add new record
        
        Delete - allows delete
        
    - link for security api’s
        
        https://github.com/jaegeral/security-apis
        
    
    ```PowerShell
    $Body = @{
            Cook = "Barbara"
            Meal = "Pizza"
    }
    
    <#$Headers = @{
            Username = "safasfsdf"
            Password = "sdfasdga" 
    }#>
    
    $Parameters = @{
            Method = "POST"
            <\#Header = ($Headers | ConvertTo-Json) this is an example of how you'd use the header section in the parameters#>
            Uri = "https://4besday4.azurewebsites.net/api/AddMeal"
            Body = ($Body | ConvertTo-Json)
            ContentType = "application/json"
    }
    Invoke-RestMethod @Parameters
    ```
    
- 5.2 Making API Calls inside PowerShell
    
    ```PowerShell
    $Number = Get-Random -Maximum 100
    Invoke-RestMethod "https://jsonplaceholder.typicode.com/todos/$Number"
    ```
    
- 5.3 Organizing Code Using Virtual Notebooks
    
    You have to do it in visual studio. Work is saved there in my Documents/Coding/PowerShell directory
    
- 5.4 PowerShell defensive operations quiz
    
    Exercise
    
- 6.1 PowerShell-Related Interview Questions
    
    PowerShell is object based
    
    requires .NET framework to run
    
    does have security vulnerabilities built in
    
    common exploits happen through them
    
    execution policies will always come up
    
    how to change them
    
    there are 5. We typed them in a previous lesson
    
    - PipeLines
        
        Chained together commands and commandlets
        
        output from first command becomes input for second command
        
        Command-1 | Command-2 | Command-3 | Command-4
        
    
      
    
- 6.2 Resources to checkout
    
    Microsoft PowerShell documentation
    
    [https://learn.microsoft.com/en-us/powershell/](https://learn.microsoft.com/en-us/powershell/)
    
    [https://www.comparitech.com/net-admin/powershell-cheat-sheet/](https://www.comparitech.com/net-admin/powershell-cheat-sheet/)
    
    search github and read through some code
    
    look online for other resources to help you write your own