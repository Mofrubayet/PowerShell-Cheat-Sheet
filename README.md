# PowerShell Journal - Mofizul Haque Chowdhury - 100952733

This repository serves as a comprehensive resource for learning PowerShell, featuring detailed cmdlet documentation and practical classwork assignments to develop scripting and system management skills.

The repository provides:

Documentation and examples for essential PowerShell cmdlets.
Classwork exercises covering various administrative tasks, data handling, remote management, and automation.

Usage: 

Navigate through the repository to access explanations, code samples, and step-by-step guides to enhance your PowerShell proficiency.


# 40 PowerShell Commands

## Cmdlet names:

### 1. Write-Host
##### Description: Displays the specified message or output in the PowerShell console.
##### Syntax: Write-Host "Your message here"
##### Example: Write-Host "Hello, World!"
##### Screenshot: 
![image](https://github.com/user-attachments/assets/d33531e1-53cb-452f-8e92-0c72efbe4e2d)

### 2. Get-Service
##### Description: Retrieves the status of services on a local or remote computer.
##### Syntax: Get-Service
##### Example: Get-Service | Where-Object { $_.Status -eq "Running" }
##### Screenshot:
![image](https://github.com/user-attachments/assets/aa1dc169-3352-4a2a-9669-2bba07272da0)

### 3. $host.version
##### Description: Displays the version of the current PowerShell host.
##### Syntax: $host.version
##### Example: $host.version
##### Screenshot: 
![image](https://github.com/user-attachments/assets/5fbc64b3-ba46-42c2-b568-d70dcc82257d)

### 4. Get-History
##### Description: Shows a list of all commands previously entered in the session.
##### Syntax: Get-History
##### Example: Get-History | Select-Object -First 5
##### Screenshot:
![image](https://github.com/user-attachments/assets/a35b2809-525f-4b1a-bbd2-23b2f8ed4c40)

### 5. Invoke-History
##### Description: Runs a command from the command history based on its ID.
##### Syntax: Invoke-History -Id <HistoryID>
##### Example: Invoke-History -Id 3
##### Screenshot:
![image](https://github.com/user-attachments/assets/faf2cc4b-d02b-424a-ac4c-2debe7e40cbc)

### 6. Get-Help
##### Description: Provides information about cmdlets and functions.
##### Syntax: Get-Help <CmdletName>
##### Example: Get-Help Get-Service
##### Screenshot:
![image](https://github.com/user-attachments/assets/6668a008-2f24-4143-b8a2-1424eb186ac9)

### 7. Set-ExecutionPolicy
##### Description: Configures the user preference for the PowerShell script execution policy.
##### Syntax: Set-ExecutionPolicy <PolicyName>
##### Example: Set-ExecutionPolicy RemoteSigned
##### Screenshot:
![image](https://github.com/user-attachments/assets/623a6c53-0312-41ea-a743-dfc5363e5998)

### 8. Export-Csv
##### Description: Exports the results of a command to a CSV file.
##### Syntax: <Command> | Export-Csv -Path <FilePath> -NoTypeInformation
##### Example: Get-Service | Export-Csv -Path "C:\Services.csv" -NoTypeInformation
##### Screenshot:
![image](https://github.com/user-attachments/assets/698e27b6-a487-4992-86b8-eebdbf4c0f97)

### 9. Select-Object
##### Description: Selects specific properties of an object or rearranges them.
##### Syntax: Select-Object <Property1>, <Property2>
##### Example: Get-Service | Select-Object Name, Status
##### Screenshot:
![image](https://github.com/user-attachments/assets/1ff5207a-dab0-4118-b20e-1bbf9ad365d5)

### 10. Get-Process
##### Description: Retrieves the processes that are currently running on a local or remote computer.
##### Syntax: Get-Process
##### Example: Get-Process | Where-Object { $_.CPU -gt 1 }
##### Screenshot:
![image](https://github.com/user-attachments/assets/abdf343a-c89a-4e0b-ad54-747a10a20cab)

### 11. Stop-Process
##### Description: Stops one or more running processes on a local or remote computer.
##### Syntax: Stop-Process -Name <ProcessName> -Force
##### Example: Stop-Process -Name "notepad" -Force
##### Screenshot: 
![image](https://github.com/user-attachments/assets/a5637310-79ed-4a38-a6fd-a96135ee1bc5)

### 12. Get-WmiObject
##### Description: Retrieves management information from local and remote computers.
##### Syntax: Get-WmiObject -Class <ClassName>
##### Example: Get-WmiObject -Class Win32_ComputerSystem
##### Screenshot:
![image](https://github.com/user-attachments/assets/929f88a9-e240-454d-aed9-dbfc2243741c)

### 13. Get-EventLog
##### Description: Retrieves events from the event logs on the local or remote computer.
##### Syntax: Description: Retrieves events from the event logs on the local or remote computer.
##### Example: Get-EventLog -LogName Application -Newest 10
##### Screenshot:
![image](https://github.com/user-attachments/assets/c68e4b58-6f90-4a96-96e3-7a603149ad04)

### 14. Get-Content
##### Description: Description: Gets the content of a file.
##### Syntax: Get-Content -Path <FilePath>
##### Example: Get-Content -Path "C:\example.txt"
##### Screenshot:
![image](https://github.com/user-attachments/assets/5d5592bb-c3b5-4972-ac6f-8c1d4e587a26)

### 15. Get-NetAdapter
##### Description: Retrieves the network adapter properties and configuration.
##### Syntax: Get-NetAdapter
##### Example: Get-NetAdapter | Select-Object Name, Status
##### Screenshot:
![image](https://github.com/user-attachments/assets/4c5bc3c1-f18e-4175-b679-f8fa31df5926)

### 16. Get-Process | Export-Csv
##### Description: Exports process details to a CSV file.
##### Syntax: Get-Process | Export-Csv -Path <FilePath> -NoTypeInformation
##### Example: Get-Process | Export-Csv -Path "C:\Processes.csv" -NoTypeInformation
##### Screenshot:
![image](https://github.com/user-attachments/assets/4b08d641-4ba0-43e8-8450-2a1d41ea2487)

### 17. Get-Service | ConvertTo-CSV
##### Description: Exports service details to a CSV file.
##### Syntax: Get-Service | Export-Csv -Path <FilePath> -NoTypeInformation
##### Example: Get-Service | Export-Csv -Path "C:\Services.csv" -NoTypeInformation
##### Screenshot:
![image](https://github.com/user-attachments/assets/d7d872a3-eaaa-4879-8d8b-666603781793)

### 18. Start-Process
##### Description: Starts a process on the local computer.
##### Syntax: Start-Process -FilePath <Path> -ArgumentList <Arguments>
##### Example: Start-Process -FilePath "notepad"
##### Screenshot:
![image](https://github.com/user-attachments/assets/b2da3a3d-6b82-477f-83b6-a9f804b8df06)

### 19. Get-ChildItem
##### Description: Retrieves the items (files and directories) in a specified location. It can be used to navigate the file system, registry, or other hierarchical structures.
##### Syntax: Get-ChildItem [-Path] <String> [-Recurse] [-Filter <String>]
##### Example: Get-ChildItem -Path "C:\Users"
##### Screenshot:
### 20. Stop-Process
##### Description:
##### Syntax:
##### Example:
##### Screenshot:
### 21. Get-ADComputer
##### Description:
##### Syntax:
##### Example:
##### Screenshot:
### 22. Get-EventLog –LogName Security –Newest 100
##### Description:
##### Syntax:
##### Example:
##### Screenshot:
### 23. Get-Credential
##### Description:
##### Syntax:
##### Example:
##### Screenshot:
### 24. New-PSSession
##### Description:
##### Syntax:
##### Example:
##### Screenshot:
### 25. Get-Module
##### Description:
##### Syntax:
##### Example:
##### Screenshot:
### 26. Get-Module -ListAvailable
##### Description:
##### Syntax:
##### Example:
##### Screenshot:
### 27. Import-Module
##### Description:
##### Syntax:
##### Example:
##### Screenshot:
### 28. Import-Module -PSSession##### Description:
##### Syntax:
##### Example:
##### Screenshot:
### 29. Get-RemoteNetAdapter##### Description:
##### Syntax:
##### Example:
##### Screenshot:
### 30. Get-RemoteNetAdapter | Format-List*##### Description:
##### Syntax:
##### Example:
##### Screenshot:
### 31. Get-PSSession
##### Description:
##### Syntax:
##### Example:
##### Screenshot:
### 32. Remote-PSSession
##### Description:
##### Syntax:
##### Example:
##### Screenshot:
### 33. Get-CimClass
##### Description:
##### Syntax:
##### Example:
##### Screenshot:
### 34. Get-CimInstance
##### Description:
##### Syntax:
##### Example:
##### Screenshot:
### 35. Get-Command
##### Description:
##### Syntax:
##### Example:
##### Screenshot:
### 36. Set-Content
##### Description:
##### Syntax:
##### Example:
##### Screenshot:
### 37. New-ScheduledTaskAction
##### Description:
##### Syntax:
##### Example:
##### Screenshot:
### 38. New-ScheduledTaskTrigger
##### Description:
##### Syntax:
##### Example:
##### Screenshot:
### 39. Register-ScheduledTask
##### Description:
##### Syntax:
##### Example:
##### Screenshot:
### 40. Get-ScheduledTask
##### Description:
##### Syntax:
##### Example:
##### Screenshot:


## Summaries of Classworks:
#### Classwork 1: Configuring PowerShell Environment
##### Summary: Learned to set up and customize PowerShell for optimal use, including pinning to the taskbar, adjusting properties for elevated privileges, and configuring visual settings such as font type, color, and layout. Enhanced usability through enabling QuickEdit Mode and Insert Mode. Practiced running basic cmdlets like `Write-Host`, `Get-Service`, and `Get-History` to confirm proper configuration and tested QuickEdit mode with Notepad for copying and pasting. This improved PowerShell workflow and accessibility for future administrative tasks.

#### Classwork 2: Using `Get-Help` for Command Explanations
##### Summary: Explored Get-Help to understand cmdlets and their functionalities. Gained insights into using cmdlets like `Set-ExecutionPolicy`, `Export-CSV`, `Select-Object`, `Get-Process`, and `Get-Service`, learning their application in system management. Get-Help provided examples, descriptions, and parameter details to effectively use these cmdlets. This improved the ability to find and apply PowerShell commands for automating and troubleshooting tasks.

#### Classwork 3: Working with CSV Files and Commands
##### Summary: Learned how to create, read, and manipulate CSV files using `Export-CSV`, `Get-Content`, and `Import-CSV` cmdlets. Explored the importance of data formatting, handling delimiters, and parsing file content. This classwork demonstrated how to extract and display data from CSV files and emphasized best practices for working with structured data in PowerShell.

#### Classwork 4: Domain-Wide Service and WMI Queries
##### Summary: Explored the use of `Get-ADComputer`, `Get-Service`, and `Get-WmiObject` for querying and managing services and WMI classes on networked computers. Learned how to adapt PowerShell commands to pull data from multiple domain computers and identified potential challenges in remote queries. This practice improved the ability to manage domain-wide service checks and WMI queries effectively.

#### Classwork 5: PowerShell Remoting and Session Management
##### Summary: Studied PowerShell remoting and session management using `Invoke-Command`, `New-PSSession`, and `Enter-PSSession` to run commands remotely. Used `Get-Module -PSSession` to check available modules in sessions and learned how to list network adapters with `Get-RemoteNetAdapter`. This reinforced understanding of remote management, crucial for handling systems across networks.

#### Classwork 6: CIM/WMI Cmdlets and Troubleshooting
##### Summary: Used CIM/WMI cmdlets like `Get-CimInstance` and `Get-WmiObject` to query system information such as network adapter settings and hotfix details. Explored `Win32_NetworkAdapterConfiguration` and `Win32_BIOS` classes to gather specific configuration data. This enhanced the understanding of how to use CIM/WMI cmdlets for system analysis and troubleshooting.

#### Classwork 7: Profile Script Creation and Variables
##### Summary: Created a custom profile script with `New-Item` and edited it using `$PROFILE`. Learned variable handling, including variable naming, types, and the use of `$()` for subexpression. This practice emphasized how to set up scripts that run on PowerShell startup and how to declare and use variables efficiently.

#### Classwork 8: Bowling Score Script
##### Summary: Developed a PowerShell script to collect bowling scores, validate user input, and display results. Used a loop to gather 9 scores, stored them in an array, and printed them with labels for each frame. The script also saved scores to a text file using `Out-File`. This task reinforced array handling, user input validation, and file writing.

#### Classwork 9: Running and Scheduling PowerShell Scripts
##### Summary: Created a script to list running services using `Get-Service` and learned how to schedule it as a task with `New-ScheduledTask` and `Register-ScheduledTask`. This task emphasized the automation of PowerShell scripts to run at login and how to use Task Scheduler for task management and execution.

#### Classwork 10: Creating Shared Folders and Printers
##### Summary: Learned how to create shared folders between two servers using `New-SmbShare` and set permissions with `Set-SmbShare`. Practiced adding a printer using `Add-Printer`, configuring it for network sharing. This demonstrated the setup of shared resources and network printer integration, essential for collaboration and resource management across systems.
