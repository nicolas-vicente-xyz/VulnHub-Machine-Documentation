# De-ICE: S1.100

## Machine Scenario 
The scenario for this LiveCD is that a CEO of a small company has been pressured by the Board of Directors to have a penetration test done within the company. The CEO, believing his company is secure, feels this is a huge waste of money, especially since he already has a company scan their network for vulnerabilities (using nessus). To make the BoD happy, he decides to hire you for a 5-day job; and because he really doesn't believe the company is insecure, he has contracted you to look at only one server - a old system that only has a web-based list of the company's contact information.

The CEO expects you to prove that the admins of the box follow all proper accepted security practices, and that you will not be able to obtain access to the box. Prove to him that a full penetration test of their entire corporation would be the best way to ensure his company is actually following best security practices.

## Reconnaissance

### Nmap Scan

```bash
# Nmap 7.98 scan initiated Mon Apr  6 18:33:48 2026 as: /usr/lib/nmap/nmap --privileged -T4 -A -p- -oN nmap_results.txt 192.168.1.100
Nmap scan report for 192.168.1.100
Host is up (0.0014s latency).
Not shown: 65527 filtered tcp ports (no-response)
PORT    STATE  SERVICE  VERSION
20/tcp  closed ftp-data
21/tcp  open   ftp      vsftpd (broken: could not bind listening IPv4 socket)
22/tcp  open   ssh      OpenSSH 4.3 (protocol 1.99)
|_sshv1: Server supports SSHv1
| ssh-hostkey:
|   2048 83:4f:8b:e9:ea:84:20:0d:3d:11:2b:f0:90:ca:79:1c (RSA1)
|   2048 6f:db:a5:12:68:cd:ad:a9:9c:cd:1e:7b:97:1a:4c:9f (DSA)
|_  2048 ab:ab:a8:ad:a2:f2:fd:c2:6f:05:99:69:40:54:ec:10 (RSA)
25/tcp  open   smtp?
|_smtp-commands: Couldn't establish connection on port 25
80/tcp  open   http     Apache httpd 2.0.55 ((Unix) PHP/5.1.2)
|_http-server-header: Apache/2.0.55 (Unix) PHP/5.1.2
|_http-title: Site doesn't have a title (text/html).
110/tcp open   pop3     Openwall popa3d
143/tcp open   imap     UW imapd 2004.357
|_imap-capabilities: IMAP4REV1 SASL-IR NAMESPACE MULTIAPPEND SORT THREAD=REFERENCES MAILBOX-REFERRALS AUTH=LOGINA0001 IDLE LOGIN-REFERRALS LITERAL+ CAPABILITY completed UNSELECT STARTTLS THREAD=ORDEREDSUBJECT SCAN BINARY OK
443/tcp closed https
MAC Address: 00:0C:29:D5:02:0A (VMware)
Aggressive OS guesses: Linux 2.6.13 - 2.6.32 (96%), Linux 2.6.18 - 2.6.32 (95%), Linux 2.6.22 - 2.6.23 (95%), SonicWALL Aventail EX-6000 VPN appliance (94%), Linux 2.6.16 - 2.6.21 (92%), Linux 2.6.16 - 2.6.25 (92%), Linux 2.6.23 (92%), Linux 2.6.17 - 2.6.36 (92%), Linux 2.6.9 - 2.6.24 (92%), Linux 2.6.9 - 2.6.30 (92%)
No exact OS matches for host (test conditions non-ideal).
Network Distance: 1 hop
Service Info: OS: Unix

TRACEROUTE
HOP RTT     ADDRESS
1   1.42 ms 192.168.1.100

OS and Service detection performed. Please report any incorrect results at <https://nmap.org/submit/> .
# Nmap done at Mon Apr  6 18:40:31 2026 -- 1 IP address (1 host up) scanned in 402.90 seconds
```
