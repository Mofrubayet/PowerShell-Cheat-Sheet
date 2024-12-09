# PowerShell Journal - Mofizul Haque Chowdhury - 100952733

This repository serves as a comprehensive resource for learning PowerShell, featuring detailed cmdlet documentation and practical classwork assignments to develop scripting and system management skills.

The repository provides:

Documentation and examples for essential PowerShell cmdlets.
Classwork exercises covering various administrative tasks, data handling, remote management, and automation.

Usage: 

This repository is created to enhance PowerShell proficiency and to access explanations, code samples, and step-by-step guides.

## Table of Cmdlets:

| #  | PowerShell Command             |
|----|--------------------------------|
| 1  | Write-Host                     |
| 2  | Get-Service                    |
| 3  | $host.version                  |
| 4  | Get-History                    |
| 5  | Invoke-History                 |
| 6  | Get-Help                       |
| 7  | Set-ExecutionPolicy            |
| 8  | Export-Csv                     |
| 9  | Select-Object                  |
| 10 | Get-Process                    |
| 11 | Stop-Process                   |
| 12 | Get-WmiObject                  |
| 13 | Get-EventLog                   |
| 14 | Get-Content                    |
| 15 | Get-NetAdapter                 |
| 16 | Get-Process | Export-Csv       |
| 17 | Get-Service | ConvertTo-CSV    |
| 18 | Start-Process                  |
| 19 | Get-ChildItem                  |
| 20 | Start-Service                  |
| 21 | Get-ADComputer                 |
| 22 | Get-EventLog –LogName Security –Newest 100 |
| 23 | Get-Credential                 |
| 24 | New-PSSession                  |
| 25 | Get-Module                     |
| 26 | Get-Module -ListAvailable      |
| 27 | Import-Module                  |
| 28 | Import-Module -PSSession       |
| 29 | Test-Connection                |
| 30 | Test-NetConnection             |
| 31 | Get-PSSessionConfiguration     |
| 32 | Remote-PSSession               |
| 33 | Get-EventSubscriber            |
| 34 | Get-CimInstance                |
| 35 | Get-Command                    |
| 36 | Set-Content                    |
| 37 | New-ScheduledTaskAction        |
| 38 | New-ScheduledTaskTrigger       |
| 39 | Register-ScheduledTask         |
| 40 | Get-ScheduledTask              |



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
![image](https://github.com/user-attachments/assets/8abfd6dc-5238-4ecb-b7a6-9717c6e09e46)

### 20. Start-Service
##### Description: This cmdlet starts a service on a local or a remote computer. 
##### Syntax: Start-Service -Name "name"
##### Example: Start-Service -Name "wuauserv"
##### Screenshot:
![image](https://github.com/user-attachments/assets/6665959a-024a-42e4-88e3-8b1cba1b3ac4)

### 21. Get-ADComputer
##### Description: Retrieves information about computer accounts in Active Directory.
##### Syntax: Get-ADComputer -Filter *
##### Example: Get-ADComputer -Filter * | Select-Object Name
##### Screenshot:
![image](https://github.com/user-attachments/assets/233d6d59-c105-4523-acdc-22bbc7d6fa30)

### 22. Get-EventLog –LogName Security –Newest 100
##### Description: Retrieves the 100 most recent security events from the event log.
##### Syntax: Get-EventLog -LogName Security -Newest 100
##### Example: Get-EventLog -LogName Security -Newest 100
##### Screenshot:
![image](https://github.com/user-attachments/assets/747d30d1-b54a-4809-b0c4-14ee89fb0481)

### 23. Get-Credential
##### Description: Prompts for and returns a credential object.
##### Syntax: Get-Credential
##### Example: $credential = Get-Credential
##### Screenshot:
![image](https://github.com/user-attachments/assets/6152922f-4e0a-4819-a4e1-6bb43d2260b4)

### 24. New-PSSession
##### Description: Creates a persistent PowerShell session on a local or remote computer.
##### Syntax: New-PSSession -ComputerName <ComputerName>
##### Example: $session = New-PSSession -ComputerName Server1
##### Screenshot:
![image](https://github.com/user-attachments/assets/9b546cc9-5d03-4ffe-88a3-10eb381a81f4)

### 25. Get-Module
##### Description: Lists the modules that are imported in the current session.
##### Syntax: Get-Module
##### Example: Get-Module | Select-Object Name, Version
##### Screenshot:
![image](https://github.com/user-attachments/assets/c04c38a5-4452-4d16-b929-7530e23149b0)

### 26. Get-Module -ListAvailable
##### Description: Lists all modules available for import.
##### Syntax: Get-Module -ListAvailable
##### Example: Get-Module -ListAvailable | Select-Object Name, Version
##### Screenshot:
![image](https://github.com/user-attachments/assets/8c343584-548c-461f-93ea-6415223cfe6f)

### 27. Import-Module
##### Description: Imports a module into the current PowerShell session.
##### Syntax: Import-Module <ModuleName>
##### Example: Import-Module ActiveDirectory
##### Screenshot:
![image](https://github.com/user-attachments/assets/bb61704f-3005-4814-8be9-e427e90f6d7a)

### 28. Import-Module -PSSession
##### Description: Imports a module into an existing remote session.
##### Syntax: Import-Module -PSSession <SessionObject> -Name <ModuleName>
##### Example: Import-Module -PSSession $session -Name NetAdapter
##### Screenshot:
![image](https://github.com/user-attachments/assets/e116325c-69f2-448d-ae1a-20094731684c)

### 29. Test-Connection
##### Description: Tests the network connectivity to a specified computer.
##### Syntax: Test-Connection -computername> "<name>" 
##### Example: Test-Connection -ComputerName "Server1" -Count 4
##### Screenshot:
![image](https://github.com/user-attachments/assets/deae2447-7701-46df-852a-749c52e7d718)

### 30. Test-NetConnection
##### Description: Diagnoses network connectivity and provides detailed information about a connection.
##### Syntax: Test-NetConnection -ComputerName "website" -Port <port>
##### Example: Test-NetConnection -ComputerName "www.google.com" -Port 80
##### Screenshot:
![image](https://github.com/user-attachments/assets/18d37bd2-baa3-4a78-a87c-cbd08104bbf4)

### 31. Get-PSSessionConfiguration
##### Description: Retrieves information about registered PowerShell session configurations on the local computer.
##### Syntax: Get-PSSessionConfiguration
##### Example: Get-PSSessionConfiguration
##### Screenshot:
![image](https://github.com/user-attachments/assets/ef4c1641-8887-42f3-b063-243f45dc15dc)

### 32. Remote-PSSession
##### Description: Starts a remote PowerShell session.
##### Syntax: Enter-PSSession -Session <SessionObject>
##### Example: Enter-PSSession -Session $session
##### Screenshot:
![image](https://github.com/user-attachments/assets/7ccbaaaf-9604-4a42-aad4-b1b37baae8c7)

### 33. Get-EventSubscriber
##### Description: Retrieves the event subscribers that are registered on the computer. 
##### Syntax: Get-EventSubscriber
##### Example: Get-EventSubscriber | Format-List
##### Screenshot:
![image](https://github.com/user-attachments/assets/1c4f61e9-abe2-4000-a7de-64fa260d01d8)

### 34. Get-CimInstance
##### Description: Retrieves CIM instances from a computer.
##### Syntax: Get-CimInstance -ClassName <ClassName>
##### Example: Get-CimInstance -ClassName Win32_OperatingSystem
##### Screenshot:
![image](https://github.com/user-attachments/assets/c59e140d-ef8b-44a6-aa74-041d3ef4f0cf)

### 35. Get-Command
##### Description: Retrieves all cmdlets, functions, workflows, aliases installed on the system. 
##### Syntax: Get-Command
##### Example: Get-Command -Module ActiveDirectory
##### Screenshot:
![image](https://github.com/user-attachments/assets/05e7593a-ba7d-4166-9fe0-68e5f3605e98)

### 36. Set-Content
##### Description: Writes or replaces the content in a file.
##### Syntax: Set-Content -Path <FilePath> -Value <Content>
##### Example: Set-Content -Path "C:\example.txt" -Value "New content"
##### Screenshot:
![image](https://github.com/user-attachments/assets/a7d606be-f655-4727-a117-24103e53be4e)

### 37. New-ScheduledTaskAction
##### Description: Creates a new action for a scheduled task.
##### Syntax: New-ScheduledTaskAction -Execute <Path> -Argument <Arguments>
##### Example: New-ScheduledTaskAction -Execute "notepad.exe"
##### Screenshot:
![image](https://github.com/user-attachments/assets/dc09bf58-8c7b-4e23-bd8b-f55bd37e16e7)

### 38. New-ScheduledTaskTrigger
##### Description: Creates a new trigger for a scheduled task.
##### Syntax: New-ScheduledTaskTrigger -At <DateTime> -Daily
##### Example: New-ScheduledTaskTrigger -At "8:00AM" -Daily
##### Screenshot:
![image](https://github.com/user-attachments/assets/a13e3d01-81a0-4dc0-8c71-09176dcc7bbe)

### 39. Register-ScheduledTask
##### Description: Registers a new scheduled task.
##### Syntax: Register-ScheduledTask -TaskName <Name> -Trigger <Trigger> -Action <Action>
##### Example: Register-ScheduledTask -TaskName "Open Notepad" -Trigger $trigger -Action $action -RunLevel Highest
##### Screenshot:
![image](https://github.com/user-attachments/assets/b59ac36a-c060-42c6-8fe4-8fd6a00baf79)

### 40. Get-ScheduledTask
##### Description: Retrieves information about scheduled tasks.
##### Syntax: Get-ScheduledTask
##### Example: Get-ScheduledTask | Select-Object TaskName, State
##### Screenshot:
![image](https://github.com/user-attachments/assets/4b1e304c-52cf-4f5c-8c4a-bfae2c3fbabe)


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
