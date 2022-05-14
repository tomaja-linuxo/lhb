---
author: tomaja
date: "2002-05-27T15:47:23Z"
excerpt: |
  <p>- Instaliranje Windows fontova preko Drak fonta<br />
  - Neispravan &quot;CheckInstall&quot; RPM<br />
  - Uklonite startni &quot;Bootup&quot; ekran<br />
  - Shift-Insert više ne radi u konzoli (KDE3)
guid: https://forum.linuxo.org/2002/05/27/par-trikova-mandrake-linux-8-2/
id: 181
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Par trikova &#8211; Mandrake Linux 8.2
url: /par-trikova-mandrake-linux-8-2/
---
&#8211; Instaliranje Windows fontova preko Drak fonta  
&#8211; Neispravan "CheckInstall" RPM  
&#8211; Uklonite startni "Bootup" ekran  
&#8211; Shift-Insert više ne radi u konzoli (KDE3) <!--break-->



### <a id="fonts" name="fonts">Instaliranje Windows Fontova preko Drak Fonta </a>

Problem:

Iako ste instalirali fontove iz fonts diretorijuma vašeg MS Windows-a, programi ili ih ne vide ili se čudno ponašaju kada ih koristite.

Razlog:

Fontovi su instalirani sa progrešnim dozvolama (permissions) i 'fonts.dir' fajl je prazan.

Rešenje:

Otvorite terminal i otiđite u direktorijum sa fontovima (kao 'root'):

<kbd>cd /usr/X11R6/lib/X11/fonts/drakfont/ttf/</kbd>

Pokrenite:

<kbd>chmod 644 *.ttf</kbd>

kao i

<kbd>mkfontdir</kbd>

Restartujte font server sa naredbom

<kbd>service xfs restart</kbd>

<p class="smallright">
  <a href="http://mandrake.osny.org.yu/html/modules.php?name=News&file=article&sid=12#top">na vrh</a>
</p>

### <a id="check" name="check">Neispravan 'CheckInstall' RPM </a>

Problem:

Pokretanje 'checkinstall' neuspeva i pojavljuje se poruka: <samp>script not installed</samp>

Razlog:

loše kreiran paket.

Rešenje:

RPM sa [CheckInstall web sajta](http://asic-linux.com.mx/%7Eizto/checkinstall/download.php) radi kako treba.

<p class="smallright">
  <a href="http://mandrake.osny.org.yu/html/modules.php?name=News&file=article&sid=12#top">na vrh</a>
</p>

### <a id="splash" name="splash">Uklonite Startni (Bootup) Ekran</a>

Problem:

Ne sviđa vam se novi startni ekran.

Rešenje:

Uklonite nasrtljivca kao 'root' sa komandom:

<kbd>urpme bootsplash</kbd>

<p class="smallright">
  <a href="http://mandrake.osny.org.yu/html/modules.php?name=News&file=article&sid=12#top">na vrh</a>
</p>

### <a id="konsole" name="konsole">Shift-Insert više ne radi u konzoli (KDE3)</a>

Problem:

Više ne možete da ubacite tekst iz druge aplikacije u konzolu korištenjem <kbd><shift ins="">tastera</shift></kbd>.

<shift ins="">

Razlog:

Ovo nije bag, već opcija :-). Standardna "shortcut" kombinacija tastera za ubacivanje iz sistemskog clipboard-a se promenila i sada je <kbd><ctrl ins="" shift=""></ctrl></kbd>.

<ctrl ins="" shift="">

Rešenje:

Da bi mogli da koristite stari raspored tastera morate izmeniti '/opt/kde3/share/apps/konsole/linux.keytab'. Promenite

`key Insert+Shift -Control : emitClipboard<br />
key Insert+Shift +Control : emitSelection`

u

`key Insert+Shift +Control : emitClipboard<br />
key Insert+Shift -Control : emitSelection`

<p class="smallright">
  <a href="http://mandrake.osny.org.yu/html/modules.php?name=News&file=article&sid=12#top">na vrh</a>
</p>

### <a id="usb" name="usb">USB Ulazni uređaji se blokiraju prilikom instalacije</a>

Problem:

Tokom instalacije, USB ulazni uređaji (miš, tasatura) iznenada prestaju da rade (obično tokom ili nakon instalacije paketa).

Razlog:

NIje poznat, verovatno se radi o problemu u instalacionom kernelu (ovi uređaji obično rade sasvim dobro nakon instalacije).

Rešenje:

Koristi USB-to-PS/2 adapter tokom instalacije.

<p class="smallright">
  <a href="http://mandrake.osny.org.yu/html/modules.php?name=News&file=article&sid=12#top">na vrh</a>
</p>

<p class="smallright">
  <font color="#999999"><small>Izvor: MUO</small> <small>2002 god</small></font>
</p>

</ctrl></shift>

&nbsp;

&nbsp;

&nbsp;

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=181)