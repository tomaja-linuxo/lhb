---
author: tomaja
date: "2003-05-07T14:50:29Z"
excerpt: |
  Konzolni  režim rada ima svojih prednosti, poput brzine, stabilnosti
  i nadasve fleksibilnosti  u rešavanju svakodnevnih problema putem
  datoteka za serijsko izvršavanje instrukcija - skripti. MeÄ‘u nedostacima
  se sigurno nalazi, možda i kao jedan od najbitnijih, izostanak
  strukture za privremeno ?uvanje obrisanih datoteka dok je u grafi?kom
  okruženju X Windows to rešeno primenom tzv. kante za sme?e ("trash can"
  - engl.). Bilo je pokušaja izrade adekvatnog rešenja za povra?aj
  obrisanih datoteka, ali su se uglavnom oni zasnivali na primenjivanju
  specijalnih zakrpa za jezgro, kao i primeni šestog inode-a koji je u
  razvoju ext2 sistema organizacije podataka bio rezervisan za tu namenu.
  Inode predstavlja uskladišten opis individualnog podatka na UNIX fajl
  sistemu. U tom slu?aju vra?anje u preÄ‘ašnje stanje treba uraditi u što
  kra?em roku od onog kobnog koriš?enja komande "rm", jer su postojali
  dobri izgledi da ?e se u meÄ‘uvremenu na to  mesto na disku upisati nove
  informacije. Opširnije o sistemu inode oporavka fajlova pogledati:<a
  href="http://www.praeclarus.demon.co.uk/tesh/e2-undel/howto.txt"
  target="_blank">
  http://www.praeclarus.demon.co.uk/tesh/e2-undel/howto.txt</a> .
guid: https://forum.linuxo.org/2003/05/07/bash-korpa-za-otpatke/
id: 316
image: /wp-content/uploads/2003/05/tekst.php_.png
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";s:3:"315";s:11:"_thumb_type";s:5:"thumb";}
title: bash &#8211; korpa za otpatke
url: /bash-korpa-za-otpatke/
---
Konzolni režim rada ima svojih prednosti, poput brzine, stabilnosti  
i nadasve fleksibilnosti u rešavanju svakodnevnih problema putem  
datoteka za serijsko izvršavanje instrukcija &#8211; skripti. MeÄ‘u nedostacima  
se sigurno nalazi, možda i kao jedan od najbitnijih, izostanak  
strukture za privremeno ?uvanje obrisanih datoteka dok je u grafi?kom  
okruženju X Windows to rešeno primenom tzv. kante za sme?e (&#8222;trash can&#8220;  
&#8211; engl.). Bilo je pokušaja izrade adekvatnog rešenja za povra?aj  
obrisanih datoteka, ali su se uglavnom oni zasnivali na primenjivanju  
specijalnih zakrpa za jezgro, kao i primeni šestog inode-a koji je u  
razvoju ext2 sistema organizacije podataka bio rezervisan za tu namenu.  
Inode predstavlja uskladišten opis individualnog podatka na UNIX fajl  
sistemu. U tom slu?aju vra?anje u preÄ‘ašnje stanje treba uraditi u što  
kra?em roku od onog kobnog koriš?enja komande &#8222;rm&#8220;, jer su postojali  
dobri izgledi da ?e se u meÄ‘uvremenu na to mesto na disku upisati nove  
informacije. Opširnije o sistemu inode oporavka fajlova pogledati:<a
 href="http://www.praeclarus.demon.co.uk/tesh/e2-undel/howto.txt"
 target="_blank"><br /> http://www.praeclarus.demon.co.uk/tesh/e2-undel/howto.txt</a> .<!--break-->U ovom broju Radionice ?emo se baviti implementacijom korpe za

  
otpatke pri radu u komandnoj liniji. Odlu?ili smo se da to izvedemo u  
nekom prevodila?kom programskom jeziku, a imaju?i u vidu to da smo ve?  
ranije pisali o upotrebi Perl-a (videti Radionicu iz oktobra 2001,  
?lanak &#8222;Gimp i Perl u zajedni?koj akciji&#8220;) izbor je pao na BASH (Bourne  
Again Shell). Za neupu?ene BASH, kao i svi ostali shell prevodioci,  
pored prevoÄ‘enja standardnih svakodnevnih sistemskih komandi može se  
sasvim komotno iskoristiti za skript programiranje.



Pre nego preÄ‘emo na pisanje programskih listinga, ovaj projekat  
?emo podeliti na više zasebnih celina, u skladu sa funkcijama koje nam  
je cilj da obezbedimo:



1.Izrada skripta za brisanje

2.Izrada skripta za oporavak obrisanih datoteka i

3.Izrada svojevrsnog daemona koji ce periodi?no brisati zastarele  
datoteke



<div align="center">
  <p>
    <b> Delete komanda</b>
  </p>
</div>



Na samom po?etku da napomenemo da ovaj skript nikako NE SME da  
zameni naredbu &#8222;_rm_&#8222;. To zna?i da je za normalno funkcionisanje  
sistema najbolje ovaj skript nazvati imenom &#8222;_delete_ &#8220; i smestiti  
ga u neki od direktorijuma u vašoj putanji za pretragu izvršnih  
programa, npr. _/usr/local/bin_ . Proverite koji su direktorijumi  
izlistani u vešoj sistemskoj putanji naredbom **echo $PATH**.  
Ukoliko /usr/local/bin nije unet, unesite ga na slede?i na?in: **export  
PATH=$PATH:/usr/local/bin** . Ovu komandu unesite i u datoteku _.profile_  
u vašem ku?nom direktorijumu na nalogu pod kojim radite ili pak, ukoliko  
imate administratorski pristup sistemu na kom radite, u datoteku _/etc/profile_,  
tako da ?e biti u putanji svih korisnika koji se nakon te izmene  
uloguju.



Poto smo to regulisali, krenu?emo sa programskim delom. U prvoj  
liniji pri izradi bilo kojeg skripta uvek se navodi ta?na putanja do  
prevodioca, u našem slu?aju ona glasi **#!/bin/bash**. Lokaciju  
bilo koje datoteke u vašoj putanji e?te na?i naredbom **whereis  
<ime_datoteke>** pa ukoliko se BASH kod vas ne nalazi u  
direktorijumu _/bin,_ to je na?in da ga pronadjete. Po instalaciji  
bilo koje linux distribucije bi?e tu smešten, mada ako ste sami  
instalirali BASH, verovatno je u folderu  _/usr/local/bin_ .



Skript [delete](http://popeye.ekof.bg.ac.yu/tekst.php?id=8) 



Sve obrisane datoteke mora?emo privremeno skladištiti u nekom  
direktorijumu. On se mora nalaziti u okviru vašeg ku?nog direktorijuma  
da bismo spre?ili poklapanje sa tudjim i na taj na?in omogu?ili rad u  
višekorisni?kom okruženju. Najbolje rešenje zatim nalaže da naziv  
pocinje ta?kom, jer se u UNIX okruženju podrazumeva da se takva imena  
ne izlistavaju standardnim koriš?enjem naredbe &#8220;_ls_<span
 style="font-style: normal;">&#8221;. U našem slu?aju, opredelili smo se za<br /> naziv <b>.kanta</b><span style=""> . Sa tim </span></span> u vidu, naš  
skript za brisanje mora pri startu vršiti proveru da li na sistemu ve?  
postoji skladište za datoteke i ukoliko ga nema, napravi?emo ga.



Slede?i problem sa kojim se susre?emo je preklapanje imena  
datoteka. Naime, vrlo je verovatno da ako danas obrišete recimo neki  
izveštaj ili ?lanak, sutra napravite drugi ali ga snimite pod istim  
nazivom. To bi moglo dovesti do prepisivanja jedne datoteke preko druge  
istoimene. Ukoliko datotekama u skladištu nazive menjamo u skladu sa  
vremenom kada su obrisane, pa nazive korigujemo dodatno slu?ajno  
generisanim brojem (treba imati u vidu da u jednom minutu možete  
obrisati više datoteka) izbe?i?emo navedene nedostatke. Naravno, u cilju  
štednje prostora na hard disku ili eventualnog probijanja kvote sve što  
se skladišti ?emo prethodno kompresovati tar arhiverom. Prilikom  
vra?anja tih fajlova u prethodno stanje, da bismo znali prave nazive,  
vodi?e se i dnevnik o ulasku/izlasku datoteka iz skladišta.



<div align="center">
  <p>
    <b> Undelete komanda</b>
  </p>
</div>



Pri kreiranju interfejsa za oporavak podataka koristi?emo pomo?ni  
program dialog koji je podrazumevano prisutan po instalaciji  
distribucije Slackware, a ukoliko nije uklju?en u sklop vašeg sistema,  
možete ga nabaviti na adresi <u><a
 href="http://freshmeat.net/redir/dialog/13503/url_tgz/dialog-0.7.tar.gz"
 target="_blank"><br /> http://freshmeat.net/redir/dialog/13503/url_tgz/dialog-0.7.tar.gz</a> </u>



![tekst.php](https://linuxo.org/wp-content/uploads/2003/05/tekst.php_.png) 

Slika2: &#8211; izgled interfejsa za povratak obrisanih datoteka



Zahvaljuju?i prethodno napravljenom dnevniku rada, sada ta?no znamo  
iza kog broj?anog naziva se krije odreÄ‘eni fajl.Tako ?emo sa leve  
strane imati šifru, a sa desne pravi naziv dokumenta. Po izboru  
datoteke, vrši se otpakivanje arhive u teku?i direktorijum. Nakon toga  
vršimo ažuriranje dnevnika, kako nam se ne bi u listi prisutnih  
dokumenata u korpi za otpatke našao i dokument koji je ve? vra?en.



Slika3: Skript [undel](http://popeye.ekof.bg.ac.yu/tekst.php?id=9) 

<div align="center">
  <p>
    <b> Delete daemon</b>
  </p>
</div>



Preostaje nam samo da regulišemo redovno pražnjenje naše kante, kako  
ne bi došli u situaciju da nam se prepuni disk. Slede?i listing možete  
uneti u crontab, tako da se startuje svaki dan u odredjeno vreme.  
Ukoliko vam je ra?unar uklju?en 24 ?asa dnevno, najbolje vreme za  
pražnjenje kante je no?u ili rano ujutru, tako da nema opasnosti da  
?ete vršiti neko brisanje istovremeno kad se prazni kanta. U suprotnom,  
rešenje bi bilo da se skript startuje po uklju?enju ra?unara.



Starost datoteka u kanti se odreÄ‘uje na osnovu šifrovanog imena pod  
kojim su arhivirane, tako da prva cifra predstavlja broj odredjenog dana  
u godini. Od nje oduzimamo period maksimalnog vremena koje podaci mogu  
da provedu u skladištu i sve starije od dobijenog datuma brišemo.

Script [deld](http://popeye.ekof.bg.ac.yu/tekst.php?id=10) 

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=316)