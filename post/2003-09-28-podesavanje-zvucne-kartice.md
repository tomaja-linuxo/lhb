---
author: tomaja
date: "2003-09-28T13:14:55Z"
excerpt: U poslednje dve godine detekcija hardverskih komponenti je na Linux sistemima
  u mnogome uznapredovala tako da iako za pojedine uređaje nemate drajvere vrlo je
  verovatno da će sam sistem automatski prepoznati hardversku komponentu i instalirati
  i podesiti odgovarajući drajver. To je često slučaj i sa zvučnim karticama, ali
  ako vam se desi da ipak nečujete zvuk na svojim zvučnicima, verovatno je ne&scaron;to
  krenulo naopako. &Scaron;ta onda uraditi ? Verovatno je u pitanju drajver, dakle,...
guid: https://forum.linuxo.org/2003/09/28/podesavanje-zvucne-kartice/
id: 375
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Podešavanje zvučne kartice
url: /podesavanje-zvucne-kartice/
---
U poslednje dve godine detekcija hardverskih komponenti je na Linux sistemima u mnogome uznapredovala tako da iako za pojedine uređaje nemate drajvere vrlo je verovatno da će sam sistem automatski prepoznati hardversku komponentu i instalirati i podesiti odgovarajući drajver. To je često slučaj i sa zvučnim karticama, ali ako vam se desi da ipak nečujete zvuk na svojim zvučnicima, verovatno je ne&scaron;to krenulo naopako. &Scaron;ta onda uraditi ? Verovatno je u pitanju drajver, dakle,&#8230;<!--break-->

### Drajver: Od proizvođača, Alsa, ili OSS ?  


Neke zvučne kartice dolaze sa sopstvenim Linux drajverima. Opet su ponekada drajveri sa zvučnu karticu zajedno sa video drajverima kao &scaron;to je slučaj sa pojedinim matičnim pločama i čip setovima, kao &scaron;to je na primer NForce čipset. 

ALSA je obično default re&scaron;enje, osim ukoliko nema ALSA drajvera. ALSA (<a href="http://www.alsa-project.org/" target="_top">Advanced Linux Sound Architecture</a>) je poku&scaron;aj da se dobije dovoljno pouzdana podr&scaron;ka za sve tipove audio interfejsa, z a korisničke zvune kartice i provesionalne vi&scaron;ekanalne audio uređaje. 

OSS (Open Sound Systems) je prvi poku&scaron;aj kreiranje jedinstvene digitalne audio arhitekture za UNIX. On predstavlja kombinaciju podr&scaron;ke sa <a href="http://www.opensound.com" target="_top">http://www.opensound.com</a> i drajvera koji su postali OpenSource. 

Bilo &scaron;ta od ove tri mogućnosti da izaberete i ne uspete da dobijete zvuk sa svoje kartice, isprobajte druge dve mogućnosti. Pomoću  <span style="font-style: italic"></span><span style="background-image: none; background-repeat: repeat; background-attachment: scroll; background-position: 0% 50%; font-style: italic">DrakSound</span>-a ćete to veoma lako učiniti. 

<img src="http://mandrake.vmlinuz.ca/pub/TWiki/TWikiDocGraphics/warning.gif" border="0" alt="ALERT!" width="16" height="16" /> Ne zaboravite: ukoliko kupujete neku najnoviju zvučnu karticu uvek proverite da li proizvođač podržava Linux drajvere i da li postoji recimo postoji OSS drajver jer posle možete doći u problem da ne možete da pokrenete svoju ultra novu i obično skupu zvučnu karticu. 

&nbsp;

### Da li je zvučna kartica detektovana? 

Kao prvo. pokrenite lspcidrake. Ukoliko se pojavi linija za zvučnu karticu slična ovoj (ovde je u pitanju Yamaha 744B chipset) 

<pre>ymfpci          : Yamaha Corp|YMF-744B [DS-1S Audio Controller]</pre>

Ukoliko je to slučaj, možete nastaviti. Ukoliko nije, verovatno imate zvučnu karticu koja ide u ISA slot.  
Ako je u pitanju ISA kartica onda treba da u konzoli pokrenete <span style="font-style: italic">sndconfig</span> i podesite svoju karticu. 

Ukoliko se ipak radi o PCI kartici (vrlo verovatno) onda fajl _/etc/modules.conf_ treba da sadrži dve linije koje otprilike izgledaju ovako: 

<pre>alias sound-slot-0 snd-ymfpci<br />above snd-ymfpci snd-pcm-oss<br /></pre>

&nbsp;

### Proverite nivo kontrole jačine zvuka. 

Pokrenite aumixer i porverite da li su sve kontrole jačine zvuka aktivne i da li je neki kanal na nivo 0 odnosno smanjen na nulu. Takođe, proverite da li su va&scaron;i zvučnici uključeni kao i to da li su kablovi dobro spojeni ukoliko koristite HiFi uređaje. 

&nbsp;

### KDE sound server prijavljuje gre&scaron;ku 

Pokrenite lspcidrake i informacije o mofulima da bi prona&scaron;li drajver za zvuk na _/lib/modules/x-x-xx-mdk/kernel/drivers/sound_ (gde je xx.xx verzija kernela, verovatno 2.4.19-16 ukoliko imate Mandrake Linux 9.1) 

&nbsp;

Probajte modprobe (ime modula ne sadrži .o.gz ekstenziju) 

Ukoliko ovo radi, izmenite _/etc/modules.conf_ menjajući alias sound 

Kada restartujete ma&scaron;ini, trebalo bi da radi. U krajnjem slučaju, ponekada se problem može re&scaron;iti i deaktiviranjem Arts Sound servera iz KDE Kontrolnog Centra. 

&nbsp;

## Zvuk je OK, ali ne čujem AudioCD  


Postoji nekoliko razloga zbog čega se ovo može desiti: 

### Nema audio kabla 

Imate računar kojem nedostaje mali audo kablić koji unutar ma&scaron;ine povezuje CD/DVD plejer sa zvučnom karticom. 

U ovom slučaju, xmms-cdread plugin je jedno od mogućih re&scaron;enja. On čita audio zapis digitalnim putem umesto direktne reprodukcije. Instalirajte ovaj plugin sa va&scaron;eg Mandrake CDa pomoću komande urpmi, a kada to uradite aktivirajte ga u xmms. Ukoliko imate CDRW uređaj moguće je da ćete morati da uputite xmms da potraži audio cd na /dev/scd0 umesto na /dev/cdrom.  
Naravno, možete da se isprsite za 60-70 din i kupite taj audio kablić, to je već vama na volju. 

<img src="http://mandrake.vmlinuz.ca/pub/TWiki/TWikiDocGraphics/warning.gif" border="0" alt="ALERT!" width="16" height="16" /> Ne zaboravite da imate i mogućnost ripovanja Audio CDa u mp3 ili ogg fajlove (pomoću programa grip, ripperX ili nekog drugog) čime ćete ipak moći da slu&scaron;ate muziku pa čak i da produžite vek svom CD/DVD plejeru. 

&nbsp;

### Imate CDRW rezač 

Imate CDRW i _/dev/cdrom_ nije linkovan na _/dev/scd0_. 

Pokrenite u konzoli ll dev/cdrom da bi saznali gde _se /dev/cdrom_ linkuje. Ukoliko to nije _/dev/scd0_, opet u konzoli unesite ln -fs /dev/scd0 /dev/cdrom 

<img src="http://mandrake.vmlinuz.ca/pub/TWiki/TWikiDocGraphics/warning.gif" border="0" alt="ALERT!" width="16" height="16" /> Ne zaboravite da po default-u zvuk emituje sa /dev/cdrom uređaja, pa ukoliko imate 2 CD uređaja (recimo DVD i CDRW), samo **jedan** od njih će moći da reprodukuje Audio CD. 

&nbsp;

### Imate DVD uređaj 

Ponekada se pri instalaciji kreira _/dev/dvd_ ali ne i _/dev/cdrom_. Vidite na &scaron;ta linkuje _/dev/dvd_: ll /dev/dvd a zatim napravite simbolički link na _/dev/cdrom_

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=375)