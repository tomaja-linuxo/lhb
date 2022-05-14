---
author: merjadok
date: "2003-01-30T07:39:32Z"
excerpt: |
  Najbolji izvor RPM paketa za instalaciju Mplayer-a se nalazi na adresi: http://www.piorunek.pl/~dominik/linux/pkgs/mplayer/ . Sa njega treba skinuti slede?e RPM fajlove:
  <br />

  <br />
  -1. mplayer-common-0.90pre8-1.i386.rpm
  <br />
  -2. mplayer-0.90pre8-1.i386.rpm
  <br />
  -3. mplayer-skin-default-1.5-1.noarch.rpm
  <br />
  -4. mplayer-gui-0.90pre8-1.i386.rpm
  <br />

  <br />
  ili ve? one fajlove koji se tamo nalaze a imaju zajedni?ki po?etak tipa mplayer-common-xxxx-i386.rpm gde xxxx zamenjuje trenutnu verziju koja je spremna za download.
  <br />
guid: https://forum.linuxo.org/2003/01/30/uputstvo-za-instalaciju-mplayer-a-u-rpm-varijanti/
id: 283
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Uputstvo za instalaciju Mplayer-a u RPM varijanti
url: /uputstvo-za-instalaciju-mplayer-a-u-rpm-varijanti/
---
Najbolji izvor RPM paketa za instalaciju Mplayer-a se nalazi na adresi: http://www.piorunek.pl/~dominik/linux/pkgs/mplayer/ . Sa njega treba skinuti slede?e RPM fajlove: 

-1. mplayer-common-0.90pre8-1.i386.rpm  
  
-2. mplayer-0.90pre8-1.i386.rpm  
  
-3. mplayer-skin-default-1.5-1.noarch.rpm  
  
-4. mplayer-gui-0.90pre8-1.i386.rpm 

ili ve? one fajlove koji se tamo nalaze a imaju zajedni?ki po?etak tipa mplayer-common-xxxx-i386.rpm gde xxxx zamenjuje trenutnu verziju koja je spremna za download.  


<!--break-->

  
TakoÄ‘e treba skinuti i libpng-1.0.14-0.7x.4.i386.rpm koji se nalazi na Red Hat sajtu, ili ga potražite uz pomo? Google-a. Da bi mogli da se vide naši fontovi u titlu, treba skinuti definicije font-arial-cp1250.tar.bz2 , koji se nalaze na maÄ‘arskom sajtu, a takoÄ‘e se mogu na?i uz pomo? ve? pomenutog Google-a. 

Redosled instaliranja je slede?i: 

-1. libpng-1.0.14-0.7x.4.i386.rpm  
  
-2. mplayer-common-0.90pre8-1.i386.rpm  
  
-3. mplayer-0.90pre8-1.i386.rpm  
  
-4. mplayer-skin-default-1.5-1.noarch.rpm  
  
-5. mplayer-gui-0.90pre8-1.i386.rpm  
  
-6. font-arial-cp1250.tar.bz2 

Sve ove rpm pakete je najbolje instalirati iz konzole, kao root, komandom rpm -ivh ime paketa, a fontove treba raspakovati i sadržaj direktorijuma iskopirati u direktorijum ~/ .mplayer/ font, gde je ~ putanja koja definiše položaj vašeg korisni?kog direktorijuma tipa home/vaše korisni?ko ime/. Da bi ste mogli da ga vidite u Konqueror-u, morate uklju?iti opciju prikaza skrivenih fajlova. Sada je ostalo samo da otvorite konzolu i ukucate gmplayer i to je to! 

Ovo naravno podrazumeva da nemate problema sa zvukom, odnosno OSS driver-om i da film gledate sa hard diska. 

Pozdrav Dragan 

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=283)