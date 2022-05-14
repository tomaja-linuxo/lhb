---
author: tomaja
date: "2003-02-06T16:52:41Z"
excerpt: |
  Nova, ažurirana verzija kernela je sada dostupna za Mandrake linux 9.0 .
  Ova verzija nosi oznaku 2.4.19-24. Ispravljene su sve poznate greške tako
  da na  primer Supermount potpuno preraÄ‘en i sada bi trebalo da funkcioniše
  bez problema na svim ra?unarima. Ostale ispravke uklju?uju i XFS sa velikom
  moemorijom, prepravljeni netfilter, takoÄ‘e ispravku za Sony VAIO DMI, a i845
  ?ip set sada radi sa UDMA modom , a uklju?ena je i podrška za VIA C3.
guid: https://forum.linuxo.org/2003/02/06/novi-kernel-za-mandrake-9-0/
id: 288
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Novi kernel za Mandrake 9.0
url: /novi-kernel-za-mandrake-9-0/
---
Nova, ažurirana verzija kernela je sada dostupna za Mandrake linux 9.0 .  
Ova verzija nosi oznaku 2.4.19-24. Ispravljene su sve poznate greške tako  
da na primer Supermount potpuno preraÄ‘en i sada bi trebalo da funkcioniše  
bez problema na svim ra?unarima. Ostale ispravke uklju?uju i XFS sa velikom  
moemorijom, prepravljeni netfilter, takoÄ‘e ispravku za Sony VAIO DMI, a i845  
?ip set sada radi sa UDMA modom , a uklju?ena je i podrška za VIA C3.<!--break-->Ova nova verzija takoÄ‘e ispravlja sigurnosni problem koji je dozvoljavao non-root

  
korisnicima da zamrznu kernel, kao i ispravku za ranjivost u O_DIRECT  
handling koji može da kreira ograni?eno curenje informacija pomo?u koga svaki  
korisnik na sistemu sa write privilegijama na fajl sistemu može koristiti  
prethodno izbrisane fajlove.  
O ovome možete više pro?itati na linku:  
<http://cve.mitre.org/cgi-bin/cvename.cgi?name=CAN-2003-0018>

Pakete koji treba da se update-uju:

Mandrake Linux 9.0:  
ed3a07724f3b510d3d57fe35fc601e78 9.0/RPMS/kernel-2.4.19.24mdk-1-1mdk.i586.rpm  
8b5b1721639ff0f137650fed781b2061 9.0/RPMS/kernel-BOOT-2.4.19.24mdk-1-1mdk.i586.rpm  
db575a265fb967568af320072132ac50 9.0/RPMS/kernel-doc-2.4.19-24mdk.i586.rpm  
998177a07d674e2ca94c9cdcf3ee2ef4 9.0/RPMS/kernel-enterprise-2.4.19.24mdk-1-1mdk.i586.rpm  
da5d2a2cbada7b6db04468eadcf94979 9.0/RPMS/kernel-secure-2.4.19.24mdk-1-1mdk.i586.rpm  
33543e3392b9afda0f663d880a733614 9.0/RPMS/kernel-smp-2.4.19.24mdk-1-1mdk.i586.rpm  
cba769d4bdec28c862b1c84498106f2d 9.0/RPMS/kernel-source-2.4.19-24mdk.i586.rpm  
8b446dc9c29a72a34fa3e63d2ca3ae8c 9.0/SRPMS/kernel-2.4.19.24mdk-1-1mdk.src.rpm

Za update preporu?ujem koriš?enje MandrakeUpdate programa, a ko voli da to  
&#8222;ru?no&#8220; obavi može da poseti neki od Mandrake [miror sajtova](http://www.mandrakesecure.net/en/ftp.php), skine  
pakete i instalira ih pomo?u komande &#8222;rpm -Fvh *.rpm&#8220;

Svakako vam toplo preporu?ujem ovaj update.

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=288)