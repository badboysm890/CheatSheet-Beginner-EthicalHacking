# Beginner Ethical Hacking Cheat Sheet

Note : This guide will help you in the times when you need assistance with any commands and tips regarding some of the topics covered


# SQLMap💉

### Installation 

    sudo apt install sqlmap

### Automatic Analysis

    sqlmap -u “https://target.com/page/”

> Use this method to get basic info if that particular page is vulnerable or not, Note its not always reliable


### Specifying the GET Request Parameter

    sqlmap -u “https://target.com/page?para1=val1&para2=val2”

> Use this when you are sure that when the website accepts that particular parameter

### Asking SQL map to Check if particular parameter is exploitable

    “https://target_site.com/page?p1=value1&p2=value2” -p p1

> Here P1 is the first parameter and using that -p followed by p1 asks SQLmap to check that particular parameter alone.


### Specifying the POST Request Parameter

    sqlmap -u “https://target.com/page/” --data="p1=val1&p2=val2"

> This is very important since lot of web apps use POST request instead of GET request

### When a web app uses Authenticated Session With Cookie

    sqlmap -u “https://target_site.com/page/” --data="p1=value1&p2=value2" --cookie="Session_Cookie_Value"

> Get the Cookie Session for the browser's developer tools in the application section
