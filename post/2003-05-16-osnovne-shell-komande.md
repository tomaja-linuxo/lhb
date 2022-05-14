---
author: tomaja
date: "2003-05-16T15:38:41Z"
guid: https://forum.linuxo.org/2003/05/16/osnovne-shell-komande/
id: 324
image: /wp-content/uploads/2018/12/osnovne-shell-komande.jpg
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
tinymce-comment-field_enabled:
- "1"
title: Osnovne SHELL komande
url: /osnovne-shell-komande/
---
Za početak objasniću samu strukturu komandi. Komanda se sastoji iz tri dela i to:  
_ime komande_  
_opcije komande_ (slova ili reči kojima prethodi -) (ove opcije se takođe nazivaju i flegovi)  
_argumenti_ (nazivi fajlova, direktorijuma, proizvoljni tekst)

Primer za početak nek bude bude komanda `ls -d /home`. Sada da objasnimo šta je šta. Prvo `ls` je ime komande kojom zadajemo da nam se izlista sadržaj direktorijum, `-d` je fleg, njegovo dejstvo na komandu je da prilikom izlistavanja sadržaja ditektorijuma na ekranu prikaže samo  
ulazne ditektorijume. I na kraju `/home` je argument, ustvari on &#8222;pokazuje komandi&#8220; koji direktorijum se treba izlistati, inače ukoliko se komanda unese bez ovog argumenta izlista ce se tekući direktorijum.<!--break-->

I pre nego što počnem da pišem o bilo kojoj komandi daću vam objašnjenje `man` komande.

`man` &#8211; Manual (uputstvo) za komandu. Koristi se program `less` za ispis. Znači objašnjenje bilo koje komande možete saznati ovako!!!

(Većinu komandi sam ovako naučio, i man smatram za najboljeg prijatelja tokom rada sa SHELL-om)  
`man write` &#8211; Uputstvo za naredbu `write`.  
`man -k` &#8211; Spisak svih komandi u kojima se javlja.  
`--help` &#8211; Znatno kraći i sažetiji help sa kratkim opisom sintakse i argumenata koji se mogu pojaviti u komandi. Radi za većinu naredbi.

Ovo je bio uvod za apsolutne početnike a sada idemo malo da proširimo znanje o komandama. Za početak ćemo se upoznati sa komandama za rad sa  
datotekama.

### Promena tekućeg direktorijuma

`pwd` apsolutna putanja do tekućeg direktorijuma

`cd` Change directory, tj. promena direktorijuma.`<br />
cd ..` Vraćanje u prethodni (parent) direktorijum.

`cd /home/mika` Menjanje direktorijuma.

`cd .` Tekući direktorijum.

`cd ̃` Vraćanje u home direktorijum (može i samo: cd).

`cd ̃` Pomeranje u direktorijum unutar home direktorijuma.

Kreiranje novog direktorijuma vrši se komandom `mkdir` &#8211; Make directory tj.Pravljenje direktorijuma.

Uklanjanje direktorijuma vrši se komandom `rmdir` Remove directory Briše samo prazne direktorijume (u kojima nema drugih poddirektorijuma ili datoteka). Ukoliko direktorijum nije prazan, onda se i on i njegov sadržaj može obrisati sa `rm -rf putanja_do_direktorijuma`

### Pregled sadržaja direktorijuma

`ls` List- slično sa DOS naredbom dir

`ls -d *` Ne listaju se direktorijumi.

`ls *` Lista i one fajlove koji su unutar poddirektorijuma (dir /s u DOSu).

`ls a[Bb]*` Lista sve fajlove čije je prvo slovo je a, drugo slovo B ili b.

`ls -r *` Lista fajlove i direktorijume u obrnutom poretku (reverse order).

`ls [ 1-3]` Lista sve fajlove čije je prvo slovo 1, 2 ili 3.

`ls a?c000` ? zamenjuje bilo koje, ali tačno jedno, slovo.

`ls a*0` * je zamena za bilo koju nisku (i praznu) karaktera, pa se ovako  
listaju svi fajlovi koji počinju sa a, a završavaju se sa 0.

`ls -l` Detaljnije informacije o fajlovima, npr. atributi.

`ls -a` Spisak svih fajlova, tj. i onih koji počinju tačkom, a koji se inače ne prikazuju (slično hidden fajlovima u DOS-u) jer su ti fajlovi obično veoma važni.

`ls -la` (isto kao: ls -l -a) Detaljnije informacije o svim fajlovima.

`ls -s` pregledniji ispis (brojevi pored fajlova govore koliko je veliki fajl u kilobajtima).

`ls -R` Ispis sadržaja tekućeg direktorijuma i poddirektorijuma.

`ls -p` Da bi u screenu direktorijumi bili označeni kosom crtom (/).

`ls -o` Da bi u screenu izvesni fajlovi bili osvetljeni.

### Komande za kopiranje

`cp [ ]` Copy Kopiranje datoteke.

`cp []` Kopiranje fajlova u .

`cp [] .` Kopiranje u tekući direktorijum.

`cp [] ̃` Kopira u home direktorijum.

`cp -i` Za svaki fajl preko koga treba da piše pita da li je to u redu.

Komande za promene mesta ili imena datoteke `mv` Move Slično kao kopiranje, samo što se originalni fajl neće sačuvati, tj. ovako se vrši preimenovanje.

`mv` Promena mesta boravka fajlova.

`mv -i` Za svaki fajl pita da li da se izvrši move.

### Komande za brisanje datoteka

`rm` Remove Brisanje fajlova.

`rm -i` Pita za svaki fajl da li ga obriše.

`rm -r` Briše ceo bez daljih pitanja.

`rm -r -i` Isto kao rm -r, ali postavlja pitanje za svaki poddirektorijum unutar direktorijuma da li da ga razmatra (tj. fajlove u njemu) (descent) i da li da ga briše (remove).

`rm "axb"` Briše sve fajlove čiji naziv ima tri karaktera a,x,b.

`rm a?b` Briše sve fajlove čiji naziv ima tri karaktera i počinje sa a i  
završava sa b (npr. aab, adb,&#8230;) .

`rm a*` Briše sve fajlove čije ime pocinje sa a.

`rm a *` Briše fajl koji se zove a (rm a), i sve fajlove u direktorijumu (rm \*), u par reči briše sve fajlove u direktorijumu! Razlog je taj što shell interpretira \*, ? i [.-.] i pravi listu fajlova za brisanje.

`rm "*"` &#8211; Briše fajl koji se zove *, a ne sve fajlove u direktorijumu.

`rm -- -f` &#8211; Briše fajl -f. Ovde je neophodno navesti opciju &#8212; koja označava da dalje ide lista fajlova, a ne neka nova opcija.

`rm ./-f` &#8211; Drugi način da se izbriše fajl -f u tekućem direktorijumu. Ne postoje drugi načini osim ova dva prikazana da se ovakav fajl direktno  
izbriše.

### Još komandi za rad sa direktorijumima

`mkdir` &#8211; Make directory &#8211; Pravljenje direktorijuma.

`rmdir` &#8211; Remove directory &#8211; Briše samo prazne direktorijume.

Opcija &#8212; postoji i za većinu drugih naredbi i služi pri radu sa fajlovima čije ime počinje minusom.

Ime datoteke, odnosno direktorijuma, ne sme da sadrži : ; < > & * ? [ ] | ukoliko nije pod navodnicima. Ovo važi pri bilo kakvom navođenju imena fajla koje sadrži ovakve karaktere.  
Maksimalna dužina imena fajlova, kao i direktorijuma bi trebalo da je 255.

### Još malo komandi (rad sa datotekama)

`cat` &#8211; Catenate &#8211; Lista fajlove (kao type u DOS-u).

`cat /etc/passwd | more` &#8211; Spisak svih logina na serveru.

`cat >` &#8211; Upis teksta sa tastature u fajl do pritiska ^C. Pri tom se prethodni sadržaj fajla gubi.

`cat >>` &#8211; Dopisivanje teksta koji se unosi sa tastature na kraj fajla.

### joe

joe &#8211; Popularan editor. Iako jednostavan, u njemu je moguće praviti makroe, bookmarkove, čak je dozvoljeno i kompajliranje.  
Evo i nekih komandi za rad sa unutar JOE-a:

^KH &#8211; Help &#8211; Piše u gornjem desnom uglu ekrana. Tu pišu sve ostale  
opcije. Izlaz iz helpa je ^KH.

^[. &#8211; Next screen &#8211; Sledeća strana helpa. Umesto ^[ može se koristiti i ESC.  
^[, &#8211; Previous screen &#8211; Prethodna strana helpa.  
^- &#8211; Undo.  
^KX &#8211; Save and Exit.  
^KS &#8211; Save As.  
^C &#8211; Exit without save (abort).  
^R &#8211; Refresh.  
^KB &#8211; Begin block.  
^KK &#8211; End block.  
^KC &#8211; Copy block. Blok mora biti prethodno selektovan sa ^ KB i ^KK.  
^KM &#8211; Move block.  
^KY &#8211; Delete block.  
^KF &#8211; Find string (  
za new line, za , …).  
^L &#8211; Find next.  
^Y &#8211; Delete line.

Sada prelazimo na preusmeravanje ulaza i izlaza i pajpvanje

Preusmeravanje ulaza i izlaza može biti vrlo korisno. Ovde je dat opis kako sve to funkcioniše i iskreno se nadam da ćete naći primenu preusmeravanju

`prog < infile` &#8211; čita iz fajla šta treba u programu prog (umesto da unosimo sa tastature).

`prog > outfile` &#8211; Umesto na ekran, piše u fajl.

`prog | anotherprog` &#8211; Izlaz iz prog (ne ide na ekran) je ulaz za anotherprog.

`prog outfile` &#8211; čita iz fajla infile i rezultat programa prog upisuje u fajl outfile.

Pajpovanje ili povezivanje više komandi je korisno isto koliko i preusmeravnje, evo opisa

`| more` &#8211; Lista stranu po stranu.

`more` &#8211; Lista stranu po stranu.

`| less` &#8211; Slično kao more.

Ne morate samo da pajpujete sa less i more ovo su banalni primeri &#8211; eksperimentišite!!

Pošto sam naveo less i more da vidimo i njihove opcije

U komandi _more_, akcije su:  
h &#8211; Help &#8211; Spisak akcija.  
space &#8211; Pomeranje nadole za navedeni broj redova (otkuca se neki broj i pritisne space). Ako se ništa ne navede, po defaultu je to jedna strana.  
b &#8211; Backward &#8211; Pomeranje za stranu ili za navedeni broj redova unazad.  
q &#8211; Quit &#8211; Izlazak.

Akcije u komandi less:  
b &#8211; Vraćanje na prethodnu stranu.  
u &#8211; Vraćanje za pola strane unazad.  
d &#8211; Spuštanje za pola strane.  
v &#8211; Prelazak na slede}u stranu.  
space &#8211; Prelazak na slede}u stranu.  
/ &#8211; Osvetljava sve pojave stringa . Ako se ne navede, to znači find next.  
q &#8211; Izlaz.

Pored _less_ i _more_ postoje komande tail i head koje imaju slično dejstvo

`head` &#8211; Ispisuje pocetak fajla (prvih 10 redova).

`tail` &#8211; Ispisuje kraj fajla (poslednjih 10 redova).

`tail -f` &#8211; Ispisuje kraj fajla, kao i redove koji se naknadno (recimo iz drugog procesa) dopisuju u fajl.

U SHELL-u takodje možete i ta radite sa arhivama komanda je tar a evo i upotrebe

`tar` &#8211; Arhiver &#8211; Uobičajene ekstenzije su .tgz (pakovanje sa kompresijom &#8211; kao zip) i .tar (pakovanje bez kompresije, tj. kopiranje više fajlova u jedan).

`tar -zcvf .tgz` &#8211; Ovako se pakuju fajlovi iz navedenog direktorijuma.

`tar -ztvf` &#8211; Lista sadržaj bez raspakivanja.

`tar -zxvf` &#8211; Raspakuje arhivu.

Pri tome, opcije za tar znače (za ostale opcije se preporučuje  
tar &#8211;help):  
-c &#8211; Create &#8211; Pravljenje tar fajla.  
-t &#8211; List &#8211; Ispis sadržaja tar fajla.  
-x &#8211; Extract &#8211; Raspakivanje.  
-f &#8211; File &#8211; Znači da će se koristiti tar arhiva. Naziv arhive mora da ide odmah iza ove opcije (sa ili bez razmaka), a nakon toga mogu ići i  
još neke opcije. Preporučuje se da se ova opcija navodi kao poslednja pre imena fajlova (kao što je i u gornjim primerima).  
-z &#8211; Zip &#8211; Bolje se pakuje, jer se koristi zip metoda.  
-v &#8211; Verbose &#8211; Ispisuje fajlove koji su obrađeni (zapakovani/raspakovani).  
-w &#8211; Pita za svaki fajl (da li da se zapakuje/raspakuje).

Pored tara još mogu biti od koristi i

`zip` &#8211; Kompatibilan sa pkzipom i Winzipom. Ovako se pakuje.

`zip -T` &#8211; Testiranje ispravnosti zip arhive.

`unzip` &#8211; Raspakivanje zip arhive. Ponekad je potrebno koristiti opciju -d da bi se raspakovali i direktorijumi.

`unzip -a` &#8211; Kad se nešto zipuje u DOS-u, tada će tekst fajlove raspakovati kako treba (CR LF ce biti LF(kome je jasno, jasno a kome ne neka navede ovu opciju ako je zipovanje izvršeno u Win-u ili DOS-u)) (slično ascii prenosu podataka). Ne koristiti za raspakivanje binarnih fajlova.

`unzip -l` &#8211; Lista sadržaj zipa.

`unzip -t` &#8211; Testiramo ispravnost zipa.

`unzip -x` &#8211; Raspakovaćemo samo fajlove koji su u listi.

### Za kraj malo i o pretragama po datotekama i direktorujumima

`grep` &#8211; Ispisuje sve linije u kojima se nalazi . Ako je navedeno više od jednog fajla ispisuje se iz kog je fajla linija.

`cat /etc/passwd | grep` &#8211; Podaci o nekoj osobi.

`grep -v` &#8211; Lista sve linije osim onih koje sadrže .

`grep -F` &#8211; Pojedini specijalni karakteri . ^ $ i još neki se tretiraju kao regularni izrazi, i odmah se razvijaju u listu. Da se to ne bi dogodilo koristimo opciju -F.

`fgrep` &#8211; Isto kao grep -f.

`grep -x ''` &#8211; Spisak svih linija koje sadrže jedino .

`grep -n` &#8211; Pored svake linije ispisuje i njen redni broj (indeksira ih).

`grep -E ''` &#8211; Spisak svih linija koje sadrže .

Regularan izraz može da sadrži:  
^ &#8211; Početak linije.  
$ &#8211; Kraj linije.  
. &#8211; Bilo koji karakter.  
[] &#8211; Tačno jedan karakter iz skupa u zagradama:  
[1-2abc9-D].  
[^] &#8211; Tačno jedan karakter koji nije među navedenim.  
{n} &#8211; se pojavljuje n puta.  
* &#8211; Pojavljuje se 0, 1, ili više puta.  
+ &#8211; Pojavljuje se bar jednom.  
? &#8211; Pojavljuje se 0 ili jednom.

`grep -E '.'` &#8211; Lista sve neprazne linije u fajlovima.

`grep -Ev '.'` &#8211; Lista sve prazne linije u fajlovima.

`grep -E 'i$'` &#8211; Ispisuje sve linije koje se završavaju slovom i.

`grep -E '^A' l` &#8211; Ispisuje sve linije koje počinju slovom A.

`grep -E '^[WPM]'` &#8211; Ispisuje sve linije koje po?inju sa W, P ili M.

`grep -E '^[^C-E]'` &#8211; Ispisuje sve linije koje ne počinju slovima C, D ili E.

`grep -E '[1-2] [0-2]'` &#8211; Ispisuje sve linije u kojima su brojevi 10, 11, 12, 20, 21 ili 22.

`sort` &#8211; Ispisuje fajlove sortirane po prvom polju (koloni) na ekran (stdout).

`sort +1` &#8211; Sortira po drugom polju, tj. po polju posle prvog tabulatora, uključujući i beline (blankove). Po defaultu, separator je tabulator.

`sort +1b` &#8211; Sortira po drugom polju. Ignoriše beline na početku drugog polja.

`sort +2 -n` &#8211; Sortira po tre}oj koloni. n označava da se sortira po brojevima, pa će broj 2 da stoji pre 10.

`sort +2n` -Isto kao malopre, jedino je zapis kraći.

`sort +2nr` &#8211; Slično, samo u obrnutom redosledu.

`w | sort` &#8211; Sortira izlaz naredbe w.

`w | sort +3` &#8211; Sortira po četvrtoj koloni (bukvalno: sortira po koloni posle trećeg tabulatora).

`sort -f` &#8211; Pri sortiranju se ne razlikuju mala i velika slova (ignore case).

`find []` &#8211; Štampaju se direktorijumi, fajlovi i poddirektorijumi.

`find [] -name` &#8211; Ime fajla se stavlja pod navodnike ako su u imenu neki od rezervisanih karaktera (npr. *). Ako se ne navede akcija, podrazumeva se štampanje na ekran.

`find ̃ -name "*"` &#8211; Lista sve fajlove u home direktorijumu i njegovim poddirektorijumima.

`find / -name` &#8211; Lista sve pojave fajla u svim direktorijumima hard diska.

`find . -name` &#8211; Lista sve pojave fajla od tekućeg direktorijuma naniže.

`find [] -name -print` &#8211; štampanje (ovo je default akcija).

`find [] -name -exec` &#8211; Izvršava komandu koju navedemo nad fajlovima koje je  
pronašao kao argumentima (ako imamo pristup tim fajlovima).

`find [] -perm <ovlašćenje>` &#8211; Traži fajlove po ovlašćenju.

`find -perm 700` &#8211; Primer.

`cut -d -f` -Ispisuje polja koja mu navedemo u listi polja koja su odvojena zarezom, a separator polja je i mora se navesti pod navodnicima ukoliko sadrži neke rezervisane karaktere.

`who am i | cut -d" " -f1 | cut -d! -f2` &#8211; Ispisuje samo username.

`cat /etc/passwd | grep | cut -d: -f5` &#8211; Ispisuje ime i prezime osobe čiji je username .

`grep /etc/passwd | cut -d: -f5` &#8211; Isto kao prethodni primer.

`grep /etc/passwd | cut -d: -f6 | cut -d/ -f1` &#8211; Ispisuje se prazan string jer smo stavili da je drugi separator slash  
(/).

U suštini ovo je neka osnova za rad u SHELL-u komandi ima mnogo, no ovo je neka osnova koja vam je dovoljna za početak, i ne samo za početak već  
i za malo napredniji rad.

Sa srećom!!!

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=324)