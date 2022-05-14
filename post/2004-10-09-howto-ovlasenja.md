---
author: tomaja
date: "2004-10-09T03:43:06Z"
excerpt: |
  Ovlaš?enja (Autor: <b>stale</b>)<br>
  Pri prelasku na
  UNIX operativne sisteme mnogi korisnici se zbunjuju nad nekim osnovnim
  osobinama UNIX okruženja. UNIX je stvoren kao višekorisni?ki sistem i
  kao takav je  morao da obezbedi privatnost svim korisnicima.
  Osnovni mehanizam s'kojim se to postiže jesu ovlaš?enja.
guid: https://forum.linuxo.org/2004/10/09/howto-ovlasenja/
id: 556
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: 'HOWTO: Ovlaš?enja'
url: /howto-ovlasenja/
---
Ovlaš?enja (Autor: **stale**)  
Pri prelasku na  
UNIX operativne sisteme mnogi korisnici se zbunjuju nad nekim osnovnim  
osobinama UNIX okruženja. UNIX je stvoren kao višekorisni?ki sistem i  
kao takav je morao da obezbedi privatnost svim korisnicima.  
Osnovni mehanizam s&#8217;kojim se to postiže jesu ovlaš?enja.<!--break-->Svaki fajl na vašem fajl sistemu ima neka

  
ovlaš?enja, vlasnika i vlasni?ku grupu. Ovlaš?enja govore šta mogu da  
rade vlasnik, vlasni?ka grupa i ostali. Na primer:

_ls -l_  
-rwxr-x&#8212; 2 stale users  
12493 2004-10-03 17:05 file  
(-l kaže komandi ls da prikaže  
duga?ki (long) listing)

Prvi karakter &#8211; nam govori da je ovo obi?an fajl  
(da je bio direktorijum ovde bi stojalo slovo **d**). Slede?e tri  
grupe od  
po tri  
slova nam redom govore koja su ovlaš?enja vlasnika, vlasni?ke grupe i  
svih ostalih. Ovde vlasnik stale može da piše, ?ita i izvršava fajl.  
Vlasni?ka grupa users može samo da ?ita i izvršava fajl. Dok svi  
ostali nemaju nikakva ovlaš?enja. U sistemu to se vidi kao grupa od 9  
bitova (rwxr-x&#8212; = 111 101 000) u fajlu. Da ne bismo koristili binarni  
sistem koji je pomalo kabast mi koristimo oktalni za prikazivanje i  
menjanje ovlaš?enja. U oktalnom sistemu ovlaš?enja za ovaj fajl bi  
izgledala slede?a rwx = 4 + 2 + 1 = 7, r-x = 4 + 0 + 1 = 5 , &#8212; = 0 +  
0 + 0 = 0 (r=4, w=2, x=1). To jest skra?eno **750**.  
Komanda **chmod** za  
menjanje ovlaš?enja prihvata znakovni i oktalni format ovlaš?enja.

_chmod 640 file1_

je isto što i

_chmod u=rw,g=r,o= file1_

Znakovni format je mnogo lakši za menjanje relativnih ovlaš?enja (npr.  
ako ho?emo da nam fajl bude izvršiv chmod  
+x file). Dok je oktalni format lakši za menjanje apsolutnih  
ovlaš?enja.  
Primeri za znakovni format:

    _chmod u+x file_

Dodaje prava vlasniku da izvrši fajl.

_  
chmod ug=rw, o=r  
file_

Daje vlasniku i vlasni?koj grupi prava da pišu i  
?itaju fajl, dok svima ostalima daje samo pravo da ?itaju fajl.

  _chmod go-x file_

Oduzima prava vlasni?koj grupi i svima ostalima da  
izvršavaju fajl.

 _chmod u=o file_

Izjedna?ava ovlaš?enja vlasnika i svih ostalih.  
Pored ovih 9 bitova ovlaš?enja  
postoji još tri: SetUID, SetGUID, lepljivi bit. SetUID i SetGUID nam  
govore da kada se izvrši fajl da ima ovlaš?enja vlasnika i  
vlasni?ke  
grupe fajla iz kojeg je program pokrenut a ne korisnika i njegove  
grupe. Na primer za **halt**  
komandu:

_ls -l /sbin/halt  
-rwsr-xr-x 1 root bin 8768  
2004-06-21 18:33 halt_

je namešten SetUID bit i kada budem  
izvršio ovu komandu ima?u prava root  
korisnika, a ne ovlaš?enja koja posedujem kao obi?an korisnik. SetGUID  
bit primenjen na direktorijum, kaže da svaki fajl napravljen u tom  
direktorijumu budu dodeljene vlasni?koj grupi direktorijuma a ne  
vlasni?koj grupi korisnika. Ovo je korisno za deljenje fajlova.  
Lepljivi bit za direktorijum kaze da ne možete da  
izbrišete fajl osim ako niste vlasnik direktorijuma. Nije dovoljno da  
imate prava za pisanje po direktorijumu. Na  
primer za /tmp direktorijum:

_ls -dl /tmp/  
drwxrwxrwt 32 root root 1576  
2004-10-08 06:34 tmp  
_  
(-d opcija kaže komandi **ls**  
da izvrši listing direktorijuma a ne fajlova u njemu)

SetUID ima vrednost 4000.  
SetGUID ima vrednost 2000.  
Lepljivi bit ima vrednost 1000.  
I sada da bi dodelili SetUID ovlaš?enja možemo uraditi slede?e chmod  
4750 neki_fajl.

Direktorijum je  
samo vrsta fajla koji sadrži tabelu imena i ?vorova koji povezuju fajl  
sa njegovom adresom na hard disku. Da bismo ušli u direktorijum treba  
nam prava izvršenja za taj direktorijum. Dok sa pravima ?itanja možemo  
samo da vidimo šta se nalazi u direktorijumu. Samo ako imamo prava  
pisanja za direktorijum možemo da menjamo imena fajlova u tom  
direktorijumu ili da ih kopiramo.  
E sad dolazi  
trenutak istine. Nisam vam govorio šta zna?i onaj broj desno od  
ovlaš?enja kod listinga. On nam kazuje koliko ima pokaziva?a do ?vora  
tog fajla. Kad je on na 0 fajl se fizi?ki briše. Kod svakog  
direktorijuma ovaj broj je minimum jednak 2, zato što fajl . unutar  
direktorijuma pokazuje na  
njega. Svaki fajl u direktorijumu pokazuje na sam direktorijum. Å to  
zna?i da u mom tmp  
direktorijumu postoji 31 fajl (manje .  
fajl), bilo fajlova ili tako zvanih direktorijuma. Pa da bismo  
izbrisali jedan direktorijum treba da izbrišemo sve fajlove u njemu,  
dobro je što postoji komanda koja to automatizuje rm -r (-r zna?i da  
rekurzivno briše  
direktorijum). Možemo imati više imena za isti fajl tako što svi  
fajlovi pokazuju na isti ?vor. Na primer:

_ls -li  
232295 -rw-r&#8211;r&#8211; 5 stale users  
0 2004-10-08 07:48 primer  
232295 -rw-r&#8211;r&#8211; 5 stale users  
0 2004-10-08 07:48 primer1  
232295 -rw-r&#8211;r&#8211; 5 stale users  
0 2004-10-08 07:48 primer2  
232295 -rw-r&#8211;r&#8211; 5 stale users  
0 2004-10-08 07:48 primer3  
232295 -rw-r&#8211;r&#8211; 5 stale users  
0 2004-10-08 07:48 primer4_  
(opcija -i govori programu **ls**  
da nam pokaže i inode-ove)

Prime?ujemo da su svi brojevi levo  
isti. Taj broj se po engleskom zove inode, a mi ?emo ga zvati samo ?vor  
kao i do sada. Oni su isti! I prime?ujemo da nam broj pokaziva?a kazuje  
da postoji ih 5. Sada kada bi rekao rm  
primer ja ne bi obrisao fajl fizi?ki ve? bi obrisao samo  
pokaziva? na njega. I naravno broj bi se smanjio sa 5 na 4. I sve dok  
ne bi izbrisao sva 4 fajla, fajl bi ostao na hardisku. Sada ?u vam  
otkriti tajnu kako sam napravio ovih 5 mutanata. 

_mkdir NEW  
cd NEW  
touch primer  
ln primer primer1  
ln primer primer2  
ln primer primer3  
ln primer primer4  
_  
(komanda ln služi za  
pravljenje tkz ?vrstih i mekih linkova)  
Ovo su sve teški linkovi i oni se prave na slede?i na?in sa  
komadnom **ln**

_ln staro\_ime novo\_ime  
_  
Teški linkovi su kul, ali imaju svoja  
ograni?enja. Oni su ograni?eni samo na jedan fajl sistem, iliti jednu  
particiju. Pošto na fajl sistemu postoji još jedna tabela koja povezuje  
?vorove sa adresama, i te adrese su razli?ite za svaki fajl sistem.  
Spominjao sam i meke linkove, pa je sad vreme da ih objasnim. Meki  
linkovi sadrže  
samo putanju do fajla na koji pokazuju. Recept za  
pravljenje mekih linkova je slede?i: Â¨prvo uzmemo dva jaja&#8230;Â¨  
Ne samo sam se šalio. 

_ln -s fajl pokazivac\_na\_fajl_

Da vidimo šta se dešava kada uradimo duga?ki listing mekog linka.

_ls -l meki_link  
lrwxrwxrwx 1 stale users 70 2004-09-27  
23:21 meki\_link-> /neki\_dir/neki_fajl  
_  
Ovde kod mekog linka ovlaš?enja ništa ne zna?e ve? su bitna samo  
ovlaš?enja kod neki_fajl (po tarzanski).  
Na ovlaš?enjima koja se dodeljuju fajlovima možete uticati sa komandom  
**umask**. Njoj se kao argument daju  
ovlaš?enja u oktalnom obliku koja se oduzimaju od podrazumevanih  
ovlaš?enja.

_umask 022  
_  
Oduzima pravo pisanje vlasni?koj grupi i svima ostalima, što je  
podrazumevano. Da bi ste saznali vaše maske samo ukucajte komandu umask.  
Da bi ste promenili vlasnika i  
vlasni?ku grupu možete koristiti komandu **chown**. Da bi ste  
promenili  
vlasnika  
ili vlasni?ku grupu morate biti vlasnik tog fajla i morate pripadati  
vlasni?koj grupi datoteke koje menjate, ili pak možete biti  
administrator.

_chown stale.users file  
_  
Menja vlasnika i vlasni?ku grupu fajla.

_chown .users file  
_  
Menja samo vlasni?ku grupu.

_chown stale file  
_  
Menja samo vlasnika.

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=556)