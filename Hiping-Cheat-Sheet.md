
# Hping3🥴

### Intro :

**hping is a command-line oriented TCP/IP packet assembler/analyzer. The interface is inspired to the ping(8) unix command, but hping isn’t only able to send ICMP echo requests. It supports TCP, UDP, ICMP and RAW-IP protocols, has a traceroute mode, the ability to send files between a covered channel, and many other features..**

> Its free to use and also we can use it in different ways possible

    hping3 -h

Use these options :

> Mode  
default mode TCP  
-0 --rawip RAW IP mode  
-1 --icmp ICMP mode  
-2 --udp UDP mode  
-8 --scan SCAN mode.  
Example: hping --scan 1-30,70-90 -S www.target.host  
-9 --listen listen mode

 IP  Related Stuffs

> -a --spoof spoof source address  
> --rand-dest random destionation address mode. see the man.  
> --rand-source random source address mode. see the man.  
> -t --ttl ttl (default 64)  
> -N --id id (default random)  
> -W --winid use win* id byte ordering  
> -r --rel relativize id field (to estimate host traffic)  
> -f --frag split packets in more frag. (may pass weak acl)  
> -x --morefrag set more fragments flag  
> -y --dontfrag set don't fragment flag  
> -g --fragoff set the fragment offset  
> -m --mtu set virtual mtu, implies --frag if packet size > mtu  
> -o --tos type of service (default 0x00), try --tos help  
> -G --rroute includes RECORD_ROUTE option and display the route buffer  
> --lsrr loose source routing and record route  
> --ssrr strict source routing and record route  
> -H --ipproto set the IP protocol field, only in RAW IP mode

Common  

> -d --data data size (default is 0)  
> -E --file data from file  
> -e --sign add 'signature'  
> -j --dump dump packets in hex  
> -J --print dump printable characters  
> -B --safe enable 'safe' protocol  
> -u --end tell you when --file reached EOF and prevent rewind  
> -T --traceroute traceroute mode (implies --bind and --ttl 1)  
> --tr-stop Exit when receive the first not ICMP in traceroute mode  
> --tr-keep-ttl Keep the source TTL fixed, useful to monitor just one hop  
> --tr-no-rtt Don't calculate/show RTT information in traceroute mode   ARS packet description (new, unstable)  
> --apd-send Send the packet described with APD (see docs/APD.txt)
