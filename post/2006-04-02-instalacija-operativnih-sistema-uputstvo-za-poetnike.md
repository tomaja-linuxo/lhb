---
author: tomaja
date: "2006-04-02T15:34:00Z"
excerpt: |
  Ra?unar sa jednim operativnim sistemom je kao Windows bez ijedne aplikacije. Možete da slušate muziku, gledate filmove, koristite internet, pišete tekst, narezujete diskove, štampate i igrate fliper.<br />
  Sa dva ili tri operativna sistema imate mnogo više mogu?nosti i sigurnosti. Cena je zanemarljiva, prostor na hard disku i par diskova sa besplatnim Linuxom. Najjednostavnije rešenje je da ostavite samo jedan Windows i da koristite Linux Knoppix koji se pokre?e sa CD-a. Mnogo bolje je da instalirate i neki od najpopularnijih Linuxa, recimo Linux Mandriva 2006 ili SUSE 10.0, jer su oba prevedena na srpski i relativno su laki za instalaciju. Ubuntu 5.10, Slackware 10.2, Debian 3.1 Sarge i sli?ne distribucuje bolje da ostavite za kasnije, kada se malo bolje upoznate sa GNU/Linux-om. Postoje dva na?ina koriš?enja Linuxa, instalirani Mandriva i Knoppix live, koji ne remeti raspored particija na hard disku. ?emu bi sve ovo služilo i da li bi i radilo?
guid: https://forum.linuxo.org/2006/04/02/instalacija-operativnih-sistema-uputstvo-za-poetnike/
id: 1104
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Instalacija operativnih sistema &#8211; uputstvo za po?etnike
url: /instalacija-operativnih-sistema-uputstvo-za-poetnike/
---
Ra?unar sa jednim operativnim sistemom je kao Windows bez ijedne aplikacije. Možete da slušate muziku, gledate filmove, koristite internet, pišete tekst, narezujete diskove, štampate i igrate fliper.  
Sa dva ili tri operativna sistema imate mnogo više mogu?nosti i sigurnosti. Cena je zanemarljiva, prostor na hard disku i par diskova sa besplatnim Linuxom. Najjednostavnije rešenje je da ostavite samo jedan Windows i da koristite Linux Knoppix koji se pokre?e sa CD-a. Mnogo bolje je da instalirate i neki od najpopularnijih Linuxa, recimo Linux Mandriva 2006 ili SUSE 10.0, jer su oba prevedena na srpski i relativno su laki za instalaciju. Ubuntu 5.10, Slackware 10.2, Debian 3.1 Sarge i sli?ne distribucuje bolje da ostavite za kasnije, kada se malo bolje upoznate sa GNU/Linux-om. Postoje dva na?ina koriš?enja Linuxa, instalirani Mandriva i Knoppix live, koji ne remeti raspored particija na hard disku. ?emu bi sve ovo služilo i da li bi i radilo?

<!--break-->Evo jednog od mnogobrojnih razloga za instalaciju Linux-a. Kada sa desi da Windows ne?e da se pokrene, postoje razni na?ini kako da se ra?unar dovede u ispravno stanje, bez gubitka podataka sa hard diska. Ovo je moja verzija reinstalacije Windowsa. 

  
Dok Windows još radi podelite hard disk pomo?u PowerQuest PartitionMagic 8.0 ili Knoppix-a na dve particije za Windows i dve za Linux. Na disku od 80 GB za C ostavite prostor od recimo 20 GB, druga FAT 32 particija od oko 50 GB je za podatke (mp3, slike, filmovi, neinstalirani programi i sli?no) koji mogu da se ?itaju i iz Windows-a i iz Linux-a. Ostatak od oko 5 GB formatirajte u Linux Ext3, pa odvojte 250 MB za Linux Swap. Ukoliko niste podelili hard disk na particije, a Windows ne?e da krene, pokrenite Linuks Knoppix za spašavanje podataka sa hard diska. Linux Knoppix otvara sve fascikle na NTFS i ostalim particijama, ?ak i desktop i dokumente i snima pomo?u K3B-a na diskove. Uradite ili tako ili premestite podatke sa C na drugu FAT 32 particiju koju ?ete napraviti pomo?u Linuxovog programa Qtparted v0.4.4 iz Knoppixa. Posle reinstalacije Windows-a instalirajte i Linux. Uputstva za instalaciju možete pro?itati na ovom sajtu u Arhivi tekstova.

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=1104)