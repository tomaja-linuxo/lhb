---
author: tomaja
date: "2004-09-30T09:14:02Z"
excerpt: Koliko puta ste imali problema sa ošte?enim ili loše narezanim kompakt diskovima
  sa kojih nikako niste mogli da spasete podatke? Sre?om, postoji na?in da to izvedete
  uz pomoc CDfs fajl sistema.
guid: https://forum.linuxo.org/2004/09/30/cdfs-spasite-podatke-sa-ostecenih-diskova/
id: 537
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: CDfs &#8211; Spasite podatke sa ostecenih diskova
url: /cdfs-spasite-podatke-sa-ostecenih-diskova/
---
Koliko puta ste imali problema sa ošte?enim ili loše narezanim kompakt diskovima sa kojih nikako niste mogli da spasete podatke? Sre?om, postoji na?in da to izvedete uz pomoc CDfs fajl sistema.<!--break-->Kada problemati?ni disk komandom

  
 _mount -t cdfs /dev/path\_to\_cdrom /mnt/path\_to\_cdrom\_mount\_dir_ </br>  
mountujete kao cdfs, a ne iso9660 fajl sistem, u svom /mnt/cdrom diretorijumu umesto fajlova koji se nalaze na disku, videcete jedan ili vise fajlova sa ekstenzijom *.iso (u zavisnosti od toga da li je disk snimljen kao single ili multisession) koje ?ete, za razliku od klasi?nog iso9660 mountovanja, mo?i u celini da iskopirate na hard disk. Prekopiran iso image kasnije mozete snimiti na CD ili mountovati u zeljeni direktorijum komandom mount -o loop path\_to\_isoimage path\_to\_mount_dir i to je sve. Podaci su spašeni. &#8216;Pa to radi i IsoBuster!?&#8217; Verujte, mnogo lošije od CDfs-a. Provereno. CDfs, kao i uputstvo instalaciju možete prona?i na linku  
<http://www.elis.rug.ac.be/~Eronsse/cdfs/>

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=537)