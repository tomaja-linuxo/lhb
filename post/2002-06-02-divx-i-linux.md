---
author: tomaja
date: "2002-06-02T11:12:55Z"
excerpt: '  Gledanje DivX filmova na Linux-u !? (po drugi put)<br />  Moguće je naravno,
  a broj programa koji vam to omogućavaju je sve veći.<br />  Ovom prilikom izdvajam
  dva: <strong>Xine</strong> i <strong>mplayer</strong>.<br />  Xine možete pronaći
  na instalacionim diskovima većine Linux distribucija <br />  pa je moguće da ga
  već imate instaliranog. Ako ga i niste instalirali, <br /> to možete lako učiniti
  preko aplikacije za rad sa softverskim paketima poput <em><strong>rpmdrake</strong></em>-a
  u Mandrivi.<br /> mplayer možete potražiti na<a href="http://www.freshmeat.net">
  Freshmeat</a> -u ili na <a href="http://www.mplayerhq.hu">www.mplayerhq.hu</a> i
  skinuti ga. <br />  Grafički interfejs oba programa se može menjati...'
guid: https://forum.linuxo.org/2002/06/02/divx-i-linux/
id: 187
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: DivX i Linux
url: /divx-i-linux/
---
Gledanje DivX filmova na Linux-u !? (po drugi put)  
Moguće je naravno, a broj programa koji vam to omogućavaju je sve veći.  
Ovom prilikom izdvajam dva: **Xine** i **mplayer**.  
Xine možete pronaći na instalacionim diskovima većine Linux distribucija  
pa je moguće da ga već imate instaliranog. Ako ga i niste instalirali,  
to možete lako učiniti preko aplikacije za rad sa softverskim paketima poput _**rpmdrake**_-a u Mandrivi.  
mplayer možete potražiti na [Freshmeat](http://www.freshmeat.net) -u ili na [www.mplayerhq.hu](http://www.mplayerhq.hu) i skinuti ga.  
Grafički interfejs oba programa se može menjati&#8230;<!--break-->..'slično kao i kod Winamp-a, XMMS ili BSplayer-a.

  
Kada startujete <u><strong>Xine</strong></u> otvoriće vam se prozor i mali gui plejera koji prilično liči na  
MicroDVD plejer iz Windows-a ali neka vas to ne pla&scaron;i jer uz ovu verziju (0.9.8) koja  
dolazi uz ML 8.2 imate jo&scaron; bar 4-5 skinova. Program prili?no dobro prikazuje  
DivX format mada u full screen modu možete ponekada primetiti poznate &uml;kockice&uml;.  
Xine podržava i DVD i VCD format ali koga to jo&scaron; zanima :=)  
Mo?i ?ete da reprodukujete avi, dat, mpeg, mvp, vob i dr. formate. Tako&Auml;&lsquo;e postoji i ekvilajzer sa kojim  
možete po prili?no popraviti kontrest, osvetljenje itd. Program ima i dobre mogu?nosti pode&scaron;avanja  
zvuka, dekodera za video i audio, mogu?nost prikazvanja fontova i dr.  
Punu listu opcija možete videti u terminalu pomo?u komande **_man xine_**  
Sve u svemu, sasvim solidan i bespaltan plejer koji i onako dobijate uz operativni sistem a poklonu  
se u zube (jo&scaron; ako su beli ) i ne gleda.

E sad, koliko god je Xine dobar toliko je malo dete za **<u>mplayer</u>** . Samo da bi koristili mplayer mora?ete  
malo vi&scaron;e da se pomu?ite. Prvo treba da posetite  [www.mplayer.hu](http://www.mplayerhq.hu) i skinete poslednju verziju sa izvornim  
kodom jer program prvo morate da iskopajilrate pa tek onda da ga instalirate. Kada ste ve? do&scaron;li na gore pomenuti  
sajt skinite odmah i par skinova kao i 8859-2 set fontova ako mislite da vidite na&scaron; titl.  
Kada sve to uradite sledi klasi?na pri?a ali sa malim dodatkom kod kompajliranja. Evo kako treba da iskompajlirate  
mplayer u Mandrake LINUX-u 8.2:

_./configure &#8211;disable-gcc-checking &#8211;enable-gui</p> 

./make 

./make install  
</em>  
Kod naredbe configure imamo dve dodatne opcije, prva služi za isklju?enje provere verzije gcc kompajlera (jer neke verzije mplayer-a  
imaju proiblema sa gcc 2.96) a druga nam služi da omogu?imo grafi?ko okruženje za mplayer.  
Nakon toga (po&scaron;to ste instalirali program kao root) u&Auml;&lsquo;ite u root direktorijum, na&Auml;&lsquo;ite folder za mplayer i prekopirajte fontove i skinove u  
odgovaraju?e direktorijume s tim da u poddirektorijumu /Skin kreirajte jo&scaron; jedan pod imenom /default i tu ubacite jedan vama najomiljeni skin.

Porgram možete nako toga pokrenuti i ako budete imali sre?e pojavi?e se ne&scaron;to &scaron;to ?e li?iti na ne&scaron;to &scaron;to vam je na prvi pogled ve? poznato.

Pokretanje mplayer-a za radu u grafi?kom modu :

_mplayer -gui &nbsp; &nbsp;_

nakon ?ega dobijate mali interfejs sli?an BSPlayer-u ili MicroDVD pa se dalje možete i sami sna?i. Iz grafi?kog interfejsa možete upravljati sa  
ve?inom bitnih funkcija pronalaženje fajla sa filmom na CD'u ili hardu, ubacivanje titla, pode&scaron;avanje zvuka, premotavanje filma, full screen mod itd.

Film na mplayer-u možete pustiti i direktno iz konzole s tim da onda treba da napi&scaron;ete i putanju do filma &nbsp;i titla kao npr.

<font class="content"><em>mplayer -vo x11 -fs -zoom -framedrop </em></font> &nbsp;_/mnt/cdrom/film/matrix.avi_ 

Puni raspon svih mogu?ih komandi ?ete videti ako pogledate _man mplayer_ u konzoli  
Film možete pustiti i direktno sa web-a sa komandom:

_mplayer http://mplayer.hq/example.avi_

Sa mplayer-om možete gledati i DVD filome pa ?ak i TV program sa va&scaron;e TV kartice.  
Postoji jo&scaron; mnogo toga ali to ostavljam vama !!!

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=187)