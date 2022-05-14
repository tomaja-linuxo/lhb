---
author: tomaja
date: "2005-04-16T02:25:51Z"
excerpt: |
  Nekoliko Trolltech programera je uradilo <a
  href="http://lists.freedesktop.org/archives/xorg/2005-April/007446.html">optimizaciju</a>
  x.org RENDER ekstenzije. RENDER je do sada koriš?en sa COMPOSITE da bi
  obezbedio "transparency" i "shadow" efekte, ali je njegova sporost bila
  uzrok njegove ve?e primene. Sre?om, ova optimizacija bi trebala da
  popravi stvari, iako se još uvek lome koplja o primeni XAA i uvoÄ‘enju
  bržeg KAA sistema u x.org. RENDER
  se takoÄ‘e korisit za više stvari, kao što su na primer AA fontovi, pa
  ?e ovo biti dobro za X desktop <a
  href="http://lists.freedesktop.org/archives/xorg/2005-April/007452.html">generalno
  gledaju?i</a>.
guid: https://forum.linuxo.org/2005/04/16/rad-na-ubrzanju-x-org-a/
id: 815
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Rad na ubrzanju X.Org-a
url: /rad-na-ubrzanju-x-org-a/
---
Nekoliko Trolltech programera je uradilo [optimizaciju](http://lists.freedesktop.org/archives/xorg/2005-April/007446.html)  
x.org RENDER ekstenzije. RENDER je do sada koriš?en sa COMPOSITE da bi  
obezbedio &#8222;transparency&#8220; i &#8222;shadow&#8220; efekte, ali je njegova sporost bila  
uzrok njegove ve?e primene. Sre?om, ova optimizacija bi trebala da  
popravi stvari, iako se još uvek lome koplja o primeni XAA i uvoÄ‘enju  
bržeg KAA sistema u x.org. RENDER  
se takoÄ‘e korisit za više stvari, kao što su na primer AA fontovi, pa  
?e ovo biti dobro za X desktop [generalno  
gledaju?i](http://lists.freedesktop.org/archives/xorg/2005-April/007452.html).<!--break-->

  
UporeÄ‘ivanje brzine je izvedeno koriš?enjem Xephyr-a, koje je pokazao  
ubrzanje od 3-4 puta u donosu na merenje bez pimene transformacije, a  
?ak 8 puta za bilineanu transformaciju. 

Detaljniju listu rezulatata možete pogledati na slede?a dva linka:  
<http://trolls.troll.no/lars/render/render_old.txt>  
<http://trolls.troll.no/lars/render/render_new.txt>

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=815)