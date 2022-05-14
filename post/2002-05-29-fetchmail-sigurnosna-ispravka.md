---
author: tomaja
date: "2002-05-29T17:24:00Z"
excerpt: |
  <p>Otkriven je problem u verzijama pre 5.9.10<br />
  koji se ticao prijema pošte sa IMAP servera. Fetchmail klijent alocira trag<br />
  radi smeštanja veličine poruka koje će kasnije primiti.<br />
  Ovaj trag se određuje na osnovu broja poruka koji je prijavljen<br />
  od strane servera, tako da fetchmailne će proveravati da li je<br />
  taj broj poruka preveliki. Ovo može dovesti do toga da sa neproverni server<br />
  može navesti fetchmail da upisuje podatke van dozovoljenih granica.
guid: https://forum.linuxo.org/2002/05/29/fetchmail-sigurnosna-ispravka/
id: 182
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: fetchmail &#8211; sigurnosna ispravka
url: /fetchmail-sigurnosna-ispravka/
---
Otkriven je problem u verzijama pre 5.9.10  
koji se ticao prijema pošte sa IMAP servera. Fetchmail klijent alocira trag  
radi smeštanja veličine poruka koje će kasnije primiti.  
Ovaj trag se određuje na osnovu broja poruka koji je prijavljen  
od strane servera, tako da fetchmailne će proveravati da li je  
taj broj poruka preveliki. Ovo može dovesti do toga da sa neproverni server  
može navesti fetchmail da upisuje podatke van dozovoljenih granica.<!--break-->

  
Za detalje pogledajte:

[http://tuxedo.org/~esr/fetchmail/NEWS](http://tuxedo.org/%7Eesr/fetchmail/NEWS)  
<http://cve.mitre.org/cgi-bin/cvename.cgi?name=CAN-2002-0146>

Za upgrade koristite _MandrakeUpdate_.  
Ukoliko želite da paket ažurirate ručno, skinite ga sa nekog od Mandarake FTP  
servera i instalirajte ga pomoću komande "rpm -Fvh *.rpm".  
listu dostupnih FTP mirora možete videti na adresi:</p> 

http://www.mandrakesecure.net/en/ftp.php</a>

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=182)