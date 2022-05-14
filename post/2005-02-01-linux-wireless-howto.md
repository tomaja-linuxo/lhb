---
author: tomaja
date: "2005-02-01T05:18:40Z"
excerpt: Svrha ovog dokumenta je da opi&scaron;e tačan postupak kao i potreban hardver
  i softver za uspostavljanje funkcionalne bežične veze između PC ma&scaron;ine i
  Rutera baziranog na Linux opreativnom sistemu. Ove instrukcije se odnose na opstavljanje
  i pode&scaron;avanje  wireless mreže na Mandrake 10.1
guid: https://forum.linuxo.org/2005/02/01/linux-wireless-howto/
id: 727
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Linux Wireless HOWTO
url: /linux-wireless-howto/
---
Svrha ovog dokumenta je da opi&scaron;e tačan postupak kao i potreban hardver i softver za uspostavljanje funkcionalne bežične veze između PC ma&scaron;ine i Rutera baziranog na Linux opreativnom sistemu. Ove instrukcije se odnose na opstavljanje i pode&scaron;avanje wireless mreže na Mandrake 10.1<!--break-->

  
Hardver

Za uspostavljanje ove konekcije je kori&scaron;ten slede?i hardver:

* D-Link AirPlus DWL-520+ Wireless NIC (PCI) 802.11b  
* D-Link AirPlus DI-614+ Wireless Router 802.11b

Upustvo za instalaciju

1. Instalirajte Mandrake 10.1 a nakon toga i sledeća dva paketa preko urpmi:

urpmi kernel-source-2.6.8.1-10mdk.i586.rpm  
urpmi dhcpcd

ACX drajver je takođe uključen u Mandrake 10.1, ali nije radio odmah po instalaciji. Zato ga download-ujte da bi dobili start_net skriptu (locirana u scripts podirektorijumu).

Skripta se može naći zajedno sa ACX drajverom na: <a href="http://acx100.sourceforge.net/" target="_blank">http://acx100.sourceforge.net/</a>

2. Otvorite prozor konzole/terminala (bash), i postanite "root". Ukucajte:

su &#8211; root 

3. Promenite direktorijum. Ukucajte:

cd /usr/local/src 

4. Raspakujte sadržaj ACX drajvera u /usr/local/src/acx100.

5. Pređite u taj direktorijum. Ukucajte:

cd /usr/local/src/acx100 

6. Download-ujte i pripremite drajvere. Ukucajte:

./scripts/fetch_firmware 

7. Registrujte drajver u operativnom sistemu. Ukucajte:

rmmod acx100_pci.ko  
cd /lib/modules/2.6.8.1-10mdk/kernel/3rdparty/acx100  
gunzip acx100_pci.ko.gz  
insmod acx100\_pci.ko firmware\_dir=/usr/local/src/acx100/firmware  
gzip acx100_pci.ko

8. Editujte /usr/local/src/acx100/scripts/start_net. Pronađite i promenite sledeće linije, kako je prikazano:

#if test -n "\`lsmod |grep acx\_pci\`"; then ${SCRIPT\_AT}/stop_net; fi

#$INSMOD $MODULE\_AT debug=$DEBUG firmware\_dir=$FIRMWARE_AT  
#if test "$?" = "0"; then echo "Module successfully inserted."; else echo &#8230;

9. Podesite svoju IP adresu (DHCP takođe radi). Izmenite sledeću liniju:

scripts/start_net

Linije 25 i 27 moraju biti izmenjene. Na primer:

IP=192.168.0.101  
GATEWAY=192.168.0.1

Znači pretpostavljamo da je ruter gateway, i da koristi IP 192.168.0.1.

10. Sačuvajte izmene u fajlu, zatvorite editor i pokrenite mrežu. Ukucajte:

./scripts/start_net 

11. Proverite instalaciju. Ukucajte:

iwconfig wlan0 

Primer outputa:

wlan0 IEEE 802.11b+ ESSID:off/any Nickname:"acx100 v0.2.0pre8"  
Mode:Auto Channel:6 Access Point: 00:0A:0B:0C:0D:0E  
Bit Rate=11Mb/s Tx-Power:20 dBm Sensitivity=176/255  
Retry min limit:5 RTS thr:off  
Encryption key:off  
Power Management:off  
Link Quality:100/100 Signal level:71/100 Noise level:0/100  
Rx invalid nwid:0 Rx invalid crypt:0 Rx invalid frag:0  
Tx excessive retries:0 Invalid misc:0 Missed beacon:0

12. Da bi izbegli tx 0x20 gre&scaron;ke (u /var/log/messages). Ukucajte:

iwconfig wlan0 retry min limit 250  
iwconfig wlan0 retry max limit 250  
iwconfig wlan0 txpower auto  
iwconfig wlan0 commit 

13. Izmenite /etc/resolv.conf i dodajte sopstvena imena servera. Ove vrednosti će te naravno dobiti od svog provajdera (ISP). Na primer:

nameserver 24.64.196.100  
nameserver 24.64.196.200

Za dalju pomoć i vi&scaron;e informacija možete pogledati sledeće linkove:

* [ACX 100 HOWTO](http://www.houseofcraig.net/acx100_howto.php)  
* [ACX 100 SourceForge Homepage](http://acx100.sf.net/)  
* [Ndis Wrapper](http://ndiswrapper.sourceforge.net/)

Takođe možete koristiti i sledeće komande da bi mogli da utvrdite razlog eventualnog problema:

* dmesg  
* cat /var/log/messages  
* cat /proc/interrupts  
* ifconfig wlan0 txpower 20

Takođe prepručujem da pogledate listu kompatibilnog hardvera na  
<http://www.hpl.hp.com/personal/Jean_Tourrilhes/Linux/Linux.Wireless.drivers.html>

Izgleda da kombinovanje opreme različitih proizvođača niej ba&scaron; preporučljivo iako su svi delovi 802.11b "kompatibilni." Ja sam koristio DWL-520+ i Linksys ruter, ali konekcija je bila očajna &#8212; gubici paketa su bili redovni, i nisam uspeo da to re&scaron;im (veća antena, smanjenje razdaljine između rutera i NICa ,itd.). Kako sam pre&scaron;ao na DWL-614+, gubici paketa su smanjeni (čak i pri samo 30% signala).

Takođe bi sledeće kartice trebale da budu podržane od strane Linux-a:

* Lucent Orinoco Silver  
* Netgear MA311

Greg Haze je prijavio da i sledeće kombinacije hardvera funkcioni&scaron;u:

* D-Link 802.11b DWL-122 mini-USB Prism2/2.5/3 wlan-ng drajveri  
* Broadcom Corporation BCM94306 802.11g ndiswrapper sa Windows drajverima  
* SMC 802.11b 2532W-B PCMCIA Prism2/2.5/3 wlan-ng drajveri  
* D-Link 802.11b DWL-650 PCMCIA Prism2/2.5/3 wlan-ng drajveri

Da bi koristili DHCP potrebno je da promenite scripts/start_net, kao na sledećem primeru:

if test $USE_DHCP -eq 1; then  
\# fetch an IP address from DHCP  
#rm -f /etc/dhcpc/dhcpcd-$DEV.pid > /dev/null  
dhcpcd -d $DEV -t 12  
\# OR  
\# pump -i $DEV 

Nakon pokretanja ./scripts/start_net, možete videti kanale pomoću sledeće komande:

dmesg | tail -100 | more 

autor: [Dave Jarvis](http://www.joot.com/dave)  
prevod i izmene: tomaja

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=727)