---
author: tomaja
date: "2002-08-15T14:43:41Z"
excerpt: |
  Otkriven je propust u BIND9 DNS serveru u u verzijama pre 9.2.1. Verzije
  u kojima je <br>
  potrebno izvršiti ažuriranje su ML 8.0, 8.1 i 8.2. Naravno, ovo vam je bitno
  samo ako <br>
  imate instaliran DNS server na vašoj mašni.<br>
  Proust ?e uslovitigašenje servera kada rdataset parametar dns_message_findtype()<br>
  funkcije u message.c nije NULL kako bi trebalo da bude. Ovo stanje uzrokuje
  da<br>
  server pošawe izveštaj o grešci i zatvori BIND server.<br>
  Ova greška se može iskoristiti i za napad sa mreže preko specijalnog DNS
  paketa.<br>
  Ovim se jedino može posti?i kreiranje Denial of Service na serveru; stanje
  greške<br>
  se pravilno detektuje, pa tako ne?e biti dozvoljeno napada?u da pokrene
  bilo kakav<br>
  kod na serveru
guid: https://forum.linuxo.org/2002/08/15/bind-9-2-1-sigurnosna-ispravka/
id: 211
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Bind 9.2.1 &#8211; sigurnosna ispravka
url: /bind-9-2-1-sigurnosna-ispravka/
---
Otkriven je propust u BIND9 DNS serveru u u verzijama pre 9.2.1. Verzije  
u kojima je  
potrebno izvršiti ažuriranje su ML 8.0, 8.1 i 8.2. Naravno, ovo vam je bitno  
samo ako  
imate instaliran DNS server na vašoj mašni.  
Proust ?e uslovitigašenje servera kada rdataset parametar dns\_message\_findtype()  
funkcije u message.c nije NULL kako bi trebalo da bude. Ovo stanje uzrokuje  
da  
server pošawe izveštaj o grešci i zatvori BIND server.  
Ova greška se može iskoristiti i za napad sa mreže preko specijalnog DNS  
paketa.  
Ovim se jedino može posti?i kreiranje Denial of Service na serveru; stanje  
greške  
se pravilno detektuje, pa tako ne?e biti dozvoljeno napada?u da pokrene  
bilo kakav  
kod na serveru<!--break--> Update:

Sascha Kettler je uo?io da verzija BIND9 koja je isporu?ena u osnovnohj  
verziji jeste  
ustvari 9.2.1RC1 i pogrrešno ozna?ena kao 9.2.1. paketi koji  
su sada pripremljeni su  
finalna verzija BIND 9.2.1. Ina?e, i buffer overflow u DNS resolver  
bibliotekama je  
takoÄ‘e ispravljen.

Još informacija možete prona?i na: 

 <http://www.kb.cert.org/vuls/id/739123>  
[  
http://cve.mitre.org/cgi-bin/cvename.cgi?name=CAN-2002-0400](http://cve.mitre.org/cgi-bin/cvename.cgi?name=CAN-2002-0400)  
<http://www.kb.cert.org/vuls/id/803539>  
 <http://cve.mitre.org/cgi-bin/cvename.cgi?name=CAN-2002-0651>

Paketi koje treba da ažurirate:

Mandrake Linux 8.2: (i za ostale ML verzije su isti paketi ali naravno  
u drugim direktorijumima)

c871ab517a1f789a134337dc580ab803 8.2/RPMS/bind-9.2.1-2.2mdk.i586.rpm  
15cdebfe14d8a213101d758137364c72 8.2/RPMS/bind-devel-9.2.1-2.2mdk.i586.rpm  
551bb255ed07bb0b257875190c866b42 8.2/RPMS/bind-utils-9.2.1-2.2mdk.i586.rpm  
18145fb072aaad5a7272a00ea4e0c411 8.2/RPMS/caching-nameserver-8.1-3.1mdk.noarch.rpm  
81b76c2f5bddd8b21afc1628aa0fbee3 8.2/SRPMS/bind-9.2.1-2.2mdk.src.rpm  
254bb3d6d6126039688ffa42c2c23a0e 8.2/SRPMS/caching-nameserver-8.1-3.1mdk.src.rpm

Možete koristiti _MandrakeUpdate_ opciju (preporuka) ili pakete možete  
instalirati i ru?no pomo?u  
naredbe 

&#8222;rpm -Fvh *.rpm&#8220;. A list of

listu FTP miroa možete prona?i na:  
<http://www.mandrakesecure.net/en/ftp.php>

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=211)