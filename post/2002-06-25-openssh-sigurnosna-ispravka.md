---
author: Tigerheart
date: "2002-06-25T14:28:40Z"
excerpt: |
  Detalji o novootkrivenom OpenSSH bagu ?e biti objavljeni tokom slede?e nedelje.<br>
  Po re?ima OpenSSH tima, ovaj  bag se ne može upotrebiti za napad sa mreže<br>
  kada je sshd pokrenut sa odvojenim ovlaštenjima.<br>
  Kod koji regu?iše separaciju privilegija je zna?ajno unapreÄ‘en od OpenSSH
  v3.3<br>
  koja je objavljena 21 juna. Na žalost,  postoje još neki problemi vezani
  za <br>
  ovu verziju; kompresija ne funkcioniše na svim operativnim sistemima a <br>
  PAM podrška još nije kompeltno završena.
guid: https://forum.linuxo.org/2002/06/25/openssh-sigurnosna-ispravka/
id: 192
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: OpenSSH &#8211; sigurnosna ispravka
url: /openssh-sigurnosna-ispravka/
---
Detalji o novootkrivenom OpenSSH bagu ?e biti objavljeni tokom slede?e nedelje.  
Po re?ima OpenSSH tima, ovaj bag se ne može upotrebiti za napad sa mreže  
kada je sshd pokrenut sa odvojenim ovlaštenjima.  
Kod koji regu?iše separaciju privilegija je zna?ajno unapreÄ‘en od OpenSSH  
v3.3  
koja je objavljena 21 juna. Na žalost, postoje još neki problemi vezani  
za  
ovu verziju; kompresija ne funkcioniše na svim operativnim sistemima a  
PAM podrška još nije kompeltno završena.<!--break-->Razvojni tim OpenSSH ohrabruje sve koji žele da izvrše ažuriranje na verziju

  
3.3  
i omogu?e sebi separaciju privilegija. Ovo možete u?initi tako ukoliko slede?u  
liniju ubacite u vaš /etc/ssh/sshd_config fajl:

UsePrivilegeSeparation yes

Kada je re? o nagu koji ?e biti objavljen slede?e nedelje on sam nije otklonjen  
u  
verziji 3.3, ipak ako je separacija privilegija uklju?ena, ne?ete biti ranjivi.  
Ovo je zbog toga što separacija privilegija koristi odvojen ne-privilegovani  
proces  
za ve?inu posla, što opet vodi do toga da bilo koja rupa u programu ne?e  
ugroziti  
root privilegije. 

MandrakeSoft takoÄ‘e preporu?uje svim korisnicima da unaprede OpenSSH na ovu  
  
novu verziju Ova verzija kreira novog korisnika i grupu u sistemu pod imenom  
  
sshd i koji se koriste za pokretanje ne-privilegovanih procesa.

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=192)