# Project 8 - Pentesting Live Targets

Time spent: **X** hours spent in total

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
![image](https://github.com/LMCNN/CS4984/blob/master/GIF/SQLI.gif)
-When I opened the find salesman page and selected a salesmperson, 
 I found that there was a parameter called id at the end of the url.
 I try to change the number to 'OR sleep(5)=0 --' and refresh the site.
 I waited five seconds before the page returned.

Vulnerability #2: Session Hijacking/Fixation
![image](https://github.com/LMCNN/CS4984/blob/master/GIF/Session%20Hijacking.gif)
-Open the page simultaneously with two different browsers
-Login in this page in one of the browsers
-Use the provided tool to copy the session id of the browser of
 the logged in web page to another browser
-The other browser is now logged in.

## Green

Vulnerability #1: Username Enumeration
![image](https://github.com/LMCNN/CS4984/blob/master/GIF/%20Username%20Enumeration.gif)
-Does the presence or absence of a username determine whether the return is fail or failure

Vulnerability #2: Cross-Site Scripting
![image](https://github.com/LMCNN/CS4984/blob/master/GIF/XSS.gif)
-Enter '<script> alert('success!');</script>' in the comment
-A warning window will pop up with 'success!' written on it

## Red

Vulnerability #1: Insecure Direct Object Reference
![image](https://github.com/LMCNN/CS4984/blob/master/GIF/IDOR.gif)
-When I opened the find salesman page and selected a salesmperson, 
 I found that there was a parameter called id at the end of the url.
 So I'm trying to change the value of this parameter. Then it opens 
 another salesperson's page.

Vulnerability #2: Cross-Site Request Forgery
![image](https://github.com/LMCNN/CS4984/blob/master/GIF/CSRF.gif)
-Make an HTML form that edit salesman profile
-submit a comment link with contains this form
-when the admin go to that link, it will edit salesman's profile.

## Notes

Describe any challenges encountered while doing the work
