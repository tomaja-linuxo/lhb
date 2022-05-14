---
author: tomaja
date: "2009-07-03T08:35:09Z"
excerpt: '<p align="justify">Tokom prepodneva,&nbsp;Canonical je objavio vest da su
  <strong>dostupni</strong> <strong>važni sigurnosni update-ovi</strong> za sledeće
  distribucije <strong>Ubuntu Linux</strong>-a: <strong>6.06 LTS, 8.04 LTS, 8.10 i
  9.04</strong> (naravno, ovo važi i za odgovarajuće verzije&nbsp;distribucija Kubuntua,
  Edubuntua&nbsp;i Xubuntua). Ovaj update patch-uje 15 sigurnosnih propusta otkrivenih
  u Linux kernelu od vi&scaron;e hakera.Stoga preporučujemo da &scaron;to pre uradite
  update sistema! Za Ubuntu 9.04 update je najlak&scaron;e pokrenuti komandom: <span
  style="color: #008080"><em><strong>sudo dpkg -l linux-image-2.6.28-13-generic</strong></em></span>
  (ista komanda&nbsp;važi i za druge verzije, sa promenom na odgovarajuću verziju
  kernela). <u>Važna napomena sledi u nastavku teksta</u> !</p><p align="left">Vi&scaron;e
  detalja (lista otkrivenih sigurnosnih propusta) na <a href="http://news.softpedia.com/news/New-Kernel-Vulnerabilities-Affect-Ubuntu-6-06-8-04-8-10-and-9-04-OSes-115673.shtml"
  target="_blank">news.softpedia.com</a></p>'
guid: https://forum.linuxo.org/2009/07/03/ubuntu-kernel-update-ugrozeni-xubuntu-6-06-8-04-8-10-i-9-04/
id: 2285
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: 'Ubuntu kernel update !!! Ugroženi: (x)Ubuntu 6.06, 8.04, 8.10 i 9.04'
url: /ubuntu-kernel-update-ugrozeni-xubuntu-6-06-8-04-8-10-i-9-04/
---
<p align="justify">
  Tokom prepodneva,&nbsp;Canonical je objavio vest da su <strong>dostupni</strong> <strong>važni sigurnosni update-ovi</strong> za sledeće distribucije <strong>Ubuntu Linux</strong>-a: <strong>6.06 LTS, 8.04 LTS, 8.10 i 9.04</strong> (naravno, ovo važi i za odgovarajuće verzije&nbsp;distribucija Kubuntua, Edubuntua&nbsp;i Xubuntua). Ovaj update patch-uje 15 sigurnosnih propusta otkrivenih u Linux kernelu od vi&scaron;e hakera.Stoga preporučujemo da &scaron;to pre uradite update sistema! Za Ubuntu 9.04 update je najlak&scaron;e pokrenuti komandom: <span style="color: #008080"><em><strong>sudo dpkg -l linux-image-2.6.28-13-generic</strong></em></span> (ista komanda&nbsp;važi i za druge verzije, sa promenom na odgovarajuću verziju kernela). <u>Važna napomena sledi u nastavku teksta</u> !
</p>

<p align="left">
  Vi&scaron;e detalja (lista otkrivenih sigurnosnih propusta) na <a href="http://news.softpedia.com/news/New-Kernel-Vulnerabilities-Affect-Ubuntu-6-06-8-04-8-10-and-9-04-OSes-115673.shtml" target="_blank">news.softpedia.com</a>
</p>

<!--break-->

**Usled neizbežnih&nbsp;ABI promena, kernel paketi imaju novi broj verzije,&nbsp;koji nas uslovljava da reinstaliramo ili rekompajliramo sve third-party kernel module koji su instalirani. Na primer, nakon update-a na nove verzije kernela, aplikacije poput VirtualBox-a NEĆE raditi i&nbsp;zbog&nbsp;toga moramo rekompajlirati kernel modul iz konzole. Pored toga, ukoliko koristite&nbsp;linux-restricted-modules pakete, moraćete da update-ujete i njih da bi moduli radili sa novom verzijom Linux kernela**

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=2285)