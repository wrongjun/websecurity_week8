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
    SQL injection was found on the blue site at salesperson.php?id=1. User can perform time delay attack to the database
    by 
    salesperson.php?id=1' or sleep(5)=1--'
<br />
-GIF Walkthrough: <img src="https://github.com/wrongjun/websecurity_week8/blob/master/blue_sql.gif" width="700">
    
    
Vulnerability #2: Session Hijacking/Fixation
    Session Hijacking was found on the blue site. The session id is different for differen browser and changed with each open and close. Since the all the website share the same session id for login, when user login in to other browser and get the session id, they can use this session id to login at other bworser without entering username and password.
<br />
-GIF Walkthrough: <img src="https://github.com/wrongjun/websecurity_week8/blob/master/session_blue.gif " width="700">
## Green

Vulnerability #1:Username Enumeration
    Username Enumeration was found on the green site at login.php.
    If the username is accurate, with the user name pperson
        **Log in was unsuccessful**
    If the username is not a user,
        *Log in was unsuccessful*
    This volunability give away the user name, then attack can brute force all the combination of the password or find out al the relative information such as name, email, password, other realtive website.
<br />
-[]GIF Walkthrough: <img src="https://github.com/wrongjun/websecurity_week8/blob/master/green_user.gif " width="700">      


Vulnerability #2: Cross-Site Scripting (XSS)
    Cross-Site Scripting was found on the green site at contact.php. Feedback textbox is enable the usage of srcript. Once admin open up the feedback, it will run the sript.<br />
    \<script\>alert('Two found the XSS!');\</script\> <br />
    Since one of acctacker redirect the url to facebook before the order of my script, My script was not successful runed, but the vunlunerablity was existed.
<br />
-[]GIF Walkthrough: <img src="https://github.com/wrongjun/websecurity_week8/blob/master/green_xss.gif" width="700">    

## Red

Vulnerability #1: Insecure Direct Object Reference (IDOR)
    An IDOR was found on the red site at salesperson.php.
      https://35.184.88.145/red/public/salesperson.php?id=X
    At the id x, we can input a number and direct us to the reference oject, but there are obect is secured and should not display to the public. There is not protected process to secure private information.
    <br />
-[]GIF Walkthrough: <img src="https://github.com/wrongjun/websecurity_week8/blob/master/red_csrf.gif" width="700">


Vulnerability #2:Cross-Site Request Forgery (CSRF)
    Red site dont required CSRF token to perorm edition such as change saleperson and country. CSRF token is generated when admin was login, which mean attacker can edit the information without login as admin. They can perfrom attack through the usage of php.
<br />
-[]GIF Walkthrough: <img src="https://github.com/wrongjun/websecurity_week8/blob/master/blue_sql.gif" width="700">
## Resources
-GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes



