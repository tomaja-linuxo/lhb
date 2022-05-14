---
author: tomaja
date: "2004-10-13T16:05:25Z"
excerpt: |
  Objavljena je nova verzija ovog odli?nog alata za kreiranje web
  stranica. Radi se o OpenSource projektu WYSIWYG web editora koji
  pretenduje da bude najbolji Linux program ove namene. Nova verzija je
  zasnovana na Mozilli 1.7.1 i Gecko engine-u.  U ovoj verziji se
  nalazi dosta poboljšanja (<a href="http://www.nvu.com/download.html">change
  log</a>). Kako izgleda i funkcioniše možete da pogledate na ovim
  screnshoot-ovima <a href="http://images.linspire.com/nvu/tree.png">1</a>,<a
  href="http://images.linspire.com/nvu/publish1.png">2</a>,<a
  href="http://info.linspire.com/nvu/numods/colorPicker.png">3</a> , a
  kakve su mu mogu?nosti možete pogledati <a target="_blank"
  href="http://www.nvu.com/features.html">ovde</a>.<br>
  <a href="http://www.nvu.com/"></a>NVU (N-view)<font face="Arial, Helv"
  size="2"> </font>se razvija kako za Linux tako i za Windows i Mac
  platforme i sponzorisan je od strane Lispire-a. Naravno, kako se radi o
  100% OpenSource projektu sam program možete skinuti iz naše <a
  href="modules.php?name=Downloads">download sekcije</a> (Internet)<br>
  Instrukcije za instalaciju:
guid: https://forum.linuxo.org/2004/10/13/nvu-0-5-web-editor/
id: 563
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: NVU 0.5 (web editor)
url: /nvu-0-5-web-editor/
---
Objavljena je nova verzija ovog odli?nog alata za kreiranje web  
stranica. Radi se o OpenSource projektu WYSIWYG web editora koji  
pretenduje da bude najbolji Linux program ove namene. Nova verzija je  
zasnovana na Mozilli 1.7.1 i Gecko engine-u. U ovoj verziji se  
nalazi dosta poboljšanja ([change  
log](http://www.nvu.com/download.html)). Kako izgleda i funkcioniše možete da pogledate na ovim  
screnshoot-ovima [1](http://images.linspire.com/nvu/tree.png),[2](http://images.linspire.com/nvu/publish1.png),[3](http://info.linspire.com/nvu/numods/colorPicker.png) , a  
kakve su mu mogu?nosti možete pogledati <a target="_blank"
href="http://www.nvu.com/features.html">ovde</a>.  
[](http://www.nvu.com/)NVU (N-view) <font face="Arial, Helv"
size="2"></font>se razvija kako za Linux tako i za Windows i Mac  
platforme i sponzorisan je od strane Lispire-a. Naravno, kako se radi o  
100% OpenSource projektu sam program možete skinuti iz naše [download sekcije](modules.php?name=Downloads) (Internet)  
Instrukcije za instalaciju:<!--break-->

Kako da instalirate NVU ?

Prvo pro?itajte [instrukcije  
za vašu softversku platformu](http://www.mozilla.org/build/)  
Download-ujte [program](http://www.linuxo.org/modules.php?name=Downloads&d_op=viewdownloaddetails&lid=90&ttitle=NVU_0.5_%28web_editor%29)  
iz naše Download sekcije Raspakujte fajl

bzip2 -dc nvu-0.50-sources.tar.bz2 | tar xf &#8211;

što ?e dovesti do  
kreiranja direktorijuma sa imenom mozilla PreÄ‘ite u taj direktorijum  
i mozconfig.* fajl koji odgovara  
vašem sistemu preimenujte u .mozconfig (ali ne i  
mozconfig). U diremtorujumu ?ete prona?i slede?e mozconfig fajlove:  
mozconfig.linspire, mozconfig.fedora2, mozconfig.linux, mozconfig.win,  
mozconfig.mac.  
Pokrenite komandu 

make -f client.mk build_all

Nakon završetka kompajliranja treba da se pojavi direktorijum  
mozilla/dist/bin  
(Linux) ili mozilladist#in (Windows). Dovoljno je da ga  
startujete da bi pokrenuli Nvu. 

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=563)