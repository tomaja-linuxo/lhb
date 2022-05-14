---
author: tomaja
date: "2004-10-10T19:59:02Z"
excerpt: |
  Za sve koji imaju mdk 10.1, da bi pokrenuli Intel-ov modem treba da urade sledece:<br />
  1) Otvoriti terminal i logovati se kao root sa "su"<br />
  2) Ako postoji direktorijum /usr/src/verzija_kernela/.tmp_versions i fajl /usr/src/verzija_kernela/.__modpost.cmd onda ih treba izbrisati.<br />
  3) Raspakovati arhivu sa drajverom, uci u direktorijum intel-536EP-2.56.76.0 i uraditi "make clean"<br />
  ...
guid: https://forum.linuxo.org/2004/10/10/instaliranje-drajvera-za-intel-ov-modem-na-mdk-10-1/
id: 558
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Instaliranje drajvera za Intel-ov modem na mdk 10.1
url: /instaliranje-drajvera-za-intel-ov-modem-na-mdk-10-1/
---
Za sve koji imaju mdk 10.1, da bi pokrenuli Intel-ov modem treba da urade sledece:  
1) Otvoriti terminal i logovati se kao root sa &#8222;su&#8220;  
2) Ako postoji direktorijum /usr/src/verzija\_kernela/.tmp\_versions i fajl /usr/src/verzija\_kernela/.\__modpost.cmd onda ih treba izbrisati.  
3) Raspakovati arhivu sa drajverom, uci u direktorijum intel-536EP-2.56.76.0 i uraditi &#8222;make clean&#8220;  
&#8230;<!--break-->) U fajlu coredrv.c koji se nalazi u direktorijumu coredrv, ubaciti &#8222;//&#8220; na pocetku redova 295-297 tako da izgledaju ovako:

// case PM\_SAVE\_STATE:  
// printk(KERN_WARNING&#8220;Saving power state is not implemented  
&#8222;);  
// break;

Ove tri linije koda i onako nemaju neku korisnu ulogu pa se mogu slobodno i izbaciti, da bi se komajliranje moglo uspesno izvrsiti.

5) Iz direktorijuma intel-536EP-2.56.76.0 treba uraditi &#8222;make 536&#8220;.

6) Nakon toga &#8222;make install&#8220;

Ovo uputstvo vazi za sledece drajvere:

intel-536EP-2.56.76.0  
intel-536ep-4.69  
intel-536ep-4.69-mdk10-up

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=558)