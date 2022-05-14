---
author: tomaja
date: "2002-12-28T14:39:19Z"
excerpt: |
  Prvo da napomenem da je ovo uputstvo za pocetnike i ljude koji zele da koriste Apache na lokalnoj masini ili kao mali server.
  Dakle u ovom tekstu necu ulaziti u ozbiljne price o portovima, IP adresama, sigurnosti i slicno.
  Ako ste Linux i Apache profesionalac ili administrator neke ozbiljne mreze ili servera onda ce ovo za vas biti nesto sto odavno znate, a ako niste citajte do kraja i mozda resite neke nedoumice ili probleme :)
guid: https://forum.linuxo.org/2002/12/28/uputstvo-za-pocetnike-apache-i-resenja-nekih-cestih-problema/
id: 258
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: 'Uputstvo za pocetnike: Apache i resenja nekih cestih problema.'
url: /uputstvo-za-pocetnike-apache-i-resenja-nekih-cestih-problema/
---
Prvo da napomenem da je ovo uputstvo za pocetnike i ljude koji zele da koriste Apache na lokalnoj masini ili kao mali server.  
Dakle u ovom tekstu necu ulaziti u ozbiljne price o portovima, IP adresama, sigurnosti i slicno.  
Ako ste Linux i Apache profesionalac ili administrator neke ozbiljne mreze ili servera onda ce ovo za vas biti nesto sto odavno znate, a ako niste citajte do kraja i mozda resite neke nedoumice ili probleme 🙂

<!--break-->Ovo kratko uputstvo sam napisao iz razloga sto me dosta ljudi i prijatelja pitalo o nekim osnovnim stvarima, pa pretpostavljam da ce se jos neko susresti sa takvim problemima pri instalaciji i koriscenju Apache Web Servera.

**INSTALACIJA:**  
Prvo ako imate instalacione diskove vase Linux distribucije (ja koristim Mandrake 9.0) na njima mozete naci Apache i sve naophodne module za isti (dakle cgi, php, perl&#8230;)  
U tom slucaju instalaciju prepustite vasem sistemu tj. ili pri instalaciji OS-a izmedju ostalog selektujte i Apache i sve vama neophodne module (mod\_php, mod\_cgi&#8230;) ili otvorite neki od menadzera za instalaciju paketa (rpmdrake i sl.) koje nadam se imate instalirane u KDE ili GNOME grafickom okruzenju.

**TESTIRANJE:**  
Nakon instalacije da bi proverili da li vam radi Apache na lokalnoj masini ili u konzoli ukucajte  
#apachectl status  
ili otvorite bilo koji browser i ukucajte za URL http://localhost (trebala bi se ucitati strana sa nekim podacima o Apache serveru i linkovima na help)

**KONTROLA:**  
Za kontrolu samog Apache-a mozete koristiti komandu apachectl (dizajnirana je za pomoc u administraciji i kontroli httpd daemona tj. samog servera)  
Neke od najcesce koriscenih komandi su:  
#apachectl start  
(startuje web server),  
#apachectl stop  
(zaustavlja web server),  
#apachectl restart  
(ime samo kaze :)) i  
#apachectl configtest  
(proverava sintaksu [konfiguracionih fajlova](https://linuxo.org/?p=4#konff) i ispisuje ili Syntax Ok ili detaljne informacije o sintaksnim greskama)

Pored apachectl komande mozete za razna konkretna podesavanja koristiti komandu:  
httpd  
koja ima razne sviceve a ja bi vam predlozio da probate recimo:  
#httpd -v  
(stampa verziju httpd-a) i  
#httpd -h  
(kratak prikaz svih mogucih opcija komandne linije tj. neka vrsta help-a za tu komandu)  
Tako cete videti da li sve radi ok, a za detaljnije informacije pogledajte help koji vam dolazi uz Apache i pocetno mu mozete pristupiti preko  
http://localhost iz vaseg web browsera.

Uz navedene komande za sve vas koji ne volite komandnu liniju i ne zelite da proucavate komande za Apache mozete sve sto vam je neophodno vrlo lako podesiti iz WebMin-a (nadam se da vam je isti instaliran, ako nije obavezno ga instalirajte jer ce vam ulepsati zivot :))

**<a name="konff">KONFIGURACIONI FAJLOVI:</a>**  
Dakle osnovni konfiguracioni fajlovi za vas novoinstalirani Apache web server su httpd.conf  
i commonhttpd.conf.  
Istima se najlakse pristupa iz WebMin-a a ako nemate njega onda ih potrazite u vasem apache direktorijumu na hdd-u (obicno se nalazi u /usr/local/) i slobodno ih otvorite nekim obicnim editorom a ako ste u konzoli mozete ih pogledati i sa:  
#cat httpd.conf | more  
i  
#cat commonhttpd.conf  
Oba ova fajla sadrze glavna podesavanja vaseg servera, od toga gde se nalaze njegovi direktorijumi i koji su moduli aktivni (AddModule i LoadModule linije) do toga kome ce biti dozvoljen ili zabranjen pristup, koje dozvole ce koji korisnik imati, koji je maximalan moguci broj istovremenih zahteva (svaka komunikacija nekog korisnika sa vasim serverom, bilo da browserom gleda sajt koji hostujete ili pristupa preko ftp-a ili telneta apache tretira kao zahtev ali na koliko ce zahteva server moci istovremeno odgovoriti zavisi od vase veze sa internetom, snage vaseg hardvera i zbog zastite od preopterecenja postavlja se taj parametar)  
zatim podesavanja ping timeout-a (tj. kad ce server prestati da pokusava da obradi neciji zahtev ) i tako dalje&#8230;  
Posto su ti konfiguracioni fajlovi detaljno i veoma pametno komentarisani, mozete vecinu stvari sami da shvatite ako znate solidno engleski.  
Ako vam to nije dovoljno imate detaljan help koji je vec ranije pomenut, a ako i to nije dovoljno pisite na neki forum (mozete i na ovaj) i pitajte sve sta vas zanima ili posetite:  
[www.apache.org](http://www.apache.org/)

**RESENJA NEKIH POCETNICKIH GRESAKA:**  
Dakle prvo da napomenem da bi mogli da izvrsavate .php strane ili neke druge skripte morate svemu tome da pristupate preko servera tj. preko localhost-a ili IP adrese ili URL-a koji pokazuje na vas server.  
To je u krajnjem slucaju i logicno jer sve vrste skripti obicno zahtevaju neku obradu od servera (od interpretacije samih strana i skripti do raznih post, get, id i ostalih metoda koje se koriste u asp, php, cgi i slicnim skriptama)

Ako dobijate gresku 403 pogledajte i sredite vas commonhttpd.conf [konfiguracioni fajl](https://linuxo.org/?p=4#konff), konkretno deo za dozvole pristupa direktorijumima.  
Ili obratite paznju na sledece:  
za direktorijum i sve fajlove u direktorijumu mora se podesiti da pored read (r)  
imaju i execute (x):

na primer:  
u folderu: /var/www/html/anketa2/ [marko@localhost anketa2]$ ls -l

  
total 40  
dr&#8211;r&#8211;r&#8211; 2 marko marko 4096 Dec 19 21:42 anketa/  
-rw-rw-r&#8211; 1 marko marko 12147 Nov 30 15:39 anketa.php  
-rw-rw-r&#8211; 1 marko marko 6521 Dec 16 11:53 glasaj.php  
drwxrwxr-x 2 marko marko 4096 Dec 19 19:12 include/  
-rwxrwxrwx 1 marko marko 11116 Dec 19 21:41 opste.php*</p> 

sa takvim stanjem stvari kada bi u browser ukucao sledece (podesi.php postoji):  
http://localhost/anketa2/anketa/podesi.php  
server bi javljao gresku 403:

Forbidden

You don&#8217;t have permission to access /anketa2/anketa/podesi.php on this server.

Apache-AdvancedExtranetServer/1.3.26 Server at localhost.localdomain Port 80

kad uradim jedno:  
[marko@localhost anketa2]$ chmod a=rx,u+w anketa  
[marko@localhost anketa2]$ ls -l  
total 40  
drwxr-xr-x 2 marko marko 4096 Dec 19 21:42 anketa/  
-rw-rw-r&#8211; 1 marko marko 12147 Nov 30 15:39 anketa.php  
-rw-rw-r&#8211; 1 marko marko 6521 Dec 16 11:53 glasaj.php  
drwxrwxr-x 2 marko marko 4096 Dec 19 19:12 include/  
-rwxrwxrwx 1 marko marko 11116 Dec 19 21:41 opste.php*

sve radi OK!

E sad da bi pristupili fajlovima preko interneta (dakle kad se radi o serveru koji radi na  
netu i neko u browseru otvara njegovu adresu) svi fajlovi koje zelite da ljudi mogu  
pogledati moraju biti i r (read) i x (execute).  
Kad kazem svi onda mislim i na sve .html i sve .php i sve .gif i sve .jpg dakle  
bas sve fajlove koji trebaju biti dostupni korisniku kroz http protokol iz bilo kog  
browsera.  
Meni se desilo par puta da neke .gif slike nece da ucita na nekoj .html strani  
jer sam zaboravio da uradim chmod (konkretno chmod a=rx) na istoj.

Zakljucak:  
Dakle direktorijumi moraju biti izvrsni (tj. korisnici moraju biti u mogucnosti da  
im pristupaju tj. da ih &#8222;izvrsavaju&#8220; kroz browser) i svi fajlovi unutar direktorijuma  
moraju biti isto izvrsni uz to sto mora biti omoguceno citanje.

Za sve dodatne informacije posetite:  
[www.apache.org](http://www.apache.org/)

Toliko za ovaj put pa neki drugi put kad budem imao vise vremena mozda napisem tekst o sigurnosti i zastiti servera od mogucih napada i raznih problema pri aktivnom radu na internetu.

Zelim svima prijatan rad sa Apache web server-om i Linux-om uopste 🙂 

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=258)