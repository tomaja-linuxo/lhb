---
author: tomaja
date: "2011-02-01T07:42:03Z"
excerpt: iliti kako će to da izgleda nova <strong>Mandriva 2011</strong>. Osnovna
  promena, kako smo već pisali jeste prelazak na RPM5 i to kako u repoima tako i u
  build sistemu, što je dovelo do, za sada, pomeranja roka za pojavu nove finalne
  Mandrive za dve nedelje. <strong>RPM5</strong> bi trebao da donese brži rad i manje
  problema rpm paketima, što svakako vredi sačekati. Zbog obećanja, a opet zbog ovog
  pomeranja, Mandrivini ljudi su odlučili da daju preview novog sistema, i onoga što
  će biti dostupno u prvoj alfa verziji.
guid: https://forum.linuxo.org/2011/02/01/mandriva-2011-technology-preview/
id: 2476
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Mandriva 2011 Technology Preview
url: /mandriva-2011-technology-preview/
---
iliti kako će to da izgleda nova **Mandriva 2011**. Osnovna promena, kako smo već pisali jeste prelazak na RPM5 i to kako u repoima tako i u build sistemu, što je dovelo do, za sada, pomeranja roka za pojavu nove finalne Mandrive za dve nedelje. **RPM5** bi trebao da donese brži rad i manje problema rpm paketima, što svakako vredi sačekati. Zbog obećanja, a opet zbog ovog pomeranja, Mandrivini ljudi su odlučili da daju preview novog sistema, i onoga što će biti dostupno u prvoj alfa verziji. Pored pomenutog rpm5, tu je _native_ systemd, podrška za _networkmanager_, KDE 4.6.0, kernel 2.6.37, firefox 4b10, X.org server 1.9, clementine 0.6 i mnogo ažuriranih softverskih paketa.

Sada novi _release_ kalendar za Mandrivu 2011 izgleda ovako:  
&#8211; Mandriva 2011 Alpha: 14 februar 2011  
&#8211; Mandriva 2011 Alpha 2: 28 februar 2011  
&#8211; Mandriva 2011 Beta 1: 14 mart 2011  
&#8211; Mandriva 2011 Beta 2: 11 april 2011  
&#8211; Mandriva 2011 RC: 9 maj 2011  
&#8211; Mandriva 2011 Final: 13 jun 2011

Ovaj Technology Preview pokazuje i novi način kako su kreatori Mandrive smislili pokretanje i instalaciju Mandriva Desktop-a. Od sada će biti moguće koristiti isti Mandriva image za pokretanje live sistema, bilo sa cdrom-a ili flash uređaja (moguće je koristiti _Addons/livecd-iso-to-disk_ skriptu koja se nalazi u iso fajlu), ili je instlirati na hard disk. Tako dolazimo do “**Mandriva Desktop**” izdanja koje će zameniti dosadašnja **Mandriva Free** i **Mandriva One** izdanja, koja smo imali sve do 2010.12 verzije.

Ipak, TP, odnosno alfa verziji za sada fali dosta stvari:  
– Networkmanager demon se još uvek ne pokreće automatski pri startu sistema. Da bi se koristio potrebno je pokrenuti `systemctl start networkmanager.service` nakon boot-a.  
– Artwork još uvek nije ažuriran na poslednju verziju.  
– Još uvek ima mnogo bagova koje treba razrešiti.

Ipak, ako ste radoznali da proverite kako je trenutno stanje u Mandriva Cooker-u, i da isproabota rpm5 i native-systemd-powered verziju Mandrive, potražite TP na vašem omiljenom miror serveru – iso fajlovi bi već trebalo da se tamo nalaze.

<p class="download">
  http://ftp.join.uni-muenster.de/pub/linux/distributions/mandrakelinux/devel/iso/2011/
</p>

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=2476)