---
title: Under The Wire2
date: 2023-12-24 21:55:20 +0300
category: [War_Games]
tags: [windows, powershell, putty, ssh, century]
---
![img-description](/assets/img/wargames/UnderTheWire.png)  
Welcome back. In the previous article we discussed what wargames are and tackled three levels(centuries). In this article, we will cover five levels. i.e century 4 thru' century 8.  
Let's get right in...  
## Century 4
Host → century.underthewire.tech  
username → century4  
password → 123  

Goal: → to enter into a directory with space in the name  

![img-description](/assets/img/wargames/g4.png)  

We know that within Windows OS, we can easily have a directory name with spaces in it. But how do we actually change into the directory from the commandline? The first attempt would be straight forward, use _cd directory name_. This will however not work as expected due to the space after the first word. To do this, we need to use the ' ' to wrap and treat the directory name as a single word. 

![img-description](/assets/img/wargames/g4.1.png)  

And the password for century 5 is: _**49125**_  

## Century 5
Host → century.underthewire.tech  
username → century5   
password → 49125

Goal: → To retrieve the domain name  
![img-description](/assets/img/wargames/g5.png)  

![img-description](/assets/img/wargames/g5.1.png)  


## Century 6
Host → century.underthewire.tech  
username → century6  
password → underthewire3347  

Goal: → To count the number of folders/directories
![img-description](/assets/img/wargames/g6.png)

![img-description](/assets/img/wargames/g6.1.png)

## Century 7
Host: century.underthewire.tech  
username: century7  
password: 197   

Goal:  
![img-description](/assets/img/wargames/g7.png)  

SOlution  
```powershell
Get-ChildItem -Path C:\users\century7 -Recurse | Where-Object { $_.Name -like “*README*” }
```
![img-description](/assets/img/wargames/g7.1.png)

## Century 8
Host: century.underthewire.tech  
username: century8  
password: 7points  

Goal: Getting the unique entries within the file  

![img-description](/assets/img/wargames/g8.png)  

Solution

```powershell
(Get-Content -Path “C:\users\century8\desktop\unique.txt” | Select-Object -Unique).count
```
![img-description](/assets/img/wargames/g8.1.png)