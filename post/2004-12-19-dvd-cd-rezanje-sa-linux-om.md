---
author: Loading
date: "2004-12-19T13:00:02Z"
excerpt: 'U ovom uputstvu sam se trudio da opisem postupak rezanja DVD/CD-a u konzoli.
  Poznavanje postupka rezanja DVD/CD-a u konzoli moze da Vam olaksa zivot  u nekim
  situacijama, poput automatizacije posla stavljanjem komandi u skripte,... '
guid: https://forum.linuxo.org/2004/12/19/dvd-cd-rezanje-sa-linux-om/
id: 667
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: DVD/CD Rezanje sa Linux-om
url: /dvd-cd-rezanje-sa-linux-om/
---
U ovom uputstvu sam se trudio da opisem postupak rezanja DVD/CD-a u konzoli. Poznavanje postupka rezanja DVD/CD-a u konzoli moze da Vam olaksa zivot u nekim situacijama, poput automatizacije posla stavljanjem komandi u skripte,&#8230; <!--break-->Kod Linux-a postupak rezanja je odvojen u dve faze: pravljenje fajl sistema (FS) i samo rezanje. To odvajanje poslova je svojstveno za Linux, jer to omogucava da imamo mocne i male alatke koje kada ukombinujemo dobijamo mogucnosti koje se nemogu prevazici sa namenskim alatkama.

**Priprema CD-a sa podacima**

Kada pravimo CD sa podacima moramo voditi racuna o raspolozivom prostoru, i korisno je imati u vidu da FS zauzimaju nekoliko MB. Moramo pre samog rezanja biti nacisto sta cemo da stavimo na CD, jer naknadno dodavanje fajla na multisesijski disk je skupa avantura, moramo imati u vidu da dodatni _TOC_(Tabela Sadrzaja(_Table Of Content_)) zauzima znatan prostor na CD-u. Osnovni FS za CD-ove je ISO9660, on je ogranice u dubini direktorijuma (8) i duzini imena fajlova (do 32 karaktera). Da bi smo zaobisli ta ogranicenja koristimo dodatne FS. Ja cu ovde navesti samo dva FS: Joliet (win), Rock&Ridge (unix). Glavna razlika izmedju ova dva FS je ta sto je Joliet napravljen za win masine i ne podrzava unix mogucnosti FS, dok Rock&Ridge podrzava sve napredne mogucnosti unix fajl sistema.

_#mkisofs -r -J -o slika.iso /dir1_

**-r** Rocke&Ridge FS. Stavlja vlasnika i vlasnicku grupu na nule. Ako je fajl citljiv korisniku, onda stavlja da fajl bude globalno citljiv, isto to vazi i za izvrsivost fajlova. Naravno svim fajlovima su izbrisana ovlascenja za pisanje. Ako zelite da sacuvate ovlascenja onakva kakva su na hardu koristite opciju **-R**.  
**-J** Stavlja Joliet FS.

Ako zelimo da rezemo multisesijski CD moracemo da _mkisofs_ prosledimo dodatne podatke.

_  
#SLEDECA_STAZA=\`cdrecord -msinfo dev=0,6,0\`  
#mkisofs -R -o cd\_slika2 -C $SLEDECA\_TRAKA -M /dev/scd5 /dir2  
_  
I kada budemo rezali sa _cdrecord_-om vise sesijski disk moramo mu dati opciju _-multi_, sve dok zelimo da dodajemo sesije na taj disk. 

**Rezanje CD-a**

Za rezanje CD-a koristimo program _cdrecord_ ili program _cdrdao_. Razlika izmedju ova dva programa je ta da _cdrecord_ podrzava samo rezim rezanja traka po traka (_Track at Once_), dok _cdrdao_ podrzava rezanje disk odjedanput (_Disc at Once_). Ovo je bitno zato sto ako rezemo u TAO modu mogu nam promaci skrivene zastite na CD-u, i na audio CD-ovima imacemo 2 sekunde pauze izmedju pesama. Za sad cu da ovde navedem primere samo sa _cdrecord_ programom, a kasnije planiram da ubacim i primere za _cdrdao_.

_#cdrecord -v dev=0,0,0 speed=16 -data slika.iso_  
Korisne opcije sa _cdrecord_-om:  
**-v** Pricljiv mod.  
**dev=SCSI\_BUS, SCSI\_ID, SCSI_LUN** kazemo kojim uredjajem zelimo da rezemo.  
**speed=broj** 1x brzina = 150KB/s.  
**-data** Kada rezemo podatke.  
**-audio** Koristimo kada rezemo audio CD.  
**-scanbus** Skenira SCSI magistrale i lista dostupne pisace.  
**-eject** Izbacuje CD posle rezanja  
**-dummy** Iskljucuje laser u toku rezanja. Dobra opcija ako ocemo da vidimo kako bi teklo rezanje, a da ne ugrozimo CD.  
**-isosize /dev/cdrom** Ako zelimo da rezemo sa jednog na drugi CD u letu.

Primeri:

_#cdrecord -v dev=0,0,0 speed=16 -audio track1.wav, track2.wav,&#8230;_  
Kada rezemo audio CD moramo da _cdrecord_-u damo .wav, .au, .cdr fajlove. On ne moze da radi sa .mp3 fajlovima. Zato ih prethodno moramo konvertovati.

_#mkisofs -r -J /dir | cdrecord -v dev=0,0,0 speed=4 -data &#8211;  
_  
Neki rezaci zahtevaju da znaju velicinu FS pre rezanja i za njih predhodna komanda ne obavlja posao. Nego to radimo ovako:  
_  
#VELICINA_FS=\`mkisofs -quiet -print-size -r -J /dir\`  
#mkisofs -r -J /dir | cdrecord -v dev=0,0,0 speed=4 tsize={VELICINA_FS}s -data &#8211;  
_  
Ako zelimo da radimo kopiranje CD-a u letu, to mozemo uraditi na sl. nacin:  
_  
#cdrecord -v dev=0,0,0 speed=4 -isosize /dev/cdrom  
_ 

**Rezanje DVD**

Da bi smo rezali DVD koristimo program _growisofs_. On u sebi sadrzi program za rezanje i pripremu FS. Inace koristi _mkisofs_ program za pravljenje FS.  
Primeri:

_#growisofs -Z /dev/dvd -r -J /dir1 /dir2_  
**-r**, **-J** Opcije sam vec prethodno objasnio.  
**-Z** Zapocinje nultu (Zero) sesiju.  
**-M** Dodaje (Merge) sesije.  
**-dry-run** Isto sto i opcija _-dummy_ u _cdrecord_-u.  
**-overburn** Moramo navesti ovu opciju ako planiramo da rezemo vise od samog kapaciteta diska (uobicajeno 4.33GB). DVD ima 4700000 bajtova i oni kada se podele sa 2 na 20, dobijamo da je pravi kapacitet 4.33GB, sta da Vam kazem marketing je cudo.  
**-dvd-compat** Zavrsava DVD.

_#growisofs -M /dev/dvd -r -J /dir3_  
Dodaje /dir3 na prethodnu kompilaciju (/dir1, /dir2). Vodite racuna da opcije za FS ostanu iste.  
_#growisofs -dvd-compat -video-dvd /dev/dvd /root_video/_  
Reze video DVD, iz /root\_video direktorijuma koji mora sadrzati VIDEO\_TS i AUDIO_TS direktorijume. Naravno prethodno morate skinuti (ripovati) DVD. Ovde sam stavio _-dvd-compat_ opciju da bi DVD bio citljiv na sto vecem broju DVD plejere (TV), to znaci da je kompatibilan sa vecim brojem uredjaja.  
_#dvd+rw-format -blank /dev/dvd_  
Brzo praznjenje DVD-a.  
_#dvd+rw-format -blank=full /dev/dvd_  
Sporo praznjenje, ali puno. Traje koliko i pisanje citavog DVD-a.  
_#readcd dev=/dev/dvd f=slika.raw_  
Pravi sliku od DVD-a, isto mozemo uraditi i sa CD-om.  
  
Vecinu primera sam uzeo iz CD-Writing HowTo koji mozete naci na [www.tldp.org](http://www.tldp.org). Ovo jos uvek nije zavrsen tekst i nastojacu da ga dopunjujem. Naravno ne preuzimam odgovornost ako neki od ovih primera ne rade.

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=667)