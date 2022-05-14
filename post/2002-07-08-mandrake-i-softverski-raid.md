---
author: tomaja
date: "2002-07-08T18:29:00Z"
excerpt: |
  Kao što možda ve? znate, <a href="http://www.mandrakelinux.com/en/demos/Demo/Mandrake8.2/Install/Expert/images/expertA6.png" target="_blank">DrakX</a>,
  grafi?ki instalacioni program za Mandrake Linux poseduje veoma mo?an program
  za particioniranje hard diskova. On ve? podržava široki spektar journaling faj
  sistema (reiserfs, ext3, xfs, jfs), Linux softverski RAID, LVM, promenu veli?ine
  Windows particija... pa ipak jedna važna stvar nedostaje: detekcija postoje?eg
  softverskog RAID-a. Sada je i to rešeno.
guid: https://forum.linuxo.org/2002/07/08/mandrake-i-softverski-raid/
id: 196
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Mandrake i softverski RAID
url: /mandrake-i-softverski-raid/
---
Kao što možda ve? znate, <a href="http://www.mandrakelinux.com/en/demos/Demo/Mandrake8.2/Install/Expert/images/expertA6.png" target="_blank">DrakX</a>,  
grafi?ki instalacioni program za Mandrake Linux poseduje veoma mo?an program  
za particioniranje hard diskova. On ve? podržava široki spektar journaling faj  
sistema (reiserfs, ext3, xfs, jfs), Linux softverski RAID, LVM, promenu veli?ine  
Windows particija&#8230; pa ipak jedna važna stvar nedostaje: detekcija postoje?eg  
softverskog RAID-a. Sada je i to rešeno.<!--break-->U stvari, osnovna podrška je davno kreirana, ali je bila bazirana na ioctl-u

  
koji postavlja upit kernelu za &#8222;autodetekcijut&#8220; RAID-a&#8230; a ioctl  
se ne može kompajlirati kao &#8222;md.o&#8220;, Linux Software RAID driver, što  
je bitno ako želimo da kernel ostane što manji po veli?ini. Ipak, DrakX glavni  
developer, Pixel,je ru?no uspeo da reši problem i od sada Mandrake instaler  
može da prepoyna vašu postoje?e RAID particije! 

Veliki plus za Linux Software RAID korisnike, o?igledno. 

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=196)