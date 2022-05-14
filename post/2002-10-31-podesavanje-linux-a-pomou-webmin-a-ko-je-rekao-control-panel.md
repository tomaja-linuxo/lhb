---
author: tomaja
date: "2002-10-31T15:40:44Z"
excerpt: |
  ?esto se po?etnici ali i iskusniji sre?u sa problemom gde se nalaze pojedini<br>
  konfiguracioni fajovi. "Ma gde ono beše conf fajl za sambu ?" Iako Mandrake
  <br>
  Linux ima svoj Kontrolni Centar on ipak još uvek nije predviÄ‘en za takve vrste
  podešavanja.<br>
  Ali rešenje postoji: <b>webmin</b>  Dobro, možda ?e se neki pobuniti
  i re?i ma daj, <br>
  podesi to ru?no, ali mislim da ve?inu stvari iz njega možete brzo i sigurno
  da namestite<br>
  i da vas ne boli glava. Sve što treba da uradite...
guid: https://forum.linuxo.org/2002/10/31/podesavanje-linux-a-pomou-webmin-a-ko-je-rekao-control-panel/
id: 229
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Podešavanje Linux-a pomo?u Webmin-a (ko je rekao Control Panel ?)
url: /podesavanje-linux-a-pomou-webmin-a-ko-je-rekao-control-panel/
---
?esto se po?etnici ali i iskusniji sre?u sa problemom gde se nalaze pojedini  
konfiguracioni fajovi. &#8222;Ma gde ono beše conf fajl za sambu ?&#8220; Iako Mandrake  
  
Linux ima svoj Kontrolni Centar on ipak još uvek nije predviÄ‘en za takve vrste  
podešavanja.  
Ali rešenje postoji: **webmin** Dobro, možda ?e se neki pobuniti  
i re?i ma daj,  
podesi to ru?no, ali mislim da ve?inu stvari iz njega možete brzo i sigurno  
da namestite  
i da vas ne boli glava. Sve što treba da uradite&#8230;<!--break-->&#8230; jeste da imate instaliran i pokrenut webmin servis. Ako ga i niste

  
instalirali, ne brinite,  
imate ga na isntalacionim diskovima Mandrake Linux 8.0, 8.1, 8.2 i  
9.0. Naravno, instalirajte onaj koji se nalazi  
na disku verzije koju trenutno koristite

Dakle, otvorite svoj omiljeni web pretraživa? (ja li?no preferiram Galeon)  
i u prostoru za unos web adrese ukucajte:

_**https://localhost:10000/**_ 

Nakon toga, unesite root za user-a i njegovu lozinku i pogledajte šta ste  
dobili.  
Ako vas ?uti da je u pitanju secure server znajte da je u osnovi webmin namenjen  
kontroli sa udaljenih (mrežnih) mašina ali  
?e i desktop korisnicima dobro odraditi posao.A koji je to posao ?  
Pa iz njega možete da podesite gotovo sve. Od **sistemskih opcija** kao  
što su backup sistema, podešavanje shutdown opcije, podešavanje korisnika,  
lozinki, startnih ili init servisa, podešavanje lokalnih i mrežnih fajl sistema,  
sheduled komandi, podešavanje nivo sigurnosti, rpm paketa i još mnogo toga.  
Å to se ti?e **servera** možete podesiti gotovo sve: Apache web server,  
Sambu, DNS, CVS servere, fetchmail, ftp servere, MySQL i druge baze, PPP,  
postfix, proxy server i da ne nabrajam dalje.  
Kada je u pitanju **hardver** tu je podešavanje RAID-a, CD reza?a, Grub  
startera, mrežna konfiguracija, particije na hard diskovima, štampa?i i dr.  
+ još nekoliko desetina drugih opcija. 

Treba napomenuti da se, naravno može podešavati i sam webmin pa ?ak možete  
da menjate i njegov izgled jer možete da odaberete jednu od 7 ponuÄ‘enih tema  
ili da ubacite neku novu.

Dakle, toplo preporu?ujem da gabar pogledate a kome se dopadne nek izvoli.

**PAÅ½NJA**: pomo?u webmin-a možete štošta da podesite ali i mnogo toga  
da pokvarite pa ?ak i da oštetite sistem, zato pazite šta radite. Ako vam  
nešto nije jasno ili niste sigurni, nemojte da dirate default postavku.

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=229)