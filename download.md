---
layout: page
title: Download
permalink: /download
---

Windows 64-bit        
[Streembit v.1.0.4 Win64 executable](http://streembit.github.io/downloads/streembit_win64.zip)      
MD5 hash: b908c01524715b9dd6bac7ad28268c77     

--------


#### The v.1.0.4 Linux and MAC OS X build and binary update is in progress ... please check the downloads later or build it from source for the time being.

-----



### Installation instructions
**To provide users with the most secure solution and to avoid placing dependencies on your computer the Streembit software is not an installed application. You can run the software by extracting the downloaded file and execute the Streembit binary.**   
Please follow the steps below to execute the application.

1. Download one of the above the compressed files which is relevant to your operating system (OS).
2. Extract the compressed file into any directory on your computer e.g. "C:\streembit" (on Windows) or "/home/username/streembit" on a Linux or Mac OS X machine.

Windows
-------
On Windows, right click on the streembit.exe file, select "Run as administrator" from the menu to execute the Streembit software.   
Optional: create a shortcut from the Streembit executable at your Desktop or Taskbar for quick access.


Linux
-----
Open the terminal.    
On Linux, change to the directory where the zip file was extracted.   

```
$ cd /path/to/extracted_files
```     

Execute the Streembit binary file.  

```
$ ./streembit
```   

Optional: create a [.desktop file](https://wiki.archlinux.org/index.php/Desktop_entries) for quick access.

Mac OS X
--------
Open the terminal.    
Add read/write permission to the nwjs.app package and its entire content.

```
$ cd /path/to/extracted_files
```

Execute the Streembit binary file.     

```
$ sudo nwjs.app/Contents/MacOS/nwjs .
```   

(Even our software is fully open sourced and anyone can verify that there are no backdoors exist nor malicious activities executed by the application, Apple makes the execution of the software a very difficult task. We are working on creating a signed, more user friendly package for MAC OS X users.   
We suggest to get the source using Git on MAC OS X it from the terminal by executing “nwjs.app/Contents/MacOS/nwjs .” until a more user friendly MAC OS X package is not available.)




