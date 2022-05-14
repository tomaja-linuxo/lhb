---
author: tomaja
date: "2003-05-07T15:08:43Z"
excerpt: |
  Programski paket GIMP nije novijeg datuma, naprotiv, postoji ve? duže
  vreme  na tržištu programa otvorenog koda, i predstavlja izuzetno par?e
  software-a   namenjeno obradi slika i izradi animacija. Od sli?nosti sa
  Adobe Photoshop-om,   kao de facto standardom na tom polju, izdvajamo
  ikonice na komandnoj strukturi,   Ä…to je pohvalno jer omogu?ava lako i
  brzo snalaženje.
guid: https://forum.linuxo.org/2003/05/07/gimp-i-perl/
id: 320
image: /wp-content/uploads/2003/05/micro.jpeg
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";s:3:"317";s:11:"_thumb_type";s:5:"thumb";}
title: Gimp i Perl
url: /gimp-i-perl/
---
Programski paket GIMP nije novijeg datuma, naprotiv, postoji ve? duže  
vreme na tržištu programa otvorenog koda, i predstavlja izuzetno par?e  
software-a namenjeno obradi slika i izradi animacija. Od sli?nosti sa  
Adobe Photoshop-om, kao de facto standardom na tom polju, izdvajamo  
ikonice na komandnoj strukturi, Ä…to je pohvalno jer omogu?ava lako i  
brzo snalaženje.<!--break-->MeÄ‘utim, GIMP poseduje i opcije koje njegov stariji brat nema, a

  
slobodno mogu re?i da ga u brzini ostavlja za dve dužine. Tu posebno  
isti?emo izvanredne opcije za izradu animacija, koje vam omogu?avaju  
da za desetak minuta napravite impresivne video kreacije, u MPEG 1  
ili MPEG 2 formatu. Program sli?nih mogu?nosti, uz ovakvu brzinu i  
slobodu u radu, nije skoro vidjen ni na jednoj platformi.

Prava snaga GIMP-a nije u filterima, kojih ima stvarno viÄ…e nego  
dovoljno, sa obzirom na to da uvek možete skinuti dodatne filtere sa  
interneta, ve? u mogu?nosti koriš?enja skripti, popularno nazavanih  
Script-Fu. Sve poznate funkcije u GIMP-u su dostupne kroz tzv.  
procedural database (PDB). Sve PDB funkcije mogu biti pozvane iz  
Perl-a ili Python-a, Ä…to pravljenje i koriš?enje skripti olakšava za  
svakog ko se bavio programiranjem CGI skripti pod Linux-om. Ove PDB  
funkcije ili postoje u okviru GIMP-a, ili su dostupne preko plug-in  
dodatka ili script extension-a, ali što se programera ti?e, razlike  
nema. 

Programiranje skripti je izuzetno jednostavno, i spisak svih PDB  
instrukcija sa kompletnom specifikacijom o ulaznim i izlaznim  
vrednostima možete dobiti preko DB Browser-a ili PDB Explorer-a, u  
meniju Xtns.

Neophodno je imati:  
Gimp verziju 1.1.25 ili noviju,  
Perl verziju 5.005 ili noviju,  
Gtk Perl modul, verziju 0.7003  
Gimp Perl modul, verziju 1.201 ili noviju  
PDL Perl modul (opciono).

Module za Perl možete na?i na adresi [  
http://www.cpan.org](http://www.cpan.org) . 

Nakon instalacije oba modula, spremni ste za pisanje skripte. Posebnost  
Perl skripti, pisanih za koriš?enje u okviru Gimp-a je funkcija register  
(listing Register, komentar: Funkcija za prijavljivanje skripte Gimp  
programu). U okviru nje, dostavljamo programu slede?e informacije:  
naziv, opis skripte, pomo? za korisnike, ime autora, autorska prava,  
datum izrade, položaj u komandnoj strukturi Gimp-a, tip slike, kao i  
ulazne parametre. Ovo je pojednostavljena metoda za prihvatanje i  
unos parametara kroz GTK omota?. Na kraju se navodi i poziv za  
podfunkciju koja ?e biti izvršena. Naime, može se odraditi i bez  
poziva, jednostavnim porgramiranjem u nastavku tipa:

sub {  
($text, $color) = @_ ;  
&#8230;  
}

Od ove podfunkcije se ne o?ekuje da prikaže sliku nakon što je iscrta,  
ve? da je vrati kao izlaznu vrednost u skladu sa tipom koji smo uneli u  
register rutini. Sada možemo da unesemo naš prvi primer, koji samo  
treba da vam do?ara strukturu i na?in programiranja.

Listing [Tekst.pl](http://popeye.ekof.bg.ac.yu/tekst.php?id=25)  
&#8211; Ispis teksta preko perl skripte) 

Pazite da unesete ta?nu putanju do Perl-a u prvoj liniji (linija koja  
po?inje sa #! ), lokaciju perl prevodioca ?ete dobiti komandom whereis  
perl. Nakon toga listing snimite pod nazivom skripta.pl. Zatim, dajte  
joj pravo izvršavanja komandom chmod 755 skripta.pl. Slede?i korak je  
postavljanje naše skripte u plug-ins direktorijum aplikacije. To  
izvodimo preko gimptool komande, a pravilna sintaksa glasi: gimptool  
&#8211;install-bin skripta.pl. Pre unošenja skripte u Gimp, bilo bi dobro  
testirati sintaksu naredbom perl -c <skripta>.

NAPOMENA: Ne možete instalirati skript u ve? startovan program, morate  
ga zatvoriti i ponovo podignuti da bi se plug-in u?itao pri startu.  
Jednom postavljen i pravilno inicijalizovan skript možete menjati i  
nakon podizanja programa. TakoÄ‘e, ve?inu ovih skripti možete  
koristiti i bez Gimp-a što ?ete videti na primeru kasnije.

Trebalo bi da vam se u Xtns > Perl-Fu > Radionica meniju pojavila  
stavka Tekst. Kad je startujete, otvori?e vam se prozor gde ?ete mo?i da  
izaberete font i unesete tekst.

Primeti?ete da je ovde koriš?ena funkcija xfld_size koja na osnovu X11  
imena fonta daje veli?inu slova. Koriš?enje ove funkcije je neophodno  
zbog toga tšo slede?a funkcija, gimp\_text\_fontname ignoriše veli?inu  
slova u nazivu fonta. TakoÄ‘e treba znati da ?e tekst koji kreiramo  
ovim putem biti postavljen kao plutaju?i sloj, koji moramo usidriti  
funkcijom gimp\_floating\_sel_anchor().

![micro](https://linuxo.org/wp-content/uploads/2003/05/micro.jpeg) 

Rad sa tekstom iz skripte)

Listing [Zastava.pl](http://popeye.ekof.bg.ac.yu/tekst.php?id=24)  
&#8211; Primena postoje?ih skriptova)

Osim direktnih komandi za iscrtavanje ili ispis, možemo vršiti i pozive  
ka drugim skriptama, koje se ve? nalaze u okviru paketa koji ste  
instalirali, navodjenjem odgovaraju?ih ulaznih parametara. Uze?emo ve?  
navedeni primer kao osnovu za naš slede?i listing, gde ?emo prvo  
izraditi zaštitni znak našeg ?asopisa, a nakon toga primeniti na njega  
skriptu Ripply, ?ime ?emo dobiti malu animaciju zastave koja se  
vijori na vetru.  
Primeti?ete da se nakon izvršavanja skripta dobilo 2 slike, od kojih  
je jedna logo, a druga zastava. Animaciju možete pogledati na Filters  
> Animation > Animation Playback.

Ovde prime?ujete da se može iskoristiti objektna orijentacija Perl  
jezika, tako što prosto navedemo Objekat->Metoda. Na primer, umesto:  
gimp\_image\_add\_layer($drw,-1); koristimo: $img->add\_layer($drw,-1);  
Pravilo za zamenu PDB sintakse metodom je prosto izbacivanje  
gimp_image iz poziva funkcije, a sli?no je i sa ostalim.

![micro_v](https://linuxo.org/wp-content/uploads/2003/05/micro_v.png) 

Petlja ovde, perspektiva tamo, iseci pa prenesi i&#8230;

Sad ?emo primeniti i sve ono što Perl ?ini jednim od najomiljenijih  
prevodila?kih programskih jezika meÄ‘u Linux administratorima. Kreira?emo  
šahovsku tablu, koju ?emo nakon toga nakriviti u perspektivi, pod  
proizvoljnim uglom. Po završenom prora?unu neophodnih parametara i  
iscrtavanju table, primeni?emo filter PageCurl, a zatim iz prethodno  
uradjene slike (ako ste uneli listing Zastava.pl, primeti?ete da u  
vašem ku?nom direktorijumu sada postoji slika mikro.jpg) napraviti  
pozadinu.

Listing [Sah.pl](http://popeye.ekof.bg.ac.yu/tekst.php?id=26)  
&#8211; Prora?unavanje parametara na osnovu ugla nagiba, Rad sa filterima i  
fajlovima)

Pošto nismo dodali Perl modul za trigonometriju, koji se ne nalazi u  
osnovnoj postavci, morali smo da koristimo sopstvenu funkciju za  
pretvaranje stepeni u radijane, što nam je bilo neophodno za prora?un  
perspektive. 

Kreiranje Foto Albuma za Internet prezentacije

Nakon ovoga, pre?i?emo i na jedan pravljenje foto albuma. Ova skripta  
može se koristiti i bez startovanja Gimp-a, a može na?i svoju primenu i  
kao CGI, za brzo on-line ažuriranje slika. Izradi?emo umanjene prikaze  
svake slike u jpeg formatu koja se nalazi u izvornom direktorijumu,  
snimiti ih u odredišni direktorijum i nakon toga napraviti index.html  
fajl, koji ?e sadržati te sli?ice, ulinkovane sa originalima, tako da  
se oni otvaraju u novom prozoru. 

Listing [Galerija.pl](http://popeye.ekof.bg.ac.yu/tekst.php?id=27) 

![velika](https://linuxo.org/wp-content/uploads/2003/05/velika.png) 

Jednostavan primer kako da brzo postavite kolekciju slika na  
prezentaciju

Dosad smo sve skripte pokretali iz komandne strukture u okviru Gimp-a,  
ali postoji i alternativni na?in, da se skripte pokrenu iz komandne  
linije, kao normalni Perl program. Ona ?e po startovanju pokušati da se  
poveže sa Perl-Serverom, a ako ga ne pronaÄ‘e, samoinicijativno ga  
pokre?e. Lakše je ru?no ga startovati, jer u?itavanje Gimp-a oduzima  
na vremenu. Nalazi se u meniju Xtns. Kada se Perl::Fu skript pozove iz  
komandne linije, razlika je u tome što se može startovati sa &#8211;output  
parametrom, tako da ?e rezultat biti snimljen na disk, umesto  
prikazan na ekranu.

Program možete skinuti sa adrese [www.gimp.org](http://www.gimp.org)  
.

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=320)