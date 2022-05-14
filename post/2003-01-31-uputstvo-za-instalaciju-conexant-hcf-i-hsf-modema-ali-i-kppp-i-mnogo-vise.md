---
author: tomaja
date: "2003-01-31T18:50:11Z"
excerpt: |
  Ovo je detaljno uputstvo o instaliranju drajvera za modeme sa Conexant HCF i HSF ?ipsetom!!!<br>
  TakoÄ‘e ovde su i predlozi rešenja nekih naj?eš?ih problema koji vam se mogu pojaviti u radu sa vašim modemom ako koristite kppp dial-up tool.<br>
  Ovde ?u pokušati navesti sve probleme na koje sam naišao u Mandrake, RedHat i SuSe distribuciji i to verzije Mandrake 9.0, RedHat 8.0 i SuSe 8.1 kao i sva moja rešenja tih istih problema.
guid: https://forum.linuxo.org/2003/01/31/uputstvo-za-instalaciju-conexant-hcf-i-hsf-modema-ali-i-kppp-i-mnogo-vise/
id: 285
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Uputstvo za instalaciju Conexant HCF i HSF modema ali i KPPP i mnogo više!
url: /uputstvo-za-instalaciju-conexant-hcf-i-hsf-modema-ali-i-kppp-i-mnogo-vise/
---
Ovo je detaljno uputstvo o instaliranju drajvera za modeme sa Conexant HCF i HSF ?ipsetom!!!  
TakoÄ‘e ovde su i predlozi rešenja nekih naj?eš?ih problema koji vam se mogu pojaviti u radu sa vašim modemom ako koristite kppp dial-up tool.  
Ovde ?u pokušati navesti sve probleme na koje sam naišao u Mandrake, RedHat i SuSe distribuciji i to verzije Mandrake 9.0, RedHat 8.0 i SuSe 8.1 kao i sva moja rešenja tih istih problema.<!--break-->

NAGLAÅ AVAM da je mogu?e da se pojave neki dodatni problemi na koje nisam dao odgovor, i u tom slu?aju pitajte na forumu i prou?ite detaljno man stranice i dokumentaciju do koje možete do?i.

Administratorima predlažem da prvo referišu ljude na ovaj link, a korisnicima da ovo uputstvo detaljno pro?itaju i tek zatim postavljaju pitanja na forumu, pošto prime?ujem da je tema aktuelna i da se pitanja previše ?esto ponavljaju.

Unapred napominjem da NE odgovaram za bilo kakvu štetu koja može biti posledica koriš?enja saveta iz ovog uputstva ili drajvera koje obezbeÄ‘uju Conexant Systems Inc. i Marc Boucher.  
Ko se nije uplašio ovog nek nastavi da ?ita 🙂

Dakle evo jedne ve?eri seo sam i odlu?io da podelim sa svim posetiocima www.mandrake.co.yu sajta ono do ?ega sam došao u mukama sa mojim softverskim modemom (ako nekog zanima radi se konkretno o Diamond Supra 56v PRO modemu sa Conexant HCF ?ipsetom).  
Zbog razloga navedenog u zagradi iako su drajveri, problemi i rešenja sli?na za Conexant HCF i HSF porodicu modema, ipak bi rekao da imam mnogo više iskustva sa HCF ?ipsetom, pa da se neko ko ima HSF ?ipset ne naljuti ako nešto ne bude ispalo kako je Marko rekao 🙂 ali svi samo hrabro na ?itanje jer ovde ?ete na?i uglavnom sve što ste hteli da pitate.

**KAKO DA SAZNAM DA LI IMAM OVAJ ?IPSET ?**  
Pa ja vam predlažem da odete prvo na: <http://linmodems.org/>  
Tamo ?ete na?i detaljno uputstvo kako da saznate koji ?ipset na vašem modemu imate.

Nakon toga treba da posetite stranicu: <http://www.idir.net/~gromitkc/winmodem.html>  
To je stranica jednog super ?oveka po imenu Rob Clarke (ovim putem posebno hvala njemu) i tamo vam se nalazi najve?i listing svih modema, winmodema i linmodema.  
Tamo prosto kliknete na: view pci list ili view usb list ili nešto tre?e zavisno od vrste modema koji imate (u slu?aju Conexant HCF i HSF modema to je na pci listi).

**OK, ZNAM DA IMAM TA?NO CONEXANT HCF ILI HSF ?IPSET, Å TA DALJE ?**  
Pa prvi korak jeste naravno na?i odgovaraju?e drajvere.  
Da bi to uspešno odradili potrebno je da znate slede?e:  
1. Koju distribuciju Linuxa posedujete (to sigurno svi znate al svejedno napominjem)  
2. Verziju kernela koju posedujete.  
Da bi saznali verziju kernela u konzoli u Linuxu kucajte:  
#uname -r  
i ispisa&#230;e vam se nešto sli?no ovome u slu?aju Mandrake 9.0:  
2.4.19-16mdk  
ili npr. ovo ako imate SuSe 8.1  
2.4.19-4GB  
3. Nije zgoreg znati i koju procesorsku porodicu imate tj. kako vas je deklarisao vaš Linux. Isto možete saznati sa:  
#uname -m

Kada ste saznali sve te podatke onda kliknite [ovde za HCF ?ipset](https://linuxo.org/?p=4#hcf) ili [ovde za HSF ?ipset](https://linuxo.org/?p=4#hsf) ili skrolujte niže ovu stranu.

**<a name="hcf">HCF ?IPSET: DRAJVERI I INSTALACIJA</a>**  
Idite na stranicu: <http://www.mbsi.ca/cnxtlindrv/hcf/> i tamo ?ete prvo na?i opis vašeg ?ipseta i modema.  
Sazna?ete da se radi o modemu bez kontrolera:  
Conexant Systems, Inc. formerly Rockwell Semiconductor Systems  
PCI bus controllerless (HCF) modem

Na toj istoj www stranici s leve strane na?i ?ete **link za download drajvera**, a ako niste sigurni možete to i odavde direktno preko stranice: <http://www.mbsi.ca/cnxtlindrv/hcf/downloads-license.html>

Kada se složite sa licencom i uslovima (kliknete na ono I Agree :-)) mo?i ?ete da birate vašu Linux distribuciju i zatim odreÄ‘eni .rpm fajl koji ?ete izabrati prema vašem kernelu i eventualno procesorskoj porodici.  
Downloadujte odgovaraju?i fajl.  
Detaljno uputstvo o instalaciji tih drajvera se nalazi na adresi: <http://www.mbsi.ca/cnxtlindrv/hcf/install.html>  
Uglavnom se sve svodi na to da kopirate .rpm fajl na vašu Linux particiju i uradite jedno:  
#rpm -i ime\_rpm\_paketa  
Trebalo bi da se pokrene instalacija drajvera i po završetku da vam modem bude dostupan preko /dev/ttySHCF0, /dev/cuaHCF0 (call-out device) ili simboli?kog linka /dev/modem (koji je ustvari link na ttySHCF0).  
Ako nemate simboli?ki link takvog imena možete ga sami napraviti komandom:  
#ln -s /dev/modem /dev/ttySHCF0

Nakon instalacije raznim podešavanjima u vezi modema mo?i ?ete da pristupite komandom:  
#hcfpciconfig  
a optimalno izvršite:  
#hcfpciconfig &#8211;country  
Ne?ete mo?i odabrati Jugoslaviju jer je nema na listi (heh a ne?e je biti uskoro ni na karti evrope) ali meni je modem sasvim dobro radio sa USA kao izborom zemlje.

Zatim pokrenite kppp i uÄ‘ite u Setup (ili Podešavanja za korisnike Mandrake 9.0 na srpskom) i idite na stavku Modem i probajte opciju Query Modem (ATI Upiti modema) da bi videli da li vam kppp registruje drajvere i modem.  
Možete takoÄ‘e probati i da otvorite Terminal i da ukucate neku od AT komandi kao npr. ATA (trebalo bi da ?ujete vaš modem kako kr?i i šušti tj. inicijalizuje se i javlja svoje prisustvo).  
Zatim podesite svoje internet konekcije (naglašavam da to NE radite pomo?u Wizarda (?arobnjaka) ) i sre?no surfovanje i sve ostalo ?ime se zanimate na internetu.

**Ako imate problema sa radom sa vašim modemom pro?itajte [OVO](https://linuxo.org/?p=4#faq).**

**<a name="hsf">HSF ?IPSET: DRAJVERI I INSTALACIJA</a>**  
Idite na stranicu: <http://www.mbsi.ca/cnxtlindrv/hsf/> i tamo ?ete prvo na?i opis vašeg ?ipseta i modema.  
Sazna?ete da se radi o soft modemu:  
Conexant Systems, Inc. formerly Rockwell Semiconductor Systems  
PCI bus soft (HSF) modem 

Na toj istoj www stranici s leve strane na?i ?ete **link za download drajvera**, a ako niste sigurni možete to i odavde direktno preko stranice: <http://www.mbsi.ca/cnxtlindrv/hsf/downloads-license.html>

Kada se složite sa licencom i uslovima (kliknete na ono I Agree :-)) mo?i ?ete da birate vašu Linux distribuciju i zatim odreÄ‘eni .rpm fajl koji ?ete izabrati prema vašem kernelu i eventualno procesorskoj porodici.  
Downloadujte odgovaraju?i fajl.  
Detaljno uputstvo o instalaciji tih drajvera se nalazi na adresi: <http://www.mbsi.ca/cnxtlindrv/hsf/install.html>  
Uglavnom se sve svodi na to da kopirate .rpm fajl na vašu Linux particiju i uradite jedno:  
#rpm -i ime\_rpm\_paketa  
Trebalo bi da se pokrene instalacija drajvera i po završetku da vam modem bude dostupan preko /dev/ttySHSF0, /dev/cuaHSF0 (call-out device) ili simboli?kog linka /dev/modem (koji je ustvari link na ttySHSF0).  
Nakon instalacije raznim podešavanjima u vezi modema mo?i ?ete da pristupite komandom:  
#hsfconfig  
a optimalno izvršite:  
#hsfconfig &#8211;country  
Ne?ete mo?i odabrati Jugoslaviju jer je nema na listi (heh a ne?e je biti uskoro ni na karti evrope) a ne bi znao koju zemlju da vam preporu?im jer nisam li?no probao HSF modem i drajvere. Za HCF ?ipset radilo je sve ok sa USA.

Zatim pokrenite kppp i uÄ‘ite u Setup (ili Podešavanja za korisnike Mandrake 9.0 na srpskom) i idite na stavku Modem i probajte opciju Query Modem (ATI Upiti modema) da bi videli da li vam kppp  
registruje drajvere i modem.  
Možete takoÄ‘e probati i da otvorite Terminal i da ukucate neku od AT komandi kao npr. ATA (trebalo bi da ?ujete vaš modem kako kr?i i šušti tj. inicijalizuje se i javlja svoje prisustvo).  
Zatim podesite svoje internet konekcije (naglašavam da to NE radite pomo?u Wizarda (?arobnjaka) ) i sre?no surfovanje i sve ostalo ?ime se zanimate na internetu.

**Ako imate problema sa radom sa vašim modemom pro?itajte [OVO](https://linuxo.org/?p=4#faq).**

**<a name="faq">MOGUÄ†I PROBLEMI I NJIHOVA MOGUÄ†A REÅ ENJA KAO I MOGUÄ†A PITANJA I MOGUÄ†I ODGOVORI 🙂</a>**  
Pre nego što vam ponudim rešenja problema na koje sam ja li?no naišao prvo bi vas uputio na:  
[HCF (controllerless) Driver FAQ (Frequently Answered Questions, iliti odgovori na ?esta pitanja)](http://www.mbsi.ca/cnxtlindrv/hcf/faq.html)  
i  
[HSF (softmodem) Driver FAQ (Frequently Answered Questions, iliti odgovori na ?esta pitanja).](http://www.mbsi.ca/cnxtlindrv/hsf/faq.html)  
Iste te stranice pored interneta možete na?i i na sopstvenom kompjuteru nakon instalacije drajvera, pošto .rpm paket instalira i svu potrebnu dokumentaciju iako vam to nigde ne prijavljuje.  
Ta dokumentacija obi?no se nalazi u /usr/share/doc/ime_paketa/ direktorijumu na vašoj Linux particiji.

Sada ?u pokušati da prvo po distribucijama navedem sve probleme na koje sam  
naišao i da objasnim kako sam ih rešio, a zatim da objasnim rešenja i par zajedni?kih problema za sve distribucije.

MANDRAKE 9.0

PITANJE:  
Kada pokušam da zovem neki broj ili uradim Query Modem (ati upit modema) kppp mi prijavljuje grešku can&#8217;t find modem (ne mogu da pronaÄ‘em modem), modem not present(modem ne postoji) ili can&#8217;t initialize modem(ne mogu da inicijalizujem modem). To se dešava odmah nakon instalacije drajvera ili posle restarta mašine. U ?emu je problem?  
ODGOVOR:  
Prvo što treba da uradite jeste da odete u vaš /dev/ direktorijum gde vam se nalaze svi ureÄ‘aji koje posedujete na ra?unaru (tj. njihovi izvršni fajlovi, pošto je pojam ureÄ‘aja mnogo širi od jednog direktorijuma) i da izlistate sadržaj istog.  
Ako je sve ok na listi ureÄ‘aja trebali bi da pronaÄ‘ete za HCF modeme fajl po imenu: ttySHCF0  
a za HSF modeme fajl: ttySHSF0  
U devfs baziranim operativnim sistemima kao što je Mandrake može do?i do toga da postoje drajveri ali nisu pravilno u?itani i inicijalizovani pa odgovaraju?i modul (device node) ne vidite. Dakle ako doti?ni fajl ne postoji na listi ureÄ‘aja u direktorijumu /dev/ mora?ete da malo &#8222;prodrmate&#8220; vaše drajvere da bi se pravilno u?itali i pokrenuli.  
**Za HCF modeme to možete uraditi komandom:**  
  
#modprobe hcfpciserial  
i po potrebi možete uraditi još jedno:  
#hcfpciconfig &#8211;country  
U svakom slu?aju probajte prvo jedno pa proverite da li vam se sad pojavio ttySHCF0 ureÄ‘aj pa ako nije probajte drugo i trebalo bi da se pojavi na listi ureÄ‘aja.  
**Za HSF modeme to možete uraditi komandom:**  
#modprobe hsfserial  
i po potrebi možete uraditi još jedno:  
#hsfconfig &#8211;country  
U svakom slu?aju probajte prvo jedno pa proverite da li vam se sad pojavio ttySHSF0 ureÄ‘aj pa ako nije probajte drugo i trebalo bi da se pojavi na listi ureÄ‘aja.

U slu?aju da su drajveri dobro u?itani i da ureÄ‘aji postoje, a dobijate i dalje poruku **can&#8217;t initialize modem (ne mogu da inicijalizujem modem)** probajte da menjate svoj Initialization string 0 u Setup-u kppp-a (ili Podešavanju za one koji teraju Mandrake na srpskom). Kod mene je sve radilo super sa stringom ATZ, a isto tako sam ?uo da je i kod drugih, dakle obavezno prvo probajte sa tim stringom a posle možete probati ATX3 ili neki drugi string, iako ja mislim da je ATZ ono što ?e najbolje raditi posao.

REDHAT 8.0

E pa RedHat moram da pohvalim u vezi rada sa ovom vrstom softverskih modema sa Conexant HCF ili HSF ?ipsetom, pošto jedino mi on nije pravio nikakvih posebnih i karakteristi?nih problema, a drajveri su radili dobro. Jedino je tražio pristup kppp-u kao root ali to je verovatno mogu?e podesiti pa da i obi?ni korisnici mogu startovati kppp (detaljna uputstva u vezi administracije možete na?i u helpu kppp-a)  
Ovo što navodim ovde ne zna?i da treba da preÄ‘ete na RedHat 🙂 jer glavna stvar je u drajverima, koji su nažalost još uvek u beta verziji i verovatno nisu baš jednako kvalitetno napisani za svaku distribuciju što morate priznati i da je dosta teško uraditi (treba ipak znati strukturu svake distribucije i potencijalne izmene u novim verzijama plus naravno sve mogu?e probleme koji se mogu pojaviti)  
Dakle ovo nije nikakva reklama RedHat-a nego ?isto objektivan komentar rada sa modemom, ako je neko naišao na neke probleme u toj distribuciji i karakteristi?ne za tu distribuciju, nek piše o tome i nek navede svoja rešenja.

SUSE 8.1

Ovaj deo uputstva napisan je iz li?nog iskustva i na osnovu pomo?i jednog korisnika www.mandrake.co.yu sa korisni?kim imenom Sava iz Beograda i gospodina po imenu Harri Porten koji održava FAQ stranice kppp-a i u?estvuje u razvoju istog.  
Ovim putem hvala obojici na pomo?i.  
PITANJE:  
Zašto nemam instaliran kppp?  
ODGOVOR:  
Pa to možete da pitate autore SuSe-a 🙂 objašnjenje je vrlo jednostavno. Default dial-up tool za SuSe je kinternet, a default pppd deamon smpppd. Dakle ako instalirate KDE sa instalacionih diskova, SuSe ?e vam instalirati kinternet i wvdial a kppp mora?ete eksplicitno da navedete (u prevodu da sami pronaÄ‘ete isti i kliknete na install) ili da naknadno instalirate isti preko Install or remove software plugin-a ili YAST kontrolnog centra.

PITANJE:  
Kada prvi put startujem kppp on mi prijavljuje greške sli?ne ovome:  
1) smpppd has no suid set  
2) there is no resolv.conf file  
Kako da eliminišem te greške?  
ODGOVOR:  
1) Idite u direktorijum /usr/sbin/ i naÄ‘ite fajl po imenu smpppd. Izvršite u konzoli komandu:  
#chmod u+s smpppd  
ili podesite Set UID preko properties dijaloga fajla smpppd iz bilo kog file browsera (koji naravno mora biti pokrenut od strane root-a).  
2) Napravite prazan tekst fajl po imenu resolv.conf i snimite ga u vaš /etc/ direktorijum.  
Nakon ova dva koraka trebalo bi da možete startovati kppp bez da vam prijavljuje bilo kakve greške.

PITANJE:  
Ok ovo iz prethodnog pitanja je rešeno ali nailazim na slede?i problem. Query modem radi ok, isto tako kppp krene da zove broj mog provajdera ali u momentu kada bi trebao da se priklju?i na mrežu (kad stane negotiation tj. ono šuštanje i kr?anje :-)) odjednom pukne veza i izbaci mi slede?u grešku:  
The pppd daemon died unexpectedly!  
Exit status: 2  
See &#8216;man pppd&#8217; for an explanation of the error codes or take a look at the kppp FAQ on http://devel-home.kde.org/~kppp/index.html  
ODGOVOR:  
Da bi rešili taj problem uradite slede?e korake:  
1. u /etc/ppp/peers/ napravite tekstualni fajl koji ?ete nazvati kppp i koji ?e sadržati samo jednu liniju teksta i to:  
plugin passwordfd.so  
2. proverite da imate istu liniju u /etc/ppp/peers/ppp fajlu (bi?e verovatno tamo pošto SuSe napravi taj fajl prilikom instalacije)  
3. naÄ‘ite fajl sa imenom: passwordfd.so (nalazi se u: /usr/lib/pppd/2.4.1/ ) i proverite da svi korisnici mogu da ?itaju i izvršavaju taj fajl (po potrebi uradite chmod) dakle da ima (r i x dozvole za root-a, grupu i ostatak sveta 🙂 ).  
Listing tog direktorijuma trebalo bi da izgleda otprilike ovako:  
marko@linux:/usr/lib/pppd/2.4.1> ls -l  
total 144  
-rwxr-xr-x 1 root root 63657 2002-09-10 18:42 capiplugin.so  
-rwxr-xr-x 1 root root 5295 2002-09-09 22:32 minconn.so  
-rwxr-xr-x 1 root root 7725 2002-09-09 22:32 passprompt.so  
-rwxr-xr-x 1 root root 5913 2002-09-09 22:32 passwordfd.so  
-rwxr-xr-x 1 root root 10564 2002-09-09 22:32 pppoatm.so  
-rwsr-xr-x 1 root root 37244 2002-09-09 22:32 pppoe.so  
-rwsr-x  
r-x 1 root root 3026 2002-09-10 18:42 userpass.so  
4. editujte /etc/ppp/options fajl i komentarišite liniju:  
lock  
5. naÄ‘ite kppp izvršni fajl (nalazi se u: /opt/kde3/bin/ ) i uradite:  
#chmod u+s kppp  
Posle svega toga sve bi trebalo da radi ok ako kppp pokrenete kao root.  
Da bi omogu?ili da sve radi ako pokre?ete kppp kao obi?an korisnik morate ponovo da editujete fajl options u direktorijumu /etc/ppp/ i da komentarišete (tj. dodate jedno # na njen po?etak) liniju:  
noauth

ZAJEDNI?KI PROBLEMI DISTRIBUCIJA TJ. PROBLEMI SA KPPP-om

PITANJE:  
kppp zove broj telefona, zatim ?ujem pregovaranje izmeÄ‘u mog modema i provajdera (tj. za vaše uho ?uveno kr?anje i šuštanje:-) ) MeÄ‘utim kada o?ekujem da se priklju?im na mrežu u Log prozoru (koji sam naravno otvorio da bi pratio poruke u vezi rada modema!) mi se pojavljuju neke kuke i kvake a zatim se ubrzo prekida veza. Å ta je problem?  
ODGOVOR:  
Pa verovatno se radi o tome da niste poslušali uputstvo da ne koristite wizarda (iliti ?arobnjaka) pri pravljenu konekcije za provajdera. Idite u Setup (Podešavanja) i tamo idite na Accounts (Nalozi) tab i selektujte nalog u prozoru ispod i kliknite na Edit (Izmeni) s desne strane. Unutar dijaloga koji vam se otvori potražite Login Script (login skripte) opciju i pristupite istoj. Tamo NE sme ništa da vam bude zapisano u suprotnom traži?ete od vašeg dial-up programa da o?ekuje odreÄ‘ene identifikacije od provajdera ili odreÄ‘enu razmenu podataka koju naši provajderi ne podržavaju. Obrišite ako imate bilo šta zapisano tamo, kliknite na ok koliko puta treba i pokušajte ponovo da se priklju?ite. Nadam se da ?e sada biti sve ok.

Toliko u ovom uputstvu, nadam se da ?e nekome zaista pomo?i.

Kopiranje teksta za li?nu upotrebu dozvoljeno, a ako neko planira da ga komercijalizuje:-) bio bi zahvalan da mi piše pa da se zajedno obogatimo:-).

Autor:  
[Markominus](mailto:mmarko@softhome.net)

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=285)