---
author: tomaja
date: "2006-10-22T01:28:41Z"
excerpt: <p>Za&scaron;to ba&scaron; Xgl a ne AIGLX? OK, da pričamo o NVIDIA drajverima
  to bi svakako bilo racionalno re&scaron;enje, jer je AIGLX inkorporiran u X.Org
  a novi NVIDIA drajveri v1.0-9626 svakako podržavaju AIGLX. Naravno, ovde je mnogo
  lak&scaron;e uraditi naknadni upgrade 3D grafičkog okruženja, odnosno dovoljno je
  update-ovati X.Org i/ili NVIDIA drajvere.&nbsp; Ali, dobar deo nas koristi ATI grafičke
  kartice. ATI-jevi drajveri jo&scaron; uvek ne podržavaju &quot;composite&quot; ekstenziju
  pa samim tim sa &quot;proprietary&quot; drajverima možemo koristiti samo Xgl. Non-propiertary
  ili &quot;radeon&quot; drajveri rade i sa AIGLX tehnologijom ali smo sa te strane
  veoma o&scaron;tećeni po pitanju performansi.</p><p>Dakle, kako podesiti Xgl na
  GNU/Debian-u (a vrlo verovatno uz možda manje korekcije i na Knoppix, Kanotix, Kubuntu,
  SimplyMEPIS distroima) ?<br /> </p>
guid: https://forum.linuxo.org/2006/10/22/kako-instalirati-xgl-i-compiz-sa-ati-fglrx-drajverom-na-gnu-debian-u/
id: 1380
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Kako instalirati Xgl i compiz sa ATI fglrx drajverom na GNU/Debian-u
url: /kako-instalirati-xgl-i-compiz-sa-ati-fglrx-drajverom-na-gnu-debian-u/
---
Za&scaron;to ba&scaron; Xgl a ne AIGLX? OK, da pričamo o NVIDIA drajverima to bi svakako bilo racionalno re&scaron;enje, jer je AIGLX inkorporiran u X.Org a novi NVIDIA drajveri v1.0-9626 svakako podržavaju AIGLX. Naravno, ovde je mnogo lak&scaron;e uraditi naknadni upgrade 3D grafičkog okruženja, odnosno dovoljno je update-ovati X.Org i/ili NVIDIA drajvere.&nbsp; Ali, dobar deo nas koristi ATI grafičke kartice. ATI-jevi drajveri jo&scaron; uvek ne podržavaju "composite" ekstenziju pa samim tim sa "proprietary" drajverima možemo koristiti samo Xgl. Non-propiertary ili "radeon" drajveri rade i sa AIGLX tehnologijom ali smo sa te strane veoma o&scaron;tećeni po pitanju performansi.

Dakle, kako podesiti Xgl na GNU/Debian-u (a vrlo verovatno uz možda manje korekcije i na Knoppix, Kanotix, Kubuntu, SimplyMEPIS distroima) ? 

<!--break-->

Prvo, pretpostavka je da ste već instalirali ATI "fglrx"grafičke drajvere. Zatim sledi sledeći postupak:

<span style="text-decoration: underline">1.Instalirajte sledeće pakete sa standardnih Sebian Sid repozitorijuma:</span>  
<span style="font-weight: bold">libdrm2</span>  
<span style="font-weight: bold">libpng3</span>  
<span style="font-weight: bold">libxdamage1</span>  
<span style="font-weight: bold">libxcomposite1</span>  
<span style="font-weight: bold">libxfont1</span>  
<span style="font-weight: bold">libglitz1</span>  
<span style="font-weight: bold">libglitz-glx1</span>  
<span style="font-weight: bold">libgl1-mesa-glx</span>  
<span style="font-weight: bold">libfontenc1</span>

Napomena: Čak i pored činjenice sa su sada compiz paketi dostupni za Sid, oni su namenjeni korisnicima GNOME-a i ne dolaze sa alatkama poput "Preferences" i "Theme Selector"-a. Pa ćemo zato ne&scaron;to kasnije instalirati funkcionalnije compiz pakete.

<span style="text-decoration: underline">2. Dodajte sledeće repozitorijume u /etc/apt/sources.list:</span>  
deb <http://cairographics.org/packages/debian/> unstable/  
deb-src <http://cairographics.org/packages/debian/> unstable/

<span style="text-decoration: underline">Zatim pokrenite "apt-get update" i instalirajte:</span>  
<span style="font-weight: bold">libsvg-cairo1</span>  
<span style="font-weight: bold">libsvg1</span>

<span style="text-decoration: underline">3. Dodajte u /etc/apt/sources.list:</span>  
deb <http://www5.autistici.org/debian-xgl/debian/> binary-i386/

<span style="text-decoration: underline">Zatim pokrenite ponovo "apt-get update" i instalirajte:</span>  
<span style="font-weight: bold">xgl</span>  
<span style="font-weight: bold">compiz</span>  
<span style="font-weight: bold">cgwd-themes</span>

<span style="text-decoration: underline">4. Izmenite /etc/kde3/kdm/kdmrc:</span>  
u sekciji "<span style="font-weight: bold">[X-:*-Core]</span>":  
promenite "<span style="font-weight: bold">ServerCmd=/usr/bin/X -br</span>"  
u&nbsp; "<span style="font-weight: bold">ServerCmd=/usr/bin/Xgl :1 -fp /usr/share/fonts/X11/misc -fullscreen -ac -accel glx:pbuffer -accel xv:pbuffer -br</span>"

Možda je jo&scaron; bolje i da komentirate postojeću liniju "ServerCmd" da bi mogli da se lako prebacujete između Xgl-a i sandardnog X okruženja.

<span style="text-decoration: underline">5. Izmenite /etc/X11/xorg.conf:</span>  
U opcijama za tastaturu: "<span style="font-weight: bold">Option "XkbOptions" "altwin:super_win"</span> "  
U opcijama za ekran, proverite da je default color depth&nbsp; 24  
U delu za gafičku karticu proverite da je je opcija&nbsp; "<span style="font-weight: bold">sw_cursor</span>" is isključena/komentirana

<span style="text-decoration: underline">6. Izmenite /etc/init.d/kdm:</span>  
Nakon "<span style="font-weight: bold">set -e</span>" linije, dodajte liniju:  
"<span style="font-weight: bold">export LIBGL_DRIVERS_PATH=/usr/lib/dri</span>"

Od ove tačke, Xgl bi trebao da radi kada se ulogujete u KDE.

<span style="text-decoration: underline">7. Da bi pokrenuli compiz:</span>  
Otvorite terminal (konzolu) u i ukucajte "compiz-start.py &" Trebalo bi sa sada imate compiz dekoracije na prozorima, 3d kockku na desktopu i ostale efekte.  
TAkođe bi trebali da imate i cgwd ikonu u sistemskom tray-u sa kojom možete menjati opcije i graf.teme

Da bi pokretali compiz pri pokretanju KDE-a, kreirajte fajl sa imenom "compiz.desktop" u koji ćete ubaciti sledeće linije: [Desktop Entry] Encoding=UTF-8

  
Exec=xmodmap -e 'keycode 113 = Mode_switch' -e 'keycode 22 = BackSpace';compiz-start.py  
GenericName[en_US]=  
StartupNotify=false  
Terminal=false  
TerminalOptions=  
Type=Application  
X-KDE-autostart-after=kdesktop</p> 

Dvokliknite na njega, i ono &scaron;to bi trebalo da se desi jeste pokretanje compiz-a sa svim efektima. Takođe bi trebalo da imate i malo pre pomenutu ikonicu.

Ukoliko želitee da ga pokrećete pri svakom logovanju u KDE, ubacite ovaj fajl u&nbsp; ~/.kde/Autostart.

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=1380)