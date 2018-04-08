# CodePathWeek8

# Project 8 - Pentesting Live Targets

Time spent: **3** hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:
* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each version of the site has been given two of the six vulnerabilities. (In other words, all six of the exploits should be assignable to one of the sites.)

## Blue

Vulnerability #1: SQL Injection
<img src="https://github.com/sk8wt/CodePathWeek8/blob/master/BlueSQL.gif" width="800">
Changed the ID session to 'OR 1=1--' to allow me access to a different user
Vulnerability #2: Session Hijacking/Fixation
<img src="https://github.com/sk8wt/CodePathWeek8/blob/master/BlueSession.gif" width="800">
Started a session on a different browser, changed the session ID using a tool we used from an earlier CodePath assignment to gain access into the system from that different browser without ever having to input login credentials. 


## Green

Vulnerability #1: User Enumeration
<img src="https://github.com/sk8wt/CodePathWeek8/blob/master/GreenEnumeration.gif" width="800">
Noticed that for invalid users (such as admin), the error message was in regular typeface font. However, for valid users in the system (such as jmonroe99 and pperson), the error message was in boldface. This is an error on the side of the developer, as it gives a potential hacker insight into valid usernames. 

Vulnerability #2: Cross-Site Scripting
<img src="https://github.com/sk8wt/CodePathWeek8/blob/master/GreenXSS.gif" width="800">
Inserted a cross-site script into the feedback form so that when an admin selected the feedback form, they would get an alert message. 

## Red

Vulnerability #1: Insecure Direct Object Reference
<img src="https://github.com/sk8wt/CodePathWeek8/blob/master/RedIDOR.gif" width="800">
Noticed that certain employees should not be accessed by users. However, if the ID value was incremented to 11 (a page that was not clickable by users), they could access sensitive employee data that they should not have had access to .

Vulnerability #2: Cross-site request forgery


## Notes

Describe any challenges encountered while doing the work


