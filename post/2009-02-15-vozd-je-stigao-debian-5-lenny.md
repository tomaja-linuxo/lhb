---
author: tomaja
date: "2009-02-15T16:08:05Z"
excerpt: '<img class=" alignright size-full wp-image-1327" src="https://linuxo.org/wp-content/uploads/2006/09/debian.png"
  alt="Debian" title="Debian" hspace="4" width="93" height="114" align="right" />Nakon
  dugih meseci i&scaron;čekivanja <a href="http://www.debian.org/News/2009/20090214">Debian
  5</a> je konačno stigao donoseći dosta unapređenja u odnosu na svog predhodnika:
  Java je konačno u Debianovim repozitorijumima&nbsp; zahvaljujući IcedTea-u i OpenJDK;
  Firefox (odnosno Iceweasel) je konačno stigao do verzije 3.0&nbsp; (tačnije 3.0.6.),
  a tu je i Gnome 2.22, KDE 3.5.9, OpenOffice.org 2.4.1; Ovaj put izbor i svežina
  softverskih paketa nisu tako lo&scaron;i, mada skoro 22 meseca od poslednje verzije
  i dalje daje prilično lo&scaron; utisak. Za sada nema izgleda da će se to mnogo
  popraviti. Da ne bi zanovetali previ&scaron;e, pravo vreme je vreme da vidimo &scaron;ta
  je novo u Lenniju:'
guid: https://forum.linuxo.org/2009/02/15/vozd-je-stigao-debian-5-lenny/
id: 2225
image: /wp-content/uploads/2006/09/debian.png
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";s:4:"1327";s:11:"_thumb_type";s:5:"thumb";}
title: 'Vožd je stigao: Debian 5 (Lenny)'
url: /vozd-je-stigao-debian-5-lenny/
---
<img class=" alignright size-full wp-image-1327" src="https://linuxo.org/wp-content/uploads/2006/09/debian.png" alt="Debian" title="Debian" hspace="4" width="93" height="114" align="right" />Nakon dugih meseci i&scaron;čekivanja [Debian 5](http://www.debian.org/News/2009/20090214) je konačno stigao donoseći dosta unapređenja u odnosu na svog predhodnika: Java je konačno u Debianovim repozitorijumima&nbsp; zahvaljujući IcedTea-u i OpenJDK; Firefox (odnosno Iceweasel) je konačno stigao do verzije 3.0&nbsp; (tačnije 3.0.6.), a tu je i Gnome 2.22, KDE 3.5.9, OpenOffice.org 2.4.1; Ovaj put izbor i svežina softverskih paketa nisu tako lo&scaron;i, mada skoro 22 meseca od poslednje verzije i dalje daje prilično lo&scaron; utisak. Za sada nema izgleda da će se to mnogo popraviti. Da ne bi zanovetali previ&scaron;e, pravo vreme je vreme da vidimo &scaron;ta je novo u Lenniju:<!--break-->

  * SELinux ije instaliran kao default opcija prilikom novih insltalacija. Ukoliko se radi upgrade sistem&nbsp; sa prethodne verzije potrebno je pokrenuti komandu "_aptitude install selinux-basics_" kao root korisnik. Naravno, treba znati da iako je SELinux is instaliran, to neznači i da je uključen po default-u, pa bi za to trebalo slediti sledeće [instrukcije](http://wiki.debian.org/SELinux/Setup)
  * Iceweasel (Firefox) i Icedove (Thunderbird) su "unapređeni" iz 2.0 u 3.0 i&nbsp; iz&nbsp; 1.5 u 2.0, &scaron;to će verovatno usrećiti veći broj korisnika.
  * Debian se sada zvanično može pokretati u live modu. Za to treba pogledati [Debian Live! stranicu](http://debian-live.alioth.debian.org/).
  * Kao &scaron;to već napomenusmo Java je konačno u Debianu. Da bi je pokrenuli, treba instalirati openjdk-6-jre ili openjdk-6-jdk pakete.
  * Debian 5.0 doalzi za sada o&scaron; uvek aktuelnim 2.6.26 kernelom (mada bez podr&scaron;ke za ext4), koji uključuje NTFS-3g i podr&scaron;ku za KVM.
  * X.org 7.3 koristi auto pode&scaron;avanje hardvera kao standardnu opciju za veliki broj grafičkih komponenti.
  * Lenny takođe donosi sjajnu podr&scaron;ku za najpolpularnije netbook računare, poput Eee PC-ja koji je dobio sopstveni paket ACPI "out of the box" skipti.
  * Podr&scaron;ka za 32-bit SPARC je izbačena, ali je ubačena za ARM EABI ("armel").
  * Zaista je mnogo toga na svom mestu a opet obnovljeno. Gotovo 3/4 svih softverskih paketa je ažurirano, pa sada tako Lenny sadrži preko&nbsp; 7700 novih, &scaron;to čini da ukupan broj prelazi&nbsp; 23,000.

Novi Lenny se može preuzeti sa ogromnog broja **[HTTP/FTP](http://www.debian.org/CD/http-ftp/)** mirora, **[BitTorrent-a](http://www.debian.org/CD/torrent-cd/)** ili&nbsp; **[Jigdo](http://www.debian.org/CD/jigdo-cd/)**-a. Uživajte. 

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=2225)