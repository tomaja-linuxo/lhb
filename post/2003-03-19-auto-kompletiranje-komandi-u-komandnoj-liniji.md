---
author: tomaja
date: "2003-03-19T15:28:51Z"
excerpt: |
  Auto-kompletiranje naredbi je veoma korisna funkcija, i svi moderni
  shell-ovi (naravno i bash) imaju ovu mogu?nost. Njena svrha je omogu?i
  koriniku što brže kucanje i rad u komandnoj liniji, odnosno konzoli.
  Najbolji na?in da prikažemo kompletiranje jeste da to uradimo kroz
  primer. Vrrlloooo korisna stvar, a i kada vas neko vidi kako radite brzo
  u konzoli, dobijate poen kod doti?ne osobe !<br>
  Pretpostavimo da vaš li?ni direktorijum sadrži
  fajl_sa_veoma_dugim_imenom_koje_je _teško_za_kucanje, a želite da ga
  pogledate, raspakujete, prekopirate i sli?no. TakoÄ‘e, možemo da
  pretpostavimo da , u istom direktorijumu, imate i još jedan fajl sa
  imenom fajl_text. Ako se nalazite u tom direktorijumu, ukucajte slede?i
  komandu:
guid: https://forum.linuxo.org/2003/03/19/auto-kompletiranje-komandi-u-komandnoj-liniji/
id: 297
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Auto-kompletiranje komandi u komandnoj liniji
url: /auto-kompletiranje-komandi-u-komandnoj-liniji/
---
Auto-kompletiranje naredbi je veoma korisna funkcija, i svi moderni  
shell-ovi (naravno i bash) imaju ovu mogu?nost. Njena svrha je omogu?i  
koriniku što brže kucanje i rad u komandnoj liniji, odnosno konzoli.  
Najbolji na?in da prikažemo kompletiranje jeste da to uradimo kroz  
primer. Vrrlloooo korisna stvar, a i kada vas neko vidi kako radite brzo  
u konzoli, dobijate poen kod doti?ne osobe !  
Pretpostavimo da vaš li?ni direktorijum sadrži  
fajl\_sa\_veoma\_dugim\_imenom\_koje\_je \_teško\_za_kucanje, a želite da ga  
pogledate, raspakujete, prekopirate i sli?no. TakoÄ‘e, možemo da  
pretpostavimo da , u istom direktorijumu, imate i još jedan fajl sa  
imenom fajl_text. Ako se nalazite u tom direktorijumu, ukucajte slede?i  
komandu:<!--break-->

  
$ less fa<TAB>

(odnosno ukucajte less fa a zatim pritisnite taster TAB). Shell ?e sam  
prošiti komandu za vas:

$ less fajl_

a prikaza?e vam i listu mogu?ih fajlova koji po?inju sa fajl_.  
Zatim ukucajte slede?i sekvencu:

less file_s<TAB>

i onda ?e shell proširiti komandnu liniju da bi vam prikayao  
rezultat koji ste želeli:

fajl\_sa\_veoma\_dugim\_imenom\_koje\_je \_teško\_za_kucanje

Sve što nakon ovoga treba da uradite je da pritsnete taster Enter da bi  
pro?itali ovaj fajl.  
Naravno, umesto naredbe less možete koristiti i druge naredbe , kao na  
primer dir, ls, &#8230;

<span style="text-decoration: underline;">Drugi metodi<br /> auto-kompletiranja</span>

Taster TAB nije jedini na?in za izvoÄ‘enje auto kompletiranja naredbi,  
iako je jedan od naj?eš?e koriš?enih. Kao opšte pravilo, prva re? može  
biti kompletirana u komandnoj liniji (nsl<TAB> ?e nam dati  
nslookup), kao i imena fajlova i svega drugoga, osim ukoliko re? ne  
sadrži &#8222;specijalne&#8220; karaktere kao što su ~, @ ili $, kada ?e  
shell pokušati da dovrši korisni?ko ime, ime ra?unara ili promenljivu  
(ovde ne treba zaboraviti da linux razlikuje velika i mala slova pa  
tako promenljiva HOME i home nisu ista stvar). TakoÄ‘e postoje  
specijalni znakovi za dovršavanje imena komande(!) ili imena fajla (/). 

Druga dva na?ina za auto-kompletiranje su sekvence Esc-<x> i  
Ctrl+x <x>, gde je <x> jedan od specijalnih karaktera koje  
smo gore pomenuli. Esc-<x> ?e pokušati da prikaže samo jednu  
kompletiranu komandu. Ako ne uspe, pokaza?e najve?u mogu?u listu  
izbora. Ukoliko ?ujete sistemski zvu?nik, ili izbor nije jedinstven, ili  
jednostavno nema odgovaraju?eg izbora. Sekvenca Ctrl+x <x>  
prikazuje listu mogu?eg izbora bez pokušaja da uradi  
auto-kompletiranje. Pritiskom na taster TAB jednostavno sukcesivno  
izvršavate sekvence Esc-<x> i Ctrl+x <x>

A jedan od na?ina da vidite sve sistemske promenqive jeste da ukucate  
sekvencu Ctrl+x $ u praznoj liniji.  
Još jedan primer: ukoliko recimo želite da vidite man stranicu za  
komandu hdparm, samo ukucajte hdp a zatim Esc-!, i shell ?e  
automatski dovršiti naredbu o man hdparm.

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=297)