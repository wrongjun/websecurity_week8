# Project 8 - Pentesting Live Targets

Time spent: 7 hours spent in total

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

Vulnerability #1: __________________

Vulnerability #2: __________________


## Green

Vulnerability #1: __________________

Vulnerability #2: __________________


## Red

Vulnerability #1: Insecure Direct Object Reference (IDOR)
    An IDOR was found on the red site at salesperson.php.
      https://35.184.88.145/red/public/salesperson.php?id=X
    At the id x, we can input a number and direct us to the reference oject, but there are obect is secured and should not
    display to the public. There is not protected process to secure private information.

Vulnerability #2: __________________


## Notes

Describe any challenges encountered while doing the work


