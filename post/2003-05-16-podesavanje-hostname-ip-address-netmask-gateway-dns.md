---
author: tomaja
date: "2003-05-16T13:30:29Z"
excerpt: |
  Sva podešavanja se vrše u ?etiri fajla: <b>/etc/hosts</b> ,  <b>/etc/sysconfig/network</b> ,  <b>/etc/sysconfig/network-scripts/ifcfg-eth0</b> i  <b>/etc/resolv.conf</b> .
  Problemi koji mogu nastati ako sve nije ispravno podešeno mogu biti razni. Na primer, problemi sa mrežom, nemogu?nost konektovanja klijent ra?unara na web  preko gataway-a, konektovanje na web ali bez mogu?nosti surfovanja ( bez ikakvog u?itavanja u browser ), itd. Na primer, ako želite da izmenite Vašu mrežnu konfiguraciju na :
guid: https://forum.linuxo.org/2003/05/16/podesavanje-hostname-ip-address-netmask-gateway-dns/
id: 323
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Podešavanje hostname, IP address, netmask, gateway, DNS
url: /podesavanje-hostname-ip-address-netmask-gateway-dns/
---
Sva podešavanja se vrše u ?etiri fajla: **/etc/hosts** , **/etc/sysconfig/network** , **/etc/sysconfig/network-scripts/ifcfg-eth0** i **/etc/resolv.conf** .  
Problemi koji mogu nastati ako sve nije ispravno podešeno mogu biti razni. Na primer, problemi sa mrežom, nemogu?nost konektovanja klijent ra?unara na web preko gataway-a, konektovanje na web ali bez mogu?nosti surfovanja ( bez ikakvog u?itavanja u browser ), itd. Na primer, ako želite da izmenite Vašu mrežnu konfiguraciju na :<!--break-->

hostname: makina  
  
domainname: ja.com  
  
Static IP address: 192.168.12.21  
  
Netmask: 255.255.255.0  
  
Gateway: 192.168.12.254  
  
Primary DNS server: 192.168.12.21  
  
Secondary DNS server: 192.168.12.23 

Prvo je neophodno dodati host u /etc/hosts fajl ( linija sa &#8222;127.0.0.1&#8220; je neophodna &#8211; nemojte je brisati! ):

127.0.0.1 localhost.localdomain localhost  
  
192.168.12.21 makina

U /etc/sysconfig/network , treba da bude:

NETWORKING=yes  
  
HOSTNAME=makina  
  
GATEWAY=192.168.12.254

U /etc/sysconfig/network-scripts/ifcfg-eth0 , treba da bude:

DEVICE=eth0  
  
BOOTPROTO=static  
  
BROADCAST=192.168.12.255  
  
IPADDR=192.168.12.21  
  
NETMASK=255.255.255.0  
  
NETWORK=192.168.12.0  
  
ONBOOT=yes

DNS servers se podešava u: /etc/resolv.conf. U našem primeru: 

domain ja.com  
  
search ja.com  
  
nameserver 192.168.12.21  
  
nameserver 192.168.12.23

Ovo dosada je sve bilo peša?ki. Za definisanje IP address, route i gataway se mogu koristiti slede?e komande:

_ifconfig eth0 192.168.12.56 netmask 255.255.255.0 up  
  
route add default gw 192.168.12.1 eth0_ 

**Izbor iz FAQ**

Ako Vas sistem izveštava da nije pronašao mrežnu karticu, proverite da li Vaše mrežne kartice ima u kernelu. Otkucajte u konzoli:

_modprobe eth0_

_dmesg | less_

Pogledajte informacije o eth0, mogu Vam pomo?i da rešite problem.

_cat /etc/modules.conf_

Pogledajte da li postoji linija:

alias eth0 driver-name-like-wdi or 3c503

Nadam se da ?e ovo kratko uputstvo pomo?i po?etnicima!

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=323)