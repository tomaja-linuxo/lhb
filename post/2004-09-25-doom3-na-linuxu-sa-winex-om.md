---
author: tomaja
date: "2004-09-25T04:26:10Z"
excerpt: |
  Za one koji su nestrpljivi da sa?ekaju Linux verziju igrice Doom3
  evo kako možete da instalirate na Linux verziju ove igrice koja je predviÄ‘ena za MS Windows. Prvo da vidimo šta
  nam je potrebno. Treba da poznajete Linux konzolu i njene naredbe a naravno treba da posedujete i Doom3 koji
  dolazi na 3 CDa, a potrebna vam je i internet konekcija. <br>Naravno i jedna preporuka,
  a to je da prebacite diskove na hard pomo?u naredbe dd a zatim da ISO image montirate kao loopback ureÄ‘aje.
  Ovo je dobro zbog toga što pri pokretanju  "doom3_installer.sh" fajla ne?ete morati uopšte da ubacujete ili menjate
  diskove u CD plejeru.<br>Preporuka:
guid: https://forum.linuxo.org/2004/09/25/doom3-na-linuxu-sa-winex-om/
id: 529
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Doom3 na Linuxu sa WineX-om
url: /doom3-na-linuxu-sa-winex-om/
---
Za one koji su nestrpljivi da sa?ekaju Linux verziju igrice Doom3  
evo kako možete da instalirate na Linux verziju ove igrice koja je predviÄ‘ena za MS Windows. Prvo da vidimo šta  
nam je potrebno. Treba da poznajete Linux konzolu i njene naredbe a naravno treba da posedujete i Doom3 koji  
dolazi na 3 CDa, a potrebna vam je i internet konekcija.  
Naravno i jedna preporuka,  
a to je da prebacite diskove na hard pomo?u naredbe dd a zatim da ISO image montirate kao loopback ureÄ‘aje.  
Ovo je dobro zbog toga što pri pokretanju &#8222;doom3_installer.sh&#8220; fajla ne?ete morati uopšte da ubacujete ili menjate  
diskove u CD plejeru.  
Preporuka:<!--break-->Skinite najnoviju verziju wine sa linka http://www.ibiblio.org/pub/Linux/ALPHA/wine/development/

  
cd wine-xxxxx/  
tools/wineinstall

**Instalacija/podešavanje transgaming winex-a:**  
cvs -d:pserver:cvs@cvs.transgaming.org:/cvsroot login (lozinka je &#8216;cvs&#8217;)  
cvs -z3 -d:pserver:cvs@cvs.transgaming.org:/cvsroot co winex  
wget http://www.linux-militia.net/howtos/doom3/GlobalMemoryStatusExFixed.patch  
dos2unix GlobalMemoryStatusExFixed.patch  
cd winex  
patch -po < ../GlobalMemoryStatusExFixed.patch  
./configure &#8211;enable-pthreads &#8211;prefix=/usr/lib/winex-cvs/winex  
make  
make install  
touch /usr/lib/winex-cvs/.transgaming/tg\_config\_version  
cp ./documentation/sample/config ~/.transgaming  
wget http://www.linux-militia.net/howtos/doom3/winex-cvs  
mv winex-cvs /usr/bin  
chmod +x /usr/bin/winex-cvs  
wget http://www.linux-militia.net/howtos/doom3/pthreads\_stack\_test  
mv pthreads\_stack\_test /usr/lib/winex-cvs/winex/bin  
chmod 755 /usr/lib/winex-cvs/winex/bin/pthreads\_stack\_test  
cp -a ~/.wine ~/.transgaming  
cd ~/.transgaming  
mv drive\_c c\_drive  
mkdir c_drive/windows/system32

**Instalacija/podešavanje Doom3:**  
wget http://www.linux-militia.net/howtos/doom3/doom3_installer.sh  
chmod +x doom3_installer.sh  
./doom3_installer.sh  
cd ~/doom3/  
wget http://www.linux-militia.net/howtos/doom3/Doom3.exe.gz  
mv Doom3.exe Doom3.exe.old  
gzip -d Doom3.exe.gz  
winex-cvs Doom3.exe

I to je to.

(Ovaj HOWTO je baziran na upustvu Roba Smith-a sa http://linux-militia.net/howtos/doom3/doom3.html)</pre> 

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=529)