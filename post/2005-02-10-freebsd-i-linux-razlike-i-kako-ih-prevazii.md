---
author: tomaja
date: "2005-02-10T12:50:10Z"
excerpt: |
  Ovaj tekst je namenjen svim korisnicima koji žete da probaju FreeBSD a
  ve? su koristili Linux sistem. Jedna od stvari koja zna da bude
  iritiraju?a Linux korisnicima koji probaju FreeBSD jesu razlike u
  radnom okruženju. Jedna od prvih je nedostatak bash-a .Sre?om, ako ste
  ve? navikli na bash komande i izgled ne?e vam trebati puno vremena da
  ga integrišete u FreeBSD. Kao root korisink dodajte bash paket:
guid: https://forum.linuxo.org/2005/02/10/freebsd-i-linux-razlike-i-kako-ih-prevazii/
id: 743
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: FreeBSD i Linux-razlike i kako ih prevazi?i
url: /freebsd-i-linux-razlike-i-kako-ih-prevazii/
---
Ovaj tekst je namenjen svim korisnicima koji žete da probaju FreeBSD a  
ve? su koristili Linux sistem. Jedna od stvari koja zna da bude  
iritiraju?a Linux korisnicima koji probaju FreeBSD jesu razlike u  
radnom okruženju. Jedna od prvih je nedostatak bash-a .Sre?om, ako ste  
ve? navikli na bash komande i izgled ne?e vam trebati puno vremena da  
ga integrišete u FreeBSD. Kao root korisink dodajte bash paket:<!--break-->

  
\# pkg_add -r bash

ovom komandom ?ete direktno sa Interneta prona?i prekompajlirani paket,  
automatski instalirati paket i udate-ovati /etc/shells. Ne zaboravite  
da je putanja za bash druga?ija u FreeBSDu, jer je bash za FreeBSD  
third-party aplikacija pa je putanja:

$ which bash  
/usr/local/bin/bash

U FreeBSD, korisni?ki binarni fajlovi koji dolaze sa operativnim  
sistemom se nalaze u /bin, sistemski binarni fajlovi u /sbin, a  
sistemski konfiguracioni fajlovi u /etc. Ekvivalentno tome, third-party  
aplikacije i njeni konfiguracioni fajlovi se nalaze u /usr/local/bin,  
/usr/local/sbin, i /usr/local/etc. Ovim lako možete do?i i do zaklju?ka  
šta je od aplikacija došlo zajedno sa opretativnim sistemom a šta ne.

Posle instalacije bash-a, iz obi?nog korisni?kog naloga možete kreirati  
alias za komandu ls kojom postižete ispis u boji:

$ vi ~/.bashrc  
alias ls=&#8217;ls -G&#8217;

Kada snimite izmene, ukucajte bash za pokretanje shell-a i pokrenite i  
komandu ls za testiranje.

Pretpostavljam da bi stalno potretanje bash-a pri svakom logovanju u  
sistem bilo zamorno, verovatno ?ete hteti da promenite default shell za  
svoj korisni?ki nalog. Kao i ve?ina Linux distribucija, FreeBSD koristi  
shadow bazu podataka za lozinke. MeÄ‘utim, za razliku od Linux-a, ona se  
ne nalazi u /etc/shadow.Umesto toga ona je smeštena u  
/etc/master.passwd, i&#8211;što je veoma bitno&#8211;ne morate editovati ovaj  
fajl direktno.

Umesto toga, koristite alatku chpass da bi update-ovali bazu sa  
lozinkama. Evo kako možete podesiti shell okruženje za korisni?ko ime  
sima:

\# chpass -s /usr/local/bin/bash sima  
chpass: updating the database&#8230;  
chpass: done

Kao i Linux komanda usermod, chpass ima ima i dgure parametre, pa zato  
pogledajte man chpass. Ipak, ako volite da vidite šta menjate i znate  
da koristite vi editor koristite vipw. Ovo ?e otvoriti bazu sa  
lozinkama u vi editoru. I oko vi editora ima manjih razlika. FreeBSD  
kao default koristi nvi pa ako ste navikli na vim onda ga možete i  
instalirati: 

\# pkg_add -r vim5

Naravno, možete ga na?initi i default editorom dodavanjem nove linije u  
korisni?ki fajl ~/.bashrc :

export EDITOR=/usr/local/bin/vim

Ne zaboravite da ukucate . ~/.bashrc da bi obavestitli bash o promenama  
u konfiguracionom fajlu. Sada ?e vipw koristiti vim umesto vi  
editora.

Kreiranje korisni??kog naloga

Unix omogu?ava nekoliko na?ina za kreiranje korisni?kih naloga, pa ?ete  
tu veroavtno na?i i komandu adduser, samo što u FreeBSD verzija koristi  
interaktivni mod.  
Ukoliko više volite da koristite grafi?ko okruženje onda koristite  
/stand/sysinstall meni. Njegova Configure opcija vam omogu?ava da  
instalirate softver, kreirate korisnike, podešavate mrežu i X okruženje.

Imena ureÄ‘aja

Ovde takoÄ‘e postoje manje razlike. Na primer, vaša prva mrežna kartica  
ne?e biti /dev/eth0. Umesto toga, ime ureÄ‘aja ?e ukazivati na chipset  
koji koristi vaša kartica. Evo jednog od na?ina da saznate ime vaše  
kartice(a):

$ dmesg | grep Ethernet  
rl0: Ethernet address: 00:05:5d:d2:19:b7  
rl1: Ethernet address: 00:05:5d:d1:ff:9d  
ed0: <NE2000 PCI Ethernet (RealTek 8029)> port 0x9800-0x981f irq  
10 at  
device 11.0 on  
pci0

Ovaj konkretni sistem ima tri mrežne kartice: dve Realtek kartice (rl0  
i rl1) i jednu generi?ku (ed0). :

$ whatis rl  
rl(4)  
&#8211; RealTek 8129/8139 Fast Ethernet device driver

$ whatis ed  
ed(1),  
red(1)  
&#8211; text editor  
ed(4)  
&#8211; ethernet device driver

TakoÄ‘e ?e na?i da se razlikuju i imena vaših hard diskova i particija:

$ df  
Filesystem 1K-blocks Used Avail  
Capacity Mounted on  
/dev/ad0s1a 253678 65594  
167790 28% /  
devfs  
1  
1 0  
100% /dev  
/dev/ad0s1e 253678 18482  
214902 8% /tmp  
/dev/ad0s1f 13147670 6526230 5569628  
54% /usr  
/dev/ad0s1d 253678 42232  
191152 18% /var  
linprocfs  
4  
4 0  
100% /usr/compat/linux/proc

Uopredimo ovo gore sa df output-om iz Red Hat sistema:

$ df  
Filesystem 1K-blocks Used Available  
Use% Mounted on  
/dev/hda2 9506024  
2080628 6942516 24% /  
/dev/hda1 99043  
9275 84654 10% /boot  
none  
63016  
0 63016 0%  
/dev/shm  
/dev/cdrom 636408  
636408 0  
100% /mnt/cdrom

Red Hat koristi hd za prikaz IDE hard diskova; dok FreeBSD koristi ad.  
Red Hat koristi slovo a za prikaz primarnog master diska; FreeBSD  
koristi 0. Red Hat zatim koristi broj za prikaz odreÄ‘ene particije&#8211;u  
ovom slu?aju 1 i 2 su prve dve primarne particije. FreeBSD  
koristi ise?ke a ovaj sistem ima 1 FreeBSD ise?ak izdeljen u nekoliko  
particija. Po konvenciji, particija a je / dok je b /swap.  
Ovaj konkretni sistem ima i d montiran na /var, e montiran na  
/tmp, kao i f montiran na/usr.

Kao i Linux, FreeBSD koristi fajl /etc/fstab za odreÄ‘ivanje  
na?ina montiranja fajl sistema; meÄ‘utim on ne koristi /etc/mtab.  
(ukoliko ste instakirali Linux compatibility, koristi više  
/usr/compat/linux/proc/mtab). Komande mount i df prikazuju trenutno  
montirane fajl sisteme.

Å ta se desilo sa /proc (virtuelnim fajl sistemom)?

FreeBSD korisiti svoj mo?ni sysctl mehanizam meÄ‘utim ako ste  
instalirali Linux compatibility mo?i ?ete da pronaÄ‘ete ve?inu stvari u  
/usr/compat/linux/proc.  
Ipak, preporu?ujem vam da probate FreeBSD-jev sysctl.

Kucanje naredbe sysctl -a | more (a for &#8222;all&#8220;) je ekvivalentno  
svakog /proc unosa odjednom. Ovo je odli?an na?in da ne samo  
vidite šta se dogaÄ‘a u aktivnom i teku?e radnom sistemu ve? i da  
razumete šta termin &#8222;kernel state&#8220; zna?i. 

Naravno, primenom naredbe grep možete vam pomo?i ukoliko znate šta  
tražite. Na primer, da bi videli trenutnu iskorištenost memorije :

% sysctl -a | grep -i memory  
Virtual Memory: (Total: 614K,  
Active 185444K)  
Real Memory: (Total: 295928K  
Active 100972K)  
Shared Virtual Memory: (Total: 74960K Active: 68524K)  
Shared Real Memory: (Total: 43296K Active: 40048K)  
Free Memory Pages: 36412K  
p1003\_1b.memory\_protection: 0  
p1003\_1b.shared\_memory_objects: 1

superuser ili root korisnik ima kogu?nost menjanja sysctl opcija u  
letu. Na primer, da bi videli sistemski TTL:

\# sysctl -a | grep ttl  
net.inet.ip.ttl: 64

Da bi ga promenili (upisali):

\# sysctl -w net.inet.ip.ttl=100  
net.inet.ip.ttl: 64 -> 100

#sysctl net.inet.ip.ttl  
net.inet.ip.ttl: 100

man sysctl vam svakako preporu?ujemo.

Mnoge Linux komande(kao što su npr., ps, top, i free) pretražuju  
/proc radi informacija o tome šta se trenutno dogaÄ‘a u sistemu. Sli?no  
tome mnoge FreeBSD komade pretražuju sysctl. Iako bi anravno  
mogli ru?no da pošaljete informacije u /proc grep-u kroz sysctl-a,  
obi?no je lakše imati komandz koja ?e sama obaviti upite i prikazati  
vam rezultate.Na primer, na FreeBSD 5.x sistemu, devinfo ?e  
prikazati sistemske resource-ove, i to po tipu:

$ devinfo -ru  
Interrupt request lines:  
0x0 (root0)  
0x1 (atkbd0)  
0x3 (sio1)  
0x4 (sio0)  
0x5 (rl0)  
0x6 (fdc0)  
0x7-0x8 (root0)  
0x9 (acpi0)  
0xa (pcm0)  
0xb (uhci0)  
0xc (psm0)  
0xd (root0)  
0xe (ata0)  
0xf (ata1)  
DMA request lines:  
0-1 (root0)  
2 (fdc0)  
3-7 (root0)  
I/O ports:  
0x0-0xf (root0)  
0x10-0x1f (acpi_sysresource0)  
0x20-0x21 (root0)  
<snip>  
I/O memory addresses:  
0x0-0x9ffff (root0)  
0xa0000-0xbffff (vga0)  
0xc0000-0xcbfff (orm0)  
0xcc000-0xfbffffff (root0)  
0xfc000000-0xfdffffff (agp0)  
0xfe000000-0xffffffff (root0)  
open if_tun units:  
0-32767 (root0)

swapinfo ?e vam prikazati trenutno montirane swap ureÄ‘aje:

$ swapinfo  
Device  
1K-blocks Used Avail Capacity  
/dev/ad0s1b  
637704 156  
637548 0%

Postoje na desetine korisnih programa. Da bi ih pronašli iskoristite  
slede?e  
tri komande:

$ apropos info | grep 8  
$ apropos stat | grep 1  
$ apropos stat | grep 8

Moduli

kao i u Linuxu, FreeBSD kernel podržava uklju?ivanje i isklju?ivanje  
modula. Ovo omogu?ava administratorima da dodaju ili uklone drajver bez  
potrebe da rekompajliraju kernel ili restartuju sistem. Mogu?i moduli  
na kraju imena fajla imaju ekstenziju .ko u /boot/kernel.

da bi videli koji su moduli trenutno u?itani pokrenite naredbu kldstat:

$ kldstat  
Id Refs Address Size Name  
1 10 0xc0400000 3348d8 kernel  
2 1 0xc0735000 51ac8 acpi.ko  
3 1 0xc3168000 6000  
linprocfs.ko  
4 1 0xc316e000 19000 linux.ko

Ukoliko ste znatiželjni da saznate šta svaka kolona prikazuje  
pogledajte man 2 kldstat. Ina?e, na?in prikaza je sli?an Linux.ovoj  
lsmod komandi.  
U Linuxu takoÄ‘e iamte komande insmod i rmmod koji omogu?avaju  
uklju?ivanje i isklju?ivanje modula. U FreeBSD imate ekvivalentne  
komade: kldload i kldunload. Na primer, za u?itavanje podrške za USB  
skener:

\# kldload uscanner.ko

Da bi je uklonili kada završite:

\# kldunload uscanner.ko

U?itavanje ne?ega što je ve? stati?ki iskompajlirano u kernelu ?e vam  
prikazati grešku:

\# kldload snd_pcm.ko  
kldload: can&#8217;t load snd_pcm.ko: File exists

Ukoliko ne znate šta koji modul radi, koristite whatis. Pretpostavimo  
šta radi modul if_pcn.ko. U pretraživanje ne?e biti uklju?ena  
ekstenzija .ko. TakoÄ‘e ne?e biti uklju?ena ni kategorija modula  
if\_; ona odreÄ‘uje modul po tipu interfejsa. (sli?no kao što snd\_  
reprezentuje sound kategoriju.) Zna?i osta nam pcn, pa komanda izgleda  
ovako:

$ whatis pcn  
pcn(4) &#8211; AMD PCnet/PCI fast  
ethernet device driver

što zna?i da u ovoj konkretnoj mašini NIC (mrežna kartica) ubada u tu  
kategoriju a man 4 pcn ?e nam dati ta?ne opise NIC modela koji su  
pokrivenils covered by this particular kernel module.

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=743)