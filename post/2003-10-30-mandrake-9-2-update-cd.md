---
author: tomaja
date: "2003-10-30T20:14:24Z"
excerpt: |
  Mandrake Linux 9.2 je odli?na distribucija i što je još bolje, radi
  brže od svog predhodnika. A za brzinu rada podešavanje sistema je jedan
  od najbitnijih koraka (ovo je takoÄ‘e bitno i za  stabilnost
  sistema). Kako uz Mandrake Linux 9.2 dolazi i Update CD red je da
  ukratko objasnim šta dolazi na CDu i kako to iskoristiti.<br>
  Na disku se nalazi preko 370 MB softvera u obliku rpm paketa. Kako i
  kod svake distribucije, sve sitnije greške i li ispravke koje se
  naknadno uo?e treba i da se isprave i upravo tome i služi ovaj CD. Ali
  prvenstveno je bitna nova verzija kernela 2.4.22-18 koja dolazi i za
  kernel-source-om koji se veoma lako instaliraju. U principu, možete
  instalirati kompletan sadržaj CDa sa samo jednom  naredbom koji
  možete ukucati u konzoli, sa root ovlaš?enjima : <span
  style="font-style: italic;">rpm -ivh --force --nodeps *.rpm</span>
  (naravno, ovo pod pretpostavkom da ste pre toga ubacili CD u pogon i
  prešli u direktorijum /mnt/cdrom/rpm . Naravno, niste obavezni da
  instalirate sve, pogotovo ne sve kernele jer vam svi nisu
  potrebni.  Zato možete pokrenuti  Menadžer softreskog koda
  (Meni > Konfiguracija > Pakovanje  > Menadžer softverskog
  koda ) gde , kada prethodno ubacite UpdateCD u CD ureÄ‘aj, možete dodati
  ovaj CD na spisak dostupnih a nakon toga pokrenuti rpmdrake i ...
guid: https://forum.linuxo.org/2003/10/30/mandrake-9-2-update-cd/
id: 387
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Mandrake 9.2 Update CD
url: /mandrake-9-2-update-cd/
---
Mandrake Linux 9.2 je odli?na distribucija i što je još bolje, radi  
brže od svog predhodnika. A za brzinu rada podešavanje sistema je jedan  
od najbitnijih koraka (ovo je takoÄ‘e bitno i za stabilnost  
sistema). Kako uz Mandrake Linux 9.2 dolazi i Update CD red je da  
ukratko objasnim šta dolazi na CDu i kako to iskoristiti.  
Na disku se nalazi preko 370 MB softvera u obliku rpm paketa. Kako i  
kod svake distribucije, sve sitnije greške i li ispravke koje se  
naknadno uo?e treba i da se isprave i upravo tome i služi ovaj CD. Ali  
prvenstveno je bitna nova verzija kernela 2.4.22-18 koja dolazi i za  
kernel-source-om koji se veoma lako instaliraju. U principu, možete  
instalirati kompletan sadržaj CDa sa samo jednom naredbom koji  
možete ukucati u konzoli, sa root ovlaš?enjima : <span
 style="font-style: italic;">rpm -ivh &#8211;force &#8211;nodeps *.rpm</span>  
(naravno, ovo pod pretpostavkom da ste pre toga ubacili CD u pogon i  
prešli u direktorijum /mnt/cdrom/rpm . Naravno, niste obavezni da  
instalirate sve, pogotovo ne sve kernele jer vam svi nisu  
potrebni. Zato možete pokrenuti Menadžer softreskog koda  
(Meni > Konfiguracija > Pakovanje > Menadžer softverskog  
koda ) gde , kada prethodno ubacite UpdateCD u CD ureÄ‘aj, možete dodati  
ovaj CD na spisak dostupnih a nakon toga pokrenuti rpmdrake i &#8230;<!--break-->&#8230;instalirati željene rpm pakete. Naravno, svaki paket možete i

  
pojedina?no instalirati.  
Pored kernela, tu su i novije verzije sistemskih programa poput  
drakxtools, harddrake, a zatim i nove verzje nekih apliakcija kao što je  
na primer mplayer.  
Nakon instalacije kernela (postoji nekoliko optimizovanih verzija, kao  
što su enterprise, 686i , p3 &#8211; smp, zatim nekoliko verzija secure  
kernela.  
Å to se ti?e kernela, nakon instalacije paketa <span
 style="font-style: italic;">kernel-2.4.22.18mdk-1-1mdk.i586.rpm </span>dovoljno  
je retartovati mašinu i pokrenuti sistem sa novim kernelom (nova stavka  
pri izboru za podizanje sistema).  
Ukoliko za pokretanje sistem koristite<span style="font-style: italic;"><br /> lilo </span>, nakon instalacije gore pomenutog fajla dovoljno je da u  
konzoli pokrenete <span style="font-style: italic;">lilo -v </span>nakon  
?ega možete restartovati sistem. Ukoliko koristete <span
 style="font-style: italic;">grub </span>dodatna podešavanja nisu  
potrebna.  
Pored ovoga, obavezno vam preporu?ujemo instalaciju paketa  <span
 style="font-style: italic;">kernel-source-2.4.22-18mdk.i586.rpm </span>koji  
?e vam verovatno biti potreban ukoliko budete hteli da instalirate  
program oblika tar.gz ili src.rpm.

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=387)