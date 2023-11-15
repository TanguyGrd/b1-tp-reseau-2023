## 🌞 Déterminez, pour ces 5 applications, si c'est du TCP ou de l'UDP
```
 [Discord.exe]
 IP et Port serveur:34.111.115.192:443
 Port local ouvert: 443 
  TCP    10.33.78.60:51740      34.111.115.192:443     ESTABLISHED

  [SearchApp.exe]
  IP et Port serveur:10.33.78.60:59745 
  Port local ouvert: 443 
  TCP    10.33.78.60:59745      20.199.120.151:443     ESTABLISHED

   [chrome.exe]
   IP et Port serveur :  34.120.22.49:443  
   Port local ouvert :52652 
  TCP    10.33.78.60:52652      34.120.22.49:443       ESTABLISHED

  [Teams.exe]
  IP et Port serveur: 52.123.137.147:443 
  Port local ouvert:64339 
  TCP    10.33.78.60:64339      52.123.137.147:443     ESTABLISHED

   [Wireshark.exe]
    IP et Port serveur: 20.199.120.85:443 
  Port local ouvert:49419 
  TCP    10.33.78.60:49419      20.199.120.85:443      ESTABLISHED
```
## Demandez l'avis a l'os
```
netstat -a -b -n 
```
  ```
  ||. Setp virtuel 

  SSH 

## 🌞 Examinez le trafic dans Wireshark

 Déterminez si SSH utilise TCP ou UDP
 
 ```
 ssh utilise un TCP
 ```
 
## 🌞 Demandez aux OS

Depuis ma machine: [ssh.exe] TCP    10.5.1.12:55692        10.5.1.11:22                      

Depuis la VM:State   Recv-Q  Send-Q   Local Address:Port   Peer Address:Port  Process
LISTEN  0       128            0.0.0.0:22          0.0.0.0:*      users:(("sshd",pid=678,fd=3))
ESTAB   0       0            10.5.1.11:22        10.5.1.12:55692  users:(("sshd",pid=1283,fd=4),("sshd",pid=1268,fd=4))
LISTEN  0       128               [::]:22             [::]:*      users:(("sshd",pid=678,fd=4))


