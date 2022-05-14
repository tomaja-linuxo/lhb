---
author: tomaja
date: "2007-11-03T13:45:45Z"
excerpt: '<p align="justify">Njima (kreatorima) a i nama be&scaron;e drago da najavimo
  novu finalnu verziju OpenBSD-a 4.2. Ovo je već 23 izdanje ovog ultra sigurnog operativnog
  sistema koji sada ima pro&scaron;iren radijus dejstva i na nove platforme poput
  OpenBSD/sparc64, OpenBSD/hppa, OpenBSD/alpha. Pored toga do&scaron;lo je do promena
  u metodu instalacije - pomoću 200MB CD ISO fajla koji omogućava instalaciju bez
  potrebe za internet konekcijom, odnosno mrežnom instalacijom. Unapređena je značajno
  i hardverska podr&scaron;ka pa tako novi OpenBSD sadrži podr&scaron;ku za Native
  Serial-ATA, ahci(4) drajver za SATA, nove drajvere za PATA diskove, mrežne kontrolere,
  wireless kartice, drajvere za USB touch ekrane, grafičke kartice i gomile drugog
  hardvera. Tu su i novi alati poput cwm (novi &quot;lite&quot; menadžer prozora),
  zless (pregled komresovanih fajlova), mount_vnd (alaz za konfigurisanje vnode diskova
  iz fstab-a). Nove funkcionalnosti: FFS2, nova verzija brzog fajl sistema,&nbsp;
  pkg_add je značajno unapređen, itd. Zaista, sve vredno pažnje. Na sve ovo treba
  dodatni preko 4500 portova (binarnih paketa) sa pripremljenim softverom kao &scaron;to
  su:</p><div style="text-align: center"><img class=" size-full wp-image-1916" src="https://linuxo.org/wp-content/uploads/2007/11/puffy42.jpg"
  alt="OpenBSD 4.2" title="OpenBSD 4.2" width="400" height="133" />&nbsp;</div><p>o
  Gnome 2.18.<br />      o GNUstep 1.14.<br />      o KDE 3.5.7 i koffice 1.6.3.<br
  />      o Xfce 4.4.1.<br />      o OpenMotif 2.3.0.<br />      o OpenOffice.org
  2.2.1.<br />      o Mozilla Firefox 2.0.0.6.<br />      o PostgreSQL 8.2.4.<br />      o
  GHC 6.6.1 (samo amd64 i&nbsp; i386)</p>'
guid: https://forum.linuxo.org/2007/11/03/slobodan-funkcionalan-i-siguran-openbsd-4-2/
id: 1917
image: /wp-content/uploads/2007/11/puffy42.jpg
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";s:4:"1916";s:11:"_thumb_type";s:5:"thumb";}
title: 'Slobodan, funkcionalan i siguran: OpenBSD 4.2'
url: /slobodan-funkcionalan-i-siguran-openbsd-4-2/
---
<p align="justify">
  Njima (kreatorima) a i nama be&scaron;e drago da najavimo novu finalnu verziju OpenBSD-a 4.2. Ovo je već 23 izdanje ovog ultra sigurnog operativnog sistema koji sada ima pro&scaron;iren radijus dejstva i na nove platforme poput OpenBSD/sparc64, OpenBSD/hppa, OpenBSD/alpha. Pored toga do&scaron;lo je do promena u metodu instalacije &#8211; pomoću 200MB CD ISO fajla koji omogućava instalaciju bez potrebe za internet konekcijom, odnosno mrežnom instalacijom. Unapređena je značajno i hardverska podr&scaron;ka pa tako novi OpenBSD sadrži podr&scaron;ku za Native Serial-ATA, ahci(4) drajver za SATA, nove drajvere za PATA diskove, mrežne kontrolere, wireless kartice, drajvere za USB touch ekrane, grafičke kartice i gomile drugog hardvera. Tu su i novi alati poput cwm (novi "lite" menadžer prozora), zless (pregled komresovanih fajlova), mount_vnd (alaz za konfigurisanje vnode diskova iz fstab-a). Nove funkcionalnosti: FFS2, nova verzija brzog fajl sistema,&nbsp; pkg_add je značajno unapređen, itd. Zaista, sve vredno pažnje. Na sve ovo treba dodatni preko 4500 portova (binarnih paketa) sa pripremljenim softverom kao &scaron;to su:
</p>

<div style="text-align: center">
  <img class=" size-full wp-image-1916" src="https://linuxo.org/wp-content/uploads/2007/11/puffy42.jpg" alt="OpenBSD 4.2" title="OpenBSD 4.2" width="400" height="133" srcset="https://linuxo.org/wp-content/uploads/2007/11/puffy42.jpg 400w, https://linuxo.org/wp-content/uploads/2007/11/puffy42-300x100.jpg 300w" sizes="(max-width: 400px) 100vw, 400px" />&nbsp;
</div>

o Gnome 2.18.  
o GNUstep 1.14.  
o KDE 3.5.7 i koffice 1.6.3.  
o Xfce 4.4.1.  
o OpenMotif 2.3.0.  
o OpenOffice.org 2.2.1.  
o Mozilla Firefox 2.0.0.6.  
o PostgreSQL 8.2.4.  
o GHC 6.6.1 (samo amd64 i&nbsp; i386)

<!--break-->

Naravno, ceo sistem ne bi funkcionisao kako treba bez sledećih komponenti:

o Xenocara (bazirana na X.Org 7.2 sa patch-evima, freetype 2.2.1,  
fontconfig 2.4.2, expat 2.0.0, Mesa 6.5.2, xterm 225 i drugo)  
o Gcc 2.95.3 (+ patch-evi) and 3.3.5 (+ patch-evi)  
o Perl 5.8.8 (+ patch-evi)  
o Unapređena i osigurana verzija Apache 1.3, sa podr&scaron;kom za SSL/TLS i&nbsp; DSO  
o OpenSSL 0.9.7j (+ patch-evi)  
o Groff 1.15  
o Sendmail 8.14.1, with libmilter  
o Bind 9.3.4 (+ patch-evi)  
o Lynx 2.8.5rel.4 sa podr&scaron;kom za HTTPS i IPv6 (+ patch-evi)  
o Sudo 1.6.9p4  
o Ncurses 5.2  
o Latest KAME IPv6  
o Heimdal 0.7.2 (+ patch-evi)  
o Arla 0.35.7  
o Binutils 2.15 (+ patch-evi)  
o Gdb 6.3 (+ patch-evi)

A gde preuzeti OpenBSD 4.2 ?&nbsp; Svakako ga potražiti na najbližem miror sajtu na <a href="http://www.openbsd.org/ftp.html" target="_blank">http://www.openbsd.org/ftp.html</a>  
Vi&scaron;e detalja o novoj verziji na ovom <a href="http://marc.info/?l=openbsd-misc&m=119388876209736&w=2" target="_blank">linku</a> .&nbsp;

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=1917)