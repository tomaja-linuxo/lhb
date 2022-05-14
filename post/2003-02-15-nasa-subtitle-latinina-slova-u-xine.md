---
author: tomaja
date: "2003-02-15T04:47:29Z"
excerpt: |
  -Najjednostavniji nacin:
  <br />
  Iz menija se pokrene XINE pa klik na "setup video", pa na "codec" i tu u: font for avi subtitles, umesto "sans" samo ukucati "sanshu".
  <br />
  -Za ambicioznije (i ve?i izbor fontova):
  <br />
  Sa <a href="http://www.linux.cz/lists/archive/linux/ 140957.html">http://www.linux.cz/lists/archive/linux/ 140957.html</a> možete
  download-ovati fontove za XINE i "xine-fontconv" (izvorni kod), zatim je potrebno kompajliranje i instaliranje po tu priloženom uputstvu i na kraju:
  <br />
  $ xine-fontconv arial.ttf arial ISO-8859-2
  <br />
  $ mv arial-* /usr/share/xine/fonts/
  <br />
  $ vi .xine/config
  <br />
  $ grep arial .xine/config
  <br />
  codec.spu_font:arial
  <br />
  $ xine nekifilm.avi%srpskitil.sub
  <br />
  Uživajte u našim slovima!
guid: https://forum.linuxo.org/2003/02/15/nasa-subtitle-latinina-slova-u-xine/
id: 291
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Naša subtitle latini?na slova u XINE
url: /nasa-subtitle-latinina-slova-u-xine/
---
-Najjednostavniji nacin:  
  
Iz menija se pokrene XINE pa klik na &#8222;setup video&#8220;, pa na &#8222;codec&#8220; i tu u: font for avi subtitles, umesto &#8222;sans&#8220; samo ukucati &#8222;sanshu&#8220;.  
  
-Za ambicioznije (i ve?i izbor fontova):  
  
Sa <http://www.linux.cz/lists/archive/linux/ 140957.html> možete  
download-ovati fontove za XINE i &#8222;xine-fontconv&#8220; (izvorni kod), zatim je potrebno kompajliranje i instaliranje po tu priloženom uputstvu i na kraju:  
  
$ xine-fontconv arial.ttf arial ISO-8859-2  
  
$ mv arial-* /usr/share/xine/fonts/  
  
$ vi .xine/config  
  
$ grep arial .xine/config  
  
codec.spu_font:arial  
  
$ xine nekifilm.avi%srpskitil.sub  
  
Uživajte u našim slovima!

<!--break-->

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=291)