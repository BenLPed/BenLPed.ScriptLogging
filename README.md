# Logging

This module can help you create logging in your scripts. You write **write-log "what needs to happen or what happens"**. You can follow along live, which makes it easy to see what is happening. It also records which user runs the script, which line of the script is executed and the time. So if something goes wrong, it's easy to find out what went wrong.

![alt text](https://github.com/BenLPed/Images/blob/main/BenLPed.Scriptlogging/fullPic.png?raw=true)


## Command

### Write-Log
| Value | Color     |
|------:|-----------|
|  Blank| Nothing   |
|      1| Nothing   |
|      2| Yellow    |
|      3| Red       |







##
This module helps you create a log in your scripts. you can follow along live and it is possible to put color in code, depending on what you want.
By default it generates a file (dd.mm.yyyy - filename) in the desired folder. It can also be a network drive.
if you want something in the log to draw attention to yourself, you can put a 2 number after the text, then the text will turn yellow.
Eg. in a try-catch, you could put a 3 number after the text in the catch if it is an error, as the text will turn red.

Start-log -Path <> -Filename <> to start logging
Write-Log "The tekse you want to log" -Level 1
