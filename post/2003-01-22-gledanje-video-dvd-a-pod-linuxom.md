---
author: tomaja
date: "2003-01-22T19:46:36Z"
excerpt: |
  Vecina komercijalnih video DVD-a zasticena je sa tzv. "Contents Scramble"
  sistemom ili skraceno CSS.  DVD-CCA (DVD Copy Control Association) organizacija,
  koja predstavlja filmske studije i proizvodjace DVD hardvera,  ima za zadatak
  prodaju CSS licence, koju svi koji zele da naprave hardver ili softver koji
  dekodira CSS,  moraju da plate. Potpisivanjem CSS licence, proizvodjaci softvera
  i hardvera obavezuju se i na mnoge druge stvari  koje su naravno u interesu
  DVD-CCA clanova koji tvrde da je jedini razlog postojanju CSS-a, prevencija
  kopiranja DVD-a  sto je cista glupost, jer je moguce napraviti kopiju video
  DVD-a bez dekripcije CSS-a.  Bilo koji DVD plejer ili softver koji dekodira
  CSS bez placanja licence je ilegalan....
guid: https://forum.linuxo.org/2003/01/22/gledanje-video-dvd-a-pod-linuxom/
id: 280
image: /wp-content/uploads/2003/01/t2thumb.jpg
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";s:3:"272";s:11:"_thumb_type";s:5:"thumb";}
title: Gledanje Video DVD-a pod Linuxom
url: /gledanje-video-dvd-a-pod-linuxom/
---
Vecina komercijalnih video DVD-a zasticena je sa tzv. &#8222;Contents Scramble&#8220;  
sistemom ili skraceno CSS. DVD-CCA (DVD Copy Control Association) organizacija,  
koja predstavlja filmske studije i proizvodjace DVD hardvera, ima za zadatak  
prodaju CSS licence, koju svi koji zele da naprave hardver ili softver koji  
dekodira CSS, moraju da plate. Potpisivanjem CSS licence, proizvodjaci softvera  
i hardvera obavezuju se i na mnoge druge stvari koje su naravno u interesu  
DVD-CCA clanova koji tvrde da je jedini razlog postojanju CSS-a, prevencija  
kopiranja DVD-a sto je cista glupost, jer je moguce napraviti kopiju video  
DVD-a bez dekripcije CSS-a. Bilo koji DVD plejer ili softver koji dekodira  
CSS bez placanja licence je ilegalan&#8230;.<!--break-->Krajem 1999-e CSS algoritam je bio razbijen

  
i kod pod nazivom DeCSS objavljen. U Sjedinjenim Drzavama usledile su mnoge  
sudske tuzbe protiv sajtova koji su omogucivali daunload DeCSS-a. Situacija  
jos uvek nije potpuno razresena, a u medjuvremenu se pojavilo nekoliko Open  
Source projekata koji su napravili softver za gledanje CSS zasticenih DVD-a  
pod Linuxom. 

**Linux DVD Plejeri**

Da bismo mogli da gledamo CSS video DVD-e pod Linuxom, potrebno je naravno  
imati DVD-ROM i jedan od sledecih programa: Ogle, Xine, Mplayer, ili VideoLAN.  
Svi ovi programi sami po sebi mogu da citaju samo obicne (bez CSS enkripcije)  
DVD-e. Instaliranje softvera koji ovim programima omogucava da citaju CSS  
DVD-e je opcionalno. Za instaliranje ovih programa koristio sam Mandrake  
9.0 distribuciju.

**Ogle**

[[Ogle]](http://www.dtek.chalmers.se/groups/dvd/) je baziran u  
Svedskoj i jedini je od svih programa koje sam naveo namenjen iskljucivo za  
gledanje DVD-a. Svu instalaciju sam uradio iz [[RPM-ova]](http://www.dtek.chalmers.se/groups/dvd/redhat.shtml).  
Libjpeg i libxml2 sam vec imao instalirane tako da su bili preostali libdvdcss,  
libdvdread, Ogle, Ogle_gui, i xvattr. Nikakva daljnja konfiguracija nije  
bila potrebna osim stvaranja simbolicnog linka od /dev/scd0 (Gde je moj DVD  
ROM prijavljen) do /dev/dvd gde svi ovi programi ocekuju da nadju DVD uredjaj.  
Evo naravno i screenshot.

[![](https://linuxo.org/wp-content/uploads/2003/01/t2thumb.jpg)](https://linuxo.org/wp-content/uploads/2003/01/t2.jpg)

**Xine**

[[Xine]](http://xinehq.de/) je baziran u Nemackoj i vec dolazi  
sa Mandrake-om tako da taj deo nisam morao da instaliram. Da bi Xine mogao  
da cita DVD-e zasticene CSS-om, neophodno je instalirati sledece stvari: libdvdcss,  
libdvdread, libdvdnav, i xine-dvdnav. Prve dve vec imamo iz instalacije Ogle  
plejera. Druga dva sam dobio sa [[ovog]](http://sourceforge.net/projects/dvd/) sajta. Da bi mogli  
da kompajlujemo libdvdnav, trebace nam i libdvdread-devel RPM sa Ogle sajta.  
Nakon sto smo instalirali libdvdnav, kompajlujemo xine-dvdnav koji zahteva  
libxine0-devel paket koji je standardan Mandrake paket. Takodjer, moramo da  
dodamo &#8222;/usr/local/lib&#8220; u /etc/ld.so.conf. Kada startujemo Xine, za DVD-e  
bez enkripcije treba da kliknemo na &#8222;DVD&#8220;, a za ostale na &#8222;NAV&#8220; dugme.

[![](https://linuxo.org/wp-content/uploads/2003/01/ssthumb.jpg)](https://linuxo.org/wp-content/uploads/2003/01/ss.jpg)

**Mplayer**

[[Mplayer]](http://www.mplayerhq.hu/homepage/) je baziran u Madjarskoj  
i njegova instalacija je malo komplikovanija od ostalih. Moramo da ga kompajlujemo  
sa &#8211;enable-gui opcijom ako zelimo da koristimo graficki interfejs. Takodjer  
moramo da instaliramo odredjene fontove i bar jedan &#8222;skin&#8220; za graficki interfejs.  
Pored dvdnav i dvdcss paketa, Mplayer zahteva i standardni XFree86-devel RPM  
za Mandrake.

<pre>Mplayer:<br /><br />bunzip2 MPlayer-0.90rc2.tar.bz2<br />tar -xf MPlayer-0.90rc2.tar<br />cd MPlayer-0.90rc2<br />./configure --enable-gui<br />make && make install<br /><br />Fontovi:<br /><br />bunzip2 mp-iso-8859-7.tar.bz2<br />tar -xf mp-iso-8859-7.tar<br />cp iso-8859-7/arial/arial-14/* /usr/local/share/mplayer/font/<br /><br />Skin:<br /><br />bunzip2 default.tar.bz2<br />tar -xf default.tar<br />cp -r default /usr/local/share/mplayer/Skin/ <br /></pre>

Ovo ce da kompajluje i instalira Mplayer, fontove i &#8222;default&#8220; skin. Ja sam  
izabrao arial fontove velicine 14, a mogu da se koriste i bilo koji drugi  
iz iso-8859-7 direktorijuma. Graficki interfejs i mplayer startovali bi sa  
&#8222;gmplayer&#8220; komandom. Sledeci screenshot pokazuje Mplayer u akciji sa &#8222;neutron&#8220;  
skin-om. 

[![](https://linuxo.org/wp-content/uploads/2003/01/rethumb.jpg)](https://linuxo.org/wp-content/uploads/2003/01/re.jpg)

**VideoLan**

[[VideoLan]](http://www.videolan.org/) projekat je baziran u Francuskoj  
i glavni cilj mu je omogucavanje broadkastovanja video strimova sto znaci  
da mozemo da instaliramo server koji ce da salje video klijentima preko mreze.  
Ako samo zelimo da gledamo video lokalno, dovoljno je instalirati klijent  
program (vlc). Vlc zahteva liba52 i libmad standardne Mandrake RPM-ove, a  
zatim i libdvdcss-devel koji moze da se nadje na Ogle sajtu. Naravno i libdvdcss  
je potreban kao i za sve ostale. Kompilacija je standardna. Jedini problem  
sa VideoLan-om je da jedini od ovih plejera ne podrzava DVD menije i navigaciju.

[![](https://linuxo.org/wp-content/uploads/2003/01/gbuthumb.jpg)](https://linuxo.org/wp-content/uploads/2003/01/gbu.jpg)

**Za Kraj**

Svi programi koje sam naveo (osim Ogle plejera) u vecoj ili manjoj meri podrzavaju  
i mnoge druge video formate kao sto su naravno mpeg (1 i 2) i VCD, a takodjer  
i quicktime, AVI, DivX itd. Neki formati zahtevaju instaliranje specijalnih  
Windows DLL-a i malo konfiguracije. 

Svi ovi plejeri podrzavaju nekoliko razlicitih video output drajvera od kojih  
nam jedino XV daje akceleraciju i postize dovoljno visoku ratu frejmova. Skoro  
sve novije graficke karte podrzavaju XV. Medjutim, da bi bili u stanju da  
uzmemo screenshot ovih plejera u akciji, neophodno ih je startovati sa x11  
drajverom (npr. vlc -V x11 ili gmplayer -vo x11) zbog nacina na koji je DVD  
video prikazan na ekranu. 

Kao sto sam rekao, koristio sam Mandrake 9.0 distribuciju, a skoro isti postupak  
vazi i za sve novije Mandrake i Redhat distribucije, a takodjer i SuSE. Sve  
druge distribucije zahtevale bi kompajlovanje svega iz source-a.

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=280)