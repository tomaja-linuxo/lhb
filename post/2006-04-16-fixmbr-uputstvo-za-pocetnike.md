---
author: popeye
date: "2006-04-16T17:21:13Z"
excerpt: 'Često se početnicima de&scaron;ava da posle instalacije GRUB-a na MBR (Master
  boot record) i kasnije neke gre&scaron;ke, ni Linux , a ni Windows neće da se pokrenu.
  Recimo naknadna promena veličine Windows particije. Najjednostavnije re&scaron;enje
  je da se prvo popravi Windows upisivanjem novog MBR-a.              '
guid: https://forum.linuxo.org/2006/04/16/fixmbr-uputstvo-za-pocetnike/
id: 1118
title: FIXMBR &#8211; uputstvo za početnike
url: /fixmbr-uputstvo-za-pocetnike/
---
Često se početnicima de&scaron;ava da posle instalacije GRUB-a na MBR (Master boot record) i kasnije neke gre&scaron;ke, ni Linux , a ni Windows neće da se pokrenu. Recimo naknadna promena veličine Windows particije. Najjednostavnije re&scaron;enje je da se prvo popravi Windows upisivanjem novog MBR-a. <!--break-->Kada Windows neće da krene, pokreni instalaciju sa CD-a i kada se zaustavi na: Welcome to setup, ne pritiskaj enter, nego samo taster R. Dole i pi&scaron;e obja&scaron;njenje (R=repair). Sačekaj da se pokrene Recovery console. Proveri da li ti je na tastaturi uključeno Num Lock i pritisni taster 1, pa enter. Tražiće ti Administrator password, ako zna&scaron; &scaron;ifru upi&scaron;i je, pa pritisni enter (ukoliko ne zna&scaron; &scaron;ifru ili zna&scaron; da je nema, jednostavno samo pritisni enter) i kada napi&scaron;e C:WINDOWS upi&scaron;i fixmbr i pritisni enter. Na Are you sure you want to write a new MBR? upi&scaron;i y i pritisni enter. Kada napi&scaron;e: The new master boot record has been succesfuly written. upi&scaron;i exit, pritisni enter i izvadi Windowsov instalacioni CD. 

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=1118)