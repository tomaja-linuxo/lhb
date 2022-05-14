---
author: tomaja
date: "2003-11-24T14:58:04Z"
excerpt: |
  Desava se da se, prilikom instalacije X servera i podesavanja rezolucije monitora, slika na ekranu monitora deformise, i to najcese tako da se sadrzaj ekrana pomera udesno. Uzrok tome su, uglavnom, genericki drajveri za graficku karticu, i ta pojava najcese nestaje kada se instaliraju originalni proizvodjacki drajveri.
  Medjutim, postavlja se pitanje sta raditi ako proizvodjac nije napravio drajvere?
guid: https://forum.linuxo.org/2003/11/24/fino-podesavanje-rezolucije-monitora/
id: 394
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Fino podesavanje rezolucije monitora
url: /fino-podesavanje-rezolucije-monitora/
---
Desava se da se, prilikom instalacije X servera i podesavanja rezolucije monitora, slika na ekranu monitora deformise, i to najcese tako da se sadrzaj ekrana pomera udesno. Uzrok tome su, uglavnom, genericki drajveri za graficku karticu, i ta pojava najcese nestaje kada se instaliraju originalni proizvodjacki drajveri.  
Medjutim, postavlja se pitanje sta raditi ako proizvodjac nije napravio drajvere?<!--break-->Jedno od resenja je koriscenje aplikacije 

**xvidtune**. Ova aplikacije je najcesce instalirana jos prilikom instalacije linuxa. Pokrece se iz konzole tako sto se ukuca **xvidtune**. Pojavljuje se graficki interfejs koji je dovoljno jasan i za pocetnike. Treba napomenuti da, pre bilo kakvih podesavanja, treba ukljuciti opciju **&#8222;Auto&#8220;**, jer se onda svaki korak u podesavanju odmah pokazuje na ekranu (pre svih podesavanja treba se i do detalja upoznati sa mogucnostima vaseg monitora, t.j. koje rezolucije i frekvencije osvezavanja podrzava).  
Kada ste podesili sliku na vasem monitoru, sledi jos jedan bitan korak: snimiti podesavanja tako da se ucitavaju pri svakom podizanju X servera. To se postize tako sto se klikne na dugme **&#8222;Show&#8220;**, kada se u konzoli ispisuje nasto kao: **&#8222;800&#215;600&#8220; 34.40 800 816 944 1008 600 603 607 628 +hsync +vsync** . Necu ulaziti u to sta to sve znaci, ali cu naglasiti da ovaj red treba dodati na kraju **&#8222;Section &#8222;Monitor&#8220;&#8220;** fajla **&#8222;XF86Config-4&#8220;** koji se nalazi u direktorijumu /etc/X11 i to tako sto se ispred navedenog reda dopise **&#8222;ModeLine&#8220;**. Evo nekoliko redova navedenog fajla:

&#8222;&#8230;  
\# 768&#215;576 @ 100 Hz, 61.6 kHz hsync  
ModeLine &#8222;768&#215;576&#8220; 63.07 768 800 960 1024 576 578 590 616  
ModeLine &#8222;800&#215;600&#8220; 34.402 800 816 944 1008 600 603 607 628 +hsync +vsync  
EndSection  
Section &#8222;Device&#8220;  
Identifier &#8222;device1&#8243; &#8230; &#8220;

Fajl **&#8222;XF86Config-4&#8220;** se otvara pomocu nekog od editora, npr. gedit i to obavezno kao root.  
Na kraju snimite izmene i restartujte X server.  
Ukoliko nesto krene naopako (recimo trese slika ili slicno), protisnite istovremeno Ctrl, Alt i F1, ulogujte se kao root, pokrenite midnight commander (komanda mc), nadjite fajl /etc/X11/XF86Config-4, editujte ga i izbrisite red koji ste prethodno uneli, na kraju restartujte racunar (reboot) i sve se vraca na pocetno stanje.  
Nadam se da ce ovo kratko uputstvo biti korisno pocetnicima.

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=394)