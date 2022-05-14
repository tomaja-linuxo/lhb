---
author: tomaja
date: "2003-02-26T14:46:11Z"
excerpt: |
  Zbog cestih problema sa zvucnim karticama, evo detaljnog uputstva za instaliranje ALSA sound servera direktno iz sors-koda.<br />
  Zasto ALSA?<br />
  1.Zato sto je open-soruce<br />
  2.Zato sto niko ne garantuje da ce OSS patch prikazan i na ovom sajtu raditi u sledecim verzijama OSS-a<br />
  3.Zato sto zahteva manje sistemskih resursa od komercijalnog pandana<br />
  Ko treba da instalira ALSA-u iz sorsa?<br />
  1.Oni kojima distribucija nije to pravilno uradila (posledica : nema zvuka)<br />
  2.Oni sa slabijim masinama<br />
  3.Oni koji zele cist sistem, bez komercijalnih komponenti<br />
  4.Oni koji bi da nauce nesto<br />
  Pa da krenemo :)
guid: https://forum.linuxo.org/2003/02/26/alsa-instalacija-no-more-secrets/
id: 294
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: ALSA instalacija &#8211; No more secrets!
url: /alsa-instalacija-no-more-secrets/
---
Zbog cestih problema sa zvucnim karticama, evo detaljnog uputstva za instaliranje ALSA sound servera direktno iz sors-koda.  
Zasto ALSA?  
1.Zato sto je open-soruce  
2.Zato sto niko ne garantuje da ce OSS patch prikazan i na ovom sajtu raditi u sledecim verzijama OSS-a  
3.Zato sto zahteva manje sistemskih resursa od komercijalnog pandana  
Ko treba da instalira ALSA-u iz sorsa?  
1.Oni kojima distribucija nije to pravilno uradila (posledica : nema zvuka)  
2.Oni sa slabijim masinama  
3.Oni koji zele cist sistem, bez komercijalnih komponenti  
4.Oni koji bi da nauce nesto  
Pa da krenemo 🙂<!--break-->

  
Prvi korak je naravno download potrebnih fajlova sa lokacije http://www.alsa-project.org  
Znacajna su 3 fajla:  
1.alsa-driver-XXX.tar.gz  
2.alsa-lib-XXX.tar.gz  
3.alsa-utils-XXX.tar.gz  
gde je XXX trenutna verzija, preporucuje se uvek skidanje najnovije verzije.  
Alsa-driver paket u sebi sadrzi drajvere za zvucne kartice, dok je alsa-lib biblioteka neophodna za instalaciju alsa-utils paketa.  
Nakon download-a, prvo se raspakuje alsa-driver arhiva. Sve ovo raditi kao root.  
Za one potpuno neuke :  
#tar xzf alsa-driver-XXX.tar.gz  
Sad brzo:  
#cd alsa-driver-XXX  
OK, pretpostavimo da znate koji zvucni cip/karticu imate. Proverite da li postoji drajver za nju jednostavnim editovanjem fajla ./doc/SOUNDCARDS. Mozda spisak ne deluje impresivno, ali tu se nalazi 99,9% zvucnog hardvera; manje bitan je model, vazan je zvucni cip sa kojim kartica radi.  
U spisku ste locirali svoj hardver, i spremni ste za dalju instalaciju. Bilo bi jako dobro da pre bilo kakve instalacije detaljno procitate INSTALL i FAQ fajlove. Tako cete unapred spreciti eventualnu pojavu nekih  
problema, i imati prilike da vidite lavovski deo literature iz kog je iznedreno ovo uputstvo 🙂  
U mom slucaju, na starom PII racunaru sa integrisanom zvucnom, nalazio se cip ESS Solo-1 ES1938. Kool, na spisku je u SOUNCARDS fajlu. Krecemo sa instalacijom:  
\# ./configure  
\# make install  
\# ./snddevices  
Izvrsavanje gornje tri naredbe zna da potraje, narocito na sporijim procesorima. Nakon sto je kompajliranje zavrseno bez error-a, u svoj omiljeni konzolni editor ucitajte fajl /etc/modules.conf . Za neuke:  
\# joe /etc/modules.conf  
U ovaj fajl na pocetku dodajte sledece linije :

#ALSA deo (komentar)  
alias char-major-116 snd  
alias snd-card-0 snd-card-es1938  
#OSS/Free deo (oss emulacija preko alse)  
alias char-major-14 soundcore  
alias sound-slot-0 snd-card-0  
alias sound-service-0-0 snd-mixer-oss  
alias sound-service-0-1 snd-seq-oss  
alias sound-service-0-3 snd-pcm-oss  
alias sound-service-0-8 snd-seq-oss  
alias sound-service-0-12 snd-pcm-oss

Snimite fajl, a nakon toga se zapitajte odakle ja znam da u trecoj linije treba da stoji bas snd-card-es1938?  
U principu, ako se omasi ovde, nista ne vrede aliasi za OSS &#8211; kompjuter ce ostati nem. Pretpostavljam da oni koji su pazljivo procitali INSTALL fajl nece biti ni za trenutak zbunjeni, jer tamo stoji podugacak  
spisak svih modula (drajvera), sa default parametrima (IRQ,DMA i sl.). Za moju karticu ne stoji mnogo toga :

Module snd-card-es1938.o  
&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;

Module for soundcards based on ESS Solo-1 (ES1938,ES1946) chips.

Module supports up to 8 cards and autoprobe.

ali tu je jedna bitna stvar! Ime modula je snd-card-es1938.o pa sledi da u famoznu trecu liniju ubacujem bas snd-card-es1938 🙂  
Evo jos jednog primera, kada smo ja i ortak instalirali na njegovom laptopu ALSA, a tamo se nalazila integrisana zvucna sa Trident 4DWave cipom. U INSTALL fajlu stoji ovo :

Module snd-card-trident.o  
&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;-

Module for Trident 4DWave DX/NX soundcards.  
* Best Union Miss Melody 4DWave PCI  
* HIS 4DWave PCI  
* Warpspeed ONSpeed 4DWave PCI  
* AzTech PCI 64-Q3D  
* Addonics SV 750  
* CHIC True Sound 4Dwave  
* Shark Predator4D-PCI  
* Jaton SonicWave 4D

snd\_dac\_frame_size &#8211; max dac (playback) frame size in kB (4-64kB)  
snd\_adc\_frame_size &#8211; max adc (record) frame size in kB (4-64kB)  
snd\_pcm\_channels &#8211; max channels (voices) reserved for PCM  
snd\_wavetable\_size &#8211; max wavetable size in kB (4-?kb)

Module supports up to 8 cards and autoprobe.

Umesto snd-card-es1938 stavljeno je snd-card-trident, i na kraju celokupnog postupka sve je radilo kao sat.

Ovime je zavrsena instalacija samog drajvera, pa prelazimo na instalaciju preostala 2 paketa, alsa-lib i alsa-utils :  
Prvo alsa-lib:  
\# tar xzf alsa-lib-XXX.tar.gz  
\# cd alsa-lib-XXX  
\# ./configure  
\# make install  
pa alsa-utils:  
\# tar xzf alsa-utils-XXX.tar.gz  
\# cd alsa-utils-XXX  
\# ./configure  
\# make install

Kako instalirati ove dve stvarcice jasno stoji u njihovim INSTALL fajlovima, tako da pre glupih pitanja obavezno sledi gledanje istih.

Alsa-lib i alsa-utils dodaju mogucnost upotrebe utility-ja za alsa drajvere:  
1. alsactl  
2. aplay/arecord  
3. amixer  
4. alsamixer  
Svi su u man stranicama, pa opet ponavljam, RTFM pre nego sto ubedite sebe da ste dosli do nepremostive prepreke.

Dakle instalirano je sve sto treba da bude instalirano, sad sledi finalizacija :  
\# alsactl store  
cime je generisan fajl /etc/asound.conf koji je konfiguracioni fajl ALSA zvucnog servera.  
Ostaje jos podesavanje ON/OFF zvuka pri butovanju kao i njegove jacine. To mozete uraditi editovanjem /etc/asound.conf, ili tako sto cete u /etc/rc.d/rc.local ubaciti na kraju fajla sledece linije :

#ova linija se ubacuje u oba slicaja &#8211; ucitavanje drajvera!  
/sbin/modprobe snd-pcm-oss

#donje linije ukljucuju zvuk i postavljaju jacinu na 20 (max vrednost 32)  
/usr/bin/amixer set Master on  
/usr/bin/amixer set PCM on  
/usr/bin/amixer set Master 20  
/usr/bin/amixer set PCM on

I na samom kraju, rebutujte sistem i uzivajte u zvuku.  
Eto, to je sve. Srecno!

ps. I po treci put, pre bilo kakvih pitanja procitati INSTALL i FAQ fajlove i man stranice!!!

Literatura: internet, INSTALL, FAQ, man

pps. Za totalno pogubljenje, mail na salek@galeb.etf.bg.ac.yu

Salac

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=294)