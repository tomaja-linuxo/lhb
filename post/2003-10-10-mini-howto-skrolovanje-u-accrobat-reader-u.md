---
author: tomaja
date: "2003-10-10T15:37:09Z"
excerpt: |
  Ovo bi trebalo da bude jedno kratko upustvo (Mini-HOWTO) kako
  omogu?iti skrolovanje sa to?ki?em miša u acroread-u zasnovano na mom li?nom iskustvu. Kliknite na "Read more..."
guid: https://forum.linuxo.org/2003/10/10/mini-howto-skrolovanje-u-accrobat-reader-u/
id: 380
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Mini-HOWTO Skrolovanje u Accrobat Reader-u
url: /mini-howto-skrolovanje-u-accrobat-reader-u/
---
Ovo bi trebalo da bude jedno kratko upustvo (Mini-HOWTO) kako  
omogu?iti skrolovanje sa to?ki?em miša u acroread-u zasnovano na mom li?nom iskustvu. Kliknite na &#8222;Read more&#8230;&#8220;  
<!--break-->Skrolovanje u Acrobat Reader-u

Ovo bi trebalo da bude jedno kratko upustvo (Mini-HOWTO) kako  
omogu?iti skrolovanje sa to?ki?em miša u acroread-u zasnovano  
na mom li?nom iskustvu.

Ono što ?e možda neki od vas prvo da pitaju je &#8216;a zašto uopšte  
koristiti acroread, pored ve? postoje?ih programa na linuxu?&#8217;  
Razlog za to je taj što acroread ipak nudi nešto više od svih  
tih programa što se ti?e preglednosti, kontrole i pretrage po  
tekstu i poglavljima i što ima ljudi koji su prešli sa Windowsa na Linux.  
S obzirom na to da mnogi od tih ljudi nisu spremni da odmah privhate neka od  
softverskih rešenja koja nudi Linux, migrating je ipak bolja solucija od  
naglog prelaska na novo i druga?ije.  
Pa da preÄ‘emo na stvar.  
Za svu ovu akrobaciju su vam potrebni programi acroread i imwheel  
bilo u obliku tarball ili rpm paketa.  
Prvo instalirajte acroread, a nakon toga imwheeel kojeg imate na  
jednom od prate?ih diskova Mandrake distroa (takoÄ‘e ga ima i na netu).  
Kada ste to uradili, onda treba da editujete fajl koji bi trebao da  
postoji u vašem /home/neki_korisnik direktorijumu pod imenom .imwheelrc.  
Ako on ne postoji tamo onda prekopirajte onaj koji se nalazi na ovoj  
putanji: /etc/X11/imwheelrc. Obratite pažnju na to da ovaj koji se nalazi  
u /etc direktorijumu nema u imenu ta?ku ispred pa ?ete morati da ga  
preimenujete prilikom kopiranja u &#8216;.imwheelrc&#8217;.  
Ovaj konfiguracioni fajl ve? ima podešene parametre za veliku ve?inu  
aplikacija koje izvorno ne podržavaju scrolliing kao što je recimo  
Netscape. Ono što je meni smetalo jeste to što kada sam instalirao  
ovaj program acroread nije skrolovao fino red po red ve? stranicu po  
stranicu što govori u prilog tome šta ustvari radi imwheel.  
Njegova uloga je da emulira pritisak na odreÄ‘ene tastere na tastaturi  
kao što su &#8216;PageUp&#8217;, &#8216;PageDown&#8217; kada se skroluje sa to?ki?em miša.  
On se ustvari i poziva na ove tastere ali preko miša.  
Za detaljnije objašnjenje pogledajte man stranicu imwheela, a i sam  
fajl .imwheelrc je dosta dobro iskomentarisan tako da i iz njega  
možete dosta da saznate.  
Da se vratimo na pravu stvar, sam acroread ne mora biti naveden u ovom  
fajlu jer on koristi X11 izvorno i kao i sve aplikacije koje rade pod X-om  
?e imati mogu?nost skrolovanja nakon instalacije i pokretanja programa.  
Da bi smo ga fino podesili tj. da bi smo imali skrolovanje red po red  
potrebno je da u .imwheelrc fajlu pri kraju u delu koji je namenjen za  
podrazumevane vrednosti koji izgleda ovako:

\# These are the defaults, but note that the defaults for the right side of the  
\# keyboard are still handled within the program, unless you add the  
\# combinations desired here. (except for the None modifier of course!)#  
\# (fg) FIXME again: this breaks most apps using GTK, as they ALL support the  
\# wheel. But there&#8217;s no general way that I know of to tell imwheel not to send  
\# its hacked events to all GTK apps. Good point, though, the following events  
\# make kfm work with the mouse. Note also that it obsoletes the need for  
\# Netscape resources, but it&#8217;d be better if all toolkits were smart enough to  
\# support the wheel&#8230;  
&#8222;.*&#8220;  
None, Up, Page_Up  
None, Down, Page_Down  
&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;..  
&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;..

umesto &#8216;Page\_Up&#8217; i &#8216;Page\_Down&#8217;, u prva dva reda nakon komentara koji su  
obeleženi sa # upišete vrednosti &#8216;Up, 3&#8217; i &#8216;Down, 3&#8217; respektivno.  
To zna?i da bi oni na kraju trebali ovako da izgledaju:

None, Up, Up, 3  
None, Down, Down, 3

gde &#8216;None&#8217; ozna?ava modifajer tastera, &#8216;Up&#8217; koji taster se poziva (u ovom  
slu?aju je to taster za skrolovanje na gore) i &#8216;3&#8217; broj ponavljanja pritiska  
tog tastera prilikom jednog sekvencijalnog okretaja to?ki?a na mišu, odnosno  
koliki broj redova ?e se skrolovati.  
Å to se ti?e sintakse ona je na samom po?etku .imwheelrc fajla predstavljena  
tako da nju možete još dodatno da konsultujete.  
Nakon što ste izvršili modifikaciju morate u konzoli da otkucate  
komandu &#8216;imwheel&#8217; da bi ste ga aktivirali. Ako se desi da ipak ne proradi odmah  
, restartuje mašinu i proverite u acroread-u da li radi. Ovaj program ?e svaki  
put prilikom startovanja mašine biti u?itan tako da ne morate da ga  
ru?no uklju?ujete. TakoÄ‘e u istom fajlu možete da isklju?ite podršku za neke  
aplikacije i to na ovaj na?in:

&#8222;Ime_Aplikacije&#8220;  
@Exclude

Napisao: Nostromo

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=380)