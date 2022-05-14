---
author: tomaja
date: "2006-03-06T19:43:29Z"
excerpt: |
  Za instalaciju Linux-a Slackware 10.1 treba da nabaviš program PowerQuest PartitionMagic 8.0 za particionisanje hard diska iz Windows-a i naravno sam Linux. <br />
  U PartitionMagic-u pritisni desnim klikom na C particiju, ili ako ih imaš više na poslednju po redu. Pritisni resize/move u polje Free Space After upiši 5000 pritisni OK. Pojavi?e se sivo obojeno polje na koje treba da klikneš desnim klikom i izabereš Create. Pritisni strelicu pored polja Partition Type i iz padaju?e liste izaberi Linux Ext3. Pritisni OK i ponovo desni klik na tako dobijenu ext3 particiju, izaberi resize/move, a u polje Free Space After upiši 500, pritisni OK, desni klik na novo dobijeno sivo polje, pritisni strelicu pored polja Partition Type i iz padaju?e liste izaberi Linux Swap, pritisni OK. Na Linux ext3 particiju klikni desnim tasterom i izaberi Label... pa upiši Linux i pritisni OK. Sada pritisni Aplly (zeleno dugme u donjem levom uglu). Ra?unar ?e se resetovati da bi napravio particije za Linux (vide?eš bela slova na plavom ekranu, ne diraj ništa, sa?ekaj da se Windows ponovo pokrene), ukoliko sve uradi iz Windows-a, sa?ekaj i pritisni OK. Sada možeš da proveriš u PartitionMagic-u, da li imaš particije za Linux, jedna ext3 od otprilike 4500 MB i jedna swap od 500MB.
guid: https://forum.linuxo.org/2006/03/06/instalacija-linux-a-slackware-10-1-uputstvo-za-poetnike/
id: 1079
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Instalacija Linux-a Slackware 10.1 &#8211; uputstvo za po?etnike
url: /instalacija-linux-a-slackware-10-1-uputstvo-za-poetnike/
---
Za instalaciju Linux-a Slackware 10.1 treba da nabaviš program PowerQuest PartitionMagic 8.0 za particionisanje hard diska iz Windows-a i naravno sam Linux.  
U PartitionMagic-u pritisni desnim klikom na C particiju, ili ako ih imaš više na poslednju po redu. Pritisni resize/move u polje Free Space After upiši 5000 pritisni OK. Pojavi?e se sivo obojeno polje na koje treba da klikneš desnim klikom i izabereš Create. Pritisni strelicu pored polja Partition Type i iz padaju?e liste izaberi Linux Ext3. Pritisni OK i ponovo desni klik na tako dobijenu ext3 particiju, izaberi resize/move, a u polje Free Space After upiši 500, pritisni OK, desni klik na novo dobijeno sivo polje, pritisni strelicu pored polja Partition Type i iz padaju?e liste izaberi Linux Swap, pritisni OK. Na Linux ext3 particiju klikni desnim tasterom i izaberi Label&#8230; pa upiši Linux i pritisni OK. Sada pritisni Aplly (zeleno dugme u donjem levom uglu). Ra?unar ?e se resetovati da bi napravio particije za Linux (vide?eš bela slova na plavom ekranu, ne diraj ništa, sa?ekaj da se Windows ponovo pokrene), ukoliko sve uradi iz Windows-a, sa?ekaj i pritisni OK. Sada možeš da proveriš u PartitionMagic-u, da li imaš particije za Linux, jedna ext3 od otprilike 4500 MB i jedna swap od 500MB.<!--break-->

  
Ubaci CD 1 sa Linux Slackware 10.1 i resetuj ra?unar. Kada na pozdravnom ekranu napiše &#8220;Welcome to Slackware 10.1&#8220; i tako dalje, posle root: otkucaj  
bareacpi.i  
trebalo bi da u poslednjem redu piše ovako:  
root:bareacpi.i  
Sada pritisni enter (ukoliko umesto instalacije Linuxa krene Windows treba da u BIOS-u podesiš but ovim redosledom: 1.disketa; 2.CD; 3.hard disk). Tek sada ubaci disketu. Sa?ekaj da se na ekranu na dnu pojavi tekst &#8222;Enter 1 to select a keyboard map:&#8220; Ništa ne upisuj, samo pritisni enter.  
Sada piše:  
You may now login as &#8217;root&#8217;  
Slackware login:  
upiši:  
root  
i pritisni enter.  
Opet ?itamo samo donji red:  
root@slackware:/#  
upiši:  
setup  
i pritisni enter, da se pojavi:  
Slackware Linux setup (version10.1)  
Izabrano je Help i kursor trep?e na . Na tastaturi pritisni dva puta strelicu na dole tako da bude izabrano:  
ADDSWAP Setup your swap partition(s)  
Kursor trep?e na , pritisni enter.  
SWAP SPACE DETECTED  
Kod mene piše da je pronašao particiju:  
/dev/hda9 (neki brojevi) 82 Linux swap  
Trep?e , pritisni enter.  
SWAP SPACE CONFIGURED  
Pritisni enter.  
SELECT LINUX INSTALATION PARTITION  
Pošto je u Windows-ovom Partitiom Magic-u u polje Label za ext3 particiju upisano Linux, sada piše:  
/dev/hda8 Linux 4831471K  
Kursor je na , pritisni enter.  
FORMAT PARTITION /dev/hda8  
Kod tebe piše broj tvoje particije za Linux. Ostavi izabrano:  
Format Qick format with no bad block checking  
Enter na .  
SELECT FILESYSTEM FOR /dev/hda8  
Naravno ponovo piše broj tvoje particije za Linux, izaberi strelicom na gore, na tastaturi:  
ext3  
Enter na .  
SELECT INODE DENSITY FOR /dev/hda8  
Ostavi:  
(default)  
Enter na .  
Kada završi formatiranje na  
DONE ADDING LINUX PARTITIONS TO /dev/hda8  
pritisni enter na .  
Pošto na ra?unaru ve? imaš instaliran Windows, pita te da li želiš da se iz Linuxa vide Windowsove NTFS i FAT particije, pritisni enter na .  
SELECT PARTITION TO ADD TO /etc/fstab  
Sada radi pažljivo. Ako u Windowsu imaš samo jednu C-e particiju, pisa?e:  
/dev/hda1 (vrsta particije) (veli?ina u KB)  
Ta particija je ve? izabrana pa pritisni enter na .  
PICK MOUNT POINT FOR /dev/hda1  
Kursor trep?e u praznom polju, upiši:  
/windows  
enter na .  
Ako imaš više od jedne particije za Windows ponovo smo na:  
SELECT PARTITION TO ADD TO /etc/fstab  
Ozna?ena je prva particija, piše:  
(IN USE)  
pritisni strelicu na dole, na tastaturi, da izabereš slede?u particiju pa zatim pritisni enter na i upiši:  
/windows2  
Ako imaš još particija, ponovi postupak tako što ?eš strelicom na dole na tastaturi do?i do slede?e neizabrane particije i obeležiti je sa /windows3 pa /windows4 i tako dalje. Radi se zapravo o tome da je jedino bitna kosa crta na po?etku, a posle možeš da upišeš bilo koji naziv za particiju tako da su imena razli?ita i najbolje je da su kratka i bez ikakvih razmaka i velikih slova. Ponavljam: kosa crta na po?etku i razli?iti nazivi.  
Kada završiš sa obeležavanjem particija, treba da stigneš do:  
DONE ADDING FAT or NTFS Partitions  
piše  
/dev/hda1 /windows  
i tako dalje za sve particije, pritisni enter na .  
SOURCE MEDIA SELECTION  
Ostavi izabrano:  
1.Instal from a Slackware CD or DVD  
enter na .  
SCANING FOR CD or DVD DRIVE  
Ostavi na:  
auto  
enter na .  
Sa?ekaj da se pojavi:  
PACKAGE SERIES SELECTION  
i samo pritisni enter na .  
SELECTION PROMPTING MODE  
Ostavi na:  
full  
enter na .  
Kre?e instalacija paketa sa prvog CD-a. (Ja imam Slackware 10.1 na 2 CD-a.) Kada završi sa prvim CD-om otvara drajv, zameni disk i pritisni enter, Linux sam zatvara vratanca i nastavlja instalaciju.  
INSTALL LINUX KERNEL  
Spusti strelicom na dole na:  
skip  
enter na .  
MAKE BOOTDISK  
Spusti strelicom na dole na:  
skip Skip making a bootdisk  
strelica na desno, enter na .  
Pošto verovatno imaš winmodem, ostavi izabrano:  
no modem  
enter na .  
ENABLE HOTPLUG SUBSYSTEM AT BOOT  
Enter na .  
INSTAL LILO  
Spusti strelicom na dole na:  
expert  
enter na .  
EXPERT LILO INSTALLATION  
Ostavi:  
begin  
enter na .  
OPTIONAL LILO append=&#8221;&#8221; Line  
Prepiši ono što piše gore:  
hdc=ide-scsi  
enter na .  
CONFIGURE LILO TO USE FRAME BUFFER CONSOLE  
Kod mene je izabrano:  
1024x768x256  
Izaberi odgovaraju?u rezoluciju za tvoj monitor i pritisni enter na .  
SELECT LILO TARGET LOCATION  
Proveri da li je disketa uba?ena, izaberi strelicom na dole:  
Floppy  
enter na .  
CHOSE LILO TIMEOUT  
Strelicom na dole izaberi 30 sek. Enter na .  
Ponovo smo na:  
EXPERT LILO INSTALLATION  
Sada izaberi strelicom na dole:  
Linux  
enter na .  
Još jednom:  
EXPERT LILO INSTALLATION  
Strelicom na dole na:  
Windows  
SELECT WINDOWS PARTITION  
Upiši ono što piše ispod Device Boot, a ozna?eno je zvezdicom, trebalo bi da bude:  
/dev/hda1  
zna?i upisuješ bez zvezdice, enter na .  
SELECT PARTITION NAME  
Upiši:  
Windows  
enter na .  
Još jednom:  
EXPERT LILO INSTALLATION  
Ovaj put idemo na:  
/install  
enter na .  
MOUSE CONFIGURATION  
Izaberi svoju vrstu miša (ja biram: usb), enter na .  
GPM CONFIGURATION  
Enter na .  
CONFIGURE NETWORK  
Izaberi strelicom na desno na tastaturi i pritisni enter.  
CONFIRM STARTUP SERWEES TO RUN  
Ovde ostavi sve kako jeste i pritisni enter na .  
CONSOLE FONT CONFIGURATION  
Enter na .  
HARDWER CLOCK SET TO UTC?  
Ponovo ostavi na:  
NO  
enter na .  
TAMEZONE CONFIGURATION  
Drži strelicu na dole na tastaturi dok ne doÄ‘eš do:  
Europe/Belgrade  
ako preteraš, a to se uvek desi, vrati se naravno strelicom na gore, enter na .  
SELECT DEFAULT WINDOW MANAGER FOR X  
Ostavi na:  
xiniutrc.kde  
enter na .  
WARNING: NO ROOT PASSWORD DETECTED  
Strelicom na desno do , enter.

SETUP COMPLETE  
Pritisni kombinaciju tastera ctrl+alt+del kao što i piše (ne pritiskaj enter). Izvadi disk, ostavi disketu. Kada se pojavi crveni Lilo, pritisni enter da krene Linux (strelicom na dole biraš Windows kao što i piše).  
Kada se u donja dva reda na crnom ekranu belim slovima pojavi:  
Welcome to Linux 2.4.29 (tty1)  
darkstar login:  
upiši  
root  
i pritisni enter.  
Pingvin sedi gore na slovima, a dole piše:  
root@darkstar:~#  
upiši  
startx  
i pritisni enter. Evo slike.  
Pritiskaj nekst ili presko?i ?arobnjaka. Ne biraj srpsku tastaturu jer ne rade sva slova. Windows particije su ti u Home-Devices. Za GNOME umesto root upiši gde pa kad zatraži username piši root. Za ?itanje Linux particija iz Windowsa možeš pored dodatka za Komander da koristiš i PartitionMagic 8.0.

&#8212; Ovo uputstvo odštampaj ili prepiši, treba?e ti, jer budala pamti,  
a pametan piše.&#8212;  
zorand@EUnet.yu tel. 064/110-26-18

Saljem ponovo ovaj tekst, nesto nije bilo dobro prekopirano. Nadam se da je sada sve u redu.Jedino nisam siguran u ispravnost opisa instalacije, uglavnom kod mene tako radi.

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=1079)