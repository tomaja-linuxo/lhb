---
author: tomaja
date: "2004-12-14T09:07:54Z"
excerpt: Zakazivac je jedan od najvaznijih delova sistema, pored upravljaca memorijom
  i kontrole hardvera. On u njegovoj najjednostavnijoj formi formira listu zadataka
  sortiranu po prioritetima. I posle dodele prioriteta
guid: https://forum.linuxo.org/2004/12/14/zakazivai-na-linuxu/
id: 661
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Zakaziva?i na Linuxu
url: /zakazivai-na-linuxu/
---
Zakazivac je jedan od najvaznijih delova sistema, pored upravljaca memorijom i kontrole hardvera. On u njegovoj najjednostavnijoj formi formira listu zadataka sortiranu po prioritetima. I posle dodele prioriteta<!--break-->Zakazivac je jedan od najvaznijih delova sistema, pored upravljaca memorijom i kontrole hardvera. On u njegovoj najjednostavnijoj formi formira listu zadataka sortiranu po prioritetima. I posle dodele prioriteta dodeljuje mu procesorsko vreme i druge bitne resurse.

  
Proces se izvrsava u toku svog vremena ili dok ga ne prekinu ulazno/izlazne operacije, signali,&#8230; Ako proces nije zavrsen prebacuje se u listu cekanja (_waiting queue_) i dodeljuje mu se novi prioritet.  
  
Glavni delovi algoritma za zakazivanje su sledeci:

  * Uredjivanje zadataka po prioritetima</ul> 
  * Preracunavanje prioriteta</ul> 
  * Odabir zadataka sa najvisim prioritetom</ul> 
Kod odabira algoritma za zakazivac moramo da vodimo racuna o vrsti zadataka koji ce se obavljati. Kod sistema velikog odziva na integrisanim sistemima bitno je da se sistemski procesi izvrsavaju sa malim vremenom odziva. Dok kod desktop sistema je bitno da smanji vreme cekanja i da se maksimalno iskoristi CPU(Glavna Procesorska Jedinica).

**Linux v2.4**

Kod v2.4 Linux kernela imamo dve liste **Aktivnu Listu** i **Isteklu Listu**. Zadaci koji treba da se izvrsavaju se nalaze u Aktivnoj Listi i kad se izvrse prebacuju se u Isteklu Listu. Kad se isprazni Aktivna Lista uzimamo procese iz Istekle Liste i dodeljujemo im nove prioritete i formiramo novu Aktivnu Listu. Ovde slozenost algoritma raste linearno sa brojem procesa, zato sto pri dodeljivanju novih prioriteta se ide redom kroz listu.  
  
I kod SMP(Vise Procesorski Sistemi) i jedno procesorskih sistema imamo jednu globalnu Aktivnu Listu. I kada jedan od procesora oce da menja listu mora da otkljucava VELIKU BRAVU (GLOBAL BIG KERNEL LOCK) i naravno posle zakljucava.  
  
Lose je da kod SMP sistema npr. jedan zadatak Z1 se izvrsava na procesoru P1. Posle nista ne garantuje da ce se sledeci put zadatak Z1 izvrsavati na procesoru P1, sto znaci da ce ponovo morati da se puni kes procesora P2 sa relevantnim podacima.  
  
Ovaj kernel je tzv. _non-preemtive kernel_, sto znaci da kada se neki proces u kernelu izvrsava, makar on bio i niskog nivoa, svi ostali procesi sede i cekaju. To je lose kod sistema visokog odziva.  
Sve ove lose osobine Linux v2.4 kernela su ispravljene u novom v2.6 kernelu a sada cemo i videti kako.

**Linux v2.6**

Ovaj kernel spada u _preemtible_ kernele. Ali ne u potpunosti jos uvek postoje neki procesi u kernelu koje nije moguce prekidati. Jer naravno u svemu treba biti umeren.  
  
Da sada imamo novi algoritam za zakazivac kod kog neraste linearno sa brojem procesa slozenost. Ovaj algoritam kada se izvrsi zadatak iz aktivne liste prebacuje je u isteklu listu i dodelju je joj novi prioritet. I kada se isprazni aktivna lista umesto da seta po istekloj listi on samo promeni pokazivac tako da pokazuje na isteklu listu i pocinje redom da izvrsava zadatke. Lepo zar ne?  
  
Sto se tice SMP sistema, sada imamo jednu listu za svaki procesor. Tako da vreme utroseno na ponovno punjenje kesa svodimo na minimum. Ovde moramo imati u vidu da bi bilo lose ako bi se neki procesi izvrsavali samo na jednom procesoru svo vreme jer drugi procesor bi mogao biti manje iskoriscen. Pa se i ovde postuje pravilo umerenosti.

**Zakljucak**

Naravno ovo nije kraj i nije napravljen savrseni zakazivac, ali smo na dobrom putu. Uvek kao kod svih drugih stvari treba postaviti nedostizan cilj i ici ka njemu kao da je dostizan jer tek tada cemo dati maksimum od sebe.

> <tt><br /> Ovaj clanak je vecim delom uzet sa <a href="http://www.linuxgazette.com/node/9746">Linux Gazett</a> sajta. Zahvaljujem se Nikhil Bhargava na sjajnom clanku.<br /> Wrote by Stale.<br /> </tt> 

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=661)