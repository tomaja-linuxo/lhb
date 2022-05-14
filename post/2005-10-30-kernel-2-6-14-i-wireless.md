---
author: tomaja
date: "2005-10-30T04:45:12Z"
excerpt: |
  Linux
  kernel 2.6.14 je izašao kao ?etvrto veliko izdanje u toku 2005, sa
  gomiloma poboljšanja, uklju?uju?i i nove update-ove drajvera, nove
  virtualne sisteme i poboljšanja za wireless konekcije. 2.6.14 kernel
  dolazi samo 2 meseca nakon <a
  href="http://www.internetnews.com/dev-news/article.php/3531276">objavljivanja</a>
  2.6.13 kernela u avgustu. Ovo takoÄ‘e ozna?ava i po?etak novog razvojnog
  procesa u razvoju kernela. A sada malo detaljnije o samom kernelu i
  wireless poboljšanjima...
guid: https://forum.linuxo.org/2005/10/30/kernel-2-6-14-i-wireless/
id: 985
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Kernel 2.6.14 i wireless
url: /kernel-2-6-14-i-wireless/
---
Linux  
kernel 2.6.14 je izašao kao ?etvrto veliko izdanje u toku 2005, sa  
gomiloma poboljšanja, uklju?uju?i i nove update-ove drajvera, nove  
virtualne sisteme i poboljšanja za wireless konekcije. 2.6.14 kernel  
dolazi samo 2 meseca nakon [objavljivanja](http://www.internetnews.com/dev-news/article.php/3531276)  
2.6.13 kernela u avgustu. Ovo takoÄ‘e ozna?ava i po?etak novog razvojnog  
procesa u razvoju kernela. A sada malo detaljnije o samom kernelu i  
wireless poboljšanjima&#8230; <!--break-->

Wireless konekcije doijaju na zna?aju u 2.6.14 kernel, zahvaljuju?i  
verziji 19 Wireless Extensions API ([definicija](http://inews.webopedia.com/SHARED/search_action.asp?Term=API&Template_Name=inews.webopedia.com)),  
koji je uba?en u kernel. 

Linux Wireless Ekstenzija i Wireless alati su OpenSource projekat  
sponzorisan od strane HP-a i postoji još od 1996. HP kaže da Wireless  
ekstenzije predstavljaju generi?ki API koji omogu?ava drajverima da  
olakšaju konfigurisanje za korisnike i statistiku specifi?nu za ve?inu  
Wireless  
LAN mreža. 

Ipak, uprkos novoj verziji, HP Linux Wireless Estenzije i Alati kaže  
da ve?ina Linux korisnika ne?e mnogo dobiti sa novom verzijom Wireless  
Ekstenzija. 

&#8222;Ovo je minor verzija, sa uglavnom malim izmenama iza zavese,&#8220; Kako  
je rekao Turil na internetnews.com. &#8222;Ve?ina idljivih promena je vezana  
za sreÄ‘ivanje Wireless statistics API-ja.&#8220; 

Turil kaže da Wireless Ekstenzije predstavljaju samo deo ukupne  
Linux Wireless  
infrastrukture i da nove vesti dolaze u 2.6.14 kernelu. Uzmite na  
primer u razmatranje novi 802.11. Ovaj deo kernela za 802.11 je još  
uvek u teškom razvoju ali ?e u dužim koracima pomo?i kreiranju  
jednostavnijih i boljih wireless drajvera. Turil kaže, &#8222;Kernel 2.6.14  
je takoÄ‘e prvi kernel koji uklju?uje HostAP i IPW (Centrino) drajvere.  
Ovi drajveri su do sada bili široko koriš?eni u Linux zajednici.&#8220; 

Turil je upozorio da se ne o?ekuje da ?e sav novi kod vezan za  
wireless biti od koristi. 

&#8222;Na primer, podrška za WPA (WE-18) je uba?ena u kernel 2.6.13, ali  
samo novi drajveri vam omogu?avaju da radite sa tim &#8220; kaže Turil. 

2.6.14 kernel takoÄ‘e uklju?uje drajvere za nove virtuelne fajl  
sisteme. Jedan od novo uba?enih fajl sistem je relayfs, koji omogu?ava  
velike brzine u transferu podataka izmeÄ‘u korisni?kog prostora i  
kernela. Securityfs  
je još jedan novi virtuelni fajl sistem ?iji je cilj koriš?enje  
sigurnosnih mofula 

TakoÄ‘e treba imati na umu da novi kernel sadrži i patch-eve i  
drajvere za serijski prika?ene SCSI (SAS) hardove, uklju?uju?i i novi  
LSI Logic MegaRAID SAS RAID drajver.

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=985)