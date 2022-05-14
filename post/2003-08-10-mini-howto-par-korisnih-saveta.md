---
author: tomaja
date: "2003-08-10T06:08:21Z"
excerpt: |
  Ovim tekstom sam želeo da pomognem svima koji prelaze ili pokušavaju da preÄ‘u sa WIndows-a na Linux ili su to ve? uradili ali neke stvari još nisu jasne. Radi se o konkretnim pitanjima i odgovorima jer se takav metod pokazao kao najbolji.
  Ovde ?ete na?i odgovore o tome kako da podesite KDE, podeiste XFree , pokrenete više grafi?kih okruženja istovremeno, pustite DVD pomo?u programa Xine, itd.</br>
  ?itajte dalje...
guid: https://forum.linuxo.org/2003/08/10/mini-howto-par-korisnih-saveta/
id: 367
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Mini HOWTO &#8211; par korisnih saveta
url: /mini-howto-par-korisnih-saveta/
---
Ovim tekstom sam želeo da pomognem svima koji prelaze ili pokušavaju da preÄ‘u sa WIndows-a na Linux ili su to ve? uradili ali neke stvari još nisu jasne. Radi se o konkretnim pitanjima i odgovorima jer se takav metod pokazao kao najbolji.  
Ovde ?ete na?i odgovore o tome kako da podesite KDE, podeiste XFree , pokrenete više grafi?kih okruženja istovremeno, pustite DVD pomo?u programa Xine, itd.</br>  
?itajte dalje&#8230;<!--break-->

<p align="left">
  <font size="+1"><b>Nekoliko korisnih Linux saveta (kada<br /> prelazite sa Windows-a na Linux 🙂<br /> </b></font>
</p>

<a name="terms"></a>**_Termini u tekstu:_**  
cli : interfejs komande linije, &#8216;nalik dos promptu&#8217;  
mcc: mandrake kontrolni centar (možete mu pristupiti preko desktop  
ikone, ili start menija)  
kB, KB, K: kilobajt  
kb: kilobit  
kde, KDE: K Desktop Okruženje  
kdecc: kde control center (start menu, control center)  
Start meni, start taster: taster u obliku&#8217;to?ki?a&#8217; sa slovom K na  
njemu, obi?no na levoj strani taskbara. Meni se pojavljuje kada kliknete  
levim tasterom miša na njega.  
OS: operativni sistem.  
OSS: softver otvorenog koda.  
`<font color="darkgreen" style="color: rgb(255, 255, 0);">comande<br />
koje treba da ukucate imaju ovu boju</font><br />
<font color="darkred">tasteri koje treba da pritisnete imaju ovu boju</font><br />
ltm = levi taster miša, stm = srednji taster miša, dtm = desni taster<br />
miša` 

<a name="mdkde"></a>**_Kako da koristim Mandrake Linux i KDE,  
koji programi mogu da koristim i za šta?_**  
Ovde možete videti mali izbor programa koje i ja sam koristim:  
za Web (internet pretraživa?): `mozilla, koqueror, opera`  
(koju morate skunuti sa neta ili sa neke od naših Linux kompilacija )`,<br />
galeon`  
za elektronsku poštu (Mail): `evolution` , `KMail,<br />
mozilla mail, opera mail`  
Muzi?ki/audio plejeri: `xmms, noatun`  
Audio mikseri: `kmix` , `alsamixer-gui`  
Video plejeri (DVD, DivX, itd.) : `mplayer, xine` (ima ih  
naravno još, ali su ova dva možda i najkompletniji)  
Narezivanje CDa: `k3b,cdbakeoven, gcombust` (podaci, audio,  
iso), `gcdmaster` (potreban mu je instaliran cdrdao) da bi  
pripremili wav-fajlove i napravili audio cd recimo bez pauza izmeÄ‘u  
pesama.  
Audio editovanje: `glame, audacity (i mali milion drugih programa)<br />
Office paketi: OpenOffice, KOffice<br />
` Ukoliko vam treba širi spisak programa pogledajte tekst <http://www.mandrake.co.yu/modules.php?name=News&file=article&sid=160&mode=&order=0&thold=0>  
u kom možete prona?i tabelu sa odgovaraju?im programima za  
Windows i i Linux.

<a name="kdewin"></a>**_Kako da optimizujem ponašanje KDE  
prozora_**  
Slede?e je za mene idealno podešavanje KDEa, istovremeno i ono  
što se ne može posti?i na Windows-u, a samo delimi?no na HP-UX/CDE  
(ili VUE).  
Ovo nisam uspeo da postignem na gnome2, što mi je žao jer je sada  
gotovo u potpunosti lokalizovan na srpski, ali se nadam nekoj slede?oj  
verziji. U svakom slu?aju, ako je neko uspeo ovo da uradi sa  
Gnometom, neka javi. Ja želim da selektujem stvari u prozoru koji nije  
aktivan, i prenesem ih opet u prozor koji nije aktivan. I želim da  
trenutni aktivni prozor to i ostane.  
KDEcc, izgled, ponašanje prozora (možete mu pristupiti ako kliknete  
desnim tasterom miša na gornju levu ikonicu bilo kog prozora). Postoje 4  
tabam prvi je &#8216;fokus&#8217; &#8212; izaberite : fokus prati kursor, a  
deselektujte &#8216;auto raise&#8217;. Slede?i tab: &#8216;akcije&#8217; &#8212; izberite bilo  
koju funkciju recimo za &#8216;inactive inner window&#8217; opcija &#8216;activate and  
pass click&#8217;. Ne zaboravite da snimite izmene klikon na taster apply  
ili (primeni).  
TakoÄ‘e, sada možete da definišete kako da spustite/podignete/pomerite  
ili promenite veli?inu prozora; meni odgovara alt-taster kao izmenjiva?,  
i alt+levi , alt+srednji: toggle raise lower, alt+desni: . Još jedna  
lepa mogu?nost je &#8216;senka&#8217; pri dvostrukom kliku na title bar. U tabu  
Napredno (advanced tab), možete izabrati &#8216;omogu?i hoover&#8217; kao i  
vremeski period za ovu opciju. Zatim možete da postavljate prozore u  
pozadinu, a ukoliko postavite kursor miša na traku sa naslovom  
(koja je i jedini vidljivi deo), prozor se otvara nakon što proÄ‘e  
izabrani vremenski period.  
. 

<a name="ghost"></a>**_Kako da koristim Linux da bi napravio  
backup mojih windows sistemskih particija, umesto ghost image-a._**  
Ukoliko imate dovoljno mesta na disku, slobodno jednostavno  
prekopirajte sve fajlove. Ovo vam ne?e uštedeti prostor jer fajlovi nisu  
kompresovani.  
Ovo možete uraditi preko nekog fajl menadžera ili iz komandne linije:  
cp /mnt/win_c (ili drugi direktorijum, odnosno onaj gde vam je  
montirana windows c particija) /putanja/gde/želite/da/napravite/backup  
(proverite da li imate dovoljno prostora na toj particiji).  
Da bi znali da li imate dovoljno prostora na particiji pokrenite u  
konzoli  
<code style="color: rgb(255, 255, 0);">df -h | grep /win</code>  
i sistem ?e vam re?i koliko je veli?ina svih fajlova na windows  
particijama. Zatim možete proveriti da li imate dovoljno mesta:  
 <span style="color: rgb(255, 255, 0);">df -h</span>  
Ukoliko želite da kreirate jedan, kompresovan fajl možete da  
iskoristite jedan od programa za arhiviranje (iz menija) koji dolaze uz  
Mandrake.  
Da bi vratili podatke iz backup kopije, jesdnostavno uklonite sve sa  
windows c-ureÄ‘aja/particije i prekopirajte fajlove nazad, ili upotrebite  
program za arhiviranje da bi raspakovali fajlove na isto mesto. Ono što  
je važno jeste da ukoliko želite da sa?uvate datume fajlova morate  
koristiti metod sa kompresovanjem jer cp naredba ih ne?e o?uvati .  
(Na drugim fajl sistemima, kao što su linux ext2 ili 3 ovo možete  
uraditi pomo?u naredbe: cp -p \[fajl\] \[novi fajl\] ) 

<a name="dvd"></a>**_Kako da koristim xine za puštanje dvd  
diskova_**  
ovde samo nekoliko napomena, jer je sve prili?no o?igledno. Proverite  
da je sistem pronašao dvd ureÄ‘aj, jer bi Mandrake ovo trebao automatski  
da uradi. Proverite sa  
<code style="color: rgb(255, 255, 0);">ls -l /dev/dvd</code>  
i ukoliko vam izbaci nešto kao:  
<code style="color: rgb(255, 255, 0);">lr-xr-xr-x    1 root     root 30&lt;br />
Dec  1 13:10 /dev/dvd -> ide/host0/bus1/target1/lun0/cd</code>  
onda je sve u redu. Ukoliko vam izbaci nešto kao  
<code style="color: rgb(255, 255, 0);">ls: /dev/dvd: No such file or&lt;br />
directory</code>  
mora?ete da se uogujete kao root, (komanda: `<font
 color="darkgreen">su</font>` nakon koje unosite root lozinku) i  
pokrenete slede?u naredbu:  
<code style="color: rgb(255, 255, 0);">ln -s /dev/hdd /dev/dvd</code>  
ukoliko je vaš dvd sekundarni ureÄ‘aj na drugom ide kontroleru.Ovo  
naravon promenite ako ovo nije slu?aj na hdc, hdb,&#8230; promenite hdd u  
hdb ukoliko se ureÄ‘aj nalazi koa sekunradni na primarnom kontroleru a  
hdc ukoliko je primarni ureÄ‘aj na sekundarnom kontroleru. Ukoliko ne  
znate gde je priklju?e vaš dvd, ne morate da otvarate ku?ište. Ako ste  
još uvek ulogovani kao root (superuser/admin), ukucajte i pokrenite:  
<code style="color: rgb(255, 255, 0);">cat /var/log/dmesg | grep -A 4&lt;br />
hda</code>  
Ovo bi trebalo da pokaže (izmeÄ‘u ostalog) pozicije vaših ureÄ‘aja (na  
primer)  
<code style="color: rgb(255, 255, 0);">hda: MAXTOR 6L060J3, ATA DISK&lt;br />
drive hdc: PCRW1208, ATAPI CD/DVD-ROM drive hdd: Pioneer DVD-ROM&lt;br />
ATAPIModel DVD-105S 013, ATAPI CD/DVD-ROM drive</code>  
(napomena, ukoliko imate jedan hard disk, cd reza? i dvd plejer ovo je  
preporu?ena konfiguracija)  
U slu?aju problema, pokrenite xine iz komndne linije, da bi mogli da  
vidite u ?emu je problem. TAkoÄ‘e, proverite da li imate instalirane `libdvdcss2,<br />
xine-ui, xine-dvdnav` pakete.  
Kada se pojavi xine, ubacite dvd u dvd-rom ureÄ‘aj i kliknite na dvd  
taster, dvd ?e se zavrteti, xine ne?e primati naredbe u slede?ih  
par sekundi. Zatim pritisnite strelicu/play taster. Ovo bi trebalo da  
pokrene DVD.  
Još nekoliko saveta: možete da kontrolišete jezik/audio trake tokom  
puštanja filma, klikom na malu sterlicu na gore ili na dole ispred re?i  
&#8216;aud&#8217; (audio) na grafi?kom prikazu programa. Isto važi i za titlove  
&#8216;sub&#8217; . (Neki dvd diskovi mogu imati samo Nema?ki, ili Engleski sa  
Nema?kim titlom, i navaodno se titlovi ne mogu menjati, bar tako piše na  
omotu. TO je možda i ta?no na nekim Operativnim sistemima, ali ne i na  
Linuxu, jer na njemu samo izaberite (audio) jezik, ksao onaj bez  
titlova, a zatim ga zamenite tokom ve? pokrenutog filma).  
Ukoliko protisnete &#8216;i&#8217; tokom puštanja filma uklju?ujete ili  
isklju?ujete deinterlacing; možete izabrati de-interlace metod u  
konfiguracionom meniju. (Ikonica za alat, donji levi deo skina, blizu  
tastera za gašenje programa) U istom meniju možete promeniti i podesiti  
brojne druge opcije  
kao što je broj zvu?nika itd.

<a name="mplayer"></a>**_Kako da gledam TV pomo?u programa  
mplayer_**  
POstoje namenske aplikacije za gledanje programa sa TV kartica kao što  
su Xawtv ili Zapping (another tv app) ali još uvek nedaju potpuni  
full screen. Pored te opcije mplayer vam omogu?ava da radite on-the-fly  
de-interlacing i 3D denoising (prevedeno: umanjuje smetnje u oba pravca  
). KOmanda koja dobro obavlja posao je:  
<code style="color: rgb(255, 255, 0);">mplayer -tv&lt;br />
on:driver=v4l:device=/dev/v4l/video1:input=0:channel=61:width=768:height=576:fps=25&lt;br />
-vop lavcdeint,denoise3d=4:3:6</code>  
Ovo sve mora da ostane u jednoj liniji! U ovom datom slu?aju tv-tuner  
je postavljen na kanal 61 (ina?e BK televizija) ; za gledanje signala  
preko kompozitnog video ulaza na tv kartici koristite:  
<code style="color: rgb(255, 255, 0);">mplayer -tv&lt;br />
on:driver=v4l:device=/dev/v4l/video1:input=1:width=768:height=576:fps=25&lt;br />
-vop lavcdeint,denoise3d=4:3:6</code>  
TakoÄ‘e, da bi imali zvuk sa TV kartice, proverite da mikser kontrola za  
ulazni kanal vaše zvu?ne kartice ima nivo podešen bar na 70% ili više. 

<a name="mencoder"></a>**_Kako da snimam sa TVa pomo?u  
programa mencoder_**  
OVo ide prili?no teško jer sam imao problema sa zvukom, jer ga nije  
bilo. Iz neznanog razloga kmix i alsamixergui nisu mogli da odrade  
posao ali aumix (kojeg možete da pokrenete i pod konzolom) je odradio  
posao. Dakle, pošto ja volim konzolu pokrenuo sam:  
<code style="color: rgb(255, 255, 0);">aumix -l R -l 75 </code>  
što je podesilo kanal za snimanje na ulaz zvu?ne kartice a nivo ja?ine  
je 75. Sada bi trebali da budete u mogu?nosti da snimate, što možete  
uraditi sa komandom:  
<code style="color: rgb(255, 255, 0);">mencoder -tv&lt;br />
on:driver=v4l:device=/dev/v4l/video1:channel=27:width=768:height=576:fps=25&lt;br />
-vop lavcdeint,denoise3d=4:3:6 -oac mp3lame -lameopts abr=:preset=128&lt;br />
-ovc lavc -lavcopts vcodec=mpeg4:vbitrate=1500 -info&lt;br />
name=test:artist=channel-27:genre=trash:subject=snippet:copyright=aRTee:srcform=teevee:comment='just&lt;br />
testing' -frames 500 -o videocap.avi</code>  
Pogledajte i <code style="color: rgb(255, 255, 0);">man mencoder</code>  
za pravilnu sintaksu naredbi i opcije; the -frames 500 odgovara 20  
sekundi (25 drejmova u sekundi)što sam ja koristio za testiranje. SA  
ovim odnosom možete da smestite 1 sat videa na 770MB 

<a name="startx"></a>**_Kako da podignem grafi?ko okuženje  
ukoliko mi se sistem startuje u konzolnom modu_**  
Najlakši na?in: jednostavno ukucajte <code
 style="color: rgb(255, 255, 0);">startx</code>  
Ukolik vaše opstavke nisu u redu, verovatno ?ete morati da pokrenete <code
 style="color: rgb(255, 255, 0);">xf86config</code>. Da bi instalirali  
NVidia drajvere (ukoliko imate NVidia grafui?ku karticu, naravno),  
pratite instrukcije koje ?ete na?i na ovom sajtu, recimo na linku <http://www.mandrake.co.yu/modules.php?name=News&file=article&sid=170&mode=flat&order=0&thold=0>  
, a takoÄ‘e pogledajte i upustvo na `<font color="darkgreen"><br />
www.nvidia.com</font>` <span style="color: rgb(255, 255, 0);">.</span>  
?ak i ukoliko ne možete da podignete grafi?ko okruženje, ovaj sajt kao i  
druge možete da pretražite pomo?u naredbe lynx www.nvidia.com 

<a name="xfree"></a>**_Kako da izvu?em više iz grafi?kog  
okruženja XFree86_**  
-Možete da promenite rezoluciju prikaza ukoliko iskoristite slede?u  
kombinaciju tastera: ctrl-alt-+ (plus) or ctrl-alt&#8211; (minus)  
-Možete da ubijete x-server (= grafi?ko okruženje) pomo?u `<font
 color="darkred">ctrl-alt-backspace</font>`  
Ali nemojte da radite ovu poslednju kombinaciju osim ukoliko se nije  
zamrznuo ili blokirao grafi?ki sistem ili ukoliko uopšte ne reaguje.  
Ukoliko ne reaguje samo jedan program iskoristite kombinaciju `<font
 color="darkred">ctrl-alt-esc</font>` da bi oslobodili kursor a  
zatim ubijte zamrznuti prozor. KAo opciju, omžete ubiti odreÄ‘eni  
proces preko konzole , što je svakako bolje rešenj. Alternatively you  
can just kill the process through the cli, which is definitely the  
preferred method; iskoristite `<font color="darkred">ctrl-alt-esc</font>`  
da bi ubili prozor ?iji je proces ve? ubijen iz konzole.  
Fajl <code style="color: rgb(255, 255, 0);">/etc/X11/XF86Config-4</code>  
sadrži opcije i postavke za x-server. Ukoliko je vaša rezolucija manja  
od mogu?e možete da editujete fajl: postavite ve?e minimalno  
horizontalno osvežavanje, i restartujete x-server (izlogujte se, a  
zatim izaberite opciju sa restartovanje x-servera) 

Još jedna lepa stvar kod XFree-a je u slu?aju da ste umreženi.  
Možete se jednostavno prijaviti na drugi ra?unar koji koristi linux (ili  
X, na BSD ili sli?no) i pokretati porgrame, možete videti i  
kontrolisati grafi?ko okruženje na vašem desktopu. Na primer, ukoliko  
vaš ra?unar nema reza?, ali druga mašina ima, ali je i koristi neko  
drugi, jednostavno ubacite prazan cd, ulogujte se daljinski preko ssh i  
pokrenite program za narezivanje diskova (naravno, podaci moraju biti  
dostupni za mašinu na kooj se nalazi rea?, kao i to da morate imati sva  
ovlaš?enja za pristup i koriš?enje cd reza?a. 

<a name="multix"></a>_**Kako da kreiram više x-servera**_  
Kao prvo ova mogu?nost može biti korisna. , ali šta su ustvari  
&#8216;višestruki x-serveri&#8217;?  
Za razliku od MSwindows-a, grafi?ki deo je izgraÄ‘en na vrhu jezgra  
sistema. Ovo je razlog zbog ?ega iammo razli?ita grafi?ka okruženja, sa  
razli?itim window i desktop menadžerima.  
U Linuxu imamo: jezgro sistema kernel (linux), preko koga ide grafi?ko  
okruženje (koje se još naziva X-server, ve?inom je to XFree, ali postoje  
i komercijalne alternative), preko koga opet ide window menadžer  
(twm, mwm, icewm, metacity, sawfish ili neki drugi), preko njega opet  
(ukoliko to želite; na starijim sistemima oni se nisu koristili) idu  
desktop menadžeri (KDE ili Gnome na primer).  
Dakle, radi se o grafi?kom delu, ili x-serveru? Pa zašto bi pokretali  
dva ili više njih istovremeno?  
Pa na primer, ukoliko vi i nekoliko drugih ljudi koristi isti pc, a  
jedan od vas je ve? ulogovan i ne želi da se izloguje. (na primer, kada  
imate stalnu internet konekciju (cable, adsl) i pokrenuli ste neki  
download, kaoi još neke programe, ili ne želite da se izlogujete jer  
skidate sa interneta važan program, a želite da utrošite vreme koje  
?ekate igraju?i igricu kaoja zahteva nižu rezoluciju(npr. starcraft). 

Protisnite ctrl-alt-F1 (možete da koristite F1 sve do F6 za konzole,  
a F7 do F12 za grafi?ka okruženja) da bi prešli u konzolu.  
Ukoliko želite da imate drugu x-sesiju za drugog korisnika, ulogujte se  
kao taj korisnik. Ukucajte:  
<code style="color: rgb(255, 255, 0);">X :1 &</code>  
(ukoliko želite da proverite XFree86 konfiguracioni fajl probajte &#8222;<code
 style="color: rgb(255, 255, 0);">X -xf86config /path/to/test/config :1&lt;br />
&#038;</code>&#8222;; broj &#8216;1&#8217; je broj datog grafi?kog okruženja, koji  
?e vam biti potreban kasnije; možete da koristite i druge brojeve  
ukoliko želite mislim da je ograni?enje 255 ili tako nešto &#8230;)  
Pokrenite ponovo ctrl-alt-F1 da bi se vratili u konzolu i ukucajte:  
<code style="color: rgb(255, 255, 0);">export DISPLAY=:1</code>  
i sada ste spremni da pokrene window menadžer. Za kde, koritite komandu  
&#8216;startkde&#8217; a za gnome &#8216;gnome-session&#8217;. Za neko lakše, manje zahtevno  
okruženje probajte &#8216;icewm&#8217; ili &#8216;twm&#8217;.  
I stavite &#8216;&&#8217; posle komande ukoliko i dalje želite da  
koristite konzolu. Upotrebite ctrl-alt-F7 da bi prešli u orginalno  
grafi?ko okruženje, a ctrl-alt-F8 da bi prešli u novo. 

<a name="network"></a>**_Kako da podesim ku?nu mrežu_**  
&#8211; Å½elite da delite internet konekciju: ukoliko imate više pc mašina a  
samo jednu internet konekciju (telefonski modem -koriš?enje u isto  
vreme, da bi uštedeli novac ili cable i adsl &#8211; ?esto ne možete da  
konektujete više od jednog modema).  
Ovo zahteva da imate dve mrežne kartice u mašini koja vrši deljenje  
interenet konekcije, kao i to da podesite te dve mrežne kartice na  
ispravan na?in: kartica koja je povezana na modem treba da je podešena  
preko DHCP a druga treba da ima adresu u dozvoljenom rasponu adresa za  
privatne tj. lokalne mreže: `192.168.x.y` (gde y ne sme da  
bude 0 ili 255, x i y moraju biti u rasponu od 0 do 255). Na primer,  
koristite `192.168.0.1` za server, `192.168.0.2`  
za prvi slede?i pc (bilo da je u pitanju linux ili windows mašina ) itd.  
Samo da vam pomenem da sve ovo možete da odradite iz mcc ->  
network.Na windows ili linux mašinama, postavite da je  
internet gateway i dns server `192.168.0.1` (veoma  
dosadno podešavanje na Win98se jer morate da restartujete mašinu svaki  
put kada izvršite pormene u network dijalogu. Prvo proverite da li ovo  
radi pod Linuxom, a zatim podesite svoju(e) windows mašine sa istim  
opcijama. Iskoristite komandu <code style="color: rgb(255, 255, 0);">ping&lt;br />
192.168.0.1</code> da bi proverili da li možete da vidite svoj linux  
server sa druge pc mašine. Ili , na drugi na?in, možete da pingujte  
druge mašine sa LInux servera.  
Zapamtite  
da u veoma viskom sigurnosnom nivou linux pc ne?e odgovarati  
na ping. (ovo se takoÄ‘e dešava kada delite svoju internet konekciju)  
&#8211; Sada da i po?eno da koristimo zajedni?ku internet konekciju:  
Samo pokrenite Mandrake kontrolni centar, izaberite network/internet na  
levoj strani, a zatim deljenje konekcije (connection sharing). Slediti  
upustva ?arobnjaka (wizard).  
&#8211; Deljenje fajlova: mandrake kontrolni centar, ta?ke montiranja,  
deljenje pariticija. U potpuno linux okruženju, dovoljno je da koristite  
nfs. Ukoliko želite da imate mogu?nost ?itanja vaših particija/deljenih  
direktorijuma sa windows mašina koristite samba-u. Da bi ovo sve lepo  
podesili možete da koristite i program linuxconf.  
&#8211; Sli?no prethodnom, možete podesiti nfs ili samba deljene resurse sa  
drugih mašina u meniju za ta?ke montiranja.Naravno, i za ovo možete da  
koristite linuxconf.  
&#8211; Kada druge mašine koriste windows ili linux, možete da ih daljisnki  
kontrolišete pomo?u VNC, koji je uklju?en u Mandrake Linux. 

Na Linux-u (nasuprot windows-u) VNC sesija nije u stvati ono što je  
pokrenuto na ekranu; pokre?e se drufa x-sesija, koja može imati  
druga?iju rezoluciju ili broj boja. Možete je pokrenuti kucanjem (kao  
korisnik, ne kao root!):  
<code style="color: rgb(255, 255, 0);">vncserver :1</code> (zapamtite  
broj!)  
Ukliko niste podesili lozinku, prvo ?e vam re?i da je kreirate  
(vncpasswd).  
Nakon toga, možete da se konektujete sa druge (ili iste mašine,  
radi testiranja) mašine ukucavaju?i: <code
 style="color: rgb(255, 255, 0);">vncviewer</code>ili preko K-menija &#8211;  
Mreža &#8211; Daljinski pristup &#8211; TightVNC  
Sada ukucajte adresu servera, koja na kraju ima znak(:), a zatim i proj  
pokrenutog servera: <code style="color: rgb(255, 255, 0);">192.168.0.1:1</code>  
Sada ukucajte vašu vnc lozinku u slede?em boxu. 

Ukoliko vaš sistem nije pokrenut sa grafi?kim okruženjem (može se  
desiti da server uopšte nema prika?en monitor), još uvek možete da  
pokrenete. Ukoliko grafi?ka karta na serveru ne dozvoljava ništa više od  
8 bita na 1024&#215;768, možete da dobojete ve?u rezoluciju preko vašeg  
vncservera; Na primer, pokrenite ga sa:  
<code style="color: rgb(255, 255, 0);">vncserver :3 -geometry 1280x1024&lt;br />
-depth 16</code> i tako dobijate i ve?u rezoluciju i broj boja od onoga  
što bi mogli da dobijete direktno na serveru. (ovo nije mogu?e sa  
windows-om.) Ovo doduše može malo da uspori vezu, ali recimo u ovom  
slu?aju radi se o 20KB/s, što i nije mnogo na 100Mbit/s mreži.  
Dobra stvar sa vncserverom je da možete da recimo ugasite svoj  
klijentski pc, konektujete se ponovo kasnije itd. Na primer, ukoliko vaš  
server skida veliki fajl, možete da ugasite vaš pc a ostavite server  
aktivnim. 

&#8211; logovanje sa ssh i pokretanje aplikacija lokalno koje se pokre?u  
na serveru na koji ste se ulogovali. (aplikacije takoÄ‘e možete pokrenuti  
prek vnc, dako da ustvari možete sve da uradite na serverui) Sa klijetn  
mašine uradite slede?e:  
<code style="color: rgb(255, 255, 0);">ssh 192.168.0.1</code> dajte  
korisni?ko ime (ukoliko se tazlikuje od predloženog) i lozinku. Sada bi  
trebali da ste na tom drugom sistemu, gde možete da izdajete naredbe kao  
što je: <code style="color: rgb(255, 255, 0);">vncserver :1</code>  
ili sli?no (što je ono što se koristi da bi pokrenuli vncserver nakon  
što je server restartovan)  
&#8222;telnet&#8220; bi trebao da odradi isti ili sli?an posao, ali pošto je  
manje siguran, savetujem da ga ne koristite , pa ?ak i da ga ne  
instalirate.

<a name="newhd"></a>**_Kako da dodam novi hard disk_**  
Sa Mandrake-om (ili bilo kojom drugom linux distribucijom)  
&#8211; samo priklju?ite disk u ra?unar, proverite da li je bios pravilno  
detektovao disk, i restartujte mašinu. Sada, nakon što se sistem  
podigao, pokrenite mcc, hardware, lista hardvera, izaberite novi hard  
disk, i kliknite na &#8216;pokreni konfiguracioni alat&#8217;.  
U diskdrake-u (konfiguracioni alat), možete izabrati prazan prostor,  
kreirati particije, i namestiti ta?ke montiranja. Sa malo sre?e, ne?ete  
morati ni da restartujete mašinu da bi po?eli da koristite hard disk i  
novokreirane particije; samo uradite format nakon kreiranja  
particija(ext3 particije su one koje se obi?no koriste pod  
linuxom, fat32 za one koje ?e biti koriš?ene ili ?e biti vidljive  
iz windows-a), i montirajte particije. 

<a name="xmmsaudiocds"></a>**_Kako da slušam audio cd pomo?u  
xmms-a_**  
Naravno da postoji milion programa koji mogu da obave ovaj posao,  
recimo: Kmenu-multimedia-sound-KsCD. Ali xmms poseduje veoma dobre  
dodatke (plugins) (synaesthesia!!), tako da možete do maksimuma da  
iskoristie svoju jaku mašinu.  
Da bi slušali mp3 fajlove (ili fajlove na hard disku) jednostavno ih  
možete potražiti iz programa. Muzi?kim diskovima se mora pri?i na  
druga?iji na?in pošto oni nisu cd-rom-omovi i podležu drugim standardima  
(još gore je ako imate neki od novijih audio cd-a koji su zašti?eni od  
kopiranja).  
Bilo kako bilo, da bi pustili muzi?ki cd pomo?u xmms, uradite slede?e:  
otvorite opciju za unošenje: open URL, i upišite /dev/cdrom (ili  
/dev/cdrom0 ili 1 ili onaj borj koji odgovara postavkama u sistemu  
odnosno onome što je u /dev direktorijumu). Da bi to saznali, ako ve? ne  
znate, u konzloli ukucajte:  
<code style="color: rgb(255, 255, 0);">ls -l /dev/cdrom*</code>  
(takoÄ‘e možete da koristite i naredbu <code
 style="color: rgb(255, 255, 0);">ll</code> umesto <code
 style="color: rgb(255, 255, 0);">ls -l</code> na ve?ini linux sistema)  
što nam kao rezultat daje:  
`lr-xr-xr-x    1 root     root           13 Jan 29 19:43<br />
/dev/cdrom -> cdroms/cdrom0<br />
lr-xr-xr-x    1 root     root           13 Jan 29 19:43 /dev/cdrom0<br />
-> cdroms/cdrom0<br />
lr-xr-xr-x    1 root     root           13 Jan 29 19:51 /dev/cdrom1<br />
-> cdroms/cdrom1</p>
<p>/dev/cdroms:<br />
total 0<br />
lr-xr-xr-x    1 root     root           33 Jan  1  1970 cdrom0 -><br />
../ide/host0/bus1/target1/lun0/cd<br />
lr-xr-xr-x    1 root     root           34 Jan  1  1970 cdrom1 -><br />
../scsi/host0/bus0/target2/lun0/cd` 

iz ?ega možete zaklju?iti da je cdrom0 sekundarni ureÄ‘aj na  
sekundarnom ide kontroleru (u mom slu?aju dvd-rom) a da je cdrom 1 moj  
cd reza?, koji je prihva?en od sistema preko scsi emulacije. 

<a name="konq"></a>**_Konqueror_**  
Da li više volite detaljan prikaz fajlova? Kliknite na ikonu za prikaz.  
Å½elite da imate iste postavke i slede?i put kada startujete program? TO  
možete podesiti kada odete u meni Window -> save profile. Ovde  
takoÄ‘e možete izabrati opciju da vidite prozor u istoj veli?ini.  
Konqueror vam takoÄ‘e dozvoljava da imate više od jednog panela sa  
fajlovima, što je mnogo bolje pri kopiranju ili premeštanju fajlova i  
direktorijuma, odnosno ono što ste ve? navikli sa Windows  
Commander-om. 

<a name="resetuserpw"><b><i>Kako da resetujem korisni?ku lozinku</i></b></a>  
U slu?aju da je bilo koji obi?ni korisnik zaboravio lozinku, postoji  
veoma jednostavan na?in da ispravite ovaj problem:  
`<font color="darkgreen" style="color: rgb(255, 255, 0);">su</font><br />
<font color="darkred">[unesite root lozinku]</font><br />
<font color="darkgreen" style="color: rgb(255, 255, 0);">passwd<br />
[ime_korisnika_koji_je_zaboravio_lozinku]</font><br />
<font color="darkred">[unesite novu lozinku za korisnika]</font>`  
Na ovom koraku vas sistem može obavestiti da je lozinka LOÅ A jer je  
previše jednostavna, prekratka ili ve? šta. Ovu poruku možete slobodno  
da ignorišete, to je ve? do vas.  
`<font color="darkred">[unesite novu lozinku još jednom]</font>`  
I gotovo. Naravno, ovo sve možete da uradite i pomo?u programa userdrake``. 

<a name="resetrootpw"><b><i>Kako da resetujete root lozinku</i></b></a>  
Ukoliko ste izgubili root lozinku, diskonektujte vaš ra?unar sa mreže.  
Ubacite prvi CD, i kada se pojavi prvi ekran, pritisnite F1, a zatim  
ukucajte <code style="color: rgb(255, 255, 0);">rescue</code> i  
sa?ekajte da ra?unar podigne sistem u rescue modu. Pored nekoliko  
ponuÄ‘enih opcija izaberite `mount the existing partitions`  
a zatim preÄ‘ite na `shell / konzolu`. Zatim uradite  
slede?e:  
`cd /mnt/etc`  
a zatim izmenite slede?e fajlove u bilo kom tekst editoru (recimo  
editor `vi` ):  
`vi passwd`  
zatim izmenite prvu liniju da izgleda koja izgleda ovako:  
`root:x:0:0:root:/root:/bin/bash`  
u:  
`root::0:0:root:/root:/bin/bash`  
(sa vi eitorom dovoljno je da iskoristite kursor na mesto karaktera  
koji želite da izbrišete a zatim samo kliknite na taster x)  
Snimite izmene pomo?u `<font color="darkred">[esc]</font> <font
 color="darkgreen" style="color: rgb(255, 255, 0);">:wq</font> <font
 color="darkred">[enter]</font>`  
Zatim izmenite fajl shadow:  
<code style="color: rgb(255, 255, 0);">vi shadow</code> i prvu liniju  
izmenite da izgleda kao (ona koja po?inje sa `root`) slede?a  
linija:  
`root:*::::`  
(jedna dvota?ka, &#8216;*&#8217; i ?etiri dvota?ke na kraju). Ponovo snimite  
izmene kucaju?i `<font color="darkred">[esc]</font> <font
 color="darkgreen" style="color: rgb(255, 255, 0);">:wq</font><br />
 <font
 color="darkred">[enter]</font>`  
Restartujte mašinu i ulogujte se kao obi?an korisnik, zatim pomo?u `<font
 color="darkgreen">su</font>` postanite root, a zatim pomo?u  
komande <code style="color: rgb(255, 255, 0);">passwd</code> <span
 style="color: rgb(255, 255, 0);"></span>postavite novu root lozinku.  
Ne mojte da se konektujete na internet ili lokalnu mrežu sve dok ne  
postavite novu root lozinku. 

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=367)