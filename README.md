# Cyber-Security-Assignment-8
# Project 8 - Pentesting Live Targets

Time spent: 4 hours spent in total

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

Vulnerability #1: Challenge 3: SQL Injection
Details: Injecting a SQL statement in the URL will actually cause the statement to process. Here the statement 'OR SLEEP(10)--' was used to cause a 10 second delay before reloading the page.
![](https://imgur.com/a/dChR4)

Vulnerability #2: Challenge 6: Session Hijacking/fixation
Details: Copying and pasting the URL from the red site, and changing red to blue, will work to bypass privledgies in the blue site without even being logged in.
https://imgur.com/a/wicgr
## Green

Vulnerability #1: Challenge 1: Username Enumeration
Details: Logging in at the green site, incorrect username will cause the "Log in was unsuccessful" will be plain text, Valid username but incorrect password will force "Log in was unsuccessful" to be bold. This allows you to verify if a username is valid or not (security flaw)
https://imgur.com/a/XLxJW

Vulnerability #2: Challenge 4: XSS
Details: Posting a simple XSS command in the contact us section, will force an alert message when someone clicks the feedback button.
https://imgur.com/a/2sVRf


## Red

Vulnerability #1: Challenge 2: Insecure Direct Object Refference
Details: You can manupulate the URL to change the ID of the salesperson you are viewing. This allows access to people that cannot be seen in the IDOR. Here I changed ID=1 to ID=11 and a mysterious person appeared.
https://imgur.com/a/gQjFm

Vulnerability #2: Challenge 5: CSRF
Details: Creating a post form and sending it too a given site (our give address) will create a new salesperson. Here I created a Allie Med but opening up the csrf file.
https://imgur.com/a/dbvlo


## Notes

Describe any challenges encountered while doing the work
