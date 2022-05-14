---
author: tomaja
date: "2005-02-03T06:21:30Z"
excerpt: |
  Ako želite da kupite novi ra?unar, ili želite da instalirate Linux na
  mašini na kojoj je do sada bilo neki drugi operativni sistem, verovatno
  se pitate da li ?e sve komponente --
  grafika, modem, mrežna, zvu?na -- raditi na Linux-u. ProizvoÄ‘a?i ne
  mogu ili ne žele da vam kažu da li ?e njihov hardver raditi ili ne. Da
  bi to saznali morate znati na kojem ?ip setu je zasnovana odreÄ‘ena
  komponenta. Linux dolazi sa nekoliko odli?nih alata koji služe za
  pribavljanje podataka o hardveru kojeg imate u ra?unaru. Naj?eš?e
  korišteni programi su  lspci, dmesg, i /proc.
guid: https://forum.linuxo.org/2005/02/03/linux-i-detekcija-hardvera/
id: 730
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Linux i detekcija hardvera
url: /linux-i-detekcija-hardvera/
---
Ako želite da kupite novi ra?unar, ili želite da instalirate Linux na  
mašini na kojoj je do sada bilo neki drugi operativni sistem, verovatno  
se pitate da li ?e sve komponente &#8212;  
grafika, modem, mrežna, zvu?na &#8212; raditi na Linux-u. ProizvoÄ‘a?i ne  
mogu ili ne žele da vam kažu da li ?e njihov hardver raditi ili ne. Da  
bi to saznali morate znati na kojem ?ip setu je zasnovana odreÄ‘ena  
komponenta. Linux dolazi sa nekoliko odli?nih alata koji služe za  
pribavljanje podataka o hardveru kojeg imate u ra?unaru. Naj?eš?e  
korišteni programi su lspci, dmesg, i /proc.<!--break-->

  
Naravno, pod pretpostavkom da ne želite da u potpunosti rastavite svoj  
ra?unar preporu?ujemo da koristite ove programe.

**Detekcija hardvera pomo?u lspci**

\# /sbin/lscpi# /sbin/lspci -v# /sbin/lspci -vv

Da bi videli sumarno prikaz svih komponenti poveyanih na PCI bus,  
koristimo naredbu:

$ /sbin/lspci  
00:00.0 Host bridge: VIA Technologies, Inc. VT8363/8365 \[KT133/KM133\] (rev 02)  
00:01.0 PCI bridge: VIA Technologies, Inc. VT8363/8365 [KT133/KM133 AGP] 00:06.0 Ethernet controller: Linksys Network Everywhere Fast Ethernet  
10/100 model NC100 (rev 11)  
&#8230;

Koriš?enjem parametara -v ili -vv možemo dobiti više informacija:

\# /sbin/lspci -v  
0000:01:00.0 VGA compatible controller: 3Dfx Interactive, Inc. Voodoo 3  
(rev 01) (prog-if 00 [VGA])  
Subsystem: 3Dfx Interactive, Inc.: Unknown device 1252  
Flags: 66MHz, fast devsel, IRQ 10  
Memory at d4000000 (32-bit, non-prefetchable) <span class="d4pbbc-font-size" style="font-size: 32M"></span> Memory at d8000000 (32-bit, prefetchable) <span class="d4pbbc-font-size" style="font-size: 32M"></span> I/O ports at c000 <span class="d4pbbc-font-size" style="font-size: 256px"></span> Expansion ROM at <unassigned> [disabled] <span class="d4pbbc-font-size" style="font-size: 64K"></span> Capabilities: [54] AGP version 1.0  
Capabilities: [60] Power Management version 1

Ako želite da pronaÄ‘ete drajver za odreÄ‘eni ureÄ‘aj možete iskoristiti  
listing za pretraživanje na primer na google.com (npr.,  
VT8363/8365 ili 3Dfx Interactive, Inc. Voodoo 3 (rev 01)) 

lspci neke podatke prikuplja direktno sa ureÄ‘aja a zatim neke dodaje  
informacije koje sadrži u svojoj bazi podataka &#8212; prizvoÄ‘a?i, ureÄ‘aji,  
klase i podklase &#8212; u /usr/share/misc/pci.ids. Postoji komanda sa kojom  
možete update-ovati ovaj fajl:

\# update-pciids

Naravno ljudi koji razvijaju lspci maintainers ?e vam zahvaliti za  
slanje novih podataka; pro?itajte /usr/share/misc/pci.ids kako da im to  
pošaljete.  
Ukoliko ureÄ‘aj koji se nalazi u mašini nije prepoznat d strane  
lspci-ja, kao što može biti slu?aj sa starim ISA ureÄ‘ajima, mora?ete da  
ipak otvorite ku?ište i vidite o ?emu se radi ili ?ete iskoristiti  
program dmesg.

**Detekcija hardvera pomo?u dmesg**

Ok, dobar deo hardvera jeste u PCI slotovima, ali imate vi i možda  
i  
USB ureÄ‘aje, SCSI ureÄ‘aje, memoriju pa ?ak i procesor (CPU).  
E, tu nam može pomo?i dmesg. dmesg ustvari snima sve što je  
prepoznao kernel. A da bi to i videli ukucajte komandu:

$ dmesg | less

naravno, sli?no prethodnom programu i ovde možete koristiti paremetre  
za pronalaženje odreÄ‘enih komponenti. Na primer da bi videli listu  
svih USB ureÄ‘aja ukudajte:

$ dmesg | grep -i usb

Za listu ISA ureÄ‘aja pokrenite:

$ dmesg | grep -i isa  
isapnp: Scanning for PnP cards&#8230;  
isapnp: SB audio device quirk &#8211; increasing port range  
isapnp: Card &#8216;SupraExpress 56i Voice&#8217;

Da bi videli koliko fizi?ke RAM memorije imate pokrenite:

$ dmesg | grep -i memory  
Memory: 256492k/262080k available (1467k kernel code, 5204k reserved,  
516k data, 96k init, 0k highmem)

Da bivideli koji IDE ureÄ‘aji koriste SCSI emulaciji (koja se koristi na  
2.4 i starijim kernelima):

$ dmesg | grep -i scsi  
Kernel command line: root=/dev/hda6 ro hdb=scsi hdc=scsi  
ide_setup: hdb=scsi  
ide_setup: hdc=scsi  
SCSI subsystem driver Revision: 1.00  
hdb: attached ide-scsi driver.  
hdc: attached ide-scsi driver.  
scsi0 : SCSI host adapter emulation for IDE ATAPI devices  
&#8230;

A sada i pravi SCSI ureÄ‘aji:

$ dmesg | grep -i scsi  
SCSI subsystem driver Revision: 1.00  
scsi0 : Adaptec AIC7XXX EISA/VLB/PCI SCSI HBA DRIVER, Rev 6.2.8  
<Adaptec aic7892 Ultra160 SCSI adapter>  
aic7892: Ultra160 Wide Channel A, SCSI Id=7, 32/253 SCBs  
&#8230;Vendor: IBM-PSG Model: DPSS-336950M M Rev: S9HA  
Attached scsi disk sda at scsi0, channel 0, id 0, lun 0  
(scsi0:A:0): 160.000MB/s transfers (80.000MHz DT, offset 63, 16bit)  
SCSI device sda: 71096640 512-byte hdwr sectors (36401 MB)  
Partition check:  
sda: sda1 sda2 sda3 sda4 < sda5 sda6 >

Dole prikazana informacija se ti?e USB kamere prika?ene na ra?unar,  
uklju?iju?i i njenu lokaciju u fajl sistemu. Obi?no izveštaj o USB  
ureÄ‘aju sadrži nekoliko linija:

$ dmesg | grep -i usb  
&#8230;  
usb.c: registered new driver ibmcam  
ibmcam.c: IBM PC Camera USB camera found (model 2, rev. 0x030a)  
usbvideo.c: ibmcam on /dev/video0: canvas=352&#215;240 videosize=352&#215;240

Za prikaz serijskih portova koristite:

$ dmesg | grep -i tty  
ttyS00 at 0x03f8 (irq = 4) is a 16550A

za prikaz procesora:

$ dmesg | grep -i cpu  
Initializing CPU#0  
CPU: L1 I Cache: 64K (64 bytes/line), D cache 64K (64 bytes/line)  
CPU: L2 Cache: 64K (64 bytes/line)  
Intel machine check reporting enabled on CPU#0.  
CPU: After generic, caps: 0183f9ff c1c7f9ff 00000000 00000000  
CPU: Common caps: 0183f9ff c1c7f9ff 00000000 00000000  
CPU: AMD Duron(tm) Processor stepping 01

Initializing CPU#0  
Detected 801.446 MHz processor.

dmesg vam uvek daje nove informacije, ?ak i ukoliko ?esto menjate svoj  
hardver (na primer menjanje USB  
ureÄ‘aja).

**Detekcija hardvera pomo?u /proc**

Ako želite da praitite svoj sistem u toku rada, i vidite informacije o  
radnoj memoriji ili procesoru ili recimo hard diskovima onda je /proc  
(virtuelni fajl sistem) pravo rešenje za vasv. Ono što možete koristiti  
za dobavljanje informacija iz /proc -a je naredba _cat_ kao i  
alati koji  
su kreirani a tu svrhu kao što su _sysctl, lspci,  
ps, i top._ (ne mojte koristiti tekst editore). Sintaksa naredbe je  
kao da pregledate saržaj bilo kog drugog fajla:

$ cat /proc/filename

/proc možete pretraživati kao i svaki dugi fajl sistem i lako  
prona?i sve potrebne informacije. Potražite imena direktorijuma radi  
dobavljanja informacija o hardveru:

$ ls /proc  
bus cmdline cpuinfo devices dma driver filesystems ide kcore kmsg ksyms  
loadavg  
meminfo misc modules mounts mtrr partitions pci scsi swaps sys tty

Na primer, za prikaz informacija o procesoru (CPU), korisite:

$ cat /proc/cpuinfo  
processor : 0  
vendor_id : AuthenticAMD  
cpu family : 6  
model : 3  
model name : AMD Duron(tm) Processor  
stepping : 1  
cpu MHz : 801.442  
&#8230;

Za memoriju koristite:

$ cat /proc/meminfo  
total: used: free: shared: buffers: cached:  
Mem: 262746112 237740032 25006080 0 11575296 150138880  
Swap: 534601728 81661952 452939776  
MemTotal: 256588 kB  
MemFree: 24420 kB  
&#8230;

da bi saznali informacije o IDE hard diskovima:

$ cat /proc/ide/via  
&#8212;&#8212;-VIA BusMastering IDE Configuration&#8212;&#8212;&#8212;  
Driver Version: 3.37  
South Bridge: VIA vt82c686a  
Revision: ISA 0x22 IDE 0x10  
Highest DMA rate: UDMA66  
BM-DMA base: 0xd400  
PCI clock: 33.3MHz  
&#8230;

Da bi vidili geometriju diska, kako realnih tako i logi?kih korisite :

$ cat /proc/ide/ide0/hda/geometry  
physical 39870/16/63  
logical 2501/255/63

da bi identifikovali ureÄ‘aj korisite:

$ cat /proc/ide/ide0/hda/model  
IBM-DTLA-305020

Da bi prikazali verziju drajvera za sve IDE ureÄ‘aja:

$ cat /proc/ide/drivers  
de-scsi version 0.93  
ide-cdrom version 4.59-ac1  
ide-floppy version 0.99.newide  
ide-disk version 1.17  
ide-default version 0.9.newide

To show capabilities of CD drives, use:

$ cat /proc/sys/dev/cdrom/info  
CD-ROM information, Id: cdrom.c 3.12 2000/10/18  
drive name: sr1 sr0  
drive speed: 40 32  
&#8230;  
Can read multisession: 1 1  
Can read MCN: 1 1  
Reports media changed: 1 1  
Can play audio: 1 1  
Can write CD-R: 1 0  
Can write CD-RW: 1 0  
Can read DVD: 0 1  
Can write DVD-R: 0 0  
Can write DVD-RAM: 0 0

Da bi prikazali SCSI ureÄ‘aja, koristite slede?e komande. Samo da  
napomenem da postoji razlika izmeÄ‘u ureÄ‘aja prika?enih na SCSI  
bus i IDE  
ureÄ‘aja koji koriste SCSI-emulaciju Ovo su IDE CD ureÄ‘aji:

$ cat /proc/scsi/scsi  
Attached devices:  
Host: scsi0 Channel: 00 Id: 00  
Lun: 00  
Vendor: TOSHIBA Model: DVD-ROM SD-M1202 Rev: 1020  
Type: CD-ROM ANSI SCSI revision: 02  
Host: scsi0 Channel: 00 Id: 01 Lun: 00  
Vendor: LITE-ON Model: LTR-24102B Rev: 5S54  
Type: CD-ROM ANSI SCSI revision: 02  
For AMD Users

Slede?a komanda može da vam posluži samo radi zabave (potrebno je da  
vam radi zvuk na sistemu). Upozorenje: bu?no je &#8212; u pitanju je zvuk  
vašeg procesora u akciji.Zaustavi?ete ga komandom Ctrl-C:  
\# cat /proc/kcore > /dev/dsp

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=730)