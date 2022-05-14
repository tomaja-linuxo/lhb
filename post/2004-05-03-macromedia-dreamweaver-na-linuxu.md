---
author: tomaja
date: "2004-05-03T05:06:23Z"
excerpt: |
  Veoma ?esto veliki broj ljudi ima zamerku da ne postoji dovoljno dobra
  aplikacija na Linuxu koja bi zamenila Makromedijin <span
  style="font-weight: bold; font-style: italic;">Dreamweaver</span>. <br>
  Epa, evo kako da, ukoliko baš morate da koristite Dreamweaver,
  pokrenete
  taj program pomo?u Wine emulatora (ovde se podrazumeva da ste
  instalirali Wine i pokrenuli wine servis).<br>
  Da bi instalirali Dreamweaver prvo morate da instalirate <span
  class="pn-normal">DCOM95. On nam je potreban da bi mogli da pokrenemo
  instalacioni program. DCOM95 možete skinuti <a
  href="http://prdownloads.sourceforge.net/wine/dcom95.exe?download">ovde</a>.
  Instalacija je laka. Samo ukucajte <span
  style="font-weight: bold; font-style: italic;">WINEDLLOVERRIDES="ole32=n"
  wine
  dcom95.exe</span> da bi instalirali DCOM95.<br>
  Nakon ovoga možemo da instaliramo Dreamweaver MX (naravno, ako imate
  legalnu instalacionu verziju programa, za onu drugu ne bih znao :).<br>
  Ukucajte <span style="font-weight: bold; font-style: italic;">wine
  dreamweaver mx
  installer.exe</span> da bi instalirali Deamweaver MX.<br>
  Ukoliko imate problema sa ovom komandom možete pokrenuti:
guid: https://forum.linuxo.org/2004/05/03/macromedia-dreamweaver-na-linuxu/
id: 158
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Macromedia DreamWeaver na Linuxu
url: /macromedia-dreamweaver-na-linuxu/
---
Veoma ?esto veliki broj ljudi ima zamerku da ne postoji dovoljno dobra  
aplikacija na Linuxu koja bi zamenila Makromedijin <span
style="font-weight: bold; font-style: italic;">Dreamweaver</span>.  
Epa, evo kako da, ukoliko baš morate da koristite Dreamweaver,  
pokrenete  
taj program pomo?u Wine emulatora (ovde se podrazumeva da ste  
instalirali Wine i pokrenuli wine servis).  
Da bi instalirali Dreamweaver prvo morate da instalirate <span
class="pn-normal">DCOM95. On nam je potreban da bi mogli da pokrenemo<br /> instalacioni program. DCOM95 možete skinuti <a
href="http://prdownloads.sourceforge.net/wine/dcom95.exe?download">ovde</a>.<br /> Instalacija je laka. Samo ukucajte <span
style="font-weight: bold; font-style: italic;">WINEDLLOVERRIDES=&#8220;ole32=n&#8220;<br /> wine<br /> dcom95.exe</span> da bi instalirali DCOM95.<br /> Nakon ovoga možemo da instaliramo Dreamweaver MX (naravno, ako imate<br /> legalnu instalacionu verziju programa, za onu drugu ne bih znao :).<br /> Ukucajte <span style="font-weight: bold; font-style: italic;">wine<br /> dreamweaver mx<br /> installer.exe</span> da bi instalirali Deamweaver MX.<br /> Ukoliko imate problema sa ovom komandom možete pokrenuti:<!--break-->

<span style="font-weight: bold; font-style: italic;">WINEDLLOVERRIDES=&#8220;ole32,oleaut32,rpcrt4=n&#8220;<br /> wine dreamweaver mx installer.exe</span></p> 

<p>
  Nakon instalacije Dreamweaver MX morate instalirati Windows Scripting<br /> Host. Njega možete dobaviti <a
href="http://download.microsoft.com/download/winscript56/Install/5.6/W9XNT4Me/EN-US/scr56en.exe">ovde</a><br /> Instalirajte ga komandom <span
style="font-style: italic; font-weight: bold;">wine scr56en.exe</span><br /> Sada iskopirajte slede?e dll fajlove u wineov windows system<br /> direktorujum:<br /> commctrl<br /> comctl32<br /> imm32 <br /> wininet
</p>

<p>
  Dodajte slede?e linije u wine config fajl:<br /> [AppDefaults\dreamweaver.exe\DllOverrides] &#8222;commctrl&#8220; = &#8222;native&#8220;<br /> &#8222;comctl32&#8220; = &#8222;native&#8220;<br /> &#8222;imm32&#8220; = &#8222;native&#8220;<br /> &#8222;msvcrt&#8220; = &#8222;native&#8220;<br /> &#8222;wininet&#8220; = &#8222;native&#8220;
</p>

<p>
  Ukucajte<span style="font-weight: bold; font-style: italic;"> wine<br /> dreamweaver.exe</span><br /> u instalacionom direktorijumu da bi pokrenuli Dreamweaver MX.<br /> Ukoliko vam se Dreamweaver ruši prilikom pokretanja text color dijaloga<br /> koristite text color iz menija</span>
</p>

<p>
  <a href="https://linuxo.org/nova-tema-na-forumu/?se_pid=158">Креирај тему форума везану за овај текст</a>
</p>