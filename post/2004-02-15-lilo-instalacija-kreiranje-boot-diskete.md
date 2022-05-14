---
author: tomaja
date: "2004-02-15T06:30:53Z"
excerpt: |
  Izbor izmeÄ‘u Grub ili Lilo startera je ustvari stvar li?nog izbora. Ja
  preferiram ovaj drugi jer ga dugo koristim a i zbog toga što se veoma lako podešava. Ukoliko se naÄ‘ete u
  situaciji da vas Linux sistem po defaultu koristi Grub evo kako da napravite lilo startnu disketu pomo?u koje možete da podižete sistem:
guid: https://forum.linuxo.org/2004/02/15/lilo-instalacija-kreiranje-boot-diskete/
id: 420
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Lilo &#8211; instalacija, kreiranje boot diskete
url: /lilo-instalacija-kreiranje-boot-diskete/
---
Izbor izmeÄ‘u Grub ili Lilo startera je ustvari stvar li?nog izbora. Ja  
preferiram ovaj drugi jer ga dugo koristim a i zbog toga što se veoma lako podešava. Ukoliko se naÄ‘ete u  
situaciji da vas Linux sistem po defaultu koristi Grub evo kako da napravite lilo startnu disketu pomo?u koje možete da podižete sistem:<!--break-->

  
<span style="font-weight: bold; color: rgb(0, 0, 153);"><br /> Instalacija i konfiguracija Lilo-a:<br /> <br /> </span> <span style="font-weight: bold;">1) </span> Prvo  
proverite da li su paketi <span style="font-weight: bold;">lilo</span>  
i <span style="font-weight: bold;">lilo-config</span>  
instalirani (lilo-config je KDE grafi?ki interfejs za  
konfiguraciju Lilo-a). Ukoliko je lilo-config instaliran rebalo  
bi da pokrenete <span style="font-weight: bold;">KDE Kontrolni Centar </span>(obi?no  
se nalazi u glavnom meniju pod <span style="font-weight: bold;">System<br /> Administration</span> ili <span style="font-weight: bold;">Configuration</span>).  
Ako se ne snalazite u osnovnom meniju jednostavno iz konzole (ili  
pomo?u dijaloga koji dobijate pritiskom na tastere alt+F2) pokrenite <span
style="font-style: italic;">kcontrol</span>

<span style="font-weight: bold;">2) </span> Kada prvi put  
pokrenete KDE Lilo konfiguraciju sam program ?e izvršiti auto detekciju  
vašeg sistema. Kada vam program izbaci ono što je detektovao  
proverite da li to odgovara stvarnom stanju i kliknite na <span
style="font-weight: bold;"></span>apply da bi kreirali <span
style="font-weight: bold;">/etc/lilo.conf</span> fajl. Naravno,  
možete i sami da kreirate lilo.conf ili da izvršite odreÄ‘ene  
izmene da bi starter prilagodili svojim potrebama. Fajl lilo.conf se  
obi?no nalazi u /etc direktorijumu.

<span style="font-weight: bold;">3)</span> U konzoli ukucajte <span
style="font-weight: bold;">lilo</span> ili <span
style="font-weight: bold;">/sbin/lilo</span> i pritisnite taster  
enter. Ukoliko se iza toga ne pojavi poruka o grešci lilo je sada  
instaliran i spreman za rad.

<span style="font-weight: bold; color: rgb(0, 0, 153);"><br /> Kreiranje Lilo startne (boot) diskete:</span>

Vaša Linux distribucija (kao što su Mandrake ili SuSE) verovatno ve?  
imaju alatku koja služi za kreiranje lilo startne diske. Ipak, ukoliko  
imate neki drugi Linux sistem ili nemate mogu?nost rada u grafi?kom  
okruženju evo kako da napravite lilo startnu disketu. Iz konzole  
ukucajte: <span style="font-weight: bold;">mkboot</span> ili<span
style="font-weight: bold;">mkbootdisk</span>. Na mom sistemu se  
nalazi mkbootdisk a diskteu mozete kreirati sa naredbom 

<span style="color: rgb(0, 0, 153);">#mkbootdisk &#8211;device /dev/fd0<br /> 2.24.22-10mdk <span style="color: rgb(0, 0, 0);">(ovo bi bio<br /> primer za MDK 9.2 sa default kernelom)</span></span>

MeÄ‘utim, možete i ru?no kreirati startnu ili boot disketu na slede?i  
na?in:  
<br style="font-weight: bold;" />  
<span style="font-weight: bold;">1)</span> Otvorite konzolu ,  
ubacite disketu u ureÄ‘aj i unesite slede?e naredbe:

<span style="color: rgb(0, 0, 153);">#mke2fs /dev/fd0</span>  
<span style="color: rgb(0, 0, 153);">#mount -t ext2 /dev/fd0<br /> /mnt/floppy</span><br style="color: rgb(0, 0, 153);" />  
<span style="color: rgb(0, 0, 153);">#cd<br /> /mnt/floppy</span><br style="color: rgb(0, 0, 153);" />  
<span style="color: rgb(0, 0, 153);">#mkdir etc && mkdir<br /> boot</span><br style="color: rgb(0, 0, 153);" />  
<span style="color: rgb(0, 0, 153);">#cp /boot/boot.b<br /> /mnt/floppy/boot</span><br style="color: rgb(0, 0, 153);" />  
<span style="color: rgb(0, 0, 153);">#cp /boot/initrd<br /> /mnt/floppy/boot</span><br style="color: rgb(0, 0, 153);" />  
<span style="color: rgb(0, 0, 153);">#cp /boot/<span
style="color: rgb(153, 0, 0);">vmlinuz-2.4.22-10mdk </span><br /> /mnt/floppy/boot</span>

Prva linija ?e formatirati disketu Ukoliko nemate fajl /boot/initrd  
onda tu liniju ne morate da unosite. Naravno, ovo je samo primer pa  
zato izmenite broj kernela <span style="color: rgb(153, 0, 0);">vmlinuz</span>  
koji odgovara vašem, a da bi saznali koji je to broj ukucajte u konzoli  
<span style="font-weight: bold;">uname -r</span>

<span style="font-weight: bold;">2) </span> Kreirajte tekstualni  
fajl sa imenom <span style="font-weight: bold;">lilo.conf</span> u <span
style="font-weight: bold;">/mnt/floppy/etc</span>, i u njega unesite  
slede?i tekst, a zatim snimite izmene i zatvorite fajl (za ovu  
operaciju možete koristiti bilo koji tekst editor nrp. <span
style="font-weight: bold;">vi</span>):

<span style="color: rgb(0, 0, 153);">boot=/dev/fd0</span><br
style="color: rgb(0, 0, 153);" />  
<span style="color: rgb(0, 0, 153);">install=/boot/boot.b</span><br
style="color: rgb(0, 0, 153);" />  
<span style="color: rgb(0, 0, 153);">MAP=/mnt/floppy/boot/map</span><br
style="color: rgb(0, 0, 153);" />  
<span style="color: rgb(0, 0, 153);">read-only</span><br
style="color: rgb(0, 0, 153);" />  
<span style="color: rgb(0, 0, 153);"><br /> image=/mnt/floppy/boot/<span style="color: rgb(153, 0, 0);">vmlinuz-2.4.22-10mdk</span></span><br
style="color: rgb(0, 0, 153);" />  
<span style="color: rgb(0, 0, 153);"><br /> label=linux</span><br style="color: rgb(0, 0, 153);" />  
  <span style="color: rgb(0, 0, 153);">root=/dev/<span
style="color: rgb(153, 0, 0);">hda1</span></span>

Naravno, izmenite gornje redove da bi odgovarale stanju na vešem  
sistemu, a to se odnosi na verziju kernela i particiju na kojoj je  
insatliran vaš LInux sistem.

<span style="font-weight: bold;">3)</span> Instaliranje Lilo-a na  
disketu:

<span style="color: rgb(0, 0, 153);">#cd /floppy</span><br
style="color: rgb(0, 0, 153);" />  
<span style="color: rgb(0, 0, 153);">#lilo -C<br /> /floppy/etc/lilo.conf</span>

Parametar <span style="font-weight: bold;">-C</span> nam  
omogu?ava da fajl <span style="font-weight: bold;">lilo.conf</span>  
postavimo i na drugo mesto osim uobi?ajenog u <span
style="font-weight: bold;">/etc </span>direktorijumu.

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=420)