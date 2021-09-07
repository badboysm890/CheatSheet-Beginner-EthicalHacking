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
