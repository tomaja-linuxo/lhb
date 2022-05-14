---
author: tomaja
date: "2008-11-26T04:44:17Z"
excerpt: <p>Počelo je sa Mandrivom 2009.0, nastavilo se sa Ubuntuom&nbsp;8.10, a sada
  se u trku uključuje&nbsp;i <strong>Fedora&nbsp;10</strong>. Zajednica Fedorinih
  developera je najavila i objavila zvanično izdanje&nbsp;<a href="http://fedoraproject.org/"><u>Fedora
  10</u></a>, nove verzije ove, po njenim kreatorima, najpopularnije&nbsp;open source
  Linux distribucije. Ovo izdanje je svakako obećavajući korak za Fedoru koja nam
  donosi neka nove i značajne mogućnosti i tehnologije koje donose veći robustnost
  i iskoristivost&nbsp; za desktop korisnike. </p><p align="justify"><img class="
  alignright size-full wp-image-2152" src="https://linuxo.org/wp-content/uploads/2008/11/f10release.jpg"
  alt="Fedora 10" title="Fedora 10" hspace="4" width="200" height="100" align="right"
  />Fedora 10 u osnovi nosi&nbsp;Linux kernel&nbsp;2.6.27&nbsp;&nbsp;koji sam donosi
  unapređenu podr&scaron;ku za web kamere i novi&nbsp;Atheros ath9k wireless drajver.
  Od drugih softverskih novina, svakako treba pomenuti Firefox 3.0.4 u default instalaciji.
  &Scaron;to se tiče grafičkih okruženja, Fedora 10 nudi mogućnost instalacije GNOME-a
  2.24&nbsp;i KDE-a 4.1. Čitaj dalje...</p>
guid: https://forum.linuxo.org/2008/11/26/finis-trke-sa-novim-favoritom-fedora-10/
id: 2155
image: /wp-content/uploads/2008/11/f10release.jpg
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";s:4:"2152";s:11:"_thumb_type";s:5:"thumb";}
title: 'Finiš trke sa novim favoritom: Fedora 10'
url: /finis-trke-sa-novim-favoritom-fedora-10/
---
Počelo je sa Mandrivom 2009.0, nastavilo se sa Ubuntuom&nbsp;8.10, a sada se u trku uključuje&nbsp;i **Fedora&nbsp;10**. Zajednica Fedorinih developera je najavila i objavila zvanično izdanje&nbsp;[<u>Fedora 10</u>](http://fedoraproject.org/), nove verzije ove, po njenim kreatorima, najpopularnije&nbsp;open source Linux distribucije. Ovo izdanje je svakako obećavajući korak za Fedoru koja nam donosi neka nove i značajne mogućnosti i tehnologije koje donose veći robustnost i iskoristivost&nbsp; za desktop korisnike. 

<p align="justify">
  <img class=" alignright size-full wp-image-2152" src="https://linuxo.org/wp-content/uploads/2008/11/f10release.jpg" alt="Fedora 10" title="Fedora 10" hspace="4" width="200" height="100" align="right" />Fedora 10 u osnovi nosi&nbsp;Linux kernel&nbsp;2.6.27&nbsp;&nbsp;koji sam donosi unapređenu podr&scaron;ku za web kamere i novi&nbsp;Atheros ath9k wireless drajver. Od drugih softverskih novina, svakako treba pomenuti Firefox 3.0.4 u default instalaciji. &Scaron;to se tiče grafičkih okruženja, Fedora 10 nudi mogućnost instalacije GNOME-a 2.24&nbsp;i KDE-a 4.1. Čitaj dalje&#8230;
</p>

<!--break-->

Jedna od najznačajnih novih tehnologija u&nbsp;Fedori 10 jeste&nbsp;**PulseAudio** (PA). [<u><font color="#9d0404">PA sound server</font></u>](http://arstechnica.com/journals/linux.ars/2007/10/17/pulseaudio-to-bring-earcandy-to-linux)&mdash;koji je originalno predstavljen u Fedori 8&mdash;donosi ceo novi set najnovijih mogućnosti&nbsp;za Linux audio&nbsp;poput podr&scaron;ke za kontrolu pojedinih&nbsp;audio strimova, preme&scaron;tanje&nbsp;audio strimova između uređaja, i njihovu istovremenu reporodukciju na viđe uređaja. Tu su i neke zaista impresivne napredne mogućnosti, poput dinamičkog pode&scaron;avanja jačine zvuka i transparetni mrežni sistem za redirekciju kori&scaron;ćenjem Avahi-ja za&nbsp;auto detekciju 

Fedora 10 takođe uključuje i novu verziju&nbsp;Mrežnog Menadžera, koji se koristi za pode&scaron;avanje&nbsp;Fedorinih opcija za povezivanje. Nova verzija ima ugrađenu podr&scaron;ku za deljenje konekcije &scaron;to je svakako korisno u vi&scaron;e slučajeva, čak i u slučajevima kada korisnik sa 3G karticom želi da podeli konekciju sa drugim računarima preko WiFi mreže. 

<div style="text-align: center">
  <img class=" size-full wp-image-2153" src="https://linuxo.org/wp-content/uploads/2008/11/fedora10_3.jpg" alt="Fedora 10 - Network Manager" title="Fedora 10 - Network Manager" width="450" height="337" srcset="https://linuxo.org/wp-content/uploads/2008/11/fedora10_3.jpg 450w, https://linuxo.org/wp-content/uploads/2008/11/fedora10_3-300x225.jpg 300w" sizes="(max-width: 450px) 100vw, 450px" />
</div>

Fedorin sistem za upravljanje RPM paketima je značajno prerađen. RPM 4.6 sada poseduje nove mogućnosti i bolji kod. Neka ograničenja po pitanju licenci su uklonjena a maksimalna veličina paketa je povećana na 4GB. **PackageKit**,&nbsp;generički frontend za RPM sa svojim grafičkim interfejsom&nbsp;i podr&scaron;kom za&nbsp;programibilno upravljanje preko&nbsp;D-Bus API-ja, je čvr&scaron;će integrisano sa&nbsp;Fedorom 10. Takođe je integrisan i sa GStreamer-om i može automatski instalirati kodeke kada korisnik naiđe na format koji nije podržan po default-u. Fedora i dalje ne sadrži vlasničke kodeke, međutim korisnici imaju mogućnost da preko third-party riznica (repozitorijuma)&nbsp;iste instaliraju.

Neka pobolj&scaron;anja pri podizanju sistem su takođe implementirana u&nbsp;Fedora 10. Vreme podizanja sistema, zahvaljujući&nbsp;_readahead-u,_ &nbsp;je skraćeno za oko **10%**. Ovo je prvi put da&nbsp; Fedora koristi&nbsp;**Plymouth**, novi grafički&nbsp;startup sistem kome nije potreban&nbsp;X server. Novi grafički&nbsp;boot displej ne radi na svim ma&scaron;inama, ali postoji&nbsp;tekstualni mod za svaki slučaj. Ko želi da vidi kako to sve izgled apre instalacije može pogledati ovaj&nbsp;[<u><font color="#9d0404">video</font></u>](http://katzj.fedorapeople.org/plymouth-live.ogg) materijal. 

<div style="text-align: center">
  <img class=" size-full wp-image-2154" src="https://linuxo.org/wp-content/uploads/2008/11/fedora10_1.jpg" alt="Fedora 10 - Plymouth" title="Fedora 10 - Plymouth" width="450" height="336" srcset="https://linuxo.org/wp-content/uploads/2008/11/fedora10_1.jpg 450w, https://linuxo.org/wp-content/uploads/2008/11/fedora10_1-300x224.jpg 300w" sizes="(max-width: 450px) 100vw, 450px" />
</div>

Kao &scaron;to se moglo i očekivati, Fedora 10 predstavlja značajno naprednije izdanje u odnosu na svoje prethodnike&nbsp;&scaron;to se pored pomenutih novina ogleda i u prvim testovima koji se mogu naći na netu. Evo i par&nbsp;<a href="http://pictures.smashits.com/fedora-10-screenshots.html" target="_blank"><u>screenshotova</u></a>. **Fedora 10** se može preuzeti [<u><font color="#9d0404">ovde</font></u>](http://fedoraproject.org/en/get-fedora).&nbsp;HTTP mirori su verovatno zakrčeni pa u prvim danima kao bolja opcija ostaje&nbsp;BitTorrent. Za vi&scaron;e informacija, naravno, treba pogledati&nbsp;[<u><font color="#9d0404">zvaničnu najavu</font></u>](http://docs.fedoraproject.org/release-notes/f10/en_US/index.html)&nbsp;(SR). Info:ArsTechica

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=2155)