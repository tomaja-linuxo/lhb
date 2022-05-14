---
author: tomaja
date: "2002-06-18T18:15:09Z"
excerpt: |
  <p>Pokretanje X window sistema iliti `prozora` je sada prilično<br />
  automatizovano. Međutim, ako želite da saznate kako to sve<br />
  funkcioniše kao i kako podesite određene parametre kao što su<br />
  rezolucija i sl. onda treba pročitate ovaj tekst. On se stoji iz 4 dela:<br />
  <a href="http://mandrake.osny.org.yu/modules.php?name=News&amp;file=article&amp;sid=23#xgen">Pokretanje X Window sistema-opšti deo</a>, <a href="http://mandrake.osny.org.yu/modules.php?name=News&amp;file=article&amp;sid=23#conf">Konfiguracioni fajlovi</a>,<br />
  <a href="http://mandrake.osny.org.yu/modules.php?name=News&amp;file=article&amp;sid=23#xcon">Pokrtanje iz konzole</a> i <a href="http://mandrake.osny.org.yu/modules.php?name=News&amp;file=article&amp;sid=23#xgraph">Grafi?ko pokretanje</a> .<br />
  <br />
  Dodatna pitanja vezana za X window sistem možete postaviti na <a href="http://www.linuxo.org/forum">forumu</a>
guid: https://forum.linuxo.org/2002/06/18/x-window-sistem/
id: 171
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: X window sistem
url: /x-window-sistem/
---
Pokretanje X window sistema iliti \`prozora\` je sada prilično  
automatizovano. Međutim, ako želite da saznate kako to sve  
funkcioniše kao i kako podesite određene parametre kao što su  
rezolucija i sl. onda treba pročitate ovaj tekst. On se stoji iz 4 dela:  
[Pokretanje X Window sistema-opšti deo](http://mandrake.osny.org.yu/modules.php?name=News&file=article&sid=23#xgen), [Konfiguracioni fajlovi](http://mandrake.osny.org.yu/modules.php?name=News&file=article&sid=23#conf),  
[Pokrtanje iz konzole](http://mandrake.osny.org.yu/modules.php?name=News&file=article&sid=23#xcon) i [Grafi?ko pokretanje](http://mandrake.osny.org.yu/modules.php?name=News&file=article&sid=23#xgraph) .

Dodatna pitanja vezana za X window sistem možete postaviti na [forumu](http://www.linuxo.org/forum) <!--break-->

### <a id="xgen" name="xgen">Pokretanje X Windows sistema &#8211; Opšte</a>

U osnovi, postoje dva načina kako da pokrenete X-ove: iz konzole ili preko grafičkog login menadžera. To zavisi od default runlevel moda u '/etc/inittab' fajlu. Linija

`id:3:initdefault:`

govori sistemu da startuje konzolu. Linija

`id:5:initdefault:`

vas direktno vodi do X login ekrana. Zapamtite da ove podešene opcije možete i zaobići ako pri promptu startera unesete:

<kbd>linux init 3</kbd>

što će pokrenuti konzolu, bez obzira na opcije u '/etc/inittab', i

<kbd>linux init 5</kbd>

koji startuje X-ove. Default opcije možete izmeniti ili izmenom '/etc/inittab' direktno kao 'root' ili preko Mandrake Kontrolnog Centra ('Boot' &#8211; 'Boot Config' &#8211; 'Launch the X Window system at start').

<p class="smallright">
  <a href="https://linuxo.org/?p=4#top">na početak</a>
</p>

### <a id="conf" name="conf">Konfiguracioni fajlovi</a>

X Window Sistem se sastoji od dve komponente: klijenta i servera. Zbog svoje strukture, postoje dva skupa konfiguracionih fajlova, jedan za klijenta i jedan za server. Konfiguracija klijenta može biti korigovana specijalnim fajlovima u korisnikovom home direktorijumu.

Konfiguracija klijenta:

  * '/etc/X11/Xsession': Ovaj skript određuje koji window menadžer ili desktop okruženje treba da se pokrene u X-u. Opcije mogu biti promenjene pomoću '.xinitrc' ili '.xsession' fajlova (iako se danas dosta retko koriste) ili preko opcija 'startx' komande (pogledaj gore).
  * '/etc/X11/wmsession.d/': Ovaj direktorijum sadrži startne skripte za window menadžere i desktop okruženja instalirana na sistemu. Sesije mogu biti proverene, dodavana ili brisane preko 'chksession' komande. Više o ovome pomoću _<kbd>man chksession</kbd>_.

Konfiguracija servera:

  * '/etc/X11/XF86Config-4': Ovaj fajl sadrži hardversku konfiguraciju i opcije kao što su default rezolucija ili broj boja. Obično se ručno ne edituje već preko alata kao što je 'XFdrake'. Više o ovoj mogućnosti pomoću _<kbd>man XF86Config</kbd>_.
  * '/etc/X11/xdm/Xservers': Ovaj fajl sadrži koandnu liniju za pokretanje X server(a). Ovo vam može biti interesantno kada želite da pokrenete više od jednog servera ili da isključite X' network pristup iz sigurnosnih razloga ('-nolisten' opcija). Lista opcija i sintaksa vam je dostupna ako u konzloli ukucate _<kbd>man Xserver</kbd>_.

Ostali konfiguracioni fajlovi:

  * '/etc/X11/fs/config': Konfiguracioni fajl za 'xfs' font server. Pogledajte _<kbd>man xfs</kbd>_.
  * '/etc/X11/Xressources' i fajlovi u '/etc/X11/app-defaults': Ovi fajlovi određuju način prikaza nekih programa koji su deo XFree86 paketa (kao što je 'xterm'). Opcije mogu biti promenjene '~/.Xdefaults' fajlom. Kako većina nas danas koristi GTK+ ili Qt zamene, ovo je od manjeg značaja. Ipak, pogledajte _<kbd>man xrdb</kbd>_.
  * '/etc/X11/Xmodmap' sadrži neke default podešene tastere za 'Backspace' i 'Windows' tastere.
  * '/etc/X11/XftConfig' sadrži opcije za anti-aliasing teksta preko RENDER ekstenzije. 

<p class="smallright">
  <a href="file:///home/toma/xstart.html#top">na po?etak</a>
</p>

### <a id="xcon" name="xcon">Pokretanje iz konzole</a>

Nakon što ste se ulogovali, naći ćete se u svom home direktorijumu. Da bi pokrenuli X-ove, unesite

_<kbd>startx</kbd>_

#### Startanje (detaljan opis)

'startx' je startan skripta za 'xinit', X inicijalni program.  
nakon iniciranja servera sa opcijama koje su napisane u '/etc/X11/xdm/Xservers', 'xinit' pokušava da pronađe fajl '.xinitrc' u vašem home direktorijumu. Ukoliko ga nema, on traži svoj sopstveni konfiguracioni fajl '/etc/X11/xinit/xinitrc'. Ovaj fajl u osnovu upućuje 'xinit' na '/etc/X11/Xsession', centralni startup konfiguracioni skript.

  1. '/etc/X11/Xsession' podešava default background boju, pokreće SSH agenta ukoliko je dostupan, procesira korisničke fajlove za opcije kao što su '.Xresources' i '.Xdefaults' i podešava $BROWSER promenjivu.

  2. Nakon toga izvršava `/usr/sbin/chksession -l` da bi video koji su window menadžeri i desktop okruženja dostupna na sistemu. 'chksession' dobavlja listu od skripti iz '/etc/X11/wmsession.d', a njihov red je odreden dvocifrenim brojem ispred svakog fajla.

  3. Sledeći na redu su skripte u '/etc/X11/xinit.d' (obi?no je u pitanju ažuriranje sistema menija i manje opcije za tastaturu).

  4. nakon toga se proverava da li uopšte imate određen neki od window menadžera ili desktop okruženja u komandnoj liniji. Ukoiko nemate, proverava da li je isto tak i u ~/.desktop fajlu. Ako nije , '/etc/sysconfig/desktop' se proverava zbog opcija. Ukoliko je jedna od ovih mogućnosti završila uspehom, promenjiva $DESKTOP je podešena

  5. Sledeća skripta koja ide u proveru ukoliko je XIM input server potreban (uglavnom za Azijske jezike) i ukoliko 'first time wizard' treba da se pokrene.

Nakon što se sve završi, skripta konaćno pokreće grafičko okruženje ovim redom:

  1. Window manadžer ili desktop okruženje odreÄ&lsquo;eno u $DESKTOP promenjivoj. Odgovarajuća startup skripta u /etc/X11/wmsession.d je izvršena.

  2. Ukoliko skripta ne uspe da podesi $DESKTOP promenjivu, `izvršava se &#39;/usr/sbin/chksession -F`'. Ovo opet izbacuje prvu dostupnu sesiju koja se zatim startuje.

  3. Ukoliko i ovo omane, skripta traži 'icewm' window mendžer i pokreće ga.

  4. Ako 'icewm' nije instaliranr, onda traži 'icewm-light', ili 'twm' (XFree's own very basic window manager).

#### Opcije

Kao što ste mogli da vidite, možete da utičete na proces startanja na nekoliko načina:

  1. Podešavanjem opcija u 'startx' komandi. Postoje dve grupe opcija koje se mogu podesiti preko 'startx', opcije za klijenta i opcije za server. Opcije za klijenta obično sadrže ime sesije window menadžera koji želite da koristite:
    
    _<kbd>startx WindowMaker</kbd>_
    
    pokre?e X-ove sa Window Maker window menadžerom. VAžno je re?i da morate da koristite tačno ono ime koje je prikazano u listi koju možete dobiti pomoću komande _<kbd>/usr/sbin/chksession -l</kbd>_ . Druga grupa opcija je vezana za server. One uklju?uju broj boja ili DPI postavke. Moguće opcije su prikazane u <kbd>XF86Config</kbd> fajlu. Opcije za sever se odvajaju sa duplom crticom:
    
    _<kbd>startx WindowMaker -- -depth 16 -dpi 100</kbd>_
    
    pokreće X sa Window Maker window menadžerom i brojem boja od 16 bita.  
    Opcije koje se podese preko 'startx' su važnije i izvršavaju se be obzira na druge koje se nalaze u ostalim konfig. fajlovima.

  2. Kreiranjem '.xinitrc' fajla. .xinitrc fajl govori X-ovima koje skripte ili programe preba da pokrenu i koji window menadžer da startuju. Evo i primera:
    
    `xmodmap ~/.Xmodmap<br />
xterm &<br />
exec wmaker`
    
    Prva linija pokre?e konzolni alata za promenu rasporeda tastature.  
    Druga linija pokreće emulator xterm terminala. Možete primetiti '&' na kraju linije, što je potrebno kada pokrećete grafičke programe preko a '.xinitrc' da bi ih poslali 'u pozadinu'. Inače bi proces startanja čekao sve dok se program(terminal) ne zatvori.  
    Poslednja linija koristi 'exec' komandu, koaj zamenjuje trenutni shell sa komandom koja sledi. Ova komanda je izvršno ime window menadžera (u ovom slučaju Window Maker).

  3. Preko '~/.desktop' fajla. Kreirajte fajl sa imenom '.desktop' u svom home direktorijumu sa linijom u njemu:
    
    `DESKTOP=<var>session_name</var>`
    
    gde je <var>session_name</var> ime vašeg omiljenog grafi?kog okruženja koje možete pronaći pomoću <kbd>/usr/sbin/chksession -l</kbd>.

<p class="smallright">
  <a href="https://linuxo.org/?taxonomy=freetags&#038;term=desktop">na početak</a>
</p>

### <a id="xgraph" name="xgraph">Grafičko pokretanje</a>

Grafički login-om upravljaju displej menadžeri. Mandrake Linux dolazi sa tri ovakva display menadžera: KDM (KDE Displej Menadžer), GDM (GNOME Displej Menadžer) i XDM (pogađate &#8230; ;-)), mada je KDM default.

Displej menadžeri nude prilično lako pokretanje i zaustavljanje X sesija. Oni takođe omogućavaju logovanje preko mreže. GDM nudi i dodatan broj opvija. Sa druge strane, oni same troše sistemske resurse tokom cele X sesije i mogu prestavljati sigurnosni rizik ako su loše podešeni.

KDM je deo 'kdebase' RPM paketa, GDM dolazi sa svojim 'gdm' RPM a XDM je deo XFree86 paketa. GDM-u nije potreban GNOME da bi bio instaliran.

#### Startanje (detaljan opis)

Ukoliko je podešen runlevel 5 kao default runlevel u '/etc/inittab' fajlu, izvršava se specijalna komanda:

_`x:5:respawn:/etc/X11/prefdm -nodaemon`_

Sintaksa ove linije je 'id:runlevel:action:command', u ovom slučaju: kada se izvršava runlevel 5 (id 'x'), pokreće se recurring proces pomoću komande '/etc/X11/prefdm -nodaemon'. Ovaj proces se ssam restartuje svaki puta kada se ugasi (npr. ako se izlogujete iz X sesije, displej manadžerov login prozor se ponovo pojavljuje i vi se neđete naći u konzoli).

'/etc/X11/prefdm' je skripta koja pokušava da koji display menadžer želite da koristite. Prvo proverava da li je podešen 'autologin' u '/etc/sysconfig/autologin'. Ukoliko jeste, 'autologin' komanda se izvršava i korisnik će direktno doći do svog okruženja. Ovo može da se podesi preko 'Mandrake Kontrolnog Centra' ('Boot' &#8211; 'Boot Config').

Ukoliko autologin nije aktiviran, 'prefdm' proverava '/etc/sysconfig/desktop' radi DISPLAYMANAGER promenjive (mogu vrednosti su: GDM, KDM ili XDM). Ukoiko ova pormenjiva nije podešena, skripta proverava DESKTOP promenjivu u istom fajlu. Ukoliko je ta promenjiva podešena na GNOME, GDM je pretpostavljen kao dispej menadžer, ako je KDE, onda je KDM.

Ukoliko se ne desi ništa od ovoga, skripta proverava he script koji su displej menadžeri instalirani i pokreće prvi koji pronađe. KDM se traži prvi, zatim GDM pa onda XDM.

#### Konfiguracija

I GDM i KDM se mogu podesiti preko svojih kofiguracionih modula u desktop komandnom centru. Centralni konfiguracioni fajl za GDM je '/etc/X11/gdm/gdm.conf', a KDM koristi '/usr/share/config/kdm/kdmrc'.  
GDM takođe možete podesiti kao 'root' preko <kbd>gdmconfig</kbd> komande ili preko menija ('Configuration' &#8211; 'Boot and Init'). On nudi mnogo više opcija odnosu na KDM, posebno po pitanju mrežnog pristupa.  
Ipak, treba da budete veoma pažljivi jer pogrešno podešene opcije mogu ugroziti bezbednost sistema.

Ukoiko instalirate GDM a koristite KDE, morate podesiti

`DISPLAYMANAGER=GDM`

u '/etc/sysconfig/desktop' ili će sistem nastaviti da koristi KDM.

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=171)