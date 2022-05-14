---
author: tomaja
date: "2006-03-05T15:54:00Z"
excerpt: |
  Za instalaciju Linux-a Mandriva 2006 treba da nabaviš program PowerQuest PartitionMagic 8.0 za particionisanje hard diska iz Windows-a i naravno sam Linux. <br />
  U PartitionMagic-u pritisni desnim klikom na C particiju, ili ako ih imaš više na poslednju po redu. Pritisni resize/move u polje Free Space After upiši 5000 pritisni OK. Pojavi?e se sivo obojeno polje na koje treba da klikneš desnim klikom i izabereš Create. Pritisni strelicu pored polja Partition Type i iz padaju?e liste izaberi Linux Ext3. Pritisni OK i ponovo desni klik na tako dobijenu ext3 particiju, izaberi resize/move, a u polje Free Space After upiši 500, pritisni OK, desni klik na novo dobijeno sivo polje, pritisni strelicu pored polja Partition Type i iz padaju?e liste izaberi Linux Swap, pritisni OK. Sada pritisni Aplly (zeleno dugme u donjem levom uglu). Ra?unar ?e se resetovati da bi napravio particije za Linux (vide?eš bela slova na plavom ekranu, ne diraj ništa, sa?ekaj da se Windows ponovo pokrene), ukoliko sve uradi iz Windows-a, sa?ekaj i pritisni OK. Sada možeš da proveriš u PartitionMagic-u, da li imaš particije za Linux, jedna ext3 od otprilike 4500 MB i jedna swap od 500MB.
guid: https://forum.linuxo.org/2006/03/05/instalacija-linux-a-mandriva-2006-uputstvo-za-poetnike/
id: 1077
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Instalacija Linux-a Mandriva 2006 &#8211; uputstvo za po?etnike
url: /instalacija-linux-a-mandriva-2006-uputstvo-za-poetnike/
---
Za instalaciju Linux-a Mandriva 2006 treba da nabaviš program PowerQuest PartitionMagic 8.0 za particionisanje hard diska iz Windows-a i naravno sam Linux.  
U PartitionMagic-u pritisni desnim klikom na C particiju, ili ako ih imaš više na poslednju po redu. Pritisni resize/move u polje Free Space After upiši 5000 pritisni OK. Pojavi?e se sivo obojeno polje na koje treba da klikneš desnim klikom i izabereš Create. Pritisni strelicu pored polja Partition Type i iz padaju?e liste izaberi Linux Ext3. Pritisni OK i ponovo desni klik na tako dobijenu ext3 particiju, izaberi resize/move, a u polje Free Space After upiši 500, pritisni OK, desni klik na novo dobijeno sivo polje, pritisni strelicu pored polja Partition Type i iz padaju?e liste izaberi Linux Swap, pritisni OK. Sada pritisni Aplly (zeleno dugme u donjem levom uglu). Ra?unar ?e se resetovati da bi napravio particije za Linux (vide?eš bela slova na plavom ekranu, ne diraj ništa, sa?ekaj da se Windows ponovo pokrene), ukoliko sve uradi iz Windows-a, sa?ekaj i pritisni OK. Sada možeš da proveriš u PartitionMagic-u, da li imaš particije za Linux, jedna ext3 od otprilike 4500 MB i jedna swap od 500MB.  
<!--break-->Ubaci CD 1 ili DVD sa Linux Mandrivom i resetuj ra?unar. Kada se pojavi uvodni ekran za instalaciju pritisni enter (ukoliko krene Windows treba da u BIOS-u podesiš but ovim redosledom: 1.disketa; 2.CD; 3.hard disk). Tek sada ubaci disketu (naravno neku praznu).

  
Na levoj strani je informacioni deo, a na desnoj nastavljamo instalaciju.Mišem ili strelicom na gore (na tastaturi) izaberi Evropu, pronaÄ‘i srpski (?irilicu ili latinicu), dalje instalacija te?e na srpskom. Pritisni mišem next ili enter na tastaturi.  
Prihvati licencirani ugovor, pritisni slede?i.  
Tastatura: nikako ne biraj srpski raspored tastera, pronadji US tastatura (internacionalna), kasnije ?eš u Linuxu dodati srpski raspored tastera.  
Sigurnosni nivo: izaberi standardni nivo, administracija nivoa sigurnosti ostavi prazno.  
Drax je pronašao slede?a rešenja: trebalo bi da stoji ve? izabrano &#8211; koristi postoje?u particiju.  
Izberi particije za formatiranje: kod mene je štiklirana particija za Linux,  
hda8 (4,4 GB, / ,ext3)  
Dalje ?e pisati da treba da formatira particiju, sa?ekaj da završi i kada te upita (na engleskom) da li ?eš da kopiraš disk na hard, ostavi prazno polje -Copy whole CDs- i pritisni dugme &#8211; slede?i.  
Na -Do you have a suplementary instalation media- ostavi crnu ta?ku na nijedan i pritisni dugme -u redu-.  
Sada izaberi grupe paketa tako što ?eš štiklirati sve stavke u obe kolone i obavezno polje na dnu &#8211;pojedina?no biranje paketa-.  
Izaberi pakete za instalaciju tako što ?eš prvo pritisnuti plavu strelicuna na dnu ekrana, da bi mogao da štikliraš sve kvadrati?e pored naziva programskih paketa. Kada pritisneš prvo prazno polje pojavi?e se upozorenje: Slede?i paketi treba da bidu instalirani. Pritisni -u redu- i nastavi dalje sa štikliranjem (pritiskaj ta?no u kvadrat). Odmotavaj listu i na svako upozorenje odgovaraj sa -u redu-. Postoje neka polja koja ?e i posle potvrde ostati prazna.  
Pisa?e: Ne možete selektovati/deselektovati ovaj paket. Pritisni -u redu- i nastavi dalje (neka kvadrat ostane prazan). TakoÄ‘e postoje i paketi sa nacrtanim katancem, to naravno ne diraj. Kada najzad stigneš do kraja liste, pritisni -instaliraj-.  
Na izboru servera ostavi -da- i pritisni -slede?e-.  
Kre?e kopiranje programa u toku kojeg možeš da pritiskaš dugme -detalji/bez detalja-. Instalacija sa CD-ova zahteva sada promenu diskova. Mandriva elegantno otvara drajv sa molbom da se ubaci slede?i CD. Jednostavnim pritiskom na -enter- drajv se zatvara i nastavlja instalaciju.  
Sledi konfiguracija sistema. Prvo se podešava root lozinka. Izaberi -bez lozinke- .  
Dodaj korisnika tako što ?eš u prvo polje upisati pravo ime i prezime sa velikim po?etnim slovima i razmakom izmeÄ‘u. Sada pritisni -Tab- na tastaturi i ostavi prazno polje za lozinku. Idemo na slede?i korak instalacije.  
Za auto logovanje ostavi štiklirano polje -Use this feature- i -KDE-.  
Sada ubaci disketu.  
Sažetak  
PronaÄ‘i predposlednju stavku: startanje.  
Starter &#8211; lilo &#8211; graphic na /dev/hda  
Pritisni dugme -podesi- .  
Glavne opcije startera: levi klik na prvu padaju?u listu, ponovo levi klik na -Grub with graphical menu-.  
Levi klik na padaju?u listu Startni boot ureÄ‘aj, izaberi levim klikom /dev/fd0. Ostalo neka stoji kako jeste.  
U slede?em koraku ostavi samo  
linux (boot/wmlinuz) i  
windows (dev/hda1).  
Sve ostalo izbriši, izaberi levim klikom pa pritisni -ukloni-.  
Sada pritisni levim klikom -windows(dev/hda1)-, pa levi klik na &#8211;promeni-. Å tikliraj podrazumevano, pritisni u -redu-. Sada pritisni -slede?i- da se ponovo pojavi Sažetak.  
Idemo dalje pritiskom na -slede?i-. Otvaraju se vratanca, izvadi disk, ostavi disketu i pritisni -restart-.

Kre?e Grub  
Izaberi Linux strelicom na gore na tastaturi, enter.  
Windows kre?e sam posle 10 sek. ili ako izvadiš disketu.

Kada krene Linux Mandriva 2006, presko?i ?arobnjaka.

&#8212; Ovo uputstvo odštampaj ili prepiši, treba?e ti, jer budala pamti, a pametan piše.&#8212;

Ukoliko nešto ne radi, recimo zvuk i sli?no, ponovo ubaci disk, izvadi disketu, restartuj ra?unar i uradi popravku instalacije tako što ?eš do?i do Sažetka i kao kod podešavanja Gruba pokušaš da podesiš to što ne radi.  
Ako disketa otkaže, popravi?eš je jednostavno tako što ?eš pokrenuti instalaciju Linuxa, ali umesto enter, pritisni F1, zatim otkucaj:  
rescue  
tek sada ubaci disketu i ako je izabrano -Reinstal Linux boor loader- pritisni enter. Otkucaj:  
grub  
pritisni enter, restartuj, izvadi disk, ostavi disketu.  
Za ?itanje Linux particija iz Windowsa možeš pored dodatka za Komander da koristiš i PartitionMagic 8.0. Kako se to radi neka bude doma?i zadatak za sve linuxaše.

Ista ovakva uputstva za Slackware, SuSe i Debian (strašni) mogu da postavim na forum ako to nekom treba.  
zorand@EUnet.yu tel. 064/110-26-18

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=1077)