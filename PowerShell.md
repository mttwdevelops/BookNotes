```
Help get-item -xxx 
```
can replace ```-xxx``` with -Online or with -Full

PowerShell enables you to do what you already have permission to do.

We use ```set-location``` in PS, but ```cd``` is the equivalent in Bash

```new-item``` followed by ```-itemtype xxx``` can create directories or items in a folder

We can pipe commands using ```|```. An example is get-process | export-csv procs.csv

compare-object takes two sets of info and compares them

When we have issues with multiple modules having the same name for commands we use: ```xx\command```

Objects, or individual processes in PS, have properties and methods (an action). All the properties, methods, and other things attached to an object are called its members.
- Use Get-member (gm) instead of get-help for objects

# Day 8
1. get-help random
2. get-date
3. get-date returns a DateTime object, can be converted into a string with .tostring()
4. get-date | select-object DayOfWeek
5. get-childitem or ls
6. get-childitem | sort-object lastwritetime | select name,creationtime
7. get-childitem | sort-object lastwritetime | select name,creationtime,lastwritetime | export-csv file.csv, get-childitem | sort-object lastwritetime | select name,creationtime,lastwritetime | out-file file.html

# Day 7
1. Install-Module -Name PackageManagement, Install-Module -Name PSWindowsUpdate
2. get-command -module XXX
3. find-module -command compress-archive | install-module -force
4. import-module microsoft.powershell.archive
5. new-item ~\TestFolder -itemtype Directory, foreach { new-item -path C:\Users\vm\Documents\TestFolder\$_.txt } 
6. compress-archive C:\Users\vm\Documents\TestFolder C:\Users\vm\Documents\TestFolder2.zip
7. expand-archive C:/Users/vm/Documents/Testfolder2.zip -destinationpath C:/Users/vm/Documens/TestFolder2
8. compare-object ~/TestFolder ~/TestFolder2, $reference =get-childitem ~/Documents/TestFolder | select-object -expandproperty name, $difference = get-childitem ~/Documents/TestFolder2 | select-object -expandproperty name, compare-object -referenceobject $reference -differenceobject $difference

# Day 6
1. Labq12.txt =>, labq11.txt <=
2. Issue with out-file: cannot process argument because value of argument "path" is null. Out-file won't do anything because the file is created by Export-csv.
3. stop-job can also go by instanceID, state, or filter. You can stop a job without get-job
4. -delimiter "|"
5. -includeTypeInformation
6. -noclobber, -confirm
7. -useCulture

# Day 5
1. new-item Labs -itemtype Directory
2. new-item .\Labs\Test.txt
3. ```set-item .\Labs\Test.txt -value Testing``` does not work because its provider does not support this type of operation
4. get-item env:Path
5. The Filter specifies to qualify the Path parameter, the Include specifies an array of 1+ string patterns to be matched as the cmdlet gets child items and matching items are included, and the Exclude also specifies an array of 1+ but excludes matches from output. All allow wildcards. Include and Exclude must be used with -Recurse or if you are querying a container.

# Day 4
1. gps
2. test-connection google.com
3. get-command -type cmdlet
4. get-alias
5. new-alias "ntst" netstat
6. gps -name p*
7. new-item -path .\MyFolder1 -ItemType Directory
8. remove-item .\MyFolder*

# Day 3
2. Yes, ConvertTo-Html.
3. Yes, redirect.
4. A lot
5. Set-PSBreakpoint
6. xxx-Alias cmdlets are available
7. Start-Transcript and Stop-Transcript
8. get-process
9. -IncludeUserName
10. Invoke-Command
11. 80 characters is the default, you can change the $PSDefaultParameterValues parameter to change the default
12. -NoClobber
13. Get-Alias
14. get-help process
15. 10
16. get-help array
