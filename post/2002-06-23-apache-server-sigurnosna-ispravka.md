---
author: tomaja
date: "2002-06-23T04:55:51Z"
excerpt: |
  MandrakeSoft toplo preporu?uje svim korisnicima Mandrake Linux-a da <br>
  izvrše ažuriranje svoje Apache instalacije. Za ono što se mislilo da je <br>
  DoS-only ranjivost sada je i dokazano ali je i više od toga;<br>
  mogu?nost upada je otkrivena i na 32bit i 64bit platformama. <br>
  Uspešno koriš?enje ove ranjivosti može doesti do izvršavanja <br>
  bilo kog koda na serveru sa ovim ranjivim Apache-om sa ovlaš?enjima<br>
  web serverovog child procesa (na Mandrake Linux-u ovo je korisni?ki<br>
  "apache").  Ovo može biti iskoriš?eno i za upade koji nisu vezani za <br>
  Apache ve? za lokalni sistem i potencijalno pristup root ovlaš?enja.
guid: https://forum.linuxo.org/2002/06/23/apache-server-sigurnosna-ispravka/
id: 191
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Apache server &#8211; sigurnosna ispravka
url: /apache-server-sigurnosna-ispravka/
---
MandrakeSoft toplo preporu?uje svim korisnicima Mandrake Linux-a da  
izvrše ažuriranje svoje Apache instalacije. Za ono što se mislilo da je  
DoS-only ranjivost sada je i dokazano ali je i više od toga;  
mogu?nost upada je otkrivena i na 32bit i 64bit platformama.  
Uspešno koriš?enje ove ranjivosti može doesti do izvršavanja  
bilo kog koda na serveru sa ovim ranjivim Apache-om sa ovlaš?enjima  
web serverovog child procesa (na Mandrake Linux-u ovo je korisni?ki  
&#8222;apache&#8220;). Ovo može biti iskoriš?eno i za upade koji nisu vezani za  
Apache ve? za lokalni sistem i potencijalno pristup root ovlaš?enja.<!--break-->

  
Zahvaljujemo se Gobbles-u za dokazivanje ovo baga.  
Zbog toga što je ovaj bag poznat i vezan za ve?inu platformi, ovaj update  
treba smatreati vitalno važnim i treba ga odmah izvesti.

Sve verzije Apache servera od 1.3.26 i 2.0.37 su osetljive na ovaj bag.  
MandrakeSoft je obezbedio patched verzije Apache-a za ispravljanje  
ovog baga.

Napomena; Ovi paketi se ne razlikuju od onih koji su dati u  
MDKSA-2002:039-1 tako da ako ste ve? uradili update, nema  
novih paketa za upgrade.

Više o ovome možete saznati sa slede?ih linkova:

[http://httpd.apache.org/info/security\_bulletin\_20020620.txt](http://httpd.apache.org/info/security_bulletin_20020620.txt)  
<http://online.securityfocus.com/news/493>  
<http://cve.mitre.org/cgi-bin/cvename.cgi?name=CAN-2002-0392>

Da bi ažuriranje (upgrade) izvršili automatski, koristite _MandrakeUpdate  
_ opciju.  
Verifikacija md5 kju?eva i GPG potpisa se izvodi automatski.

Ukoliko želite da paket instalirate ru?no, skinite ga sa jednog od Mandrake  
  
FTP server mirora i pokrenite komandu &#8222;rpm -Fvh *.rpm&#8220;. Listu postoje?ih  
FTP mirora možete videti na:

 <http://www.mandrakesecure.net/en/ftp.php>

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=191)