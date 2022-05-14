---
author: tomaja
date: "2018-11-14T14:16:32Z"
guid: /?p=88846
id: 88846
image: /wp-content/uploads/2018/11/Void_Linux_logo.png
tinymce-comment-field_enabled:
- "1"
title: Void Linux попуњава празнину
url: /void-linux-popunjava-prazninu/
---
Ова релативно нова Линукс дистрибуција покушава да не буде само једна од сличних. И успева у томе. Све популарнији **<a href="https://voidlinux.org/" target="_blank" rel="noopener">Void</a>** је започет и развија се као независна Линукс дистрибуција опште намене базирана на Linux кернелу.

Започета је од 0,тј. не базира се ни на једној од постојећих Линукс дистрибуција. Поседује свој хибридни бинарни/изворни менаџер пакета _&#8211; XBPS_. Он омогућава корисницима да брзо инсталирају, ажурирају и уклањају софтвер, или да исталирају софтвер директно из извора помоћу XBPS колекције source пакета. Веома подсећа на pacman, што свакако није лоша вест. На пример, команда за инсталацију пакета је `xbps-install -S package_name` а за ажурирање система `xbps-install -Su`. Више информација о XBPS-у се може наћи на [званичнoм викију](https://wiki.voidlinux.eu/XBPS).

Још једна карактеристика издваја Void од других Линукс система је и основни _init_ систем који није базиран на _runit_-у уместо на уобичајеном _systemd_-у. Такође, Void користи LibreSSL уместо OpenSSL-a.

### Arch ли је ?

У питању је rolling дистрибуција, попут Arch Linux-a, тако да ћете са редовним дневним ажурирањем система увек имати најновију верзију _Void_-a на свом рачунару или _cloud_-y. Ту се релативна сличност са Arch-ом не завршава. Дистро у доста аспеката подсећа на Arch, од начина инсталације, коришћења ресурса, брзине рада, генерално концепције креирања система и софтверских пакета.

Хардверска подршка је добра, а систем ради живахно и са брзим одзивом и на прилично старим рачунарима. И не чуди, јер је базни хардверски минимум следећи: (x86-64) EM64T CPU, 96MB RAM меморије, 350MB простора на диску, и приступ нету, за мрежну инсталацију. За графичка окружења, од којих су званично дистрибуирају live верзије за _Enlightenment, Cinnamon, LXDE, MATE_ и _XFCE_ биће нам потребно нешто више меморије: 256-512 MB. Ако сте навикли на Gnome или KDE, без бриге, ту су, и то са верзијама 3.30 односно 5.13.5 (софтверски пакети).

Иначе, ризница софтвера тренутно садржи преко 6200 пакета, што наравно није за поређење са великим играчима попут Ubuntu-a, Debian-a или Arch-a, aли је вероватно довољно. Ако нешто и зафали, увек је могућа инсталација из изворног кода.<figure id="attachment_88852" aria-describedby="caption-attachment-88852" style="width: 790px" class="wp-caption alignnone">

<img class="size-full wp-image-88852" src="/wp-content/uploads/2018/11/void-gnome.jpg" alt="" width="800" height="450" srcset="https://linuxo.org/wp-content/uploads/2018/11/void-gnome.jpg 800w, https://linuxo.org/wp-content/uploads/2018/11/void-gnome-300x169.jpg 300w, https://linuxo.org/wp-content/uploads/2018/11/void-gnome-768x432.jpg 768w" sizes="(max-width: 800px) 100vw, 800px" /> <figcaption id="caption-attachment-88852" class="wp-caption-text">Void Linux Gnome-Wayland</figcaption></figure> 

А за оне који желе да креирају софтверске пакете, ту је _xbps-src_. У основи, то је креатор пакета који је такође кодиран из почетка. Креирање софтвера се врши у контејнерима уз коришћење _Linux namespace_-ова, што омогућава изоловање процеса и монтирање, без потребе за root овлашћењима. xbps-src подржава више C библиотека за компајлирање (за сада то су glibc и muslC).

Void укључује подршку за _Intel x86®, ARM®_ и _MIPS®_ процесоре, па су тако ту верзије и за _Raspberry Pi_ и сличне хардверске платформе попут BeagleBone-а,Odroid-а и других.

### Корисни линкови

<a href="https://voidlinux.org/download/" target="_blank" rel="noopener">Преузимање </a>Void Linux-a (Live ISO)  
<a href="https://voidlinux.org/packages/" target="_blank" rel="noopener">Софтверски пакети</a> за Void Linux  
<a href="https://wiki.voidlinux.eu/Main_Page" target="_blank" rel="noopener">Документација</a> за Void Linux (није преобимна, често потребна)  
Како инсталирати и испробати <a href="https://wiki.voidlinux.eu/Install_Void_Linux_onto_a_USB_Stick" rel="noopener" target="_blank">Void Linux на USB-у</a>

Пре само 2-3 дана је објављена најновија верзија Void-a, што је идеално за чисту инсталацију. Ако испробате ову Линукс дистрибуцију напишите у коментару своје утиске.  
Поздрав до следећег читања.

[Креирај тему форума везану за овај текст](https://linuxo.org/nova-tema-na-forumu/?se_pid=88846)