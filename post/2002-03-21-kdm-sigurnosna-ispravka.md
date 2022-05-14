---
author: tomaja
date: "2002-03-21T17:48:04Z"
excerpt: |
  <p>Ugrožene verzije: 7.1, 7.2, 8.0. Problem je otkriven sa default konfiguraciji kdm<br />
  dispej menađera u Mandrake Linux-u. Po default-u, on omogućava XDMCP<br />
  konekcije sa bilo kog hosta, što može biti zloupotrebljeno.Rešenje...
guid: https://forum.linuxo.org/2002/03/21/kdm-sigurnosna-ispravka/
id: 169
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: kdm &#8211; sigurnosna ispravka
url: /kdm-sigurnosna-ispravka/
---
Ugrožene verzije: 7.1, 7.2, 8.0. Problem je otkriven sa default konfiguraciji kdm  
dispej menađera u Mandrake Linux-u. Po default-u, on omogućava XDMCP  
konekcije sa bilo kog hosta, što može biti zloupotrebljeno.Rešenje&#8230;<!--break-->

<font face="Arial, Helvetica, sans-serif" size="2">Da bi onemogućili remote konekcije, izmenite /etc/X11/xdm/Xaccess fajl promenite<br /> sledeće dve linije:</font>

<font face="Arial, Helvetica, sans-serif" size="2">* #any host can get a login window<br /> * CHOOSER BROADCAST #any indirect host can get a chooser</font>

<font face="Arial, Helvetica, sans-serif" size="2">u:</font>

<font face="Arial, Helvetica, sans-serif" size="2">#* #any host can get a login window<br /> #* CHOOSER BROADCAST #any indirect host can get a chooser</font>

<font face="Arial, Helvetica, sans-serif" size="2">Napomena: Mandrake Linux 8.1 and 8.2 nisu osetljivi na ovu pojavu jer poseduju noviju<br /> verziju kdm-a koji u konf.opcijama<br /> /usr/share/config/kdm/kdmrc fajla ima iskljuèenu XDMCP podršku.</font>

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=169)