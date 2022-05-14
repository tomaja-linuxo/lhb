---
author: tomaja
date: "2003-10-07T16:55:54Z"
excerpt: "Podrška za digitalne kamere na UNIXoidnim sistemima nije tako\njednostavna.
  Ve?ina ako ne i svi proizvoÄ‘a?i ne obra?aju mnogo pažnje na\nnon Windows (i MacOS)
  operativne sisteme. Ve?ina od njih ?ak ne\nobezbeÄ‘uje ni dokumentaciju kao podršku
  za svoje kamere. A sa pove?anjem\nbroja modela, sve ovo po?inje da raste kako Valvilonska
  kula. Sre?om,\ndanas izgleda da se izdvajaju dva pravca kada su u pitanju\nkomunikacioni
  protokoli: PTP i USB pohranjivanje podataka. Ipak, mnogi\njeftini modeli (oni koji
  imaju rezolucije manje od 1MPix \ti koštaju\nmanje od 150 USD ili 150 EUR) kamera
  još uvek neprate ove trendove ve?\nkoriste neke druge, manje popularne protokole.
  U ovom tekstu ?u\npokušati da objasnim kako da utvrdite da li vaš digitalni aparat
  može\nili ne može da radi pod Linux (Unix) sistemima. TakoÄ‘e, uz tekst dajemo\ni
  tabelu sa preko 640 razli?itih digitalnih foto aparata i to sa\npodatkom da li su
  podržani pod Linux sistemima.Dakle, kliknite na \"Read more...\" za tekst a tabelu
  sa spiskom od preko 640 digitalnih aparata možete pogledati <a\nhref=\"http://www.mandrake.co.yu/dig_kam_tab.html\"\nstyle=\"font-weight:
  bold;\">OVDE</a>\n"
guid: https://forum.linuxo.org/2003/10/07/podrska-za-digitalne-foto-aprate-za-linux-unix-i-bsd/
id: 379
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Podrška za digitalne foto aprate za Linux, Unix i BSD
url: /podrska-za-digitalne-foto-aprate-za-linux-unix-i-bsd/
---
Podrška za digitalne kamere na UNIXoidnim sistemima nije tako  
jednostavna. Ve?ina ako ne i svi proizvoÄ‘a?i ne obra?aju mnogo pažnje na  
non Windows (i MacOS) operativne sisteme. Ve?ina od njih ?ak ne  
obezbeÄ‘uje ni dokumentaciju kao podršku za svoje kamere. A sa pove?anjem  
broja modela, sve ovo po?inje da raste kako Valvilonska kula. Sre?om,  
danas izgleda da se izdvajaju dva pravca kada su u pitanju  
komunikacioni protokoli: PTP i USB pohranjivanje podataka. Ipak, mnogi  
jeftini modeli (oni koji imaju rezolucije manje od 1MPix i koštaju  
manje od 150 USD ili 150 EUR) kamera još uvek neprate ove trendove ve?  
koriste neke druge, manje popularne protokole. U ovom tekstu ?u  
pokušati da objasnim kako da utvrdite da li vaš digitalni aparat može  
ili ne može da radi pod Linux (Unix) sistemima. TakoÄ‘e, uz tekst dajemo  
i tabelu sa preko 640 razli?itih digitalnih foto aparata i to sa  
podatkom da li su podržani pod Linux sistemima.Dakle, kliknite na &#8222;Read more&#8230;&#8220; za tekst a tabelu sa spiskom od preko 640 digitalnih aparata možete pogledati <a
 href="http://www.mandrake.co.yu/dig_kam_tab.html"
 style="font-weight: bold;">OVDE</a><!--break-->

## USB kamere  


Danas su USB kamere naj?eš?e. Pošto je svaki USB ureÄ‘aj definisan  
kombinacijom ID brojem i proizvoÄ‘a?em, može se lako detektovati na  
bus-u. Obi?no sam bus može bezbedno da pretpostavi da su ureÄ‘aji  
sa sli?nim USB ID brojevima identi?ni, mada ?emo videti da ipakk postoje  
vidne razlike. 

Za protokol, postoje 2 USB standardizovana protokola koje  
koriste digitalni foto aparati ili kamere: USB Mass Storage i PTP  
(iliti Still Image Device). Ukoliko kamera ne koristi jedan od ova dva  
portokola, onda sigurno koristi podreÄ‘eni posebno licencirani protokol,  
i upravo tu stvari postajju neprijatne: ve?ina proizvoÄ‘a?a ne otkriva  
ove protokole javnosti iz raznoraznih razloga. U ovom slu?aju se  
primenjuje reversno inženjerstvo. 

### USB sistem za smeštanje podataka (Mass storage)  


USB Mass Storage je protokol koji koriste hard diskovi i prenosni  
ureÄ‘aji preko USBa. Ovo je u osnovi SCSI preko USB. Linux 2.4.x i  
*BSD sistemi po default-u mogu da obraÄ‘uju ove protokole. Sve što je  
potrebno jeste da pravilno montirate ureÄ‘aj u ta?ku montiranja po vašem  
izboru. Za Linux, pro?itajte ovo [posebno upustvo](http://www.linux-usb.org/USB-guide/x498.html)  
(eng.). 

U 2001, Olympus, Nikon, Minolta, Sony, Casio i mnogi drugi si po?eli  
standardno da koriste ovaj protoklol u svojim kamerama. Ovo je u  
mnogome pojednostavilo koriš?enje ovih aparata u razli?itim operativnim  
sistemima. Korisnici besplatnih OS su imali od ovoga najve?u korist:  
kamera radi bez ikakavih drugim pomagala ili softvera. Jedna od  
lošijih strana je ta da USB Mass Storage prtokol u osnovi protokol za  
disk ureÄ‘aje, pa zato ne možete da menjate opcije kamere ili da sa njom  
daljisnki upravljate. 

Za Casio aparate pro?itajte posebnu napomenu o [Casio specifikacijama](#casio-specifics) (eng.) 

### PTP

PTP, Picture Transfer Protokol, je standardizovani protokol koji je  
u osnovi razvio Kodak u cilju da obezbedi standardizovani na?in za  
pristup digialnim kamerama. Ovaj protokol je prihva?en od strane USB  
konzorcijuma za rad sa Still Image ureÄ‘ajima klase (6). Kompletna  
specifikacija ovog protokalo je objavljena pa je možete pro?itati [ovde](http://ptp.sourceforge.net/) (eng.). 

Od2001, Sony je izbio na drugo mesto, iza Kodaka, po  
implementaciji PTPa na svojim digitalnim aparatima, nude?i konjukciju  
sa USB Mass Storage. Do kraja 2002, Nikon je takoÄ‘e prešao na  
ovaj protokol nude?i nekoliko firmware upgrade-ova za podršku  
za PTP kao dodatak USB Mass Storage-u . Kanon je uradio istu  
stvar što je naro?ito zna?ajno jer je bio posednji od velikih  
proizvoÄ‘a?a koji nije koristio USB Mass Storage. 

### Drugi protokoli

#### Canon

Canon je verovatno poslednji veliki proizvoÄ‘a? koji se držao  
sopstvenih protokola. Upravo zbog toga je pravio i najviše problema  
kreatorima softverskih paketa kao što je na primer [gphoto2](http://gphoto.sf.net/). Oni su od skora takoÄ‘e  
prešli na PTP tako da su sada Canon kamere standardno sa USB  
konektorima, ali stariji modeli koriste stare protokole. TakoÄ‘e,  
pojedini modeli podržavaju ove vrste protokola. 

### Specifi?nosti pojedinih proizvoÄ‘a?a

Neki proizvoÄ‘a?i digitalnih foto aparata koriste sopstvene  
specifikacije koje se teže podržavaju softverom.

 <a name="casio-specifics"></a><a name="casio-specifics"></p> 

<h4>
  Casio
</h4>

<p>
  </a>
</p>

<p>
  Sve najnovije Casio kamere koriste USB Mass Storage ureÄ‘aje. Na<br /> žalost, njihova implementacija nije standardna. Sre?om, po Linux<br /> korisnike, postoji <a href="http://www.harald-schreiber.de/">dokument</a><br /> koji rešava ove probleme
</p>

<p>
  <a name="nikon-specifics"></p> 
  
  <h4>
    Nikon
  </h4>
  
  <p>
    </a>
  </p>
  
  <p>
    Prebacivanje Nikon kamera u PTP mod je dostupan (ovo zavisi od<br /> verzije firmware-a kamere): Idite na interfejs za podešavanje kamere<br /> i izaberite &#8222;PTP&#8220;. Default je obi?no &#8222;Mass Storage&#8220;.
  </p>
  
  <h2>
    Korisni linkovi
  </h2>
  
  <ul>
    <li>
      <a href="http://www.geocities.com/piccolbo/dplinux.html">Digitalna<br /> fotografija i Linux</a>
    </li>
  </ul>
  
  <p>
    Tabelu sa spiskom od preko 640 digitalnih aparata možete pogledati <a
 href="http://www.mandrake.co.yu/dig_kam_tab.html"
 style="font-weight: bold;">OVDE</a>
  </p>
  
  <p>
    <a href="https://linuxo.org/nova-tema-na-forumu/?se_pid=379">Креирај тему форума везану за овај текст</a>
  </p>