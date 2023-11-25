1. Echange ARP
## 🌞Générer des requêtes ARP
```
[tanguy@localhost ~]$ ping 10.3.1.11
PING 10.3.1.11 (10.3.1.11) 56(84) bytes of data.
64 bytes from 10.3.1.11: icmp_seq=1 ttl=64 time=0.127 ms
64 bytes from 10.3.1.11: icmp_seq=2 ttl=64 time=0.069 ms
64 bytes from 10.3.1.11: icmp_seq=3 ttl=64 time=0.078 ms
64 bytes from 10.3.1.11: icmp_seq=4 ttl=64 time=0.101 ms
64 bytes from 10.3.1.11: icmp_seq=5 ttl=64 time=0.092 ms
^C
--- 10.3.1.11 ping statistics ---
5 packets transmitted, 5 received, 0% packet loss, time 4088ms
rtt min/avg/max/mdev = 0.069/0.093/0.127/0.020 ms

Ping 10.3.1.12 avec 32 octets de données :
Réponse de 10.3.1.12 : octets=32 temps=2 ms TTL=64
Réponse de 10.3.1.12 : octets=32 temps=1 ms TTL=64
Réponse de 10.3.1.12 : octets=32 temps=1 ms TTL=64
Réponse de 10.3.1.12 : octets=32 temps=1 ms TTL=64

Statistiques Ping pour 10.3.1.12:
    Paquets : envoyés = 4, reçus = 4, perdus = 0 (perte 0%),
Durée approximative des boucles en millisecondes :
    Minimum = 1ms, Maximum = 2ms, Moyenne = 1ms
```
```
Interface�: 10.3.1.1 --- 0x13
  Adresse Internet      Adresse physique      Type
  10.3.1.11             08-00-27-ce-87-27     dynamique
  10.3.1.12             08-00-27-18-93-41     dynamique
  10.3.1.255            ff-ff-ff-ff-ff-ff     statique
  224.0.0.22            01-00-5e-00-00-16     statique
  224.0.0.251           01-00-5e-00-00-fb     statique
  224.0.0.252           01-00-5e-00-00-fc     statique
  239.255.255.250       01-00-5e-7f-ff-fa     statique
PS C:\Users\T>
```
MAC = 
[tanguy@localhost ~]$ ip n show
10.3.1.11 dev enp0s3 lladdr 08:00:27:ce:87:27 reachable
10.3.1.1 dev enp00s3 lladdr 0a:00:27:00:00:13 stale

MAC john = 08:00:27:00:00:13

[tanguy@localhost ~]$ ip n show
10.3.1.12 dev enp0s3 lladdr 08:00:27:00:00:13 stale
10.3.1.1 dev enp00s3 lladdr 0a:00:27:18:93:41 stale

Preuve que marcel est marcel depuis john
08:00:27:00:00:13 

preuve que john est john depuis marcel 
08:00:27:ce:87:27
```

2. Anlayse de trames 

Analyse de trames

```

john

dropped privs to tcpdump
tcpdump: verbose output suppressed, use -v[v]... for full protocol decode
listening on enp0s8, link-type EN10MB (Ethernet), snapshot length 262144 bytes
12:11:40.420989 IP localhost.localdomain.ssh > 10.3.1.1.54552: Flags [P.], seq 621814460:621814520, ack 2084233302, win 501, length 60
12:11:40.421738 IP localhost.localdomain.ssh > 10.3.1.1.54552: Flags [P.], seq 60:96, ack 1, win 501, length 36
12:11:40.422030 IP 10.3.1.1.54552 > localhost.localdomain.ssh: Flags [.], ack 96, win 1022, length 0