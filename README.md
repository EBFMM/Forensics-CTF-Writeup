# Forensics-CTF-Writeup

## Objective

The Forensics/Hard Disks category of a CTF, typically consists of analyzing digital artifacts from storage devices. Challenges may involve recovering deleted files or analyzing file systems. The objective in this challenge is to identify specific evidence within registry files. Some important background knowledge needed is a solid understanding of file systems and forensic analysis techniques. More importantly how to move throughout file systems easily to quickly search and assess key information. This category relates to my experience within the Ethical Hacking course, particularly the topics of incident response and forensic analysis. The lab 'Scanning, Enumeration, and Vulnerability Analysis' in the course covered a similar topic to this CTF problem. To describe, reconnaissance is conducted to gather essential information and the Windows Registry can be categorized as a database.

## Introduction To The Problem

We are to download the registry files provided to determine the current version of Firefox. To begin, I plan to use the command line tool regshell to view the software registry in greater detail. I will select to view the software instead of system or security because the question is to determine the current version of Mozilla Firefox. I plan to search deeper into this software registry because it should contain the information I am looking for.

![image](https://github.com/user-attachments/assets/9e0dcbd0-8749-494d-8cd9-8c7d578af391)

## Working Towards A Solution

![image](https://github.com/user-attachments/assets/9a01bbaf-555c-4a52-8a39-827ce7f37ac6)

Regshell command can be used with switch 'F' to specify file name. Given our options, I will select 'software' directory to dig deeper, then seeing the listed directories, Mozilla stands out because as mentioned, we are looking to determine the current version of Firefox. 

## Arriving At The Solution

![image](https://github.com/user-attachments/assets/695c19af-1b39-46ed-968d-5e5fde64a4e8)

I was able to arrive to the solution by further changing directory into the "Mozilla Firefox" which after listing contents showed me the 'CurrentVersion' value to signify the answer and flag: Mozilla Firefox version "35.0.1".

## Lessons Learned 

From this challenge, I learned the importance of prioritizing where you decide to search more in-depth to save time. Personal pitfalls included looking in the irrelevant directories within the registry. Additionally, it is worth mentioning that I experienced a pitfall when trying to “change directory” into a directory which was named utilizing a space. Tab to complete was not working, however by placing quotations around the name I was able to successfully change directory to the exact path entered. 

## Relationship To The Workplace

Capture the Flag challenges and competitions can benefit you in the workplace because they improve one's technical skills, develop critical thinking, and provide you with networking opportunities. These competitions are home to hackers and likeminded individuals all interested in cybersecurity. Many CTF competitions are team-based and require effective communication which I believe to be a crucial skill in the workplace.

## Summary

To summarize, we had gathered information regarding specific software however, there is a wealth of information to be enumerated inspecting the registry files provided. The main takeaway is that extensive background knowledge is not required to solve similar CTF problems, although it is important to be familiar with the various forensic analysis tools such as FTKImager or Autopsy in addition to proper syntax and usage of command line tools such as regshell to investigate effectively.


