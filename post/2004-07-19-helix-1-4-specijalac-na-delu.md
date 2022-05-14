---
author: tomaja
date: "2004-07-19T16:47:58Z"
excerpt: |
  Helix je izvedeni derivat Knoppixa (i to njegove najnovije verzije 3.4)
  tj. Debiana sa specijalnom namenom a to je detekcija i otklanjanje
  havarija na svim Windows  i Linux sistemima iliti na engleskom: <b>incident
  response and forensics (security, monitoring, computer crime,..) .</b>
  Ova zaista gotovo profi distribucija (koja se može instalirati i na
  hard disk) specijalne namene poseduje gomilu Linux ali i Windows alata
  koji nam mogu omogu?iti utvrÄ‘ivanje problema koju su nastali i njihovo
  otklanjanje. Za ovo nam može biti potrebna i sigurna veza sa Internetom
  a to nam sa ovom distribucijom ne?e biti problem: od klasi?nih serijskih
  modema, win modema, lan konekcija, wireless-a, bluetoth-a, IRa, itd. sa
  potrebnim alatima i za detekciju upada na mreže i ra?unare. Tu su
  2.4.26 i 2.6.5 kerneli, FluxBox grafi?ko okruženje sa elementima KDE-a,
  sopstveni kontrolni centar, gomila korisnih editora, xine, vim,
  terminali i sve što nam je potrebno kao i potrebni help. Naravno,
  postoji mogu?nost pristupa NTFS particijama u rw modu što ?e prisutnom
  clamv antivirus programu omogu?iti dezinfekciju windows pariicija.
  Specifi?nost ove distribuicije je i postojanje windows alata koji se
  kroz windows komandni shell vrlo lako mogu  koristiti direktno sa
  CDa. Ja od sada nigde ne idem bez Helix-a :). Sledi spisak specijalnog
  softvera koji se nalazi na CDu (klasi?ne programe i alate koji se
  nalaze na CDu nisam prikazao na spisku)
guid: https://forum.linuxo.org/2004/07/19/helix-1-4-specijalac-na-delu/
id: 484
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Helix 1.4 &#8211; specijalac na delu
url: /helix-1-4-specijalac-na-delu/
---
Helix je izvedeni derivat Knoppixa (i to njegove najnovije verzije 3.4)  
tj. Debiana sa specijalnom namenom a to je detekcija i otklanjanje  
havarija na svim Windows i Linux sistemima iliti na engleskom: **incident  
response and forensics (security, monitoring, computer crime,..) .**  
Ova zaista gotovo profi distribucija (koja se može instalirati i na  
hard disk) specijalne namene poseduje gomilu Linux ali i Windows alata  
koji nam mogu omogu?iti utvrÄ‘ivanje problema koju su nastali i njihovo  
otklanjanje. Za ovo nam može biti potrebna i sigurna veza sa Internetom  
a to nam sa ovom distribucijom ne?e biti problem: od klasi?nih serijskih  
modema, win modema, lan konekcija, wireless-a, bluetoth-a, IRa, itd. sa  
potrebnim alatima i za detekciju upada na mreže i ra?unare. Tu su  
2.4.26 i 2.6.5 kerneli, FluxBox grafi?ko okruženje sa elementima KDE-a,  
sopstveni kontrolni centar, gomila korisnih editora, xine, vim,  
terminali i sve što nam je potrebno kao i potrebni help. Naravno,  
postoji mogu?nost pristupa NTFS particijama u rw modu što ?e prisutnom  
clamv antivirus programu omogu?iti dezinfekciju windows pariicija.  
Specifi?nost ove distribuicije je i postojanje windows alata koji se  
kroz windows komandni shell vrlo lako mogu koristiti direktno sa  
CDa. Ja od sada nigde ne idem bez Helix-a :). Sledi spisak specijalnog  
softvera koji se nalazi na CDu (klasi?ne programe i alate koji se  
nalaze na CDu nisam prikazao na spisku)<!--break-->

Incident Response / Forensics:  
/usr/local/forensics/

  * sleuthkit 1.70 : Brian Carrier&#8217;s replacement to The  
    Coroner&#8217;s Toolkit. 
  * autopsy 2.01 : Web front-end to sleuthkit. Evidence Locker  
    defaults to /var/local/evidence
  * mac-robber 1.0 : TCT&#8217;s graverobber written in C  
    rather than perl
  * fenris .07 : code debugging, tracing, decompiling, reverse  
    engineering tool
  * wipe : wipe a partition securely.
  * secure_delete : securely delete files, swap, memory.
  * MAC_Grab : e-fense MAC time utility.
  * GRAB 1.2 : e-fense Forensic Acquisition Utility (sdd/dd/dcfldd  
    frontend).
  * foremost 0.69 : Carves out files based on header and footer  
    values.
  * fatback 1.3 : Analyze and recover deleted FAT files from Linux.
  * md5deep 1.2 : Recursive md5sum with database lookups.
  * sha15deep 1.2 : Recursive sha1sum with database lookups.
  * dcfldd 1.0 : dd replacement from the guys at the original lab  
    (DOD_DCFL).
  * sdd 1.31 : Specialized dd w/better preformance for different  
    input/output block sizes.
  * PyFLAG 0.62 : Forensic and Log Analysis GUI.
  * Faust 1.13 : A perl script for analyzing elf binaries and bash  
    scripts.
  * e2recover 1.0 : A tool for recovering deleted files in an ext2  
    file system.
  * Pasco 1.0 : Forensic tool for Internet Explorer Analysis.
  * Galleta 1.0 : Cookie analyzer for Internet Explorer.
  * Rifiuti 1.0 : &#8222;Recycle BIN&#8220; analyzer.
  * Bmap 1.0.20 : Detect & Recover data in used slackspace.
  * Ftimes 3.4.0 : A toolset for forensic data acquisition.
  * ChaosReader 0.94 : A tool to trace tcpdump/snoop files and  
    extract application data from it.
  * logsh : A script to log your terminal session (Borrowed from  
    FIRE).

Mrežni alati 

  * LinNeighboorhood 0.6.5-3 : Linux network neighborhood.
  * etherape 0.8.2-3 : Network monitor and visualization tool.
  * ntop 2.1.0 : Network top, protocol analyzer.
  * iptraf 2.7.0-5 : Network monitor.
  * arptool : Monitor and manage arp.
  * arping : Ping hosts by MAC.
  * arpwatch 2.1a11-6.1 : Another arp tool.
  * macchanger 1.4.0-1 : Change your MAC addr. works with wireless  
    too.
  * mtr 0.54-1 : X11 traceroute.
  * samba 3.0.2a-1 : File and print services to SMB/CIFS clients.

Serveri 

  * apache 1.3.29 : Open-source HTTP server.
  * sshd 3.8p1 : Server to provide secure encrypted communications.
  * vnc 3.3.7-1 : Virtual Network Computing.
  * mysql 4.0.18-7 : Open source database server.
  * netcat 1.10 : Networking utility which reads and writes data  
    across network connections.
  * GNU netcat 0.7.1 : Networking utility which reads and writes data  
    across network connections.
  * cryptcat 1.10 : Encrypted networking utility which reads and  
    writes data across network connections.

Packet Sniffers and Assemblers 

  * ethereal 0.10.3-3 : Network traffic analyzer.
  * ettercap 0.6.b-2 : Sniff on a switched network and more.
  * ngrep 1.40.1-3 : Network grep.
  * tcpdump 3.7.2-4 : The main network dump program (libpcap 0.7.2-5).
  * tcpreplay 2.1.1-1 : Replay tcpdump or snoop captures.
  * dsniff 2.4b1 : Doug Songs wonderful sniffing utilities.
  * ipgrab 0.9.8-2 : Pen Register, only gets TCP Header information.
  * TcpTrack 1.1.2 : Sniffer which displays information about TCP  
    connections.

Vulnerability Assessment 

  * nessus 2.0.10a-3 : Best open source vulnerability scanner  
    (username and password is helix).
  * nasl : Command line to nessus to trigger nasl scripts directly.
  * nmap 3.50-1 : The network port mapper (w/ a gui front-end).
  * chkrootkit 0.40 : Look for rootkits.
  * rkhunter 1.1.1 : Rootkit hunter.
  * rpcinfo : Info from RPC.
  * Nikto 1.32-1 : Whisker replacement cgi web vulnerability scanner.
  * hping2 : Port scanner, host enumerator, packet assembler,  
    traceroute on any port.

Wireless alati 

  * airsnort : Sniff, find, crack WEP.
  * airtraf 1.1 : Another wireless locator tool.
  * kismet 2004.04.R1-1 : The best 802.11x monitoring tool.
  * kismet log viewer 0.9.7 : A log management program for kismet.
  * macchanger : Change your MAC address.
  * gpsd : GPS Daemon.
  * Misc : Other wireless information.
  * Patched orinoco drivers by default. 
  * Cisco CVS drivers (cisco_wifix, eth0:wifi0, cisco). 
  * Intel Centrino IWP2100 drivers with hostap for both kernels.
[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=484)