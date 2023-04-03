# Notes taken of nmap package, used in Bash.

When we attack a device, we need the open ports, to do that we use a port scan.

Ports can be open, closed, or filtered by a firewall. Computers can have up to 65,535 different available ports.

## nmap scanning options [used after ```nmap``` command]
-sS (syn scan), stealthy, faster than TCP, NEED ROOT USER. Sends RST rather than ACK unlike TCP ACK 3-handshake

-sU (UDP scan)

-sT (TCP scan)

-O (OS detection)

-sV (open ports to determine service/device info)

-vv (output verbose)

-oA (saves output in 3 major formats)

-A (runs all scans available)

-T(#1-5) (timing template, higher speeds are noisier)

-p(#) (scans specific port number or port ranges #-#)

-p- (scans all ports)

--script=<scriptname> (activate script from nmap scripting library)
  
To look through our scripts list: ```ls -l /usr/share/nmap/scripts/scripts.db```
  
To look at a specific script: ```cat /usr/share/nmap/scripts/scriptname```
  
To search for specific thing/text: ```grep "______" /usr/....```

To perform a ICMP scan, otherwise known as a ping sweep: ```nmap -sn 192.168.0.1-254```
- Windows by default blocks ICMP packets through its firewall. To get around this, we use:
  
  -```-Pn``` (doesn't ping host before scan, can take a long time to fully scan)
  -````f``` (splits packet/fragments to avoid firewall detection)
  -```--mtu <#>``` (for max transmission size, must be a multiple of 8)
  -```--scan-delay <time in ms>```
  -```--badsum``` (determines presence of firewall)
  
  
