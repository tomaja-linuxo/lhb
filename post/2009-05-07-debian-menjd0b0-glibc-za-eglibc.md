---
author: tomaja
date: "2009-05-07T08:35:16Z"
excerpt: '<div class="item_wrapper"><p>Dosta kratkom porukom na svom&nbsp;<a href="http://blog.aurel32.net/?p=47"
  target="_blank">blogu</a>, Debianov developer Aurelian Jarno (Aur&eacute;llian Jarno)
  je najavio fundametalne promene u budućim&nbsp;<a href="http://www.debian.org/"
  target="_blank"><u>Debian</u></a> ovim izdanjima.&nbsp;EGLIBC (Embedded GNU C Library),
  koje je orginalno napravljen za&nbsp;embedded sisteme, će zameniti&nbsp;GLIBC (GNU
  C Library).</p><p>Jarno kaže da ove izmene obećavaju unapređenje razvoja, posebno
  kada su u pitanju drugi učesnici u radu, izve&scaron;taju o gre&scaron;kama i podneseni
  patch-evi.&nbsp;U ranijem periodu su&nbsp;GLIBC developeri bili ocenjivani kao&nbsp;<a
  href="http://sourceware.org/bugzilla/show_bug.cgi?id=5531" target="_blank">delimično</a>
  &quot;ne ba&scaron;&quot; <a href="http://sourceware.org/bugzilla/show_bug.cgi?id=4980"
  target="_blank">prijateljski</a> nastrojeni. Izve&scaron;taji o gre&scaron;kama
  su često odbijani zato &scaron;to su bili bazirani na prethodnim&nbsp;verzijama
  u odnosu&nbsp;aktuelne verzije sa&nbsp;CVS-a a često su bili zatvarani bez ikakvog
  obja&scaron;njenja.</p></div><!-- /HEISETEXT --><!--googleoff: index-->'
guid: https://forum.linuxo.org/2009/05/07/debian-menj%d0%b0-glibc-za-eglibc/
id: 2256
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Debian menjа GLIBC za EGLIBC
url: /debian-menj%d0%b0-glibc-za-eglibc/
---
<div class="item_wrapper">
  <p>
    Dosta kratkom porukom na svom&nbsp;<a href="http://blog.aurel32.net/?p=47" target="_blank">blogu</a>, Debianov developer Aurelian Jarno (Aur&eacute;llian Jarno) je najavio fundametalne promene u budućim&nbsp;<a href="http://www.debian.org/" target="_blank"><u>Debian</u></a> ovim izdanjima.&nbsp;EGLIBC (Embedded GNU C Library), koje je orginalno napravljen za&nbsp;embedded sisteme, će zameniti&nbsp;GLIBC (GNU C Library).
  </p>
  
  <p>
    Jarno kaže da ove izmene obećavaju unapređenje razvoja, posebno kada su u pitanju drugi učesnici u radu, izve&scaron;taju o gre&scaron;kama i podneseni patch-evi.&nbsp;U ranijem periodu su&nbsp;GLIBC developeri bili ocenjivani kao&nbsp;<a href="http://sourceware.org/bugzilla/show_bug.cgi?id=5531" target="_blank">delimično</a> "ne ba&scaron;" <a href="http://sourceware.org/bugzilla/show_bug.cgi?id=4980" target="_blank">prijateljski</a> nastrojeni. Izve&scaron;taji o gre&scaron;kama su često odbijani zato &scaron;to su bili bazirani na prethodnim&nbsp;verzijama u odnosu&nbsp;aktuelne verzije sa&nbsp;CVS-a a često su bili zatvarani bez ikakvog obja&scaron;njenja.
  </p>
</div>

<!-- /HEISETEXT -->

<!--googleoff: index-->

<!--break-->

Druge koristi, kako kaže&nbsp;Jarno, će bizi podr&scaron;ka za&nbsp;plaforme pored&nbsp;x86&nbsp;i druge &scaron;elove pored Bash-a, za koje je&nbsp;GLIBC blisko vezan. Takođe, EGLIBC ima bolje alate za testiranje koji se pokreću na raznim platformama i lak&scaron;e se pode&scaron;avaju, za na primer, komponente poput NIS&nbsp;ili RPC .

GNU C biblioteka&nbsp; (GLIBC) je&nbsp;osnova Linux distribucija, koja gotovo sve binarne pakete dinamički povezuje sa bibliotekom i koristi njene funkcije. Dinamičkim povezivanjem sa bibliotekom, smanjuje veličinu binarnih fajlova, i kada se ispravi bag u biblioteci, automatski su ispravljene i sve aplikacijeBy dynamically linking the library. Srećom, ovo takođe znači da će biti relativno lako zameniti je sa alternativom poput&nbsp;EGLIBC-a koji ima bolju podr&scaron;ku.Info: **h-online.com**&nbsp;

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=2256)