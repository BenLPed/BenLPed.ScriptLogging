# Logging

This module can help you create logging in your scripts. You write **write-log "what needs to happen or what happens"**. You can follow along live, which makes it easy to see what is happening. It also records which user runs the script, which line of the script is executed and the time. So if something goes wrong, it's easy to find out what went wrong.

![Complet view of Logfil](Images//fullPic.png?raw=true)



## What commands do I get, how are they used

You get the following commands:
- Start-Log
- Write-Log

### Start-Log

You started logging by using this command. Here you say what the script should be called, where it should be located, which company, description of what the script does, number of days the log files should be saved

.EXAMPLE
Start-Log -FilePath "\\LogShare$\ADUsers" -FileName "ListOfAdUsers" -Company "BLIT" -Description "Find all users in our AD that is Enabled" -DeletedLogDays "30"

Start-Log "\\LogShare$\ADUsers" "ListOfAdUsers" "BLIT" "Find all users in our AD that is Enabled" "30"

It checks if the folder is created, otherwise it is created. It then checks whether the file exists, otherwise it is created.
It then stores the default information, so that there is no doubt when a new run has started, especially if it runs several times on the same day.


![alt text](Images/Start-Log.png?raw=true)

### Write-Log

When you want to add something to the log, you write **write-log "what needs to happen or what happens"** and it is added to the log file. By default, it automatically sets 1 after "Text", but if you want to draw attention to something, you can write 2 numbers and the error text will turn yellow. If you write a number 3, the text turns red, it is only used in case of error.


| Value | Color     |
|------:|-----------|
|  Blank| Nothing   |
|      1| Nothing   |
|      2| Yellow    |
|      3| Red       |

![alt text](Images/LineColor.png?raw=true)


It is possible to create a very long error message, as there is room to display it if you use (THIS program)

![alt text](Images/Description.png?raw=true)


## How do I get started using this script

You can download it from [Powershellgallery.com](https://www.powershellgallery.com/packages/BenLPed.Scriptlogging) so you always get the latest version.

The command you type is
Install-Module -Name BenLPed.Scriptlogging
