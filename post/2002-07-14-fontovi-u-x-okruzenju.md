---
author: tomaja
date: "2002-07-14T12:35:20Z"
excerpt: |
  Ovaj tekst vam može pomo?i da podesite izgled i veli?inu fontova, instalirate<br>
  nove TTF i druge fontove,kako da podesite XFree konfiguracioni fajl a takoÄ‘e<br>
  su pomenute i aplikacije za pregled i manipulaciju sa fontovima. <br>
  Prikazani su i linkovi ka sajtovima sa kojih možete besplatno preuzeti fontove.
  <br>
  Tekst se sastoji iz 4 dela i to: <a
  href="http://mandrake.osny.org.yu/modules.php?name=http://mandrake.osny.org.yu/modules.php?name=News&amp;file=article&amp;sid=33#aa">Font
  Anti-Aliasing</a>, <a
  href="http://mandrake.osny.org.yu/modules.php?name=News&amp;file=article&amp;sid=33#small">Promena
  veli?ine fonta</a>, <br>
  <a
  href="http://mandrake.osny.org.yu/modules.php?name=News&amp;file=article&amp;sid=33#Add">Dodavanje
  (instaliranje) fontova</a>, <a
  href="http://mandrake.osny.org.yu/modules.php?name=News&amp;file=article&amp;sid=33#Apps">Font
  preglednici (viewers)</a>.  <br>
  Ono što je bitno a vezano je za...
guid: https://forum.linuxo.org/2002/07/14/fontovi-u-x-okruzenju/
id: 198
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Fontovi u X okruženju
url: /fontovi-u-x-okruzenju/
---
Ovaj tekst vam može pomo?i da podesite izgled i veli?inu fontova, instalirate  
nove TTF i druge fontove,kako da podesite XFree konfiguracioni fajl a takoÄ‘e  
su pomenute i aplikacije za pregled i manipulaciju sa fontovima.  
Prikazani su i linkovi ka sajtovima sa kojih možete besplatno preuzeti fontove.  
  
Tekst se sastoji iz 4 dela i to: [Font  
Anti-Aliasing](http://mandrake.osny.org.yu/modules.php?name=http://mandrake.osny.org.yu/modules.php?name=News&file=article&sid=33#aa), [Promena  
veli?ine fonta](http://mandrake.osny.org.yu/modules.php?name=News&file=article&sid=33#small),  
[Dodavanje  
(instaliranje) fontova](http://mandrake.osny.org.yu/modules.php?name=News&file=article&sid=33#Add), [Font  
preglednici (viewers)](http://mandrake.osny.org.yu/modules.php?name=News&file=article&sid=33#Apps).  
Ono što je bitno a vezano je za&#8230;<!--break-->

### <a id="aa" name="aa">Font Anti-Aliasing</a>

<big><i><b> </b></i></big>Font anti-aliasing (AA) radi tako što dodaje zasen?ene  
piksele na ivicama fontova, što ih ?ini zaobljenijim i lepšim. Ova mogu?nost  
je prvi put uvedena u XFree 4.0.3 preko &#8216;RENDER&#8217; ekstenzije i X FreeType  
interfejs biblioteke (Xft).  
Da bi u stvarnosti videli AA aaplikacije na desktopu odreÄ‘eni widget-i  
moraju takoe podržavati AA. Qt (KDE) to radi po default-u, dok GTK+ 1.2  
(GNOME, GIMP) zahteva instalaciju posebne biblioteke. GTK+ 2.0 (zajedno sa  
GNOME 2) podržava AA u startu.

Da bi prikazali AA na anšem desktopu, moramo proveriti da li XFree nudi  
RENDER ekstenziju za vašu grafi?ku karticu. Pokrenite ovu  
komandu u terminalu:

xdpyinfo | grep -c -i render

Ukoliko dobijete &#8216;1&#8217;, možete nastaviti dalje. Ukoliko ne, mora?ete da sa?ekate  
da XFree omogu?i RENDER za vašu karticu u novijoj verziji.

Uklju?ivanje AA u KDE-u je veoma prosto: Otvorite &#8216;Kontrolni Centar&#8217;: &#8216;LooknFeel&#8217;  
&#8211; &#8216;Fonts&#8217;, ozna?ite polje &#8216;Use Anti-Aliasing for fonts&#8217;, sa?uvaje izmene,  
izlogujte se pa se ponovo ulogujte. I to je to, anti-aliasing bi trebalo  
da radi.

Sa GNOME-om i GTK stvar je malo komplikovanija. Skinite RPM sa [gdkxft home page-a](http://gdkxft.sourceforge.net/) i instalirajte  
ga. Selektujte &#8216;gdkxft&#8217; temu iz GNOME Kontrolnog Centra. Ukoliko ne?ete koristiti  
GNOME kopirajte fajl &#8216;/usr/share/themes/Gdkxft/gtk/gtkrc&#8217; u vaš home direktorijum  
i preimenujte ga u &#8216;.gtkrc&#8217;. Dodajte linije

LD_PRELOAD=/usr/lib/libgdkxft.so.0  
export LD_PRELOAD

u vaš &#8216;~/.bashrc&#8217; fajl, izlogujte se i ponovo ulogujte i vaš GNOME desktop  
ili GTK aplikacije ?e biti anti-aliased. Da bi podesili veli?inu fontova  
koje su pomalo ?udne (posebno za naslove menija), izmenite vaš &#8216;~/.gtkrc&#8217;  
i smanjite veli?inu fontova.  
Ukoliko želite neku drugu temu, izaberite je iz GNOME Kontrolnog Centra,  
i izaberite &#8216;Custom Font&#8217;. Mogu?e je da ?e biti potrebno manje podešavanje,  
posebno sa meni fontovima (ovo zbog toga što GTK+ interno, za sada, ne poznaje  
AA).

Opšte postavke se mogu urediti ili u &#8216;/etc/X11/XftConfig&#8217; ili u lokalnom  
&#8216;~/.xftconfig&#8217; fajlu. Jedno stvar koju svakako morate uraditi jeste da stavite  
(#) ispred svih prikazanih direktorijuma u &#8216;XftConfig&#8217; koji nisu prikazani  
vašem sistemu. Ovo ?e imati pozitivan efekat na vreme podizanja aplikacija.  
Za više objašnjenja možete pro?itati KDot tutorijal o <a href="http://dot.kde.org/9898 

### <a id="aa" name="aa">Font Anti-Aliasing</a>

<big><i><b> </b></i></big>Font anti-aliasing (AA) radi tako što dodaje zasen?ene  
piksele na ivicama fontova, što ih ?ini zaobljenijim i lepšim. Ova mogu?nost  
je prvi put uvedena u XFree 4.0.3 preko &#8216;RENDER&#8217; ekstenzije i X FreeType  
interfejs biblioteke (Xft).  
Da bi u stvarnosti videli AA aaplikacije na desktopu odreÄ‘eni widget-i  
moraju takoe podržavati AA. Qt (KDE) to radi po default-u, dok GTK+ 1.2  
(GNOME, GIMP) zahteva instalaciju posebne biblioteke. GTK+ 2.0 (zajedno sa  
GNOME 2) podržava AA u startu.

Da bi prikazali AA na anšem desktopu, moramo proveriti da li XFree nudi  
RENDER ekstenziju za vašu grafi?ku karticu. Pokrenite ovu  
komandu u terminalu:

xdpyinfo | grep -c -i render

Ukoliko dobijete &#8216;1&#8217;, možete nastaviti dalje. Ukoliko ne, mora?ete da sa?ekate  
da XFree omogu?i RENDER za vašu karticu u novijoj verziji.

Uklju?ivanje AA u KDE-u je veoma prosto: Otvorite &#8216;Kontrolni Centar&#8217;: &#8216;LooknFeel&#8217;  
&#8211; &#8216;Fonts&#8217;, ozna?ite polje &#8216;Use Anti-Aliasing for fonts&#8217;, sa?uvaje izmene,  
izlogujte se pa se ponovo ulogujte. I to je to, anti-aliasing bi trebalo  
da radi.

Sa GNOME-om i GTK stvar je malo komplikovanija. Skinite RPM sa [gdkxft home page-a](http://gdkxft.sourceforge.net/) i instalirajte  
ga. Selektujte &#8216;gdkxft&#8217; temu iz GNOME Kontrolnog Centra. Ukoliko ne?ete koristiti  
GNOME kopirajte fajl &#8216;/usr/share/themes/Gdkxft/gtk/gtkrc&#8217; u vaš home direktorijum  
i preimenujte ga u &#8216;.gtkrc&#8217;. Dodajte linije

LD_PRELOAD=/usr/lib/libgdkxft.so.0  
export LD_PRELOAD

u vaš &#8216;~/.bashrc&#8217; fajl, izlogujte se i ponovo ulogujte i vaš GNOME desktop  
ili GTK aplikacije ?e biti anti-aliased. Da bi podesili veli?inu fontova  
koje su pomalo ?udne (posebno za naslove menija), izmenite vaš &#8216;~/.gtkrc&#8217;  
i smanjite veli?inu fontova.  
Ukoliko želite neku drugu temu, izaberite je iz GNOME Kontrolnog Centra,  
i izaberite &#8216;Custom Font&#8217;. Mogu?e je da ?e biti potrebno manje podešavanje,  
posebno sa meni fontovima (ovo zbog toga što GTK+ interno, za sada, ne poznaje  
AA).

Opšte postavke se mogu urediti ili u &#8216;/etc/X11/XftConfig&#8217; ili u lokalnom  
&#8216;~/.xftconfig&#8217; fajlu. Jedno stvar koju svakako morate uraditi jeste da stavite  
(#) ispred svih prikazanih direktorijuma u &#8216;XftConfig&#8217; koji nisu prikazani  
vašem sistemu. Ovo ?e imati pozitivan efekat na vreme podizanja aplikacija.  
Za više objašnjenja možete pro?itati KDot tutorijal o [podešavanju Anti-Aliased desktopa](http://dot.kde.org/989808269/)  
i sintakse koja se koristi u &#8216;XftConfig&#8217;.  
Ako imate TFT monitor ( ili laptop, flat panel),treba da pogledate [Justin Mason-ov mini-HOWTO za  
Sub-Pixel Font Pozicioniranje](http://jmason.org/howto/subpixel.html).  
08269/&#8220;>podešavanju Anti-Aliased desktopa</a>  
i sintakse koja se koristi u &#8216;XftConfig&#8217;.  
Ako imate TFT monitor ( ili laptop, flat panel),treba da pogledate [Justin Mason-ov mini-HOWTO za  
Sub-Pixel Font Pozicioniranje](http://jmason.org/howto/subpixel.html).

### <a id="Small" name="Small"></a>&#8222;moji fontovi su previše mali !&#8220;  


Ovo možete ispraviti na dva ili ?ak tri nivoa: na nivou sistema ili na  
nivou aplikacije. Ako koristite desktop okruženje kao što su KDE ili GNOME,  
možete promeniti default veli?inu fonta iz njihovih Kontrolnih Centara.

Na nivou sistema, mali fontovi mogu biti prouzrokovani X font serverom  
(xfs) koji prvo u?itava set manjih fontova ili sa pogrešnim DPI (dots per  
inch) opcijama ili i jednim i drugim.

Konfiguracioni fajl font servera je &#8216;/etc/X11/fs/config&#8217;. Direktorijumi  
koji su prikazani u katalogu se traže jedni za drugim zbog fontova koje zahteva  
X, pa zato prvi font koji se pronaÄ‘e &#8216;pobeÄ‘uje&#8217;:

/usr/X11R6/lib/X11/fonts/75dpi:unscaled,  
/usr/X11R6/lib/X11/fonts/100dpi:unscaled,

Ovo prvo u?itava (manje) 75 DPI fontove. Ukoliko zamenite im zamenite  
raspored, ve?i 100 DPI fontovi ?e biti koriš?eni. Ukoliko ne naÄ‘ete liniju  
za 100DPI fontove, onda prvo morate da ih instalirate (paket &#8216;XFree86-100dpi-fonts&#8217;).  
Restartujte font server kao &#8216;root&#8217; sa _service xfs restart_ da bi  
izmene koje ste napravili bile aktivirane (restartovanje X-ova ne?e pomo?i).

Po tradiciji, X pretpostavlja DPI opcije za 75. Ve?ina modernih monitora,  
meÄ‘utim, prati Windows standard i koristi 96 DPI. Da bi otkrili vaše trenutne  
DPI opcije, pokrenite:

xdpyinfo | grep dots

XFree 4 vam nudi mogu?nost korekcije ove opcije. Otvorite &#8216;/etc/X11/XF86Config-4&#8217;  
kao &#8216;root&#8217; u editoru, pronaÄ‘ite &#8216;Monitor section&#8217; i liniju koja izgleda  
ovako:

DisplaySize xx yy

Zamenite &#8216;xx&#8217; sa širinom vašeg ekrana u millimetrima,a &#8216;yy&#8217; sa visinom.  
Sa?uvajte izmene i restartujte X-ove.

### <a id="Add" name="Add">Dodavanje (instaliranje) fontova</a>  


Obi?no koristimo &#8216;**_DrakFont_**&#8216; preko Mandrake Kontrolnog Centra  
(&#8216;System&#8217; &#8211; &#8216;Fonts&#8217;). Ne samo da je najprakti?nije, ve? je i najpouzdanije.  
Ipak ako želite da to uradite na teži na?in ili zbog ne?ega DrakFont nefunkcioniše,  
pratite slede?e instrukcije:

 **PostScript (*.pcf)**

Kao &#8216;root&#8217;, kreirajte novi direktorijum za vaše fontove u &#8216;/usr/X11R6/lib/X11/fonts&#8217;  
i  
prekopirajte svoje nove fontove u njega.  
Pokrenite mkfontdir /usr/X11R6/lib/X11/fonts/new_directory  
Ovo ?e kreirati fajlove &#8216;fonts.alias&#8217; i &#8216;fonts.dir&#8217;.

Pokrenite xset fp rehash

Gotovo.  
Restartujte X Font Server kao &#8216;root&#8217; sa: service xfs restart

**TrueType (*.ttf)**

Kreirajte novi direktorijum kao &#8216;root&#8217; za fontove koje želite da dodate(npr.  
sa mkdir /usr/share/fonts/my_ttf.).

Ubacite nove fontove u ovaj direktorijum. Proverite da li se imena fontova  
sastoje isklju?ivo od malih slova. Proverite da ne bude praznog prostora u  
imenima fontova. Proverite ovlaš?enja (ls -l) za novi font direktorijum (trebalo  
bi da stoji drwxr-xr-x) i za fontove (trebalo bi da stoji -rw-r&#8211;r&#8211;).  
Ukoliko ovde pogrešite ne?ete mo?i da podignete X-ove!  
Unutar novog direktorijuma pokrenite ttmkfdir > fonts.scale da bi kreirali  
&#8216;fonts.scale&#8217; fajl kojeg ?e procesirati &#8216;mkfontdir&#8217;. &#8216;ttmkfdir&#8217; je deo &#8216;freetype-tools&#8217;  
paketa.

Ukoliko dobijete poruku kao na primer &#8216;unknown encodings&#8217; ti fontovi ne?e  
biti dodani u &#8216;fonts.scale&#8217; ili &#8216;fonts.dir&#8217; fajlove i ne?e biti dostupni.  
Da bi ih ipak omogu?ili pokrenite

ttmkfdir -c -p > fonts.scale

Opet ?ete dobiti poruku o grešci ali ?e ovi fontovi biti dodani u &#8216;fonts.scale&#8217;  
fajl. Mada se može desiti da ovi fontovi ne budu dostupni u svim aplikacijama.

Pokrenite mkfontdir.

Pokrenite chkfontpath &#8211;add new\_font\_directory kao &#8216;root&#8217;.  
Ovo ?e dodati direktorijum u &#8216;/etc/X11/fs/config&#8217;.

Pokrenite xset fp rehash kao &#8216;root&#8217; da bi omogu?ili X-ovima da prepoznaju  
nove fontove.  
Restartujte X Font Server koa &#8216;root&#8217; sa: service xfs restart

Mož+ete koristiti font direktorijume i sa drugim fajl sistemima, sve dok  
možete obzbediti  
read and write pristup za te fajl sisteme (npr. ne možete koristiti fontove  
na Windows XP NTFS particiji),  
Particija se automatski montira pri startanju,  
a putanja ka direktorijumima sa fontovima je prikazana u &#8216;/etc/X11/fs/config&#8217; 

Ipak, preporu?ujem da fontove kopirate u Linux font direktorijum.

NAPOMENA:

Vrlo se lako može desiti da nešto poÄ‘e naopako. Ukoliko se to desi ili &#8216;xfs&#8217;  
ne?e mo?i da se podigne pa X-ovi ne?e više raditi ili (ako imate XFree 4.1)  
X-ovi ?e jednostavno ignorisati grešku i novi fontovi ne?e biti dostupni.  
Ukoliko se X-ovi više nemogu podi?i , otvorite virtuelnu konzolu pomo?u  
<ALT F2>, ulogujte se kao &#8216;root&#8217;, otvorite &#8216;/etc/X11/fs/config&#8217; u editoru,  
i stavite (#) ispred linije sa novim direktorijumom, snimet izmenu i restartujte  
mašinu.

### <a id="Apps" name="Apps"></a>Font Preglednici (viewers)  


&#8216;Mandrake Kontrolni Centar&#8217; u sebi sadrži i preglednik fontova (&#8216;System&#8217;  
&#8211; &#8216;Fonts&#8217;), i ukoliko koristite desktop okruženje, možete koristiti polja  
u njihovom Kontrolnom Centru ili standardnim preview poljima dostupnim u konfiguracionim  
dijalozima ve?ine aplikacija.

&#8216;xfontsel&#8217; (deo &#8216;XF11R6-contrib&#8217; paketa) prikazuje fontove koje prepoznaje  
X server. U slu?aju zašto služi &#8216;select&#8217; taster, evo odgovora: on kopira string  
za prepoznavanje fonta u clipboard.

gfontview &#8222;je mali GTK+ preglednik fontova za PostScript Type 1 i TrueType  
fontove. On vam omogu?ava da prikažete bilo koji karakter ili string u  
pojedina?nom fontu &#8222;.

Moj omiljeni je &#8216;gtkfontsel&#8217;. Problem je u tome što se teško mož+e prona?i  
na internetu.

<big><i><b> Mesta na kojima možete prona?i fontove</b></i></big>

 [&#8216;Great TrueType Fonts&#8217;](http://www.truetype.demon.co.uk/ttfonts.htm)  
stranica prikazuje listu sajtova gde možete prona?i TT fontove.  
Obratite pažnju na copyright prava, mnogi od ovih fontova se ne mogu redistribuirati!

paketi sa fontovima su dostupni na RPM postavci na [Rufus.Org](http://rpmfind.net/linux/RPM/X11_fonts.html) u RPM-Formatu.

[  
Shareware Typefaces](http://www.masterstech-home.com/The_Library/Font_Samples/FontIndexMain.html) je velika, kolekcija freeware i shareware fontova.  
Sli?an paket je dostupan na [FontFreak](http://www.fontfreak.com/)-u.  
Još sajtova je prikazano u [Fonts  
&#8211; Collections section](http://directory.google.com/Top/Comhttp://directory.google.com/Top/Computers/Software/Fonts/
Coputers/Software/Fonts/Collections/) na Google Web Direktorijumu.

Stranica sa fontovima na [GIMP.org](http://www.gimp.org/http://www.gimp.org/fonts.html) prikazuje  
pakete koji su korisni za GIMP. Ako vas nerviraju dosadne greške tipa script-fu  
errors zbog nedostaju?ih fontova, onda je ovo pravo mesto za vas!

[Freshmeat](http://freshmeat.net/search/?query=font) lista font  
paketa i aplikcija za fontove.  
Restartujte X Font Server koa &#8216;root&#8217; sa: service xfs restart

Mož+ete koristiti font direktorijume i sa drugim fajl sistemima, sve dok  
možete obzbediti  
read and write pristup za te fajl sisteme (npr. ne možete koristiti fontove  
na Windows XP NTFS particiji),  
Particija se automatski montira pri startanju,  
a putanja ka direktorijumima sa fontovima je prikazana u &#8216;/etc/X11/fs/config&#8217; 

Ipak, preporu?ujem da fontove kopirate u Linux font direktorijum.

NAPOMENA:

Vrlo se lako može desiti da nešto poÄ‘e naopako. Ukoliko se to desi ili &#8216;xfs&#8217;  
ne?e mo?i da se podigne pa X-ovi ne?e više raditi ili (ako imate XFree 4.1)  
X-ovi ?e jednostavno ignorisati grešku i novi fontovi ne?e biti dostupni.  
Ukoliko se X-ovi više nemogu podi?i , otvorite virtuelnu konzolu pomo?u  
<ALT F2>, ulogujte se kao &#8216;root&#8217;, otvorite &#8216;/etc/X11/fs/config&#8217; u editoru,  
i stavite (#) ispred linije sa novim direktorijumom, snimet izmenu i restartujte  
mašinu.

### <a id="Apps" name="Apps"></a>Font Preglednici (viewers)  


&#8216;Mandrake Kontrolni Centar&#8217; u sebi sadrži i preglednik fontova (&#8216;System&#8217;  
&#8211; &#8216;Fonts&#8217;), i ukoliko koristite desktop okruženje, možete koristiti polja  
u njihovom Kontrolnom Centru ili standardnim preview poljima dostupnim u konfiguracionim  
dijalozima ve?ine aplikacija.

&#8216;xfontsel&#8217; (deo &#8216;XF11R6-contrib&#8217; paketa) prikazuje fontove koje prepoznaje  
X server. U slu?aju zašto služi &#8216;select&#8217; taster, evo odgovora: on kopira string  
za prepoznavanje fonta u clipboard.

gfontview &#8222;je mali GTK+ preglednik fontova za PostScript Type 1 i TrueType  
fontove. On vam omogu?ava da prikažete bilo koji karakter ili string u  
pojedina?nom fontu &#8222;.

Moj omiljeni je &#8216;gtkfontsel&#8217;. Problem je u tome što se teško mož+e prona?i  
na internetu.

<big><i><b> Mesta na kojima možete prona?i fontove</b></i></big>

 [&#8216;Great TrueType Fonts&#8217;](http://www.truetype.demon.co.uk/ttfonts.htm)  
stranica prikazuje listu sajtova gde možete prona?i TT fontove.  
Obratite pažnju na copyright prava, mnogi od ovih fontova se ne mogu redistribuirati!

paketi sa fontovima su dostupni na RPM postavci na [Rufus.Org](http://rpmfind.net/linux/RPM/X11_fonts.html) u RPM-Formatu.

[  
Shareware Typefaces](http://www.masterstech-home.com/The_Library/Font_Samples/FontIndexMain.html) je velika, kolekcija freeware i shareware fontova.  
Sli?an paket je dostupan na [FontFreak](http://www.fontfreak.com/)-u.  
Još sajtova je prikazano u [Fonts  
&#8211; Collections section](http://directory.google.com/Top/Comhttp://directory.google.com/Top/Computers/Software/Fonts/Coputers/Software/Fonts/Collections/) na Google Web Direktorijumu.

Stranica sa fontovima na [GIMP.org](http://www.gimp.org/http://www.gimp.org/fonts.html) prikazuje  
pakete koji su korisni za GIMP. Ako vas nerviraju dosadne greške tipa script-fu  
errors zbog nedostaju?ih fontova, onda je ovo pravo mesto za vas!

[Freshmeat](http://freshmeat.net/search/?query=font) lista font  
paketa i aplikcija za fontove.

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=198)