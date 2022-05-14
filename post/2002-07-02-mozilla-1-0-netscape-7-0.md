---
author: tomaja
date: "2002-07-02T17:10:31Z"
excerpt: |
  U ovom tekstu je opisan postupak podešavanja Mozille (i onih koje ne možete<br>
  direktno podesiti iz same Mozille) , nove funkcije,podešavanje iz komandne<br>
  linije, instalacija i podešavanje skinova (tema),  nove mogu?nosti  pretraživanja<br>
  sa mišem i tastaturom. Ovde možete prona?i i najbolje plugine za Mozillu
  sa <br>
  kra?im opisom kao i postupkom instalacije.<br>
  Dat je i spisak Web browsera koji su bazirani na Mozilli (Netscape, Galeon,...)<br>
guid: https://forum.linuxo.org/2002/07/02/mozilla-1-0-netscape-7-0/
id: 193
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Mozilla 1.0  (Netscape 7.0)
url: /mozilla-1-0-netscape-7-0/
---
U ovom tekstu je opisan postupak podešavanja Mozille (i onih koje ne možete  
direktno podesiti iz same Mozille) , nove funkcije,podešavanje iz komandne  
linije, instalacija i podešavanje skinova (tema), nove mogu?nosti pretraživanja  
sa mišem i tastaturom. Ovde možete prona?i i najbolje plugine za Mozillu  
sa  
kra?im opisom kao i postupkom instalacije.  
Dat je i spisak Web browsera koji su bazirani na Mozilli (Netscape, Galeon,&#8230;)  
<!--break-->

Ovaj tekst se može primenjivati na Mozilla 1.0 i Netscape 7 web browsere.  
Mozilla 1.0 (RPM paketi) za Mandrake Linux 8.2 se može skinuti [ovde](http://www.mandrakeuser.org/download.php) ili sa nekog Mandrake  
Linux FTP mirror-a a nalazi se i na  
Micro CD (06/2002).

### <a id="prefs" name="prefs">Ru?no podešavanje opcija </a>

Mozilla ima previše opcija da bi sve mogle da se prikažu u grafi?kom &#8216;Preferences&#8217;  
korisni?kom interefejsu.  
Da bi mogli da opcije podesite ru?no morate da kreirate fajl sa imenom &#8216;user.js&#8217;  
u svom Mozilla profile direktorijumu. Taj direktorijum se obi?no nalazi u  
&#8216;~/.mozilla/default&#8217; ukoliko nema instaliranih profila. U tom direktorijumu  
treba da se nalazi &#8216;prefs.js&#8217; fajl pa ne možete pogrešiti.

Da bi izmene u &#8216;user.js&#8217; fajlu mogle imati uticaja, mora?ete da zatvorite  
i restartujete Mozillu. Možete primetiti da se izmene u &#8216;user.js&#8217; upisuju  
u &#8216;pref.js&#8217;. Pa, ukoliko želite da se vratite na staru postavku možete kreirati  
backup &#8216;pref.js&#8217; fajla pre unošenja bilo ?ega u &#8216;user.js&#8217; ili ponovnom izmenom  
opcija i u &#8216;user.js&#8217; __i &#8216;pref.js&#8217; fajlu.

Ovde se prikazane neke opcije a više njih možete na?i na [Pratik Solanki&#8217;s Prefs sajtu](http://www.geocities.com/pratiksolanki/)  
kao i na [Customizing  
Mozilla](http://www.mozilla.org/unix/customizing.html) na Mozilla.org.

#### Promena Download Menadžera

Novi download menadžer nije možda odgovaraju?i baš za svakoga. Umesto  
njega možete koristiti stari download box ili isklju?iti download popup prozore  
kompletno i selektovati download status preko &#8216;Tools&#8217; &#8211; &#8216;DownloadManager&#8217;.

`user_pref("browser.downloadmanager.behavior", 0);`

aktivira novi download menadžer (default postavka).

`user_pref("browser.downloadmanager.behavior", 1);`

aktivira stari odvojeni download box.

`user_pref("browser.downloadmanager.behavior", 2);`

isklju?uje download prozore kompletno.

#### Dekativiranje Print Progress dijaloga

`user_pref("print.show_print_progress", false);`

#### Deaktiviranje &#8222;left mouse button auto-copy to clipboard&#8220; opcije

`user_pref("clipboard.autocopy", false);`

#### Deaktiviranje srednjeg tastera na mišu za paste

`user_pref("middlemouse.paste", false); user_pref("middlemouse.contentLoadURL",<br />
false); user_pref("middlemouse.scrollbarPosition", false);`

#### Deaktiviranje popup prozora za odreÄ‘enje domene

`user_pref("capability.policy.popupsites.sites", "http:// www.annoyingsite1.com<br />
http://www.popupsite2.com"); user_pref("capability.policy.popupsites.Window.open",<br />
"noAccess");`

#### Deaktiviranje JavaScript popup prozora

Korisnici Mozilla web pretraživa?a ovo mogu podesiti preko &#8216;Edit&#8217; &#8211; &#8216;Preferences&#8217;  
&#8211; &#8216;Advanced&#8217; &#8211; &#8216;Scripts & Windows&#8217; (deselektuj &#8216;Open unrequested windows&#8217;).  
Ova opcija nedostaje AOL-ovom &#8216;Netscape&#8217;-u pa zahteva ru?no podešavanje:

`user_pref("dom.disable_open_during_load", true);`

Još neki zanimljive opcije za korisnike Netscape-a

`user_pref("imageblocker.enable", true);`

što omogu?ava blokiranje slika (default u Mozilli).

#### Deaktiviranje blinkaju?eg teksta

`user_pref("browser.blink_allowed", false);`

#### Font banning

Može biti korisno ako je instaliran AbiWord (Arial font bug):

`user_pref("font.x11.rejectfontpattern", "fname=.*arial.*");`

#### Rešavanje problema sa history prozorom

Mozilla 1.0 ima jedan prili?no ?udan bag: klikom na history prozor ?ete  
naterati browser da traži adresu &#8216;www.apps5.oingo.com&#8217;. Ovo možete spre?iti  
isklju?ivanjem pogaÄ‘anja domena.

`user_pref("browser.fixup.alternate.enabled", false);`

#### Isklju?ivanje animacije na titlebar-u

Iako ne znam kome bi ovo moglo da smeta evo kako da ovu animaciju zaustavite:

`user_pref("capability.principal.default.Windows.title.set", "noAccess");`

<p class="smallright">
  <a href="https://linuxo.org/?p=4#top">na po?etak</a>
</p>

### <a id="skins" name="skins">Mozilla Skinovi</a>

Preko &#8216;View&#8217; &#8211; &#8216;Apply Themes&#8217; &#8211; &#8216;New Themes&#8217; možete skinuti i instalirati  
move Mozilla teme (skinove) ili sa [themes.mozdev.org](http://themes.mozdev.org/)  
ili sa [DeskMod](http://mozilla.deskmod.com/?show=showcat&cat_name=mozilla).  
Trebali bi da posetite ova sajta jer zaista možete prona?i prili?no dobre  
i jedinstvene skonove kao što je [LittleMozilla](http://mozilla.deskmod.com/?state=view&skin_id=11431).  
  
Instalacija se uglavnom sastoji u tome da kiliknete na link, restarujete  
Mozillu, izaberete novu temu i opet restartujete Mozillu. 

Skinovi su pisani u [XUL](http://www.mozilla.org/xpfe/xptoolkit/xulintro.html)-u, Mozillinom  
XML-baziranom jeziku, što zna?i da možete da izmenite teme po svojim afinitetima.  
Da bi ovo uradili kreirajte fajl pod imenom &#8216;userChrome.css&#8217; u &#8216;chrome&#8217; direktorijumu  
&#8216;~/.mozilla/default/<var>xx</var>.slt&#8217;.  
Ove linije na primer uklanjaju tekst ispod toolbar tastera (kao što je  
slu?aj u &#8216;Classic&#8217; skinu):

    .toolbarbutton-menubutton-button > .toolbarbutton-text,<br>.toolbarbutton-1 > .toolbarbutton-text<br>{<br>    display: none !important;<br>}<br>  
    

Da bi se rešili animirane slike sa desne strane polja za adrese:

    #throbber-box<br>{<br>    display: none !important;<br>}<br>  
    

Podešavanje veli?ine i tipa fonta dialog prozore:

    window {<br>  font-size: 3.5mm !important;<br>  font-family: helvetica !important;<br>}<br>  
    

Podešavanje veli?ine, tipa fonta kao i boje pozadine za polja za unos  
teksta (sa jednom linijom):

    input {<br>  font-family: clean !important;<br>  font-size: 13px !important;<br>  background-color: rgb(200, 255, 220) !important;<br>}<br>  
    

Ovo takože funkcioniše i za polja sa više linija. Zamenite `input`  
sa `textarea`.

Ako sami želite da kreirate teme (skinove) za Mozillu onda skinite [Chameleon](http://chameleon.mozdev.org/), grafi?ki kreator tema.

<p class="smallright">
  <a href="https://linuxo.org/?p=4#top">na po?etak</a>
</p>

### <a id="mozgest" name="mozgest">Operacije sa mišem</a>

Operacije sa mišem vam omogu?avaju da pobudite pretraživa? na radnju (vra?anje  
na prethosnu stranu, zatvraranje prozora, otvaranje novog itd) sa predefinisanim  
pokretima miša. 

[Optimoz projekat](http://optimoz.mozdev.org/gestures/index.html)  
omogu?ava ove oeracije sa mišem u Mozilli i ?ak bolje implementira ovo i  
od Opere jer možete i sami da podesite svoje pokrete, definišete koji taster  
na mišu ?ete koristiti za pokrete i dr..

Da bi instalirali Optimoz add-on,

  1. zatvorite sve otovrene delove Mozille i pokrenite novu kao &#8216;root&#8217;  
    (na primer iz terminala).

  2. OtiÄ‘ite na [Optimoz installation  
    page](http://optimoz.mozdev.org/gestures/installation.html) i kliknite na &#8216;installation&#8217; link. Pratite tok instalacije.

  3. Kada se instalacija završi, zatvorite browser. U terminalu kao &#8216;root&#8217;  
    pokrenite komandu:
    
    <kbd>chmod -R o+r /usr/lib/mozilla/chrome/mozgest/</kbd>
    
    Ova komanda omogu?uje i non-root korisnicima da koriste ovan add-on.

  4. Pokrenite Mozillu i otvorite &#8216;Edit&#8217; &#8211; &#8216;Preferences&#8217; &#8211; &#8216;Advanced&#8217; &#8211;  
    &#8216;Mouse Gestures&#8217; (nije neophodno jer default postavka radi dobro).

Po default-u, Optimoz koristi levi taster miša (mouse taster 1) za pokrete.  
Vi možete za to da postavite i srednji i desni taster.

Svi ovi tasteri ina?e ve? imaju svoju funkciju kada se pritisnu (levi  
markira tekst, srednji ima funkviju umetanja teksta, desni otvara context  
meni), pa ukoliko želite da koristite ove funkcije a ne pokrete, zaustavite  
kretanje miša pre otpuštanja tastera__. Ovo ?e re?i Optimozu da ne  
protuma?i ovo kao pokret. 

<p class="smallright">
  <a href="https://linuxo.org/?p=4#top">na po?etak</a>
</p>

### <a id="key"
 name="key">Tastatura u Mozilli</a>

Kompletnu listu [Mozilla keyboard  
shortcut-ova](http://www.mozilla.org/docs/end-user/moz_shortcuts.html) možete na?i na Mozilla.org web sajtu.

Po defaultu, Mozilla koristi <kbd><CTRL></kbd> taster kao &#8216;primarni  
akcelerator&#8217; a <kbd><ALT></kbd> za pristup menijima. U Mozilli, &#8217;17&#8217;  
je umesto <kbd><CTRL></kbd>, 18 za <kbd><ALT></kbd>, 224 za <kbd>

<META />
</kbd>
  
( &#8216;Windows tasteri&#8217; [ako su tako  
konfigurisani](http://www.mandrakeuser.org/docs/xwin/xkeys2.html#Wkey){.int}) i &#8216;0&#8217; za &#8216;off&#8217;. Ove brojeve možete koristiti za izmenu  
tastera.

`user_pref("ui.key.accelKey", 18);<br />
 user_pref("ui.key.menuAccessKey", 17);`

menja <kbd><ALT></kbd> za &#8216;primarni akcelerator&#8217; a meniji su sada  
dostupni preko <kbd><CTRL <var>letter</var>> tastera</kbd>.

TakoÄ‘e možete podesiti [custom tastere](http://www.mozilla.org/unix/customizing.html#key_example)  
.

Postoji i specijalna opcija vezana za tastere u Mozilli a to je &#8216;caret  
browsing&#8217;.  
Pritiskom na <kbd><F7></kbd> aktivirate tekst kursor koji vam omogu?ava  
da markirate tekst preko tastature korite?i <kbd><SHIFT></kbd> i tastere  
sa strelicama, da se kre?ete po stranicama i pozovete odreÄ‘eni URL koriste?i  
<kbd><ENTER></kbd>.

<p class="smallright">
  <a href="https://linuxo.org/?p=4#top">na po?etak</a>
</p>

### <a id="remote" name="remote">Udaljeno upravljanje Mozille</a>

Kao i njegovog predhodnika Netscape 4.x , i Mozillu možete da kontrolišete  
preko komandne linije:

<kbd>mozilla -remote "openurl(<var>URL</var>)"</kbd>

Ovaj primer ?e otvoriti novi tab u ve? pokrenutoj Mozilli sa nekim <var>URL-om</var>.  
Ukoliko nije pokrenuta, sada se startuje sa istim URL-om. Ukoliko preferirate  
novi prozor umesto tab-a onda ukucajte

<kbd>mozilla -remote "openurl(<var>URL</var>, new-window)"</kbd>

Ukoliko ne želite da unostite URl u komandnoj liniji ve? direktno u Mozilli  
ukucajte:

<p class="smallright">
  <kbd>mozilla -remote "openurl()"</kbd>
</p>

<p class="smallright">
  <a href="https://linuxo.org/?p=4#top">na po?etak<br /> </a>
</p>

### <a id="add" name="add">Mozilla Add-on (dodaci iliti plug-in)</a>

Mozilla se isporu?uje sa nekoliko add-ona:

  * amail / news agentom (Mozilla Messenger / News)
  * IRC cklijentom ([Chatzilla](http://www.mozilla.org/projects/rt-messaging/chatzilla/))
  * i emulatorrom terminala ([xmlterm](http://www.xmlterm.com/))

Mežutim postoji preko [70  
drugih Mozilla projekata](http://www.mozdev.org/projects.html) a mi ?emo ovde upoznati samo neke.

Ovi projekti se obi?no distribuiraju u tzv. XPI (cross-platform installation)  
arhivama (ove se arhive mogu raspakovati pomo?u &#8216;unzip&#8217; komande). Instalacija  
ovih arhiva zahteva Mozilla sa &#8216;root&#8217; privilegijama.  
Ve?ina ovih dodataka ne obezbeÄ‘uje deinstalaciju. Da bi ih deinstalirali,  
morate izmeniti &#8216;/usr/lib/mozilla/chrome/chrome.rdf&#8217;, &#8216;/usr/lib/mozilla/chrome/overlayinfo/navigator/content/overlays.rdf&#8217;  
i možda &#8216;/usr/lib/mozilla/chrome/overlayinfo/communicator/content/overlays.rdf&#8217;  
kao &#8216;root&#8217; i ukloniti odgovaraju?e linije ([primer](http://easysearch.mozdev.org/installation.html)), a onda  
i ukloniti njihove fajloves.

#### Dodavanje Banner blokera

[Banner Blind](http://bannerblind.mozdev.org/) je bloker banera  
za Mozillu koji blokira slike bazirano na njihovoj veli?ini. Set predefinisanih  
veli?ina je obezbeÄ‘en a i custom veli?ine se mogu podešavati.

Instalacija se izvodi klikom na [instalacionu stranicu](http://bannerblind.mozdev.org/installation.html).  
Restartujete browser i podesite Banner Blind preko menija &#8216;Tools&#8217; &#8211; &#8216;BannerBlind&#8217;.

#### Pretraživanje je brže pomo?u EasySearch-a

[EasySearch](http://easysearch.mozdev.org/index.html) ubacuje  
&#8216;Search&#8217; meni u personalni toolbar.

Instalirajte EasySearch sa [instalacione stranice](http://easysearch.mozdev.org/installation.html).  
Zatvorite browser. Kao &#8216;root&#8217;, pokrenite

<kbd>chmod o+r /usr/lib/mozilla/chrome/easysearch.jar</kbd>

Startujte Mozillu i polje za pretraživanje bi trebalo da se pojavi u Personalnom  
Toolbaru (možda ?ete morati da aktivirate toolbar preko &#8216;View&#8217; &#8211; &#8216;Show/Hide&#8217;).  
EasySearch se može podešavati preko &#8216;Edit&#8217; &#8211; &#8216;Preferences&#8217; &#8211; &#8216;Advanced&#8217;  
&#8211; &#8216;EasySearch&#8217;.

#### Dodajte &#8216;Google toolbar&#8217; u Mozillu

[Googlebar](http://googlebar.mozdev.org/) emulira Google-ov  
[toolbar](http://toolbar.google.com/) za MSIE.

Instalirajte Googlebar sa [download stranice](http://googlebar.mozdev.org/installation.html).  
Zatvorite Mozillu. Iz terminala, kao &#8216;root&#8217; ukucajte:

<kbd>chmod -R o+r /usr/lib/mozilla/chrome/googlebar/content/</kbd>

da bi omogu?ili i ostalim user-ima a ne samo &#8216;root&#8217;-u da prikaže bar.  
Desnim klikom na prazan prostor n novom &#8216;Googlebar&#8217;-u mo?i ?ete da ga bolje  
podesite.

#### Enkriptovanje mail-a preko Enigmail

[Enigmail](http://enigmail.mozdev.org/) interfejs sa Mozilla  
mail klijentom sa [GPG](http://www.mandrakeuser.org/docs/secure/sgpg.html){.int} ili PGP  
softverom za enkripciju.

Instalaciaj i podešavanje je nešto komplikovanije pa za detalj  
e pogledajte  
[Enigmail Help Information](http://enigmail.mozdev.org/help.html)  
.

#### Pretažite više 

[Mycroft](http://mycroft.mozdev.org/) je kolekcija velikog  
broja search plugin-a za Mozillin &#8216;search&#8217; . Ovi plugin-ovi vam omogu?avaju  
pretražujte lokacije kao što su ebay, CPAN, RPM Find, SourceForge, Xrefer,  
Slashdot, Google Groups kao i mnoge druge.

OtiÄ‘ite na [download  
stranicu](http://mycroft.mozdev.org/download.html). Ili izaberite koje ?ete plugin-ine instalirati ili skinite  
[kompletnu arhivu](http://mycroft.mozdev.org/plugins/allplugins.tar.gz)  
i respakujte je kao &#8216;root&#8217; u &#8216;/usr/lib/mozilla/searchplugins/&#8217; direktorijum.

Ukoliko ve? imate instaliran &#8216;EasySearch&#8217; add-on, mo?i ?ete da pristupite  
novim plugin-ima sa personalnog toolbara. Ako net, selektujte &#8216;Edit&#8217; &#8211; &#8216;Preferences&#8217;  
&#8211; &#8216;Navigator&#8217; &#8211; &#8216;Internet Search&#8217; &#8211; &#8216;Advanced&#8217; i otvorite search tab u sidebaru.  
Koristite padaju?i meni da bi izabrali sa kojim sajtom Ä‘elite da pretražujete.

Da bi kreirali svoj search plugin, pro?itajte [The Search  
for Mozilla](http://www.mozilla.org/projects/search/technical.html) i pogledajte malo &#8216;.src&#8217; fajlove u &#8216;/usr/lib/mozilla/searchplugins/&#8217;.

#### 

#### Mozilla na našem jeziku

Ako Engleski nije (a nije) naš maternji jezik možete skinuti &#8216;language  
packs&#8217; sa [Mozilla  
Localization Project](http://www.mozilla.org/projects/l10n/mlp_status.html) sajta.

<p class="smallright">
  <a href="https://linuxo.org/?p=4#top">na po?etak</a>
</p>

<p class="smallright">
  <a href="file:///home/toma/tmp/umoz2.html#top"></a>
</p>

### <a id="options" name="options">Opcije u komandnoj liniji</a>

IzmeÄ‘u ostalih, interesantne komande su

  * Veli?ina prozora: <kbd>-height <var>xx</var> -width <var>yy</var></kbd>  
    startuje Mozillu u prozoru <var>xx</var> piksela visokom i <var>yy</var>  
    pikselas širokom.
  * UreÄ‘ivanje profila: Koritite <kbd>-ProfileWizard</kbd> ili <kbd>-ProfileManager</kbd>  
    za editovanje ili / kreiranje novog profila. <kbd>-P <var>profile</var></kbd>  
    s pokre?e Mozillu sa sa profilom <var>profile</var> i <kbd>-SelectProfile</kbd>  
    izbacuje prozor za selekciju. Ne zaboravite da možete da kreirate [Zajedni?ki Netscape  
    Profil za Linux i Windows](http://sillydog.org/netscape/kb/linuxwindows.html).
  * Pokretanje komponenti: <kbd>-addressbook</kbd>, <kbd>-news</kbd>, <kbd>-mail</kbd>,  
    <kbd>-edit</kbd>.  
    <kbd>-compose</kbd> pokre?e &#8216;compose new mail&#8217; prozor <kbd>-chrome <var>path</var></kbd>  
    pokre?e Mozillu sa skinom koji se nalazi u <var>path</var>.

<p class="smallright">
  <a href="file:///home/toma/tmp/umoz2.html#top">na po?etak</a>
</p>

### <a id="gecko" name="gecko">Web browseri bazirani na Mozilli</a>

#### Cross Platforme

Slede?e platforme koriste NGLayout i XPFE:

  * [Netscape](http://wp.netscape.com/products/index.html)  
    jeste ustvari Mozilla, zahvaljuju?i AOL/TimeWarner (koji sponzoriše razvoj  
    Mozille). On nudi add-one (kao što su integrisani AIM i ICQ klijent) kao  
    i neka manja poboljšanja Mozille. Netscape 6.2 je baziran na Mozilli 0.94,  
    Netscape 7 na Mozilli 1.0.

  * [Beonex Communicator](http://www.beonex.com/communicator/)  
    pokušava da obezbedi unapreÄ‘enje Netscape-a bez dodataka. Verzija 0.8 je  
    bazirana na Mozilli 1.0 i dostupna je za Linux i MS Windows.

#### Single Platforme (Linux)

  * [Galeon](http://galeon.sourceforge.net/) je najpopularniji  
    i unapreÄ‘eni browser koji ima implementiran Mozillin NGLayout. Oni su zamenili  
    XPFE  
    sa jednako popularnim GTK+ widget setom. Galeon zahteva GNOME desktop  
    da bi se mogao instalirati, ali ga možete pokrenuti iz bilo kog window menadžera  
    / desktop okruženja (npr. KDE). Mandrake Linux paket: galeon.

  * [Skipstone](http://www.muhri.net/skipstone/) takoÄ‘e koristi  
    GTK+, ali je uglavnom vezan za osnovne browsing mogu?nosti. Mandrake Linux  
    paket: skipstone.

  * &#8216;Nautilus&#8217;, GNOME-ov fajl menadžerr, uklju?uje NGLayout da bi posedovao  
    neke funkcije pretraživa?a.

#### Single Platform (ostali)

  * [K-Meleon](http://kmeleon.sourceforge.net/) se deklariše  
    ako &#8216;razotkrivena Mozilla za Windows&#8217;.

  * [Chimera](http://chimera.mozdev.org/) koristi NGLayout  
    i Cocoa, osnovni Mac OS X grafi?ki toolkit.

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=193)