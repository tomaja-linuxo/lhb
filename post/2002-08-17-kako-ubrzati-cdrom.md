---
author: tomaja
date: "2002-08-17T05:06:00Z"
excerpt: "Ako koristite IDE CDrom ureÄ‘aj, koriš?njem  SCSI emulacije možete dobiti<br>\npoprili?no
  ubrzanje u ?itanju i ripovanju diskova. Kako izgleda, dma se\nne <br>\nkoristi za
  IDE drajver (bar ne u 2.4 kernelima). Da bi omogu?ili SCSI \temulaciju,\n<br>\ndodajte
  \"hdx=ide-scsi\" (gde se \"x\" u \"hdx\" zamenjuje sa odgovaraju?im slovom\nza <br>\nvaš
  CDRom ureÄ‘aj) na kraju linije \"kernel\" u  /etc/grub.conf (ukoliko\nkao starter<br>\nza
  Linux koristite grub), ili kao liniju nakon  \"root=/dev/something\"\nu /etc/lilo.conf<br>\n(ukoliko
  koristite lilo)\n"
guid: https://forum.linuxo.org/2002/08/17/kako-ubrzati-cdrom/
id: 212
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Kako ubrzati CDrom
url: /kako-ubrzati-cdrom/
---
Ako koristite IDE CDrom ureÄ‘aj, koriš?njem SCSI emulacije možete dobiti  
poprili?no ubrzanje u ?itanju i ripovanju diskova. Kako izgleda, dma se  
ne  
koristi za IDE drajver (bar ne u 2.4 kernelima). Da bi omogu?ili SCSI emulaciju,  
  
dodajte &#8222;hdx=ide-scsi&#8220; (gde se &#8222;x&#8220; u &#8222;hdx&#8220; zamenjuje sa odgovaraju?im slovom  
za  
vaš CDRom ureÄ‘aj) na kraju linije &#8222;kernel&#8220; u /etc/grub.conf (ukoliko  
kao starter  
za Linux koristite grub), ili kao liniju nakon &#8222;root=/dev/something&#8220;  
u /etc/lilo.conf  
(ukoliko koristite lilo)<!--break-->

Ako za ripovanje audio CDa koristite Grip možete isklju?iti i paranoia  
opciju ?ime dobijate i 2x ve?u brzinu.  
Ovo baš i nije preporu?ljivo osim ako baš niste sigurni u mogu?nosti vašeg  
CD ?ita?a po pitanju kvalitetne  
CDDA ekstrakcije (ili ukoliko ne uživate u kra?im preskakanjima prilikjom  
slušanja muzike)

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=212)