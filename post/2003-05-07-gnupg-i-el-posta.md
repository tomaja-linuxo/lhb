---
author: tomaja
date: "2003-05-07T15:19:05Z"
excerpt: |
  Sada ?emo se pozabaviti
  i slanjem poruka e-pošte istim putem, ali uz osiguravanje  privatnosti
  sistemom zaštite GnuPG. GnuPG (GNU Privacy Guard) je besplatan  sistem
  zaštite otvorenog izvornog koda, i kao takav predstavlja odgovaraju?u
  potpunu zamenu za PGP. Pošto je izdat pod GPL licencom, moÄ‘ete ga
  slobodno  preuzeti sa Interneta i instalirati na koliko želite
  ra?unara, kao i menjati izvorni kod ili kopirati. Skript ?emo uraditi
  u programskom  jeziku PHP zbog njegove brzine, jednostavnosti i
  portabilnosti. (GnuPG), PHP i Apache su dostupni i na Windows i na Unix
  platformama, tako da bi skript  trebao, uz eventualne minimalne izmene,
  raditi istovetno. Konkretno, mi ?emo  govoriti o Unix (Linux) platformi.
guid: https://forum.linuxo.org/2003/05/07/gnupg-i-el-posta/
id: 321
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: GnuPG i el.pošta
url: /gnupg-i-el-posta/
---
Sada ?emo se pozabaviti  
i slanjem poruka e-pošte istim putem, ali uz osiguravanje privatnosti  
sistemom zaštite GnuPG. GnuPG (GNU Privacy Guard) je besplatan sistem  
zaštite otvorenog izvornog koda, i kao takav predstavlja odgovaraju?u  
potpunu zamenu za PGP. Pošto je izdat pod GPL licencom, moÄ‘ete ga  
slobodno preuzeti sa Interneta i instalirati na koliko želite  
ra?unara, kao i menjati izvorni kod ili kopirati. Skript ?emo uraditi  
u programskom jeziku PHP zbog njegove brzine, jednostavnosti i  
portabilnosti. (GnuPG), PHP i Apache su dostupni i na Windows i na Unix  
platformama, tako da bi skript trebao, uz eventualne minimalne izmene,  
raditi istovetno. Konkretno, mi ?emo govoriti o Unix (Linux) platformi.<!--break-->

**Slanje obi?ne poruke**</i></h3> 

<p align="justify" style="margin-bottom: 0cm;">
  Za slanje poruka putem<br /> e-pošte, PHP poseduje ugradjenu mail() funkciju, koja svoj posao obavlja<br /> brzo i ?isto. Pored toga, može se koristiti i sistem cevovoda za<br /> direktno ubrizgavanje sistemskom agentu za prenos pošte ili uti?nice za<br /> slanje preko spoljnog SMTP servera.
</p>

<p align="justify" style="margin-bottom: 0cm;">
  Prvo ?emo prikazati<br /> jednostavnu upotrebu funkcije<b><i> mail()</i></b>. Moramo znati koje<br /> ulazne vrednosti funkcija o?ekuje od nas, a to su, redom: adresa na<br /> koju šaljemo, naslov (<i>subject </i>engl.), poruka, dodatni podaci za<br /> zaglavlje, dodatni parametri. Prve ?etiri vrednosti su neophodne, dok<br /> dodatni podaci i parametri vezani za zaglavlje poruke nisu obavezni.<br /> Istu poruku možemo poslati na više adresa tako što ih navedemo odvojene<br /> zarezom u okviru prve promenljive, ili navodjenjem u delu namenjenom za<br /> dopunu zaglavlja (?etvrta ulazna vrednost) pod <b>Cc:</b> ili <b>Bcc:</b><br /> opisom. Ovom funkcijom omogu?eno je i slanje priloga putem MIME<br /> kodiranja, ali o tome više neki drugi put.
</p>

<p align="justify" style="margin-bottom: 0cm;">
  Pod Windows operativnim<br /> sistemom, postoje neke razlike u odnosu na Unix, jer se ne koristi<br /> lokalni program za slanje pošte, ve? se neposredno koriste uti?nice za<br /> povezivanje sa spoljnim SMTP serverom. Dalje, u verzijama PHP-a<br /> starijim od verzije 4.3, u Windows-u je bio podržan samo <b>Cc:</b> tip<br /> zaglavlja, na šta treba obratiti pažnju.
</p>

<p align="justify" style="margin-bottom: 0cm;">
  <a
 href="http://popeye.ekof.bg.ac.yu/tekst.php?id=29">Skript mail.php</a><br /> &#8211; Skript za slanje tekstualne poruke unete preko formulara.
</p>

<p align="justify" style="margin-bottom: 0cm;">
  Ovo je upotrebljiv<br /> skript za npr. formular na prezentaciji kojim se može ostvariti povratna<br /> sprega sa posetiocima. Ako umesto toga želimo da ovaj naš skript bude<br /> deo Web klijenta za rukovanje elektronskom poštom, postavljaju se i<br /> neki posebni zahtevi. MeÄ‘u prvima bi bio zahtev za osiguranjem<br /> privatnosti poslatih poruka.
</p>

<h3 align="center">
  <i><b>Zašto GnuPG?</b></i>
</h3>

<p align="justify" style="margin-bottom: 0cm;">
  Danas je tzv.<br /> prisluškivanje kanala kojim putuju paketi na Internetu ?esta pojava.<br /> Poznata je ?injenica da svi ve?i provajderi u cilju zaštite sopstvene<br /> mreže prisluškuju promet paketa u potrazi za eventualnim zlonamernim<br /> paketima kojim hakeri napadaju servere i mrežnu opremu. Isto tako,<br /> ukoliko koristite Internet sa neke javne mreže (Internet kafe, fakultet<br /> ili biblioteka) privatnost može biti vrlo lako ugrožena (po pravilu i<br /> jeste).
</p>

<p align="justify" style="margin-bottom: 0cm;">
  Rešenja postoje i treba<br /> ih iskoristiti. Uvek kada to možete koristite sigurnosne uti?nice (SSL)<br /> koje sav kodiraju nekim algoritmom. Time ?ete se osigurati od kradje<br /> lozinki, a time i mnogo ve?e štete gde je kraÄ‘a Internet vremena kod<br /> provajdera manja stavka.
</p>

<p align="justify" style="margin-bottom: 0cm;">
  Ali kada je bezbednost u<br /> pitanju, tu se pri?a nikako ne završava. Vi možete dostaviti poruku SMTP<br /> serveru preko sigurnosnih uti?nica, ali komunikacija izmedju vašeg i<br /> SMTP servera primaoca ne?e biti kodirana. Na kraju, niko ne garantuje<br /> da možda lozinka primaoca nije kompromitovana. Korporativnim<br /> korisnicima ?e biti od naro?itog zna?aja da poruka odreÄ‘enoj osobi bude<br /> stvarno dostupna samo onome kome je i namenjena.
</p>

<h3 align="center">
  <i><b>Kona?ni skript</b></i>
</h3>

<p align="justify" style="margin-bottom: 0cm;">
  Ne?emo ulaziti u na?in<br /> konfigurisanja GnuPG sistema, kao ni u izradu klju?eva jer to nije tema<br /> ove Radionice. Više informacija o tome, zajedno sa poslednjom verzijom<br /> koju možete preuzeti, na?i?ete na adresi <a class="western"
 href="http://www.gnupg.org/">http://www.gnupg.org</a>.
</p>

<p align="justify" style="margin-bottom: 0cm;">
  Da bismo mogli da<br /> uspešno kodiramo, moramo prekopirati direktorijum koji sadrži GnuPG<br /> konfiguraciju na mesto koje je dostupno Web serveru. U tom direktorijumu<br /> su nam potrebne 3 datoteke i to: gpg.conf (GnuPG 1.2 i kasniji, a ranije<br /> verzije koriste datoteku options), pubring.gpg i trustdb.gpg, Prava<br /> pristupa su vrlo bitna i ona moraju biti takva da dozvole korisniku pod<br /> kojim radi Web server upis i ulazak u pomenuti direktorijum, ali ne i<br /> ?itanje. Takodje, nad ove 3 datoteke samo vlasnik može imati sva prava,<br /> a Web server samo za ?itanje. Ovo je vrlo bitno da dobro odradite, jer<br /> u suprotnom GnuPG ne?e mo?i da radi.
</p>

<p align="center" style="margin-bottom: 0cm;">
  <img
 src="tekst.php?id=28" /> <br /> Slika 2: kontakt.jpg &#8211; Kontakt strana u okviru prezentacije
</p>

<p align="justify" style="margin-bottom: 0cm;">
  Polaze?i od prethodnog<br /> skripta, postupno ?emo ga nadograÄ‘ivati. Prvo ?emo se pozabaviti<br /> kodiranjem. Kao argument pri startovanju gpg komande moramo navesti u<br /> okviru opcije <i>&#8211;homedir</i> lokaciju na disku gde se nalazi<br /> direktorijum sa konfiguracijom koji smo prethodno pripremili. Zatim sa<br /> opcijom <i>-r </i>navodimo kome korisniku iz spiska u datoteci<br /> pubring.gpg je poruka namenjena (adresa e-pošte na koju šaljemo bi<br /> trebalo da odradi taj deo posla) i na kraju mu opcijom <i>-e</i> kažemo<br /> da kodira podatke sa standardnog ulaza. Naravno, na standardni ulaz mu<br /> dajemo telo poruke. Pre toga, funkcijom <b><i>escapeshellarg()</i></b><br /> ?emo o?istiti telo poruke, za slu?aj da korisnik formulara želi da<br /> ubrizga u naš skript komande koje ne želimo da startujemo.
</p>

<p align="justify" style="margin-bottom: 0cm;">
  <a
 href="http://popeye.ekof.bg.ac.yu/tekst.php?id=30">Skript gpgmail.php</a>
</p>

<p align="justify" style="margin-bottom: 0cm;">
  Funkcija <b><i>exec()</i></b><br /> koju koristimo za startovanje gpg vrati?e kodiranu poruku u niz koji joj<br /> je dat kao primarni argument. Da bismo od tog niza dobili odgovaraju?i<br /> string koji ?emo poslati funkciji <b><i>mail()</i></b>, iskoristi?emo <b><i>implode()</i></b><br /> kojim ?emo spojiti redove.
</p>

<p align="justify" style="margin-bottom: 0cm;">
  Za kraj u skript ?emo<br /> uneti i proveru popunjenosti svih polja formulara. Ukoliko je neko od<br /> polja ostalo nepopunjeno, ispisa?emo upozorenje i vratiti korisnika na<br /> ponovno popunjavanje, ali zadržavaju?i ve? unete vrednosti. Svi znamo<br /> koliko nervira kada morate ponovo da unosite i vrednosti koje ste bili<br /> ukucali.
</p>

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=321)