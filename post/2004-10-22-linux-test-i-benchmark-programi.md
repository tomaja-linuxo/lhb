---
author: tomaja
date: "2004-10-22T06:28:10Z"
excerpt: |
  Da bi napravili poreÄ‘enje, ili da bi testirali svoje hardverske
  komponente trebali bi da koristite neki od test i benchmark alata.
  Možda vam ve?ina i nije poznata ali postoji dosta takvih test programa
  koji mogu da vam pomognu u optimizaciji, testiranju, poreÄ‘enju sa
  drugim mašinama. ?esto poželite da istestirate više Linux sistema ili
  više razli?itih programa na istoj mašini. Sada sledi lista od preko 60
  alata i programa:
guid: https://forum.linuxo.org/2004/10/22/linux-test-i-benchmark-programi/
id: 579
tc-thumb-fld:
- a:2:{s:9:"_thumb_id";b:0;s:11:"_thumb_type";s:10:"attachment";}
title: Linux test i benchmark programi
url: /linux-test-i-benchmark-programi/
---
Da bi napravili poreÄ‘enje, ili da bi testirali svoje hardverske  
komponente trebali bi da koristite neki od test i benchmark alata.  
Možda vam ve?ina i nije poznata ali postoji dosta takvih test programa  
koji mogu da vam pomognu u optimizaciji, testiranju, poreÄ‘enju sa  
drugim mašinama. ?esto poželite da istestirate više Linux sistema ili  
više razli?itih programa na istoj mašini. Sada sledi lista od preko 60  
alata i programa:<!--break-->

  
Hardver, softver,&#8230;  
[XHDBench](http://juanisan.homeip.net/xhdbench/): grafi?ki  
tahometar za hard disk koji prikazuje brzin rada (?itanje podataka) u  
random i sekvancijalnom modu. Ne testira fajl sistem.  
[Memtest86](http://www.memtest86.com/): Odli?an ala za  
testiranje memorije i CPU sa sopstvenog boot diska (ili se instalira na  
hard disk). Sa ovim programom treba biti pažljiv ako vam kuler sa  
procesor nije ispravan.  
[NVclock](http://linuxhardware.org/nvclock/): Evilov  
3D NVclock program je dobar na?in da testirate osnovni ?ip i brzinu  
memoriju na grafi?kim karticama koje su bazirane na NVidia  
?ipovima TakoÄ‘e je mogu?e menjati brzinu rada memorije i GPU-a.  
Novu verziju sa GTK GUI interfejsom možete skinuti sa [sourceforge](http://nvclock.sourceforge.net)-a.  
[Android  
:](http://www.wildopensource.com/larry-projects/android.html) Test program za GUI (grafi?ke) aplikacije  
[cpuburn:](http://users.ev1.net/%7Eredelm/) ovaj program je  
dizajniran za teško optere?ivanje CPU -a iliti procesora.

Fajl sistemi  
[Bonnie:](http://www.coker.com.au/bonnie++/) Bonnie++ je  
test alat koji izvodi nekoliko testiranja na hard diskovima i fajl  
sistemima.  
[dbench:](ftp://samba.org/pub/tridge/dbench/) Benckmark  
program za fajl sisteme  
[LTP:](http://sourceforge.net/projects/ltp/) Linux test  
projekat koji služi za testiranje Linux kernela i fajl sistema. U njemu  
je inkorporirano više test programa kao što su [fs_inode](http://sourceforge.net/projects/ltp/) , [fs_maim](http://sourceforge.net/projects/ltp/) , [lftest](http://sourceforge.net/projects/ltp/) , itd.  
[IOZone:](http://www.iozone.org/) Fajl sistem alat (read,  
write, re-read, re-write, read backwards, read  
strided, fread, fwrite, random read, pread, aio\_read, aio\_write)  
[PostMark:](http://www.netapp.com/tech_library/postmark.html)  
takoÄ‘e programza testiranje fajl sistema koji generiše optere?enja kao  
na enterprise sistemima sa e-mailom, vestima i web marketima.  
[stress](http://weather.ou.edu/%7Eapw/projects/stress/):  
stavlja sistem pod razli?ita optere?enaj  
[mongo](http://namesys.com/benchmarks/mongo_readme.html):  
Skup programa koji ltestiraju Linux fajl sisteme tbog brzine i  
stabilnosti  
[fsx  
:](http://www.freebsd.org/cgi/cvsweb.cgi/src/tools/regression/fsx/) program koji je portovan sa Apple-a. služi za testiranje fajl  
sistema  
[tiobench](http://sourceforge.net/projects/tiobench/):  
portabilni i robusni I/O benchmark program  
[crashme:](http://people.delphiforums.com/gjc/crashme.html)  
alat za teystiranje izdržljivosti operativnog okruženja koriš?enjem  
tehnike &#8222;Random Input&#8220; odziva  
[Cerberus:](http://sourceforge.net/projects/va-ctcs)  
Cerberus Test Kontrolni sistem(CTCS) je naaravno besplatni test alat  
koji koriste programeri i ostali radi testiranja hardvera. On generiše  
kvalitetno optere?enje sistema  
</br>  
Mreža  
[Connectathon  
NFS Testsuite:](http://www.connectathon.org/nfstests.html) Ovaj alat služi za testiranje NFS protokola  
[ISIC](http://www.packetfactory.net/Projects/ISIC/): ISIC je  
skup programa koji testira stabilnost IP Stacka  
[LTP:](http://sourceforge.net/projects/ltp/) Linux Test  
projekat koji sadrži kolekciju alata za testiranje mrežnih komponenti  
Linux kernela.  
[netperf :](http://www.netperf.org/) Ovo je benck+hmark  
program koji se koristi za testiranje performansi razli?itih tipova  
mreža  
[NetPIPE:](http://www.scl.ameslab.gov/netpipe)  
Varijabilni benchmark koji mrežnu brzinu koriste?i promenljivu veli?inu  
transfera  
[TAHI](http://www.tahi.org) : Testira IPv6  
[VolanoMark:](http://www.volano.com/benchmarks.html) Java  
chatroom benchmark/stress  
[UNH IPv6  
Tests:](http://www.iol.unh.edu/testsuites/ipv6/index.html) Nekoliko online testova za IPv6  
[Iperf:](http://dast.nlanr.net/Projects/Iperf/) Za merenje  
TCP i UDP bandwith-a  
[openCryptoki:](http://www-124.ibm.com/developerworks/projects/openCryptoki)  
nekoliko testova za openCryptoki  
[Kerberos Test  
suite:](http://www.connectathon.org/sec-readme2.html) ovi testovi se koriste za testiranje Kerberos klijenata  
(kinit,klist i kdestroy) i Kerberizovani aplkacija, ftp-a i  
telneta-a. 

Performanse  
[contest:](http://members.optusnet.com.au/ckolivas/contest/)  
testira odziv sistema preko kompajliranja kernela i raznim nivoima  
optere?enjima  
[glibench/clibench:](http://clibench.daemonware.ch/)  
benchmark alat za proveru brzine rada CPU i hard diska  
[lmbench:](http://www.bitmover.com/lmbench) Jedostavan i  
portabilan benchmark program  
[AIM Benchmark:](http://sourceforge.net/projects/aimbench)  
test brzine  
[unixbench:](http://www.tux.org/pub/tux/niemi/unixbench/)  
stariji benchmark zasnovan na BYTE UNIX Benchmarku

Skalabilnost  
[dbench](ftp://samba.org/pub/tridge/dbench) Koristi  
se za dcache test  
[Chat](http://lbs.sourceforge.net/chat) Koristi se za  
file_struct test  
[httperf](http://www.netperf.org) Koristi se za dcache test

SCSI  
[Bonnie](http://www.textuality.com/bonnie/)  
sskup programa za testiranje hard diska i fajl sistema  
[LTP](http://ltp.sourceforge.net/) disktest  
[dt](http://www.bit-net.com/%7Ermiller/dt.html) Data  
test je generi?ki test koji se koristi za proveru pravilnih operacija  
periferija, fajl sistema, dravera ili bilo kojih drugih podataka

Sigurnost  
[Nessus](http://www.nessus.org) remote security  
skener 

Standardi  
[LSB](http://www.linuxbase.org/) Test koji  
proverava LSB kompatibilnost

Upravljanje sistemom  
[SRI](http://oss.software.ibm.com/developerworks/projects/sblim/)  
&#8222;SBLIM Reference Implementation (SRI)&#8220; je deo SBLIM  
projektat.on pretpostavlja (izmeÄ‘u ostalog)  
(1) jednsotavno podešavanje, pokretanje i testiranje scenarija za  
upravljenje sistemom baziranih na CIM/CIMOM tehnologiji (2) testira CIM  
Provajdere (na lokalnim i/ili udaljenim Linux mašinama) 

Threads  
[LTP](http://sourceforge.net/projects/ltp/) ve? smo pri?ali  
o njemu  
[NGPT](http://oss.software.ibm.com/pthreads/) Next  
Generation Posix Threads sadrži nekoliko test programa  
[VSTHlite](http://www.opengroup.org/testing/downloads/vsthlite.html)  
Testira kompatibilnost sa IEEE POSIX 1003.1c ekstenzijama (pthreads).

USB  
[usbstress](http://wwwbode.cs.tum.edu/Par/arch/usb/download/usbstress/)  
Pogledajte i [Linux-usb.org](http://www.linux-usb.org/)

Kontrola vezije (CVS)  
[cvs](http://www.cvshome.org/)  
dominantni open-source network-transparent kontrolni sistem  
[BitKeeper](http://www.bitkeeper.com/Products.BK_Pro.html)  
BK/Pro  
je skalabilni konfiguracioni sistem za upravaljanje. takoÄ‘e veoma dobar  
  
[Subversion](http://subversion.tigris.org/)

Memorija  
[vmregress](http://www.csn.ul.ie/%7Emel/projects/vmregress/)  
testing i benchmark alat  
[LTP](http://sourceforge.net/projects/ltp/) ve? pri?ali 🙂  
[memtest86](http://www.memtest86.com/) isto pri?ali,  
pogledati gore  
[stress](http://weather.ou.edu/%7Eapw/projects/stress/)  
takoÄ‘e  
[memtest86+](http://www.memtest.org/) fork/unapreÄ‘ena  
verzija memtesta86  
[memtester](http://www.qcc.ca/%7Echarlesc/software/memtester/)  
Alat za testiranje grešaka u memorijskom podsistemu

Web server  
[Hammerhead](http://hammerhead.sourceforge.net) Hammerhead  
je alat za testiranje web servera i simulaciju vištestrukih konekcija i  
korisnika.  
[httperf](http://www.hpl.hp.com/personal/David_Mosberger/httperf.html)  
je popularni web server benchmark za merenje brzine rada web servera  
[siege](http://www.joedog.org/siege/index.shtml) je  
http regression test i benckmark alat  
[Trade 2](http://www-3.ibm.com/software/webservers) je J2EE  
real world webSphere benckmark alat.  
[PagePoker](http://node.to/hacks/) za testove optere?enja i  
benchmarking web servera

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=579)