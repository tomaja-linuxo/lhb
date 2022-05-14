---
author: tomaja
date: "2004-12-13T05:23:55Z"
excerpt: |
  <a href="http://www.kroah.com/" target="new">Greg Kroah-Hartman</a>
  je najavio kreiranje debugfs, in-kernel fajl sistema dizajniranog da
  pomogne programerima koji rade na razvoju kernela da lako eksportuju
  podatke koji nastaju pri dibagovanju na korisni?ki prostor. (debugfs
  nema ništa sa the ext2-ovim debuggerom iako imaju isto ime). Zajedno
  sa patch-om koji se ubacuje u 2.6.10-rc3 [<a
  href="http://kerneltrap.org/node/view/4351">tekst</a>],
guid: https://forum.linuxo.org/2004/12/13/kernel-debugfs/
id: 659
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: 'Kernel: DebugFS'
url: /kernel-debugfs/
---
<a href="http://www.kroah.com/" target="new">Greg Kroah-Hartman</a>  
je najavio kreiranje debugfs, in-kernel fajl sistema dizajniranog da  
pomogne programerima koji rade na razvoju kernela da lako eksportuju  
podatke koji nastaju pri dibagovanju na korisni?ki prostor. (debugfs  
nema ništa sa the ext2-ovim debuggerom iako imaju isto ime). Zajedno  
sa patch-om koji se ubacuje u 2.6.10-rc3 [[tekst](http://kerneltrap.org/node/view/4351)], <!--break-->

Greg je ponudio i par primera da bi pokaza kako je lako  
koristiti debugfs. Na primer, za eksportovanje pojedina?ne vrednosti u  
korisnilki prostor, da je i primer: 

struct dentry \*debugfs\_create\_u8(const char \*name, mode_t mode,  
struct dentry \*parent, u8 \*value); 

&#8222;To je to, jedna linija koda i dobijate promenljivu koju možete  
menjati iz korisni?kog prostora.&#8220;  
Kako slede?i promer on je obezbedio patch za USB uhci drajver  
konvertuju?i ga koriste?i /proc/driver/uhci debugfs, smanjuju?i  
ukupnu veli?inu drajvera. Greg je naveo da patch još mora da se doradi  
ali je u potpunosti funkcionalan i spreman za feedback.

Izvor: kerneltrap.org

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=659)