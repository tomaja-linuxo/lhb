---
author: tomaja
date: "2003-08-03T01:03:05Z"
excerpt: |
  Ovaj mini tutorial namenjen je linux newbie korisnicima koji jos uvek nisu pronikli u nacin instalacije drajvera, finog stelovanja X-windowsa i naravno dobijanja slike sa TV-outa kartice.
guid: https://forum.linuxo.org/2003/08/03/nvidia-i-x-instalacija-mis-refresh-rate-tv-out/
id: 364
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Nvidia i X (instalacija, mis, refresh rate, TV Out)
url: /nvidia-i-x-instalacija-mis-refresh-rate-tv-out/
---
Ovaj mini tutorial namenjen je linux newbie korisnicima koji jos uvek nisu pronikli u nacin instalacije drajvera, finog stelovanja X-windowsa i naravno dobijanja slike sa TV-outa kartice.  
<!--break-->1. Instalacija

NVidia je poznata po izuzetno dobroj podrsci za linux, i za to zasluzuju sve pohvale. Nove verzije linux drajvera izbacuju se redovno, tek malo kasne za odgovarajucim windows pandanima, a sto je najlepse od svega brzi su od onih u winu za nekih 10%! Ko ne veruje, neka istestira uz pomoc Quakea 3.  
No, vratimo se procesu instalacije. Jos jednom moram da pohvalim NVidiju, jer se njihovi drajveri izuzetno lako kaleme na sistem. U svakom slucaju, preporucljivo je otici na njihov sajt i skinuti SORSOVE drajvera (najbolje najnovije verzije) i NE KORISTITI nikakve *.rpm i sl. Zasto? Zato sto kompajliranje iz sorsa daje sigurno najbrze drajvere, jer ce gcc kompajler napraviti binarne fajlove koji su prilagodjeni procesoru koji se nalazi u vasoj masini. Ovo vazi ne samo za graficku karticu, vec i za sve ostale drajvere i programe.  
Proces instalacije je sa zadnjim drajverima trivijalan, cak i smesan; potrebno je samo startovati *.bin fajl. Pojavljuje se setup, odgovori se na par pitanja i tu je instalaciji kraj.  
Sve ovo treba raditi bez startovanog X-Wina, najbolje je prebaciti se u runlevel 3 i odatle zavrsiti instalaciju, pa zatim nazad u runlevel 5 da se vide rezultati.  
To bi izgledalo otprilike ovako:  
-ako je X startovan, otvori se konzola i logujte se kao root:

>su -l

(sad ide unos passworda)

-prebacite se u runlevel 3 (&#8216;pure&#8217; konzola, bez startovanog X windowsa):

\# telinit 3

-ulogujte se ponovo kao root;  
-startujte *.bin fajl drajvera:

\# sh NVIDIA-Linux-x86-1.0-4363.run

-pojavljuje se setup meni, prodjite kroz njega, i posle nekog vremena instalacija je gotova.

Za one koji imaju sorsove starijih drajvera (NVIDIA\_GLX i NVIDIA\_kernel gzipped fajlovi), instalacija je malo komplikovanija ali i dalje dosta lagana:  
-predjite u direktorijum gde su drajveri  
-ulogujte se kao root  
-raspakujte ih sa:

\# tar xzf NVIDIA_kernel-1.0-4191.tar.gz  
\# tar xzf NVIDIA_GLX-1.0-4191.tar.gz

-prvo se instalira NVIDIA_kernel:

\# cd NVIDIA_kernel-1.0-4191  
\# make

-zatim NVIDIA_GLX:

\# cd NVIDIA_GLX-1.0-4191  
\# make

I to je to sto se tice same instalacije drajvera. Nakon ovoga, potrebno je uneti dve izmene u /etc/X11/XF86Config-4 fajl.  
Prvo, u sekciji &#8216;Modules&#8217; unosi se modul za OpenGL akceleraciju:

Section &#8222;Module&#8220;  
Load &#8222;dbe&#8220;

\# modul za 3d OpenGL akceleraciju, linija koju treba uneti  
Load &#8222;glx&#8220;

SubSection &#8222;extmod&#8220;  
EndSubSection  
Load &#8222;type1&#8220;  
Load &#8222;freetype&#8220;  
EndSection

Drugo, u sekciji &#8216;Devices&#8217; prepravite &#8222;nv&#8220; na &#8222;nvidia&#8220;:

Section &#8222;Device&#8220;  
Identifier &#8222;Nvidia GeForce MX400&#8220;  
VendorName &#8222;Microstar&#8220;  
BoardName &#8222;MSI 8833 VIVO 32mb&#8220;

#ovde promeniti &#8222;nv&#8220; u &#8222;nvidia&#8220;  
Driver &#8222;nvidia&#8220;

VideoRam 32768  
Option &#8222;DPMS&#8220; &#8222;on&#8220;  
EndSection

I sad nazad u X (ili ako ste vec u njemu jednostavno ga restartujte):

\# telinit 3

ili

\# startx

X se budi, ovog puta sa 3d akceleracijom i NVidijinim drajverima, sposoban za Quake 3, UT, Doom itd itd itd.  
Ako bude nekih problema, i X nece da se podigne, pogledajte log fajlove (var/log/XF86Config.log.0 i sl.) i naravno man stranicu sa sintaksom XF86Config-4 fajla ( &#8216;man XF86Config&#8217;). Kombinacija ove 2 stvari resava sigurno sve probleme 🙂

2. Skrol dugme misa

Ranije verzije Mandrake-a su ponekad u instalacionom procesu znale da zabrljaju prepoznavanje misa, i skrol nije radio. U MDK 9.x nisam primetio da se ovo desava, ali za one koji nisu imali srece evo kako treba da izgleda &#8216;InputDevice&#8217; sekcija XF86Config-4 fajla:

Section &#8222;InputDevice&#8220;  
Identifier &#8222;Mouse1&#8220;  
Driver &#8222;mouse&#8220;  
Option &#8222;Protocol&#8220; &#8222;IMPS/2&#8220;  
Option &#8222;Device&#8220; &#8222;/dev/mouse&#8220;  
Option &#8222;ZAxisMapping&#8220; &#8222;4 5&#8220;  
Option &#8222;Buttons&#8220; &#8222;3&#8220;  
EndSection

Restartujte X i vozite!

3. Frekvencija osvezavanja monitora

Ukoliko vam se cini da X server ne izvlaci iz monitora sve sto ovaj moze(citaj: osvezavanje  
ekrana je neprijatno nisko), probajte da rucno izmenite vrednosti frekvencija za horizontalno i vertikalno osvezavanje ekrana u XF86Config. Vrednosti za vas monitor se nalazi u uputstvu koje ste dobili kada je monitor kupljen, a ako je upustvo baceno/zatureno/nije-dobijeno, potrazite ih na netu. Ok, znate vrednosti, sledece je njihovo unosenje u sekciju &#8216;Monitor&#8217;. Evo primera za moj Hansol 710DT:

Section &#8222;Monitor&#8220;  
Identifier &#8222;mymonitor&#8220;  
VendorName &#8222;Hansol&#8220;  
ModelName &#8222;Hansol 710DT&#8220;

\# HorizSync is in kHz unless units are specified.  
\# OVDE PROMENITE HORIZONTALNU FREQ  
HorizSync 30-95

\# VertRefresh is in Hz unless units are specified.  
\# OVDE IDE VERTIKALNA FREQ  
VertRefresh 47-160

EndSection

Posle izmena, normalno restart X-a kako bi izmene imale dejstvo.  
Sada ce X, na osnovu zadate rezolucije i ovih frekvencija automatski podesiti osvezavanje na najbolju mogucu vrednost. Medjutim, najbolja njemu mozda nije najbolja i vama 🙂 Ako se desi nesporazum, onda smanjujte/povecavajte vrednosti sve dok X ne uradi zeljenu stvar. Nekada davno ovakve operacije su bilo izuzetno rizicne, i nije bila nikakva retkost da ljudi preteraju sa ovim vrednostima i bukvalno uniste svoje monitore. Ali danas X nije nimalo destruktivan, najgore sto moze da se desi je da ne moze da se podigne ili se dize sa totalno izdeformisanom nesinhronizovanom slikom. Vracanjem frekvencija ( i naravno restartom) stvari se normalizuju.

4. Ukljucenje TwinView moda i aktiviranje TV Out-a

Izuzetno detaljno uputstvo o tome kako nastelovati TV izlaz (i uopste sve vezano za NVidia kartice u linuxu) nalazi se na NVidijinom sajtu, obavezno pogledati:

ftp://download.nvidia.com/XFree86/Linux-x86/1.0-4496/README.txt

U README-u nema sta nema, ljudi su napisali bukvalno SVE, pa cu ja samo da dam nekoliko kratkih napomena i primer XF86Config fajla u kome TV out podrska 100% radi (znaci, moj XF86Config-4 :)) )

Dakle, da bi TwinView radio, u &#8216;Screen&#8217; sekciji XF86Config-4 fajla MORAJU OBAVEZNO da se specificiraju sledeci parametri i opcije:

Option &#8222;TwinView&#8220;  
Option &#8222;SecondMonitorHorizSync&#8220; &#8222;hsync range(s)&#8220;  
Option &#8222;SecondMonitorVertRefresh&#8220; &#8222;vrefresh range(s)&#8220;  
Option &#8222;MetaModes&#8220; &#8222;list of metamodes&#8220;

Ono sto nije obavezno, ali moze da bude korisno su sledece opcije:

Option &#8222;TwinViewOrientation&#8220; &#8222;relationship of head 1 to head 0&#8220;  
Option &#8222;ConnectedMonitor&#8220; &#8222;list of connected display devices&#8220;

Ove opcije su specificne za TV Out, i ako se kao drugi monitor kaci TV, moraju da budu definisane:

Option &#8222;TVOutFormat&#8220; &#8222;tv out format&#8220;  
Option &#8222;TVStandard&#8220; &#8222;standard of TV device&#8220;

Kada se radi o tv outu, moraju se definisati frekvencije drugog uredjaja (u ovom slucaju TV-a) :

Option &#8222;SecondMonitorHorizSync&#8220; &#8222;30-50&#8220; #vrednosti za PAL standard  
Option &#8222;SecondMonitorVertRefresh&#8220; &#8222;60&#8220;

Ako zelite da na TV-u imate &#8216;virtuelni ekran&#8217;, tj da kretanjem misa slika na TVu skroluje gore-dole i levo-desno,  
morate da definisete takozvani &#8222;Panning Domain&#8220; u metamodovima:

Option &#8222;MetaModes&#8220; &#8222;1152&#215;864,800&#215;600 @1152&#215;864; 1024&#215;768,800&#215;600 @1024&#215;768&#8220;

U metamodovima se prva rezolucija odnosi na primarni displej a druga na sekundarni (u ovom slucaju TV), druga na TV-out.  
Ja imam 2 metamoda, i sa ctrl + alt + NUMPAD+ i ctrl + alt + NUMPAD- direktno iz X-a menjam rezoluciju na monitoru sa 1152&#215;864 na 1024&#215;768 i nazad, a na TVu je zakucano uvek 800&#215;600. Naravno vi mozete dodati koliko god hocete metamodova

I konacno evo sad kompletne &#8216;Screen&#8217; sekcije, provereno funkcionalne:

Section &#8222;Device&#8220;  
Identifier &#8222;Nvidia GeForce MX400&#8220;  
VendorName &#8222;Microstar&#8220;  
BoardName &#8222;MSI 8833 VIVO 32mb&#8220;  
Driver &#8222;nvidia&#8220;  
VideoRam 32768

#ovde pocinje deo koji se tice TV Outa  
\# TwinView za NVidia kartice, PAL rezim  
Option &#8222;TwinView&#8220;

\# Hor i Ver sinhronizacija za TV &#8211; PAL  
Option &#8222;SecondMonitorHorizSync&#8220; &#8222;30-50&#8220;  
Option &#8222;SecondMonitorVertRefresh&#8220;  
&#8222;60&#8220;

#orijentacija (Clone, RightOf, LeftOf, Above, Below)  
Option &#8222;TwinViewOrientation&#8220; &#8222;Clone&#8220;

#metamodovi  
Option &#8222;MetaModes&#8220; &#8222;1152&#215;864,800&#215;600 @1152&#215;864; 1024&#215;768,800&#215;600 @1024&#215;768&#8220;

#redosled povezanih uredjaja, prvi je CRT &#8211; monitor, drugi je TV  
Option &#8222;ConnectedMonitor&#8220; &#8222;crt,TV&#8220;

#TV standard i format za video out (COMPOSITE ili SVIDEO, i PAL-B,NTSC-M,PAL-G itd itd)  
Option &#8222;TVOutFormat&#8220; &#8222;COMPOSITE&#8220;  
Option &#8222;TVStandard&#8220; &#8222;PAL-B&#8220;  
#kraj

Option &#8222;DPMS&#8220; &#8222;on&#8220;

EndSection

Restartujte X, i uzivajte u TV Outu.

Za sam kraj evo kompletnog XF86Config-4 fajla, koji je generisao XFDrake, a ja ispravio u skladu sa tutorialom.

\# File generated by XFdrake.

\# \***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\****  
\# Refer to the XF86Config(4/5) man page for details about the format of  
\# this file.  
\# \***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\****

Section &#8222;Files&#8220;

RgbPath &#8222;/usr/X11R6/lib/X11/rgb&#8220;

\# Multiple FontPath entries are allowed (they are concatenated together)  
\# By default, Mandrake 6.0 and later now use a font server independent of  
\# the X server to render fonts.

FontPath &#8222;unix/:-1&#8220;

EndSection

\# \***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\****  
\# Server flags section.  
\# \***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\****

Section &#8222;ServerFlags&#8220;

\# Uncomment this to cause a core dump at the spot where a signal is  
\# received. This may leave the console in an unusable state, but may  
\# provide a better stack trace in the core dump to aid in debugging  
#NoTrapSignals

\# Uncomment this to disable the server abort sequence  
\# This allows clients to receive this key event.  
#DontZap

\# Uncomment this to disable the / mode switching  
\# sequences. This allows clients to receive these key events.  
#DontZoom

\# This allows the server to start up even if the  
\# mouse device can&#8217;t be opened/initialised.  
AllowMouseOpenFail

EndSection

\# \***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\****  
\# Input devices  
\# \***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\****

\# \***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\****  
\# Keyboard section  
\# \***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\****

Section &#8222;InputDevice&#8220;

Identifier &#8222;Keyboard1&#8220;  
Driver &#8222;Keyboard&#8220;  
Option &#8222;AutoRepeat&#8220; &#8222;250 30&#8220;

Option &#8222;XkbRules&#8220; &#8222;xfree86&#8220;  
Option &#8222;XkbModel&#8220; &#8222;pc105&#8220;  
Option &#8222;XkbLayout&#8220; &#8222;us&#8220;

EndSection

\# \***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\****  
\# Pointer section  
\# \***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\****

Section &#8222;InputDevice&#8220;

Identifier &#8222;Mouse1&#8220;  
Driver &#8222;mouse&#8220;  
Option &#8222;Protocol&#8220; &#8222;IMPS/2&#8220;  
Option &#8222;Device&#8220; &#8222;/dev/mouse&#8220;  
Option &#8222;ZAxisMapping&#8220; &#8222;4 5&#8220;  
Option &#8222;Buttons&#8220; &#8222;3&#8220;  
\# ChordMiddle is an option for some 3-button Logitech mice

\# Option &#8222;ChordMiddle&#8220;

EndSection

Section &#8222;Module&#8220;

\# This loads the DBE extension module.

Load &#8222;dbe&#8220;

\# modul za 3d OpenGL akceleraciju  
Load &#8222;glx&#8220;

\# This loads the miscellaneous extensions module, and disables  
\# initialisation of the XFree86-DGA extension within that module.

SubSection &#8222;extmod&#8220;  
#Option &#8222;omit xfree86-dga&#8220;  
EndSubSection

\# This loads the Type1 and FreeType font modules

Load &#8222;type1&#8220;  
Load &#8222;freetype&#8220;  
EndSection

\# \***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\****  
\# Monitor section  
\# \***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\****

\# Any number of monitor sections may be present

Section &#8222;Monitor&#8220;  
Identifier &#8222;mymonitor&#8220;  
VendorName &#8222;Hansol&#8220;  
ModelName &#8222;Hansol 710DT&#8220;

\# HorizSync is in kHz unless units are specified.  
\# HorizSync may be a comma separated list of discrete values, or a  
\# comma separated list of ranges of values.  
\# NOTE: THE VALUES HERE ARE EXAMPLES ONLY. REFER TO YOUR MONITOR&#8217;S  
\# USER MANUAL FOR THE CORRECT NUMBERS.  
HorizSync 30-95

\# VertRefresh is in Hz unless units are specified.  
\# VertRefresh may be a comma separated list of discrete values, or a  
\# comma separated list of ranges of values.  
\# NOTE: THE VALUES HERE ARE EXAMPLES ONLY. REFER TO YOUR MONITOR&#8217;S  
\# USER MANUAL FOR THE CORRECT NUMBERS.  
VertRefresh 47-160

\# This is a set of extended mode timings typically used for laptop,  
\# TV fullscreen mode or DVD fullscreen output.  
\# These are available along with standard mode timings.

\# Sony Vaio C1(X,XS,VE,VN)?  
\# 1024&#215;480 @ 85.6 Hz, 48 kHz hsync  
ModeLine &#8222;1024&#215;480&#8220; 65.00 1024 1032 1176 1344 480 488 494 563 -hsync -vsync

\# 768&#215;576 @ 79 Hz, 50 kHz hsync  
ModeLine &#8222;768&#215;576&#8220; 50.00 768 832 846 1000 576 590 595 630  
\# 768&#215;576 @ 100 Hz, 61.6 kHz hsync  
ModeLine &#8222;768&#215;576&#8220; 63.07 768 800 960 1024 576 578 590 616

EndSection

\# \***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\****  
\# Graphics device section  
\# \***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\****

Section &#8222;Device&#8220;  
Identifier &#8222;Generic VGA&#8220;  
Driver &#8222;vga&#8220;  
EndSection

Section &#8222;Device&#8220;  
Identifier &#8222;Nvidia GeForce MX400&#8220;  
VendorName &#8222;Microstar&#8220;  
BoardName &#8222;MSI 8833 VIVO 32mb&#8220;  
Driver &#8222;nvidia&#8220;  
VideoRam 32768  
\# Clock lines

Option &#8222;TwinView&#8220;

Option &#8222;SecondMonitorHorizSync&#8220; &#8222;30-50&#8220;  
Option &#8222;SecondMonitorVertRefresh&#8220; &#8222;60&#8220;  
Option &#8222;TwinViewOrientation&#8220; &#8222;Clone&#8220;  
Option &#8222;MetaModes&#8220; &#8222;1152&#215;864, 800&#215;600 @1152&#215;864; 1024&#215;768, 800&#215;600 @1024&#215;768; 800&#215;600, 800&#215;600 @800&#215;600&#8220;  
Option &#8222;ConnectedMonitor&#8220; &#8222;crt,TV&#8220;  
Option &#8222;TVOutFormat&#8220; &#8222;COMPOSITE&#8220;  
Option &#8222;TVStandard&#8220; &#8222;PAL-B&#8220;

\# Uncomment following option if you see a big white block  
\# instead of the cursor!  
\# Option &#8222;sw_cursor&#8220;

Option &#8222;DPMS&#8220; &#8222;on&#8220;  
EndSection

\# \***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\****  
\# Screen sections  
\# \***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\***\****

Section &#8222;Screen&#8220;  
Identifier &#8222;screen1&#8220;  
Device &#8222;Nvidia GeForce MX400&#8220;  
Monitor &#8222;mymonitor&#8220;  
DefaultColorDepth 24  
Subsection &#8222;Display&#8220;  
Depth 8  
Modes &#8222;1152&#215;864&#8220; &#8222;1024&#215;768&#8220; &#8222;800&#215;600&#8220; &#8222;640&#215;480&#8220;  
ViewPort 0 0  
EndSubsection  
Subsection &#8222;Display&#8220;  
Depth 15  
Modes &#8222;1152&#215;864&#8220; &#8222;1024&#215;768&#8220; &#8222;800&#215;600&#8220; &#8222;640&#215;480&#8220;  
ViewPort 0 0  
EndSubsection  
Subsection &#8222;Display&#8220;  
Depth 16  
Modes &#8222;1152&#215;864&#8220; &#8222;1024&#215;768&#8220; &#8222;800&#215;600&#8220; &#8222;640&#215;480&#8220;  
ViewPort 0 0  
EndSubsection  
Subsection &#8222;Display&#8220;  
Depth 24  
Modes &#8222;1152&#215;864&#8220; &#8222;1024&#215;768&#8220; &#8222;800&#215;600&#8220; &#8222;640&#215;480&#8220;  
ViewPort 0 0  
EndSubsection  
Subsection &#8222;Display&#8220;  
Depth 32  
Modes &#8222;1152&#215;864&#8220; &#8222;1024&#215;768&#8220; &#8222;800&#215;600&#8220; &#8222;640&#215;480&#8220;  
ViewPort 0 0  
EndSubsection  
EndSection

Section &#8222;ServerLayout&#8220;  
Identifier &#8222;layout1&#8220;  
Screen &#8222;screen1&#8220;

InputDevice &#8222;Mouse1&#8220; &#8222;CorePointer&#8220;

InputDevice &#8222;Keyboard1&#8220; &#8222;CoreKeyboard&#8220;  
EndSection

########end of config file

To bi bilo sve, nadam se da nece biti nikakvih problema.

ps. BTW, ovo nikako nije sve sto se tice X Servera i njegovih podesavanja. Da li vas nerviraju  
ruznjikavi fontovi koje prikazuje X Font Server? Cemu X Font Server kad sam X lepo renderuje  
fontove? Kako se dozvoljava  
i ogranicava pristup X Serveru? Razmisljajte, kopajte po netu,  
experimentisite

Poz

Salac  
salek@galeb.etf.bg.ac.yu  
August 2003

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=364)