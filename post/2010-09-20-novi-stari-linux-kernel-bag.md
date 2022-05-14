---
author: tomaja
date: "2010-09-20T07:08:48Z"
excerpt: |
  Što je najgore, ovaj ozbiljni sigurnosni propust je već bio otklonjen 2007 godine međutim godinu dana kasnije su kernel developeri uklonili taj patch i ponovo omogućili da se iskoristi <strong>32-bit compatibility mod</strong> u aktuelnom ali i prethodnim verzijama Linux kernela da se na 64-bit. Linux sistemima dođe do admin ovlašćenja. Na primer, napadač može upasti u sistem i iskoristiti rupu u web serveru da bi dobio pristup root ovlašćenjima na napadnutom sistemu.
guid: https://forum.linuxo.org/2010/09/20/novi-stari-linux-kernel-bag/
id: 2367
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Novi stari Linux kernel bag
url: /novi-stari-linux-kernel-bag/
---
Što je najgore, ovaj ozbiljni sigurnosni propust je već bio otklonjen 2007 godine međutim godinu dana kasnije su kernel developeri uklonili taj patch i ponovo omogućili da se iskoristi **32-bit compatibility mod** u aktuelnom ali i prethodnim verzijama Linux kernela da se na 64-bit. Linux sistemima dođe do admin ovlašćenja. Na primer, napadač može upasti u sistem i iskoristiti rupu u web serveru da bi dobio pristup root ovlašćenjima na napadnutom sistemu.

Na osnovu izveštaja, problem se javlja jer 32-bit call emulation lejer ne proverava da li je poziv istinski u Syscall tabeli. Ben Houks (Ben Hawkes), koji je otkrio problem, kaže da se ovaj sigurnosni propust može iskoristiti za pokretanje koda sa kernel ovlašćenjima. Exploit kojim već kruži mrežom u izvornom kodu je već razbijen Ubuntu 10.04 64bit. kod koga je pokrenuta konzola sa root ovlašćenjima.

Kernel developeri su postavili ispravku na svoj repo, pa se očekuje da će sve Linux distribucije ubrzo objaviti kernele koji rešavaju ovu bezbednosnu rupu.

Za sada, najednostavnije rešenje je [isključiti podršku](http://seclists.org/fulldisclosure/2010/Sep/273) za 32bitne aplikacije.

<p class="info">
  Više informacija na <a href="http://www.h-online.com/security/news/item/Hole-in-Linux-kernel-provides-root-rights-1081317.html">h-online</a> i <a href="https://bugzilla.redhat.com/show_bug.cgi?id=CVE-2010-3081">bugzilla.redhat.com</a>
</p>

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=2367)