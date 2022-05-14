---
author: popeye
date: "2005-09-03T20:40:31Z"
excerpt: |
  Mplayer, Xine i nasa slova<br />
  Pre nego sto pocnem hteo bih da napomenem da sam prilikom podesavanja subtitlova koristio<br />
  Mplayer 1.0-pre7 (koji sam skinuo sa http://packman.links2linux.org) instaliran na SuSE 9.3 Pro i libxine1-1.0cvs (xine-ui-0.99.3) . Nisam probao da ovako nesto uradim na drugim distribucijama ali verovatno nema razlike.<br />
guid: https://forum.linuxo.org/2005/09/03/mplayer-xine-hollywood-i-subtitle/
id: 950
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Mplayer, Xine, Hollywood i subtitle
url: /mplayer-xine-hollywood-i-subtitle/
---
Mplayer, Xine i nasa slova  
Pre nego sto pocnem hteo bih da napomenem da sam prilikom podesavanja subtitlova koristio  
Mplayer 1.0-pre7 (koji sam skinuo sa http://packman.links2linux.org) instaliran na SuSE 9.3 Pro i libxine1-1.0cvs (xine-ui-0.99.3) . Nisam probao da ovako nesto uradim na drugim distribucijama ali verovatno nema razlike.  
<!--break-->I- Mplayer podesavanja 

  
1. Skinite fontove sa oznakom CP1250 sa sajta http://mplayerhq.hu/homepage/design7/dload.html  
2. sadrzaj fajla otpakujte i iskopirajte u /usr/share/mplayer/fonts (tako da cete sada u njemu imati  
vise direktorijuma kao sto su font-aral-18-cp1250 font-arial-24-cp1250 itd.)  
3. U direktorijumu /usr/share/mplayer imate i direktorijum font koji je inace simbolicki link na  
direktorijum font-arial-14-iso-8859-1. Unjemu imate nekoliko .raw fajlova koji su inace fontovi koje  
koristi Mplayer kao i font.desc i osd-mplayer-a.raw i osd-mplayer-b.raw. Ja sam licno iskopirao sve fajlove iz /usr/share/mplayer/font-arial-24-cp1250 u direktorijum /usr/share/mplayer/font. Naravno morao sam da  
idem na overwrite fajlova font.desc, osd-mplayer-a.raw i osd-mplayer-b.raw. 

II- Xine  
1. Xine je jednostavan za podesavanje. Idite na Settings -> Setup pa na tab subtitles. U polju encoding  
of the subtitles ukucajte &#8222;cp1250&#8220; ( naravno bez navodnika :))

Napomena: Kod podesavanja Mplayera nemate potrebe da idete u Preferences da biste podesili fontove. Ja bar  
nisam to nikad uspeo da uradim. Kod Suse-a ne koristite PowerPlayer skin.Ne pitajte me zasto ali nesto brlja. U ovom kratkom objasnjavanju za Mplayer koristio sam font-arial-24-cp1250 velicinu slova (24) jer  
je 28 veliki a 18 mali. Tako da mislim da ce se i vama ovo odgovarati.  
Kod xine-a za SuSE 9.3 obavezno skinite xine-lib sa sajta http://packman.links2linux.org (na ovom sajtu mozete skinuti i Mplayer za SuSE i w32-codecs-all kako i vecinu popularnih programa za SuSE) jer su oni koje dolazi po defaultu za 9.3 Pro stvarno jadni pa necete moci da podesite subtitlove jer nema taba za subtitle 🙁 a i izbor codecsa je strasno los.  
P.S Nije bitno s kojim player-om se vozite vazno je samo da je pingvin vozac. Pozdrav

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=950)