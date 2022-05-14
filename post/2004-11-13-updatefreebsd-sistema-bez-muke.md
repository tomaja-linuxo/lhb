---
author: tomaja
date: "2004-11-13T16:37:17Z"
excerpt: |
  Jedna od velikih prednosti  *BSD distribucija je postojanje
  cvsup/make
  proces koji omogu?ava update sistema preko Interneta. Preko cvsup/make
  procesa možete
  ažurirati sistem kada god poželite uz uslov da imate dobar internet
  link. E pa da vidimo kako se to radi:
guid: https://forum.linuxo.org/2004/11/13/updatefreebsd-sistema-bez-muke/
id: 613
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: UpdateFreeBSD sistema bez muke
url: /updatefreebsd-sistema-bez-muke/
---
Jedna od velikih prednosti *BSD distribucija je postojanje  
cvsup/make  
proces koji omogu?ava update sistema preko Interneta. Preko cvsup/make  
procesa možete  
ažurirati sistem kada god poželite uz uslov da imate dobar internet  
link. E pa da vidimo kako se to radi:<!--break-->

Instaliranje CVSup

Prva stvar koju morate da uradite jeste da instalirate cvsup port;  
da bi ovo uradili pokrenite slede?u komandu sa root ovlaš?enjima:

\# cd /usr/ports/net/cvsup-without-gui  
\# make install clean

<p class="note">
  Kada sve ovo radimo ptreba da instaliramo i<br /> fastest_cvsup port. Iako ovo nije neophodno umnogome ?e nam ubrzati<br /> ceo proces
</p>

\# cd /usr/ports/sysutils/fastest_cvsup  
\# make install clean  
Choosing a cvsup server

Slede?e što želite jeste da pronaÄ‘ete najbrži cvsup server sa kojeg  
?ete slidati source  
fajlove. Evo kako izgleda output malopre instalirane komande:

<pre># fastest_cvsup -c us<br />>> Querying servers in countries: us<br />--> Connecting to cvsup1.freebsd.org [198.104.69.57]...<br /> - server replied: OK 17 0 SNAP_16_1e CVSup server ready<br /> - time taken: 65.72 ms<br />--> Connecting to cvsup2.freebsd.org [130.94.149.166]...<br /> - server replied: OK 17 0 SNAP_16_1h CVSup server ready<br /> - time taken: 97.60 ms<br />--> Connecting to cvsup3.freebsd.org [18.24.10.20]...<br /> - server replied: OK 17 0 SNAP_16_1e CVSup server ready<br /> - time taken: 103.64 ms<br />--> Connecting to cvsup4.freebsd.org [204.152.184.73]...<br /> - server replied: OK 17 0 SNAP_16_1f CVSup server ready<br /> - time taken: 28.44 ms<br />--> Connecting to cvsup5.freebsd.org [198.182.76.34]...<br /> - server replied: OK 17 0 SNAP_16_1f CVSup server ready<br /> - time taken: 44.37 ms<br />--> Connecting to cvsup6.freebsd.org [66.109.10.22]...<br /> - server replied: OK 17 0 SNAP_16_1f CVSup server ready<br /> - time taken: 71.33 ms<br />--> Connecting to cvsup7.freebsd.org [129.250.31.140]...<br /> - server replied: OK 17 0 SNAP_16_1g CVSup server ready<br /> - time taken: 3108.32 ms<br />--> Connecting to cvsup8.freebsd.org [129.250.31.140]...<br /> - server replied: OK 17 0 SNAP_16_1g CVSup server ready<br /> - time taken: 76.29 ms<br />--> Connecting to cvsup9.freebsd.org [209.181.243.21]...<br /> - server replied: OK 17 0 SNAP_16_1e CVSup server ready<br /> - time taken: 84.56 ms<br />--> Connecting to cvsup10.freebsd.org [216.136.204.25]...<br /> - server replied: OK 17 0 SNAP_16_1e CVSup server ready<br /> - time taken: 103.65 ms<br />--> Connecting to cvsup11.freebsd.org [63.87.62.77]...<br /> - server replied: OK 17 0 SNAP_16_1h CVSup server ready<br /> - time taken: 88.22 ms<br />--> Connecting to cvsup12.freebsd.org [128.46.156.46]...<br /> - server replied: OK 17 0 SNAP_16_1g CVSup server ready<br /> - time taken: 87.71 ms<br />--> Connecting to cvsup13.freebsd.org [63.251.223.166]...<br /> - server replied: OK 17 0 SNAP_16_1f CVSup server ready<br /> - time taken: 39.23 ms<br />--> Connecting to cvsup14.freebsd.org [208.185.175.214]...<br /> * error: Timeout<br />--> Connecting to cvsup15.freebsd.org [131.193.178.106]...<br /> * error: Timeout<br />--> Connecting to cvsup16.freebsd.org [128.143.108.35]...<br /> - server replied: OK 17 0 SNAP_16_1f CVSup server ready<br /> - time taken: 3082.32 ms<br />--> Connecting to cvsup17.freebsd.org [216.136.204.25]...<br /> - server replied: OK 17 0 SNAP_16_1e CVSup server ready<br /> - time taken: 119.61 ms<br /> <br />>> Speed Daemons:<br /> - 1st: cvsup4.freebsd.org<br /> - 2nd: cvsup13.freebsd.org<br /> - 3rd: cvsup5.freebsd.org</pre>

Po listingu možemo uo?iti da je najbrži server u ovom slu?aju  
cvsup4.freebsd.org. Naravno, u svakom konkretnom slu?aju ?e biti  
verovatno druga?ije.

Predpostavljamo da ste ve? podesili kernelov konfiguracioni fajl.  
Ukoliko niste onda obavezno pogledajte [FreeBSD  
Priru?nik](http://www.freebsd.org/doc/en_US.ISO8859-1/books/handbook/kernelconfig.html) . Mašina na kojoj je izvršen update je dual 1.8GHz Xeon  
(I686_CPU) sa 1GB RAM, SCSI diskovima, Intel (fxp) mrežna kartica i  
SBLive! (pcm)  
zvu?na kartica sa Epson USB scanerom. Kernelov konfiguracioni fajl sa  
ove mašine možete pogledati [ovde](http://members.cox.net/s.wingate/misc/XEON.txt).

### Podešavanje fajla make.conf {.arthdr}

Slede?e što treba da uradimo je izmena make.conf fajla radi  
smeštanja odreÄ‘enih parametara koje ?e koristiti sam proces za update  
sistema. Ovaj fajl ?ete prona?i u /etc/defaults/,  
ali preporu?ujemo da ne menjate ovaj fajl u tom direktorijumu ve? da ga  
prekopirate na neko drugo mesto i menjate tu kopiju. Ovako ?ete u  
mogome smanjiti mogu?nost da nešto zabrljate a sam sistem možete  
vratiti na staro pomo?u naredbe rm /etc/make.conf. Dakle:

\# cp /etc/defaults/make.conf /etc/  
\# vim /etc/make.conf

Ovaj fajl sadrži mnoge parametre ali ?emo se ovde osvrnuti samo na  
one koji su nam potrebni za update sistema:

\# CVSup update flags. Edit SUPFILE settings to reflect whichever  
distribution  
\# file(s) you use on your site (see /usr/share/examples/cvsup/README  
for more  
\# information on CVSup and these files). To use, do &#8222;make update&#8220; in  
/usr/src.  
#  
#SUP_UPDATE= yes  
#  
#SUP= /usr/local/bin/cvsup  
#SUPFLAGS= -g -L 2  
#SUPHOST= cvsup.uk.FreeBSD.org  
#SUPFILE= /usr/share/examples/cvsup/stable-supfile  
#PORTSSUPFILE= /usr/share/examples/cvsup/ports-supfile  
#DOCSUPFILE= /usr/share/examples/cvsup/doc-supfile

Ova sekcija sadrži parametre koje ?e koristiti cvsup proces kada god  
radimo update sistema. Dekomentirajte sve linije. Izmenite SUPHOST= na  
ono što odgovara vašem slu?aju i to naravno da bude najbrži server a  
njega ste ve? dobili pomo?u komade fastest_cvsup . Ukoliko želite  
da koristite FreeBSD-stable onda je stable-supfile ono što želite da  
koristite.DOCSUPFILE=  
služi za održavanje lokalne kopije FreeBSD dokumentacije i nije  
neophodna. Nakon izmena , evo kako izgleda sekcija:

<pre>SUP_UPDATE= yes<br />#<br />SUP= /usr/local/bin/cvsup<br />SUPFLAGS= -g -L 2<br />SUPHOST= cvsup4.FreeBSD.org<br />SUPFILE= /usr/share/examples/cvsup/stable-supfile<br />PORTSSUPFILE= /usr/share/examples/cvsup/ports-supfile<br />#DOCSUPFILE= /usr/share/examples/cvsup/doc-supfile<br /><br />KERNCONF=KERNELNAME</pre>

Poslednji red služi za lakše kompajliranje kernela. Treba da  
zamenite KERNELNAME sa imenom vašeg konfiguracionog fajla za  
kernel a koji bi trebao da se nalazi u /usr/src/sys/i386/conf/.

IzvoÄ‘enje Update-a

U ovom momentu sve se nalazi na svom mestu i vrlo ste blizu skoro  
automatskog ažuriranja svog FreeBSD sistema. Da bi zaista i pokrenuli  
proces ažuriranja jednostavno preÄ‘ite u direktorijum /usr/src i  
ukucajte naredbu make update. cvsup proces ?e se povezati na vaš  
izabrani server i skupiti najnoviji izvorni kod. Ukoliko sve proÄ‘e kako  
treba trebali bi da vidite na ekranu slede?e:

<pre>daemon# cd /usr/src<br />daemon# make update<br />--------------------------------------------------------------<br />>>> Running /usr/local/bin/cvsup<br />--------------------------------------------------------------<br />Parsing supfile "/usr/share/examples/cvsup/stable-supfile"<br />Connecting to cvsup4.FreeBSD.org<br />Connected to cvsup4.FreeBSD.org<br />Server software version: SNAP_16_1f<br />Negotiating file attribute support<br />Exchanging collection information<br />Establishing multiplexed-mode data connection<br />Running<br />Updating collection src-all/cvs<br />.....abbreviated output........</pre>

Vreme koje je potrebno za sve ovo zavisi od brzine vaše Internet  
konekcije kao i od toga koliko ?esto koristite ovaj proces. Kada se  
uploda završi možete da krenete sa rebuild-om sistema. Obi?no se  
pokre?e naredba buildworld a nakon nje i make installworld.  
buildworld ponovo kreira osnovu operativnog sistema a installworld  
jednostavno instalira sve što je buildworld napravio. Možete pokrenuti  
i world  
target, što kobinuje dva, malo pre pomenuta koraka. Ovaj korak traje  
oko 25  
minuta na Xeon sistemu ili nekoliko sati na recimo Celeron 400MHz  
mail/dns/nfs serveru. Naravno, ovaj proces može i ranije da se završi  
ukoliko se pojavi neka greška 🙁

Ukoliko je sve, meÄ‘utim, prošlo bez grešaka spremni ste za kreiranje  
novog kernela. Da bi to uradili jednostavno ukucajte make kernel  
u istom /usr/src direktorijumu. Sistem ?e kreirati novi kernel  
koristi?e konfiguracioni fajl kojeg ste vi imenovali pomo?u  
KERNCONF=KERNELNAME linije u  
/etc/make.conf.

Pošto se kreira novi kernel spremni ste za poslednji i kona?ni korak  
a to je pokretanje mergemaster komande. Sa ovom komadnom sistem  
vas pita da li želite da overwrite-ujete odreÄ‘ene sistemske  
konfiguracije koje su možda izmenjene . Ovde budite veoma pažljivi jer  
možete da overwrite-ujete važne fajlove kao što je /etc/passwd pa je za  
ve?inu razumnih ljudi odgovor na ovo pitanje NE. Ipak, možete dozvoliti  
sitemu da overwrite-ujefajlove za koje ste sigurni da ih sami do tada  
niste menjali. Kada završite sa ovom komandom možete da resetujete  
mašinu i da podignete potpuno novi FreeBSD Ako još više želite da  
ubrzate ovaj proces možete da iskoriste alias koji ?ete ubaciti u  
config fajl vašeg shella (tcsh) :

<pre>alias rebuild 'cd /usr/src && make update && make world && make kernel && mergemaster'</pre>

I tako, sada je  
samo potrebno da kao root ukucate naredbu rebuild u  
terminalu. Za 30-35 minuta, bi, uz malo sre?e i par odgovorenih pitanja  
na mergemaster promptu mogli dobiti bukvalno najnoviji FreeBSD! Proces  
je toliko jednostavan da vam instalranje individualnih patch-eva  
više nije ni potrebno.

Orginalni tekst (eng.)

Steve Wirgate ,  
BSDNews

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=613)