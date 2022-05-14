---
author: tomaja
date: "2003-01-18T04:31:16Z"
excerpt: |
  Dakle o instalacijama Linux Mandrake-a se puno pri?alo i ja preporu?ujem da pro?itate uputstva na slede?im adresama:
  <a href="http://mandrake.osny.org.yu/modules.php?name=News&file=article&sid=64&mode=thread&order=0&thold=0">http://mandrake.osny.org.yu/modules.php?name=News&file=article&sid=64&mode=thread&order=0&thold=0</a>
  <a href="http://mandrake.osny.org.yu/modules.php?name=News&file=article&sid=83&mode=thread&order=0&thold=0">http://mandrake.osny.org.yu/modules.php?name=News&file=article&sid=83&mode=thread&order=0&thold=0</a><br><br>
  Ja ?u pokušati samo da sumiram neke stvari oko instalacije i da dodam ono što mislim da nedostaje i jedan kratak deo o instaliranju male lokalne mreže bar onoliko koliko ja znam.
guid: https://forum.linuxo.org/2003/01/18/osnovna-instalacija-linux-a-i-male-lan-mreze/
id: 269
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Osnovna instalacija Linux-a i male LAN mreže
url: /osnovna-instalacija-linux-a-i-male-lan-mreze/
---
Dakle o instalacijama Linux Mandrake-a se puno pri?alo i ja preporu?ujem da pro?itate uputstva na slede?im adresama:  
<http://mandrake.osny.org.yu/modules.php?name=News&file=article&sid=64&mode=thread&order=0&thold=0>  
<http://mandrake.osny.org.yu/modules.php?name=News&file=article&sid=83&mode=thread&order=0&thold=0>

Ja ?u pokušati samo da sumiram neke stvari oko instalacije i da dodam ono što mislim da nedostaje i jedan kratak deo o instaliranju male lokalne mreže bar onoliko koliko ja znam.<!--break-->

**OSNOVNA INSTALACIJA:**  
Dakle prvo da krenemo o instalaciji uopšte 🙂  
Prvo pretpostavljam da ste svi bili korisnici windowsa i da ve? imate isti pre instalacije Linuxa.  
Ako želite da imate samo Linux na kompjuteru samo pokrenite instalaciju Linuxa i preformatirajte windows particije i instalirajte Linux.  
Ako želite da imate istovremeno instaliran windows i Linux onda ?ete se malo više namu?iti 🙂  
Dakle prvo ja preporu?ujem da pripremite particije za Linux pre pokretanja njegove instalacije, to možete uraditi npr. sa Partition Magic-om iz windowsa.

Minimalno su vam potrebne dve particije:  
**jedna particija** gde ?ete instalirati sam Linux (tipa ext2, ext3 ili nekog tre?eg, poreÄ‘enje tih razli?itih fajl sistema stoji na sajtu kao tekst:  
<http://mandrake.osny.org.yu/modules.php?name=News&file=article&sid=97&mode=thread&order=0&thold=0>)

Za kompletnu instalaciju svih paketa koji dolaze na 3 CD-a Mandrake Linux-a potrebno je nešto preko 2GB prostora na hard disku, dakle vi odredite sami koliko ?e vam još pored toga trebati prostora za svakodnevne potrebe i tako odredite veli?inu te particije

**druga particija** treba da bude prazna i treba da bude swap particija koju Linux koristi kao virtuelnu memoriju.  
kod mene na mom kompjuteru ta particija je 400 MB al možete staviti i više zavisno od toga koliko mislite da ?e programi u kojima ?ete raditi zahtevati upotrebu te swap particije.  
Ipak da napomenem da bi minimalno veli?ina te particije trebala da bude bar jednaka koli?ini RAM memorije koju posedujete na ra?unaru.  
Neki preporu?uju da bude dva puta ve?a od veli?ine RAM-a ali to svakako ne treba biti veli?ina u gigabyte-ima (GB) (osim ako naravno nemate toliko RAM memorije 🙂 kamo sre?e 🙂 ) jer ne?ete ništa time dobiti osim što ?e vam ostati puno neiskoriš?enog prostora.

Kad ste obezbedili particije možete krenuti u instalaciju Mandrake Linux-a.  
O samoj instalaciji je re?eno dosta i svodi se na jednostavno pra?enje uputstava i detaljno ?itanje objašnjenja koja su ponuÄ‘ena.  
Ako imate sre?e 🙂 ili samo ?este i standardne ureÄ‘aje nekih poznatijih firmi onda ?e Linux ve?inu ureÄ‘aja sam detektovati i instalirati, iz tog razloga predlažem da expert installation izaberete samo ako dobro poznajete svoju konfiguraciju i ranije ste ve? imali iskustva s instaliranjem neke verzije Linux-a.

Treba da obratite pažnju na nekoliko delova instalacije:  
**1.**Pazite koju particiju birate za instalaciju Linux-a.  
Instalacioni program ?e vam grafi?ki i tekstualno ozna?iti sve particije na vašem hard disku i ako kliknete na type onda ?ete videti kog fajl tipa je odreÄ‘ena particija.  
?ini mi se da obi?no windows-ove particije ozna?ava s plavom bojom, a Linux-ove crvenom i zelenom, al vi za svaki slu?aj proverite koja je šta.  
Dakle treba samo da proglasite prvu particiju u ext2,ext3 ili ve? nekom fajl sistemu za koji ste se odlu?ili za root particiju (u mount postavite / ) i da kažete Linux-u da se tamo instalira.

**2.**Obavezno unesite lozinku za root-a i bar još jednog korisnika

**3.**Ovo vam se može ?initi banalno, al ipak pazite na to da ne bi pitali posle kako da podesite sat:-) Dakle kad vas Linux pita kako želite da setuje sistemski sat nemojte selektovati ništa od ponuÄ‘enog nego samo kliknite ok 🙂 Na taj na?in ?e vam satovi u windows-u i Linux-u biti sinhronizovani.

**4.**Odlu?ite gde ?ete instalirati LILO (Linux boot loader).  
Instalacija vam nudi dve opcije:  
**prva ponuÄ‘ena opcija** je instalacija boot loadera u MBR (Master Boot Record tj. u prvi sektor celog hard diska) ako to odaberete LILO ?e vam pregaziti bilo koji drugi boot program koji možete imati npr. Boot Magic ali to samo zna?i da ?ete preko Linux-ovog boot loadera startovati windows pošto ?e Linux prepoznati da li imate još neki operativni sistem na vašem kompjuteru.  
**druga ponuÄ‘ena opcija** je instalacija boot loadera na prvu Linux-ovu particiju, u tom slu?aju ?e vam trebati neki windows program za bootovanje pa ?ete njime birati izmeÄ‘u windowsa i Linux-a

**5.**Obratite pažnju da li imate winmodem  
Ako imate takav modem i Linux ga nije prepoznao, najbolje je da ne unosite nikakve vrednosti u delu instalacije koja se odnosi na modem i internet.  
Ako postoje drajveri za vaš winmodem, onda ?ete morati svakako sve posle da podesite ru?no i instalirate iste.  
Podržane winmodeme u Linux-u (i oni koje prepoznaje i one za koje postoje drajveri) možete videti na strani:  
<http://www.idir.net/~gromitkc/winmodem.html>  
A više o problemu softverskih modema, možete pro?itati i na:  
<http://www.linmodems.org/>

**OSNOVNA INSTALACIJA LAN MREÅ½E:**  
Pri instalaciji samog operativnog sistema Linux ?e vam obi?no sam prepoznati koju mrežnu kartu posedujete i onda se podešavanje vaše lokalne mreže pri instalaciji svodi na unošenje imena servera, IP adrese lokalnog ra?unara i IP adrese za Gateway (IP adresa ra?unara koji je priklju?en ili s kojeg se priklju?ujete na internet).  
Za lokalne mreže obi?no se IP adrese ra?unara kre?u u opsegu od 192.168.0.0 do 192.168.255.255  
  
Ta?ne adrese pojedinih mašina mora?ete sami da odredite ali obi?no ?e vašim kompjuterima biti dodeljene adrese redom recimo 192.168.0.1 pa 192.168.0.2 itd.

Ina?e Linux vašu mrežnu kartu specificira kao eth0 (od ethernet) a ako ih imate više bi?e im dodeljene oznake eth1, eth2 itd.  
Svi programi potrebni za rad u mreži nalaze se na instalacionim diskovima Linux Mandrake-a i sli?no je i sa svim drugim distribucijama.  
Jedino bi posebno naglasio da ne zaboravite da instalirate SAMBU (Samba server) pošto je to osnova za rad u mreži sa ra?unarima na kojima su instalirani razli?iti operativni sistemi.

Ja sam za kasnija dodatna podešavanja koristio program Netconf koji možete na?i u Configuration/Network u KDE grafi?kom okruženju kada pokrenete kicker 🙂 (ono K na mestu gde je windows-ovo start dugme)  
Kad pokrenete Netconf (treba da budete logovani kao root) treba samo da obratite pažnju na Name Server Specification (DNS) i Host Name And IP Network Device.  
Neke opcije ?e tamo ve? biti ispunjene a ostale ?ete možda morati sami da podesite ali uglavnom svodi se na ve? prethodno objašnjene IP adrese lokalnog kompjutera i komšijskih 🙂

Ako ste dobro podesili sve adrese i instalirali sav neophodan softver trebalo bi da vaš kompjuter vidi sve ostale kompjutere u mreži i da iz bilo kog file browsera (npr. konqueror) možete u listi s leve strane na?i posebnu opciju (verovatno ?e stajati smb) pod kojom se nalaze kompjuteri u mreži.  
Konkretno nekom od umreženih ra?unara se iz konqueror-a pristupa kucanjem  
smb://IP\_adresa\_kompjutera  
kao URL-a u odgovaraju?em prozoru programa.  
Npr.: smb://192.168.0.2 ?e prikazati share-ovane direktorijume na umreženom kompjuteru sa tom IP adresom.

**Å ta je sharing?**  
Pa zbog zaštite privatnosti i ve?e efikasnosti mreže na svakom kompjuteru u mreži treba da odredite koji direktorijumi i fajlovi ?e biti vidljivi preko mreže i dostupni drugim korisnicima preko mreže.  
Dakle ako na drugom ra?unaru imate windows morate na njemu odrediti šta delite s mrežom, konkretno to možete uraditi prostim desnim klikom na direktorijum i biranjem opcije Sharing iz padaju?eg direktorijuma.  
Možete odreÄ‘ivati i nivo pristupa drugim korisnicima, tako možete da podesite da neki direktorijumi i fajlovi budu read-only (tj. da se preko mreže mogu samo ?itati) ili da recimo imaju full pristup (tj. da se preko mreže mogu i menjati, izvršavati, snimati itd.)  
U windows-u sadržaju umreženih kompjutera pristupate preko Network Neighborhood-a u Exploreru ili Windows Commander-u&#8230; Trebalo bi da vam se pokažu posebne ikone za svaki kompjuter u mreži sa njegovim imenom.  
S tim da postoji problem koriš?enja i vidljivosti Linux-ovih particija, ta?nije Linux bez problema vidi sve, a windows uglavnom ne vidi:-)  
Ko zna neki dobar i lak na?in da se omogu?i vidljivost preko mreže Linux-ovih share-ovanih direktorijuma iz raznih verzija windows-a nek sastavi svoj tekst samo o tome.

Da se na kraju nadovežem na svoj prethodni tekst:  
moglo bi vam biti zanimljivo da ako imate instaliran i pokrenut apache webserver na Linux mašini u mreži, kucanjem IP adrese tog kompjutera u bilo kom browser-u u windows-u ili bilo kom drugom operativnom sistemu komšijskog kompjutera otvori?e vam se sajt koji možda hostujete na tom Linux kompjuteru u odreÄ‘enom direktorijumu, dakle vaša prezentacija ili prezentacije na Apache web serveru postaju upotrebljive i vidljive svima u mreži i eto imate jedan pravi mali intranet.

Tekst napisao:[Markominus](mailto:mmarko@softhome.net)  
Umnožavanje i kopiranje je dozvoljeno do mile volje 🙂

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=269)