---
author: tomaja
date: "2018-12-12T20:03:35Z"
guid: /?p=88876
id: 88876
image: /wp-content/uploads/2018/12/BSD12_KDE5_Laptop.jpg
tinymce-comment-field_enabled:
- "1"
title: Стигао је FreeBSD 12.0
url: /objavljen-freebsd-12-0/
---
Стигао је **FreeBSD 12.0** &#8211; ово је уједно и прво стабилно издање у 12-ој серији, а неке од најбитнијих новости које доноси нови <a href="https://www.freebsd.org/" rel="noopener" target="_blank">FreeBSD</a> су:

* OpenSSL је ажуриран на верзију 1.1.1a (LTS).  
* Unbound је стигао до верзије 1.8.1, а DANE-TA је сада укључен по default-у.  
* OpenSSH је ажуриран на верзију 7.8p1.  
* Додатна подршка за capsicum је додана у ssh демон.  
* Clang, LLVM, LLD, LLDB, compiler-rt и libc++ су ажурирани на верзију 6.0.1.  
* vt Terminus BSD конзолни фонт је такође ажуриран и то на верзију 4.46.  
* bsdinstall алатка сада подржава UEFI+GELI као опцију за инсталацију.  
* VIMAGE кернелова конфигурациона опција је сада укључена по default-у.  
* NUMA опција је такође подразумевано укључена у amd64 GENERIC и MINIMAL конфигурацијама кернела.  
* додан је netdump драјвер, омогућавајући ресурс кроз који кернелови crash логови могу бити пребачени на удаљени  
рачунар у случају пада система.  
* vt драјвер је нови и са унапређеним перформансама, приказујући текст 2-6x брже него до сада.  
* Ту су и разна унапређења у графичкој подршци за актуелни графички хардвер.  
* Подршка за capsicum је укључена по default-у за armv6 и armv7.  
* UFS/FFS фајл системи су ажурирани ради консолидације ТRIM/BIO_DELETE командиc, смањујући read/write захтеве  
захваљујући мањем броју симултано послатих TRIM порука.  
* NFS сервер 4.1 сада укључује подршку за pNFS сервер.  
* pf филтер пакета сада може да се користи у jail-у преко vnet-а.  
* bhyve(8) алатка је ажурирана ради додавања емулирања NVMe уређаја.  
* KDE графичко окружење је сада ажурирано на верзију 5.12.5.  
* и много тога другог&#8230;

За комплетну листу нових могућности и познатим проблемима треба посетити следећа два линка:

* <a href="https://www.FreeBSD.org/releases/12.0R/relnotes.html" rel="noopener" target="_blank">https://www.FreeBSD.org/releases/12.0R/relnotes.html</a>  
* <a href="https://www.FreeBSD.org/releases/12.0R/errata.html" rel="noopener" target="_blank">https://www.FreeBSD.org/releases/12.0R/errata.html</a>

За више информација о активностима око изласка нове верзије треба погледати:  
* <a href="https://www.FreeBSD.org/releng/" rel="noopener" target="_blank">https://www.FreeBSD.org/releng/</a>

### Доступност

FreeBSD 12.0 je доступан за amd64, i386, powerpc, powerpc64, powerpcspe, sparc64, armv6, armv7, and aarch64 архитектуре, односно платформе. FreeBSD 12.0 се може инсталирати са бутабилних ISO image фајлова или преко мреже. Неке од платформи подржавају инсталацију са USB меморија. 

### Преузимање

FreeBSD 12.0 се може преузети преко https-а са следећих линка:

* <a href="https://download.freebsd.org/ftp/releases/ISO-IMAGES/12.0/" rel="noopener" target="_blank">https://download.freebsd.org/ftp/releases/ISO-IMAGES/12.0/</a>

FreeBSD 12.0 за виртуелне машине у облику image фајлова се може преузети са:

* <a href="https://download.freebsd.org/ftp/releases/VM-IMAGES/12.0-RELEASE/" rel="noopener" target="_blank">https://download.freebsd.org/ftp/releases/VM-IMAGES/12.0-RELEASE/</a>

За упутства како инсталирати FreeBSD или како ажурирати постојећу инсталацију на верзију 12 треба посетити линк:

* <a href="https://www.FreeBSD.org/releases/12.0R/installation.html" rel="noopener" target="_blank">https://www.FreeBSD.org/releases/12.0R/installation.html</a>

### Подршка

На основу дискусије о моделу подршке за FreeBSD, FreeBSD 12 серија ће бити подржана најмање до 30 јуна 2020. године. За више информација о званичном обавештењу које се тиче о моделу подршке треба погледати:

* <a href="https://www.FreeBSD.org/security/" rel="noopener" target="_blank">https://www.FreeBSD.org/security/</a>

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=88876)