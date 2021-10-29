# Unit-9 CodePath Written Assignment
Project 8 - Pentesting Live Targets

Time spent: 2 hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The three exploits I used:


**SQL Injection (SQLi) - Blue 
**Cross-Site Scripting (XSS) - Green
**Session Hijacking/Fixation - Red

Each color is vulnerable to only 2 of the 6 possible exploits. First discover which color has the specific vulnerability, then write a short description of how to exploit it, and finally demonstrate it using screenshots compiled into a GIF.

## Blue

Vulnerability #1: SQL Injection

Description: Use a SQL Injection to manipulate data values in a SQL database. The idea is to trigger a response, that there is a vulnerability in the SQL database, meaning you are pushing information to the dataset causing a response. 

![bluevulnerability](https://user-images.githubusercontent.com/64348938/115821657-08b01700-a3b8-11eb-982f-1cbae07195af.png)

![bluevulnerabilityimage2](https://user-images.githubusercontent.com/64348938/115821701-1ebdd780-a3b8-11eb-8e9f-e29a9bc5e5d5.png)

## Green

Vulnerability #1: XSS Cross Site Scripting

Description: The idea is to find a script that will trigger an alert tag. Here, I inputted a script tag in the comment section and triggered an alert when logged in as an admin. However, a more malicious action for an attacker is to create an SQLi injection with a malicious script that reveals senstive information such as user data.

![greenvulnerability](https://user-images.githubusercontent.com/64348938/115822051-bcb1a200-a3b8-11eb-90aa-5dd96a9c2003.png)

![greenvulnerability2](https://user-images.githubusercontent.com/64348938/115822118-d9e67080-a3b8-11eb-8c15-2392b62cd1f7.png)


## Red

Vulnerability #1: Session Fixation

Description: The idea is to use a session ID and URL to trick a user into using the session ID URL to log into their system or account; therefore gaining access to their information. Here, you navigate to the developer console, find cache, cookie session, then query value add to the end of string, URL. However, it is important to make sure the attackee is logged in first. That way the attack and the attackee sesssion mirror each other, allowing attacker to gain info from attackee.

![redsessionhijackingchrome](https://user-images.githubusercontent.com/64348938/116763472-550be000-a9d2-11eb-84f6-16fca7800878.png)

![redsessionhijackingsafari](https://user-images.githubusercontent.com/64348938/115822586-a6581600-a3b9-11eb-8030-43be6afcffbb.png)



## Notes

I encountered an issue with appending the session ID to the end of the URL for hijacking fixation. I tried several query string names, such as PHSESSION, SESSION, etc. Eventually, I figured out the correct query string name. 
