---
author: tomaja
date: "2004-08-03T17:00:51Z"
excerpt: |
  <span class="postbody"><a href="http://www.linuxo.com/user.php?op=userinfo&uname=popac">popac</a> piše "<span style="font-style: italic;">Ovo
  je mini HOWTO na srpskom koji ce vam pomo?i
  da instalirate smart modeme na linuxu, a ne da se patite kao sto sam to
  ja radio!!
  </span>" (Ovi drajveri ?esto mogu da rade i na Intelovim PCI modemima
  kao i na notebook ra?unarima kao što su nove serije Acer ili HP
  mašina  <span style="font-weight: bold;">prim.admin</span>.)
guid: https://forum.linuxo.org/2004/08/03/instalacija-smartlink-drajvera/
id: 496
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Instalacija SmartLink drajvera
url: /instalacija-smartlink-drajvera/
---
<span class="postbody"><a href="http://www.linuxo.com/user.php?op=userinfo&#038;uname=popac">popac</a> piše &#8222;<span style="font-style: italic;">Ovo<br /> je mini HOWTO na srpskom koji ce vam pomo?i<br /> da instalirate smart modeme na linuxu, a ne da se patite kao sto sam to<br /> ja radio!!<br /> </span>&#8220; (Ovi drajveri ?esto mogu da rade i na Intelovim PCI modemima<br /> kao i na notebook ra?unarima kao što su nove serije Acer ili HP<br /> mašina <span style="font-weight: bold;">prim.admin</span>.)<!--break-->

<br /> Na sajtu <a href="http://www.smlink.com" target="_blank">www.smlink.com</a><br /> moze se naci slmodem-2.9.9.tar.gz verzija drajvera:</p> 

<p>
  <a href="http://www.smlink.com/main/down/slmodem-2.9.9.tar.gz"
target="_blank">http://www.smlink.com/main/down/slmodem-2.9.9.tar.gz</a><br /> <br /> Odmah moram da vam kazem da ova verzija drajvera kod mene<br /> prijavljuje NO CARRIER na svaka 3 minuta i samim tim nece da radi, al<br /> sta je tu je, ranije verzije drajvera nisu dostupne na tom sajtu, a<br /> verujem da je to problem samo kod mene
</p>

<p>
  1. Posto ste downloadovali drajver otpakujte ga:<br /> <br /> $ gzip -dc slmdm-2.9.9.tar.gz | tar xf &#8211;
</p>

<p>
  2. udjite u direktorijum gde ste ga otpakovali:<br /> <br /> $ cd slmdm-2.9.9
</p>

<p>
  3. Po potrebi promenite Makefile da pokazuje put do vaseg kernel<br /> source-a:<br /> <br /> KERNEL_DIR=/putanja/do/linux-kernela<br /> <br /> u vecini slucajeva ova putanja ce odgovarati i nema potrebe da je<br /> menjate, a po defaultu je:<br /> <br /> KERNEL_DIR:=/lib/modules/$(shell uname -r)/build
</p>

<p>
  4. Kompajlirajte drajver:<br /> <br /> $ make
</p>

<p>
  5. Instalirajte drajver:<br /> <br /> $ make install
</p>

<p>
  6. Nakon instalacije potrebno je pokrenuti module<br /> <br /> ako koristite eksterne (USB) modeme<br /> <br /> $ modprobe slusb<br /> <br /> ako koristite AMR modem<br /> <br /> $ modprobe slamr
</p>

<p>
  Ukoliko zelite da vam se moduli podizu prilikom boot-a jednostavno<br /> upisite slamr ili slusb naprimer u /etc/modprobe.conf,<br /> /etc/modprobe.preload, /etc/modules&#8230; sto zavisi od distribucije.
</p>

<p>
  7. Sada je vrema da pokrenete aplikaciju:<br /> <br /> ukoliko koristite USB modem:<br /> <br /> $ /usr/sbin/slmodemd &#8211;country=<MojaDrzava> /dev/slusb0<br /> <br /> ukoliko koristite AMR modem:<br /> <br /> $ /usr/sbin/slmodemd &#8211;country=<MojaDrzava> /dev/slamr0
</p>

<p>
  gde je <MojaDrzava> jedna od zemalja koje se mogu izlistati<br /> pomocu<br /> <br /> $ slmodemd &#8211;countrylist<br /> <br /> a /dev/slusb0 odnosno /dev/slamr0<br /> <br /> uredjaj, tj. modem preko koga izlazite na insternet. Ukoliko imate<br /> npr. dva usb modema prvi ce biti /dev/slusb0 a drugi /dev/slusb1&#8230;
</p>

<p>
  8. Da bi drajver radio kako treba morate da napravite link:<br /> <br /> $ ln -s /dev/ttySL0 /dev/modem
</p>

<p>
  9. Ukoliko vam je tesko da stalno kada zelite da izadjete na internet<br /> pokrecete <br /> $ modprobe slusb<br /> <br /> $ /usr/sbin/slmodemd &#8211;country=<MojaDrzava> /dev/slusb0<br /> <br /> ili<br /> <br /> $ modprobe slamr<br /> <br /> $ /usr/sbin/slmodemd &#8211;country=<MojaDrzava> /dev/slamr0
</p>

<p>
  mozete probati neke od skripti koje se nalaze u slmodem-2.9.9/scripts<br /> <br /> za sada postoje skripte za mandrake, suse i debijan linux distribuciie<br /> <br /> <span style="color: red;">Nadam se da ce ovo nekome da pomogne</span></span>
</p>

<p>
  <a href="https://linuxo.org/nova-tema-na-forumu/?se_pid=496">Креирај тему форума везану за овај текст</a>
</p>