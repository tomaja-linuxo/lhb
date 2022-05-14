---
author: zchira
date: "2007-08-03T16:25:40Z"
excerpt: Ako hoćete da pomognete izradu ove igre tako &scaron;to ćete praviti nivoe
  ovo je tekst za vas.
guid: https://forum.linuxo.org/2007/08/03/uputstvo-za-pravljenje-nivoa/
id: 1835
image: /wp-content/uploads/2007/08/lavirinto-uputstvo.png
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";s:4:"1834";s:11:"_thumb_type";s:5:"thumb";}
title: Uputstvo za pravljenje nivoa
url: /uputstvo-za-pravljenje-nivoa/
---
Ako hoćete da pomognete izradu ove igre tako &scaron;to ćete praviti nivoe ovo je tekst za vas.<!--break-->

<img class=" alignleft size-full wp-image-1834" src="https://linuxo.org/wp-content/uploads/2007/08/lavirinto-uputstvo.png" align="left" alt="" width="800" height="600" srcset="https://linuxo.org/wp-content/uploads/2007/08/lavirinto-uputstvo.png 800w, https://linuxo.org/wp-content/uploads/2007/08/lavirinto-uputstvo-300x225.png 300w, https://linuxo.org/wp-content/uploads/2007/08/lavirinto-uputstvo-768x576.png 768w" sizes="(max-width: 800px) 100vw, 800px" /> 

U igri Lavirinto svi nivoi se čuvaju u tekstualnim fajlovima.  
Primer jednog nivoa&nbsp; izgleda ovako:

#&nbsp; komentar  
\# dimenzije  
dim: 4 3  
\# ide opis devet polja (3&#215;3)  
\# North East South West , 0 nema kraka, 1 ima  
1 0 1 1  
1 1 1 1  
1 1 1 1  
1 0 1 0  
1 0 0 1  
1 1 0 1  
0 1 1 1  
0 0 1 1  
1 1 0 0  
0 1 0 1  
0 0 1 1  
1 1 1 1  
dim-end

levelname:  
Look out! There is a monstero!

\# pocetna pozicija igraca &#8211; unosi se redni broj polja (pocinje od 0)  
start: 0

monsters1: 1  
2 

\# vreme za prelazenje nivoa u sekundama  
time: 150

\## end

&nbsp;

Redovi koji počinju sa # su komentari i oni nisu bitni.  
Obja&scaron;njenje ostalih redova:  
dim: 4 3&nbsp;&nbsp;&nbsp; &#8211; dimenzije table (na slici su označene crvenim brojevima)  
Po&scaron;to je 4*3=12, potrebno je redom (od 0 do 12) definisati svih 12 polja table. To se čini u sledećih 12 redova (plavi brojevi na slici). Redni broj polja je na slici označen zelenom bojom. Posle definisanja svih polja obavezno ide red u kome stoji "dim-end".  
levelname: &nbsp;&nbsp;&nbsp; &#8211; u redu ipod ove oznake ide naziv nivoa (na slici "Look out! There is monstero!")  
start: &nbsp;&nbsp; &#8211; ovde se unosi redni broj polja sa kog startuje igrač (0 na slici)  
monsters1: &nbsp;&nbsp;&nbsp; &#8211;&nbsp;&nbsp;&nbsp; broj čudovi&scaron;ta. Ispod toga se u svakom narednom redu unosi redni broj polja sa kog startuju čudovi&scaron;ta (u gornjem primeru ima jednog čudovi&scaron;ta koje startuje sa polja 2)  
time:&nbsp;&nbsp;&nbsp; &#8211;&nbsp;&nbsp;&nbsp; vreme u sekundama.  
Na kraju obavezno ide red ## end. 

&nbsp;

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=1835)