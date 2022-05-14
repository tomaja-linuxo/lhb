---
author: tomaja
date: "2002-06-06T15:11:26Z"
excerpt: |
  <p>Otkrivena je greška u BIND9 DNS serveru u verzijama koje prethode verziji 9.2.1. Ona može prouzrokovati gašenje servera kada rdataset parametar dns_message_findtype() funkcije u message.c nije NULL kao što se o?ekuje. Ovo stanje uzrokuje<br />
  da server prikaže poruku o grešci i zaustavi BIND server.&nbsp; Ovu grešku može iskoristiti uljez sa mreže specijalnim DNS paketom.<br />
  Ovo se jedino može upotrebiti za kreiranje Denial of Service na serveru; greška se pravilno detektuje pa tako napadaču neće biti dozvoljeno da izvrši ili pokrene bilo kakav kod na serveru.<br />
guid: https://forum.linuxo.org/2002/06/06/bind-sigurnosna-ispravka/
id: 185
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: bind &#8211; sigurnosna ispravka
url: /bind-sigurnosna-ispravka/
---
Otkrivena je greška u BIND9 DNS serveru u verzijama koje prethode verziji 9.2.1. Ona može prouzrokovati gašenje servera kada rdataset parametar dns\_message\_findtype() funkcije u message.c nije NULL kao što se o?ekuje. Ovo stanje uzrokuje  
da server prikaže poruku o grešci i zaustavi BIND server.&nbsp; Ovu grešku može iskoristiti uljez sa mreže specijalnim DNS paketom.  
Ovo se jedino može upotrebiti za kreiranje Denial of Service na serveru; greška se pravilno detektuje pa tako napadaču neće biti dozvoljeno da izvrši ili pokrene bilo kakav kod na serveru.  
Za update na novu verziju možete koristiti MandrakeUpdate opciju ili ručno instalirati paket sa linka;  
<http://www.mandrakesecure.net/en/ftp.php>

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=185)