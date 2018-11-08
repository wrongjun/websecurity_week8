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

Vulnerability #1: SQL Injection (SQLi)

Vulnerability #2: __________________


## Green

Vulnerability #1:Username Enumeration
    Username Enumeration was found on the green site at login.php.
    If the username is accurate, with the user name pperson
        **Log in was unsuccessful**
    If the username is not a user,
        *Log in was unsuccessful*
    This volunability give away the user name, then attack can brute force all the combination of the password or find out al the relative information such as name, email, password, other realtive website.
        

Vulnerability #2: Cross-Site Scripting (XSS)
    Cross-Site Scripting was found on the green site at contact.php. Feedback textbox is enable the usage of srcript. Once admin open up the feedback, it will run the sript.<br />
    \<script\>alert('Two found the XSS!');\</script\> <br />
    Since one of acctacker redirect the url to facebook before the order of my script, My script was not successful runed, but the vunlunerablity was existed.
    

## Red

Vulnerability #1: Insecure Direct Object Reference (IDOR)
    An IDOR was found on the red site at salesperson.php.
      https://35.184.88.145/red/public/salesperson.php?id=X
    At the id x, we can input a number and direct us to the reference oject, but there are obect is secured and should not display to the public. There is not protected process to secure private information.

Vulnerability #2: __________________

## Resources
GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes



