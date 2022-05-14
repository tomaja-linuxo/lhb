---
author: tomaja
date: "2005-01-30T06:10:37Z"
excerpt: Varijanta mrežnog crva Forbot širi se po Internetu preko MySQL servera na
  Windowsu. To je prvi poznat slu?aj automatizovanog napada na program MySQL, a prime?en
  je u sredu u Australiji. Karakteristi?na infekcija prepoznaje se po programu spoolcll.exe
  koji se povezuje na IRC server u Å vedskoj, i skenira priklju?ke 3306 (na kojima
  se obi?no nalazi MySQL).
guid: https://forum.linuxo.org/2005/01/30/nov-crv-napada-mysql-na-windows-u/
id: 725
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Nov crv napada MySQL na Windows-u
url: /nov-crv-napada-mysql-na-windows-u/
---
Varijanta mrežnog crva Forbot širi se po Internetu preko MySQL servera na Windowsu. To je prvi poznat slu?aj automatizovanog napada na program MySQL, a prime?en je u sredu u Australiji. Karakteristi?na infekcija prepoznaje se po programu spoolcll.exe koji se povezuje na IRC server u Å vedskoj, i skenira priklju?ke 3306 (na kojima se obi?no nalazi MySQL).<!--break-->

Nova verzija Forbota zloupotrebljava sisteme na kojima nisu zadate administratorske lozinke za MySQL ili se te lozinke lako pogaÄ‘aju. Johanes Ulrih, rukovodilac centra Internet Storm u institutu SANS, kaže da taj crv isprobava kombinacije oko 1000 naj?eš?ih lozinki i da je provera IRC kanala u ?etvrtak ujutro pokazala da se preko 8000 ra?unara povezalo na njega.

Ulrih smatra da još hiljade ra?unara ve? mogu biti zaražene, ali da širenje usporava zagušeni IRC server.

Nakon što crv dobije administratorski pristup sistemu MySQL, zloupotrebljava propust u dinami?koj biblioteci UDF i instalira trojance na sistem. Zaraženi ra?unari zasad samo skeniraju Mrežu i traže druge potencijalne žrtve, ali antivirusni stru?njaci smatraju da se funkcija trojanca može promeniti slanjem komandi putem IRC kanala.

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=725)